---
title: Multisensory balance
---

# Multisensory integration for control

We humans can rely on mutliple senses when moving and acting in our environment. We can even focus on one sense, blend out others, trust or distrust them, or rely on just a subset of them. This skill becomes especially important when our senses don't match up anymore.
Just imagine yourself sitting inside a train at a trainstation, looking out of the window at another train (trainception). What happens when that other train starts moving? Most likely you will briefly think that it is your train that (finally) started.

This is an every-day life example of a visuomotor illusion known as the 'moving-room illusion'. A more artificial version of a literally moving room was already used in [experiments in the 70s](https://www.youtube.com/watch?v=F4xenIulg_8) showing that people rely heavily on their visual input for keeping balance. This visual dominance also causes us problems, when the visual information is incongruent with information from our proprioceptive and vestibular system.

## Multisensory (dis-)integration for robot balance control
`status: ongoing Master's thesis`

A student of [Max](http://lauflabor.ifs-tud.de/doku.php?id=lab_members:lab_members_maximilian_alexander_stasica) and me, Sebastian, is trying to replicate this phenomenon of human visuomotor control in a reinforcement learning agent. 

To strike a proper comparison to the human behaviour, we used the same VR/ simulation environment containing a form of moving room illusion for training an inverted pendulum controller and for conducting an experiment on human participants. In the experiment we measured body and head motion, muscle activations, and ground reaction forces.

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

... poor agent.