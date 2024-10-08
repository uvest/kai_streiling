---
title: Causality
---

# Trial-history and Choice-history effects on causality perception in schizophrenia

`status: submitting` <br>
Find the pre-print at [https://osf.io/preprints/psyarxiv/8ghab](https://osf.io/preprints/psyarxiv/8ghab)


tf;dr <br>
We use Michotte Launching events to study the judgements of perceptual causality in healthy controls and schizophrenic patients. <br>
I used a fancy linear regression (GLMM) for looking at the influence of the last launching event and the choice that was made on the current choice. <br>
The last choice indeed influences our perception of causality, both, in an easy to grasp direct way and by modulating the influence of other factors.

---


## Introduction and Experiment

My friends and I have somewhat built up a tradition over the last years. Before christmas, we all dress up in the fanciest suits we can find in our cupboards, attach a vintage bow tie, have a *Glühwein* on the christmas market and head for the the casino. Some of us winning, most of us loosing, but all feeling fancy. <br>
What caught my eye on one of those evenings was the betting behaviour at the Roulette tables. Many bet on either black or red (both having on average a 48.6 % chance). Sometimes, a table spat out the same colour again and again, all black for the last 10, 15, 20 draws. Such is chance. Funnily however, if such sequences occur, more and more people are drawn to the opposite color. They are clearly influenced by the past outcomes of the gamble although there is no information in it - unless some trick is at work. Such is human nature.

Now, in our project in the course of [TAM](https://www.theadaptivemind.de/) we did not go gambling. That is nothing you should do with tax money is it?
Instead we looked at perceptual decision making or rather at the perception of causality. So, why telling you about my - seldomly successful - adventures at the casino?

For this project, I revisited an experiment conducted by [Benjamin Straube](https://tnm-lab.com/people/prof-dr-benjamin-straube/) and colleagues from the [TNM-Lab](https://tnm-lab.com/) at the Philipps-University Marburg. They showed their participants a launching event of a blue ball "colliding" with a red ball and asked them whether they perceived the event as *causal* (the blue ball did cause the red ball to move) or *non-causal*.

The following little movieclip, generated by my colleague [Yunyan Duan](https://www.psychologie.tu-darmstadt.de/perception/home_per/people_per/people_perception_detail_75264.en.jsp), gives you an impression of such a launching event:


<video controls="controls" width="500" name="Launching event">
  <source src="https://uvest.github.io/kai_streiling/assets/images/launching_event_example_by_Yunyan_Duan.mov">
  <source src="https://uvest.github.io/kai_streiling/assets/images/launching_event_example_by_Yunyan_Duan.mp4" type="video/mp4">
</video>

<!-- <figure class="video_container">
  <video controls="true" allowfullscreen="true">
    <source src="https://uvest.github.io/kai_streiling/assets/images/launching_event_example_by_Yunyan_Duan.mp4" type="video/mp4">
    <source src="/path/to/video.ogg" type="video/ogg">
    <source src="/path/to/video.webm" type="video/webm">
    <source src="https://uvest.github.io/kai_streiling/assets/images/launching_event_example_by_Yunyan_Duan.mov" type="video/mov">
  </video>
</figure>

--

<iframe src="https://uvest.github.io/kai_streiling/assets/images/launching_event_example_by_Yunyan_Duan.mp4"></iframe> -->

The experiment was conducted on patients with Schizophrenia Spectrum Disorder (SSD) and healthy control (HC) participants. It allows some insights into the differences between SSDs and HCs in the usage of temporal and spatial offset (delay and angle) when perceiving causality. <br>
We were now wondering, if there also were other factors that are used differently between SSDs and HCs. And there my casino story comes into play. I was thinking that there might be a bias given the recent history of observed events. Especially, we were curious about the effect of the last choice.

