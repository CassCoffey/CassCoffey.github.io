---
name: Speed Game Prototype
tools: [C#, Unity]
image: /assets/images/SpeedgameCover.png
description: Racing prototype with Trackmania-style determinism and replays
---

# Speed Game Prototype

I wanted to see if I could replicate Trackmania's determinism in Unity and their efficient replay files. Using script ordering and a strict tick system for all interactions and calculations, this prototype is fully deterministic accross both PC and Mac (haven't tested Linux yet but it should be too). This let me develop a replay system that only has to save the inputs and the ticks they were performed at, so the replay files can be very efficient. One of my tests had a minute of replay data stored in an 11kb file. Due to the determinism, these replays function even when transfered between machines and OS's.

<iframe width="640" height="360" src="{{ site.baseurl }}/assets/videos/SpeedGameDemo.mp4" frameborder="0" allowfullscreen="" style="margin: 1rem auto;display: block;max-width: 100%;"></iframe>

Below is the file size of the two replays being shown in the above video:

![Image]({{ site.baseurl }}/assets/images/SpeedGameReplaySize.png)

<p class="text-center">
{% include elements/button.html link="https://github.com/CassCoffey/UnitySpeedGame" text="Learn More" %}
</p>