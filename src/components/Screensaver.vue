<template>
  <div>
    <div id="engine"></div>
    <div id="logo">
      Sean Daniels
    </div>
  </div>
</template>

<script>
import Matter from "matter-js";
export default {
  mounted() {
      
    var Engine = Matter.Engine,
      Render = Matter.Render,
      Runner = Matter.Runner,
      MouseConstraint = Matter.MouseConstraint,
      Mouse = Matter.Mouse,
      World = Matter.World,
      Bodies = Matter.Bodies;

    // create engine
    var engine = Engine.create(),
      world = engine.world;

    // create renderer
    var render = Render.create({
      element: document.querySelector("#engine"),
      engine: engine,
      options: {
        wireframes: false,
        width: 650,
        height: 500,
      },
    });

    Render.run(render);

    // create runner
    var runner = Runner.create();
    Runner.run(runner, engine);

    // add bodies
    World.add(world, [
      Bodies.rectangle(400, 0, 800, 50, { isStatic: true }),
      Bodies.rectangle(400, 600, 800, 50.5, { isStatic: true }),
      Bodies.rectangle(800, 300, 50, 600, { isStatic: true }),
      Bodies.rectangle(0, 300, 50, 600, { isStatic: true }),
    ]);
    engine.world.gravity.x = 0;
    engine.world.gravity.y = 0;

    var circle = Bodies.circle(200, 200, 75, {
      restitution: 1,
      friction: 0,
      frictionAir: 0,
      density: 0.001,
      inertia: Infinity,
      render: {
        sprite: {
          texture: "/name.png",
        },
      },
    });

    World.add(world, circle);

    // add mouse control
    var mouse = Mouse.create(render.canvas),
      mouseConstraint = MouseConstraint.create(engine, {
        mouse: mouse,
        constraint: {
          stiffness: 0.2,
          render: {
            visible: false,
          },
        },
      });

    World.add(world, mouseConstraint);

    // keep the mouse in sync with rendering
    render.mouse = mouse;

    // fit the render viewport to the scene
    Render.lookAt(render, {
      min: { x: 0, y: 0 },
      max: { x: 800, y: 600 },
    });

    // context for MatterTools.Demo
    return {
      engine: engine,
      runner: runner,
      render: render,
      canvas: render.canvas,
      stop: function() {
        Matter.Render.stop(render);
        Matter.Runner.stop(runner);
      },
    };
  },
};
</script>

<style scoped></style>
