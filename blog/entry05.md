# Entry 5
##### 4/8/24

### Update/Context
Since the last blog, I have achieved a margin of accomplishments in my Freedom Project. I specifically tinkered with my selection of tools (Skeleton, A-Frame, and SASS) in various files by coding example templates. Based on my experimentations, I ended up choosing A-Frame as my permanent tool. Upon the decision, I had to familiarize myself of the engine.

### Tinkering
Beginning with my A-Frame tinkering process, I looked over the documentation provided by the software company. As I analyzed all of the concepts, the three main topics that interested me were importing 3D Models and Images, Physics and Collisions, and Video. But before I tested reached the subjects, I tested additional primitives and components for more context of how the tool functioned.

In my IDE, I began by importing the A-Frame CDN link for all of the features to work. I then pasted a skeleton base for A-Frame, which included the tags: `(html),(head),(body), and (a-scene)`. Afterwards, I watched a [introductory video](https://www.youtube.com/watch?v=j-dlO71Gsqk&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=3&t=77s) about A-Frame placed the first primitives (shapes) into my VR scene using these lines of code: `<a-sphere position="10 2 0"></a-sphere> <a-box position="0 2 0"></a-box> <a-sphere
 position="-10 2 0"></a-sphere>`. At last, the next element I used was `<a-plane>` and `<a-sky>`. For this component I utilized the `rotation` property to make a platform. I added more touches using the `color` attribute, followed by `scaling`.

 Once I learned the basics of A-Frame, I moved on to the more complex points. I first focused on importing images. I followed a [brief tutorial](https://www.youtube.com/watch?v=NYvYFtHReuElist=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=8) made by an A-Frame expert. As I looked through the informative recording, certain points became more clear. I looked over multiple 8-ball images and downloaded all of the files. During this process, I ensured that the images would fully wrap around a sphere primitive to give a better view. After searching and finding suitable visuals, I imported the downloads into GitHub and used the same code in the video. Moreover, I also added extra attributes to give the shapes a distinct look:

 ``` HTML
<a-assets>
<img src="img/8ball2.jpg" id="h3">
<img src="img/8ball3.jpeg" id="h6">
<img src="img/8ball4.jpeg" id="h7">
</a-assets>
<a-scene>
<a-sphere src="#h3" position="10 2 0" scale="2 2 2" metalness="0.9"></a-sphere>
    <a-sphere src="#h6" position="0 2 0" scale="2 2 2" metalness="0.9"></a-sphere>
    <a-sphere src="#h7" position="-10 2 0" scale="2 2 2" metalness="0.9"></a-sphere>
</a-scene>
 ```
As I learned how to put images in a VR scene, my next aim was to import 3D models and install videos. For this section, I mainly focused on two YouTube recordings: [Video](https://www.youtube.com/watch?v=5KjyTU07EHo&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=25&t=190s) and [Loading and Displaying 3D Models](https://www.youtube.com/watch?v=cS8uGfd_oG8&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=13). I watched the videos, and progressively, learned the methods for uploading videos and 3D models into GitHub. In my A-Frame scene, I created my own examples within the same scene to test the skills learned. However, my first step was downloading the files. I gathered models in [SketchFab](https://sketchfab.com/) and a video in [StoryBlock](https://www.storyblocks.com/video) and put it in relative files. Within the `<a-assets>` tag, I added the `video` tag and linked the video, further including `<a-video>` inside the `<a-scene>` to display the content. Additionally, I typed in the `<a-assets>` tag, `<a-asset-item>` and included various attributes: `id="tower" src="https://cdn.glitch.global/dc61be5e-ba3d-456f-b77d-84a20b34a952/issum_the_town_on_capital_isle.glb?v=1712191797906"`.  Afterward, I used the `<a-entity>` and applied a `id` value to make the model appear. The end code looked like this:

``` HTML
<a-assets>
  <video id="hi" src="video/3d-monochrome-abstract-art-video-animation-featuring-a-surreal-chrome-sphere-c-SBV-348789757-preview.mp4" autoplay loop="true"></video>
    <a-asset-item id="tower" src="https://cdn.glitch.global/dc61be5e-ba3d-456f-b77d-84a20b34a952/issum_the_town_on_capital_isle.glb?v=1712191797906"></a-asset-item>
</a-assets>
<a-scene>
<a-video src="#hi" width="8" height="4.5" position="5 9 0">
    </a-video>
     <a-entity gltf-model="#tower" position="0 -10 0"></a-entity>
</a-scene>

```

Although I successfully learned the concepts of importing 3D models and videos, there was one more topic to focus on. I still wanted to acknowledge how Physics and Collisions worked. A [tutorial](https://www.youtube.com/watch?v=CsXNfoXEJ2w) I followed during this process was made by Connor Kasarda. As I took in the information regarding the steps of incorporating physics in A-Frame, the next step was to create my own templates with the features.


For the physics component, I made a new file to give a new scene. I imported the skeleton structure again and the CDN link for the Javascript of A-Frame. But this time, I also inputted the CDN link for the Physics engine of A-Frame and an additional extra category of the tool to enable the features. Following these steps, I added three new sphere primitives. I used the `ammo-body` and `ammo-shape` to define the type of the primitive and whether it would move on collision (affected by gravity). I added the `dynamic` property to `ammo-body` to make the spheres be affected by gravity and put sphere under the type of shape. At last I added the physics class in my `a-scene` tag and `restitution`, which affects the bounciness of a primitive. Here is the final code:


``` HTML

 <a-scene physics="driver: ammo; restitution: 1">
    <a-sky src="#h2" radius="1350"></a-sky>
    <a-sphere src="#h3" position="10 5 0" scale="2 2 2" ammo-body="type: dynamic" ammo-shape="type: sphere"></a-sphere>
    <a-sphere src="#h6" position="0 5 0" scale="2 2 2" ammo-body="type: dynamic" ammo-shape="type: sphere"></a-sphere>
    <a-sphere src="#h7" position="-10 5 0" scale="2 2 2"></a-sphere>
</a-scene>
```

After I learned the topics that was desired, I also tested out other features. I recorded all of the experimentations in my [learning log](../tool/learning-log.md) as a way of note-taking to keep my mind refreshed within the future.


### EDP
As of now, I am inbetween stages four and five of the Engineering Design Process. I have made myself more familiar to A-Frame, learning various concepts and components. In the next few weeks, I will use the gained knowledge to create an idea that me and my peer generated in the beginning of the year.

### Skills
Tinkering with A-Frame taught me skills. The three major ones included:

* Organization - When I was learning A-Frame, many notes had to be taken. In order to make the most out of them, I organized the details in my learning log to refer back in the future.
* Attention to detail - While coding specific A-Frame scenes, there were missing closing tags for some lines of code. This caused issues when I ran the scene on various occasions. To fix these problems, I had to debug, and pay close attention to every lines of syntax.
* Management - As I was introduced to A-Frame, there were many topics to learn. To be efficient, I learned a new topic frequently and jotted down any significant information. This allowed me to make the most out of my learning experience.




[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
