---
title: Start With the Process, Not the Machine
categories: [Engineering, Automation]
tags: [machine-design, automation, concept-design, mechanical-design]
---

A machine concept can look convincing in CAD and still be based on the wrong idea.

That is why I do not think machine design should start with geometry.

It should start with the process.

What needs to happen?

What has to move?

What has to be positioned?

What has to be detected, clamped, transferred, checked, or released?

What can remain a manual process?

What really needs automation?

Which option is simpler and cheaper in the short term?

Which option is more economical over the full life of the process?

![Start with the process, not the machine](/assets/img/posts/start-with-the-process-not-the-machine.png)

These questions come before the CAD model.

A machine is not the goal.

The process is the goal.

The machine is the physical system that makes the process possible.

This distinction matters because it is easy to start designing too early.

A frame can be created.

Actuators can be selected.

A mechanism can begin to take shape.

And only later do the real process questions appear.

Where does the part come from?

How is it oriented?

What happens if it is loaded incorrectly?

What variation exists in the incoming part?

What must be checked before the next step?

What happens when something stops halfway through the cycle?

How will the operator recover from a fault?

How will the machine be cleaned, adjusted, or maintained?

These questions often influence the machine concept more than the first geometry does.

Before developing a concept, I would want to understand:

- what is the real input to the process?
- what should the output be?
- which steps actually add value?
- which steps are repetitive or unstable?
- where can variation enter the process?
- what needs human judgement?
- what should be detected automatically?
- what happens when the normal sequence is interrupted?
- what constraints come from the surrounding equipment or workplace?

Only after that does it make sense to decide how much automation is really needed.

Sometimes the best solution is a complete machine.

Sometimes it is a fixture.

Sometimes it is a guided manual operation with one sensor.

Sometimes it is only a mechanical stop, a better locating feature, or a simpler sequence.

More automation is not automatically a better concept.

The right level of automation depends on the process.

The same applies to engineering tools.

CAD, simulation, and AI can all be extremely useful.

AI can be especially helpful when we are working outside our strongest areas, or when we want to challenge our first assumptions.

It can also support analysis by surfacing questions, risks, and alternatives that may not come to mind immediately.

But tools should support the thinking, not replace the first step of it.

Before opening CAD, running a simulation, or asking an AI tool for solutions, it is still worth spending a little time understanding the process itself.

What really needs to happen?

What is creating the value?

Which step is difficult, repetitive, unstable, or unnecessary?

Tools can help us explore the solution space.

But the machine should follow the process, not the other way around.

A good machine concept usually becomes simpler when the process is understood clearly.

Once the real problem is clear, many unnecessary ideas disappear.

And the remaining design decisions become much easier to justify.
