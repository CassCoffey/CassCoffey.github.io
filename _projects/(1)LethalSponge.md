---
name: Lethal Sponge
tools: [C#, Unity, HLSL, RenderDoc]
image: /assets/images/LethalSpongeIcon.png
description: Lethal Company performance mod focused on rendering and memory
---

# Lethal Sponge

My latest project, an extensive performance, bugfix, and logging mod for Lethal Company. I performend numerous tests and investigations into the sources of Lethal Company's framedrops and memory leaks, and compiled the most impactful fixes into this mod. I've already recieved reports of it doubling framerates on lower end machines, and for many people it allows them to maintain a steady 60fps where they couldn't before.

The most technically significant change of these fixes is the complete rewrite of Lethal Company's primary shader, which was actually a major source of framedrops. The Vanilla LC shader is a DrawRenderers Custom Pass, which means every mesh on screen is drawn an additional time in order to achieve its visual style. I rewrote this shader as a Fullscreen Custom Pass so that it is accomplished in only 1 draw call while looking nearly identical. To support this, I also needed to add a new Custom Pass Injection Point into the HDRP render loop so that I could apply the effect to the lit meshes but not to the volumetric lighting and fog.

Some quotes I've gotten in the Lethal Company Modding Discord thread for the mod (names removed for privacy):
 - "one of my friends who was lagging real bad (~30fps w lagspikes) with my modpack installed this mod and got up to 60fps consistent"
 - "Practically all of my friends play below 60fps most of the time so I have basically every performance mod. LethalSponge has made the biggest difference by far, on par with CullFactory"
 - "yeah this is the most notable performance boost i've seen in a long while"
 - "Just wanna say that this mod has been a blessing to our group, the performance increase has been insane and some of our group members with lower end pcs who would previously be unplayable can how get framerates of around 30fps, and higher end to around 130-200 and its been so much better"

<p class="text-center">
{% include elements/button.html link="https://github.com/CassCoffey/LethalSponge" text="Check Out The Repo" %}
</p>