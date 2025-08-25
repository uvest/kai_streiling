---
title: Multisensory balance
---

# Multisensory integration for control

We humans can rely on mutliple senses when moving and acting in our environment. We can even focus on one sense, blend out others, trust or distrust them, or rely on just a subset of them. And most intriguingly, we do so without much mental effort. This skill becomes especially important when our senses don't match up anymore. <br>
One situation where this seamless integration breaks, at least for a few moments, is the visuomotor "moving room illusion".
Imagine yourself sitting inside a train at a trainstation, looking out of the window at another train (trainception). What happens when that other train starts moving? Most likely you will briefly think that it is your train that (finally) started moving.

A more artificial version of a literally moving room was already used in [experiments in the 70s](https://www.youtube.com/watch?v=F4xenIulg_8) showing that people rely heavily on their visual input for keeping balance. This visual dominance also causes us problems, when the visual information is incongruent with information from our proprioceptive and vestibular system.

While I won't ask why we have this visual dominance in the first place, I wonder how we robustly integrate vision and other senses when they disagree with each other. How do we detect who is lying?

## What humans do

As a baseline, we collected some data from human participants doing a simple balancing task while experiencing external-optical flow in their full visual field: Wearing a VR headset, all they saw was moved to one side! <br>
And, loo and behold, that actually does influence their stability! Especially for linear movements, we saw that at the onset of movement people followed the visually perceived movement with their head, before realising their offset and restabilizing themselves.

Have a look at the left side of my little poster here:

<object data="../assets/artifacts/poster_ecvp24.pdf" type="application/pdf" height="1000" width="100%">
</object>

## What optimal control can do

To explain the susceptibility but also the robustness to optical flow with some maths, we turned to a Linear Quadratic Gaussian (LQG) regulator, an optimal control model, that we set up for controlling an inverted pendulum to stand upright. As you might guess, we use that inverted pendulum as a *very* crude approimation of a human standing.

The magic we added was in the **combination** and **adaptation** of the state estimates that we got from a proprioceptive and a visual input stream. <br>
The combination we made dependent on the estimated noise of each stream: The less reliable an input stream was estimated to be, the less weight was placed on it. <br>
And these noise variance estimates we then adapted over time, depending on if a predicted observation matched with the actual observation of each stream.
(See right side of the poster above.)

Here, we can also strike a link to Agency. A famous model for the Sense of Agency - at least in the sensorimotor context - is the comparator model. If what we expect to observe/ sense/ perceive based on an acion we made fits with what we actually observe/ sense/ perceive, we feel agency about the result. If not, well, then we don't. Here we use this same idea to update our noise estimates and shift the weighting between different input streams: If we feel no Agency about the results in one input stream, we increase its estimated noise. If we do, we decrease the estimated noise.



## What Deep Reinforcement Learning might do
Now, we finally reached what we are still actively working on. 

One first step has been taken by a student of [Max](http://lauflabor.ifs-tud.de/doku.php?id=lab_members:lab_members_maximilian_alexander_stasica) and me who tried to replicate this phenomenon of human visuomotor control in a reinforcement learning agent. 

<!-- To strike a proper comparison to the human behaviour, we used the same VR/ simulation environment containing a form of moving room illusion for training an inverted pendulum controller and for conducting an experiment on human participants.

### Showcase
Some first impressions on what the visual part and some extracted optical flow could look like to the agent:

Optical input:
<video controls="controls" width="300" name="Optical flow 1">
  <source src="https://uvest.github.io/figures/optical_flow_1.webm"/>
</video>

Optical flow estimate extracted with a differential method:
<video controls="controls" width="300" name="Optical flow 3">
  <source src="https://uvest.github.io/figures/optical_flow_3.webm"/>
</video>

... poor agent. -->