# Tool Learning Log

Tool: **A-Frame**

---

**2/26/24**

Goal: To gain a better understanding of the basic A-Frame concepts

Steps:
* I watched a [A-Frame tutorial playlist](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) for roughly 25 minutes
* A-Frame Installation
    * Import link through `script` tag in HTML skeleton structure on CS50 IDE
    ```HTML
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
    ```
* Added primitives inside `a-scene` tags -->
```HTML
<a-box></a-box>
<a-sphere><a-sphere>
<a-cylinder></a-cylinder>
```
* Adjusted primitives with color, [positioning](https://aframe.io/docs/1.5.0/components/position.html), [scale](https://aframe.io/docs/1.5.0/components/scale.html), and [rotation](https://aframe.io/docs/1.5.0/components/rotation.html) attributes
    * X-value = left and right, Y-value = up and down, Z-value = front and back

```HTML
  <a-scene>
    <a-box color="red" rotation="10 10 35" position="0 0 -10" scale="2 2 2"></a-box>
    <a-sphere color="green" position="-7 0.5 -10" scale="2 2 2"><a-sphere>
    <a-cylinder color="orange" position="8 -1 0" scale="1.5 2 2"></a-cylinder>
  </a-scene>
```
* Positioned was relatively difficult for me. I specifically didn't understand the function of the z-value.

    * To find out my misconception, I executed trial and error processes in my IDE, along with looking at a visual diagram. Eventually, I learned that the z-value mainly applies to the viewer's perspective of "back and forth".

* I additionally learned the `<a-sky>` and `<a-entity>` element and used it in my example:
```HTML
<a-sky color="blue"></a-sky>
<a-entity environment="preset: forest; dressingAmount: 100"></a-entity> (Needs separate CDN link)
```
* `<a-entity>` is for background use and `<a-sky>`
is generally utilized for the change of atmosphere in the VR experience

NOTE: `<a-entity>` overrides `<a-sky>` - for example, when both tags are used within `a-scene`, only one result between the two will show up.


**Next time:** Learn more attributes for tags

---

**3/3/24**

Goal: To learn more about A-Frame attributes and general concepts
* Continued to watch [A-Frame tutorial playlist](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) for 15 minutes
* Added a green platform (ground component) to my existing A-Frame scene

   ```HTML
   <a-plane material="color: #53C532" scale="10 10 1" rotation="-90 0 0"></a-plane>
   ```

     * The attribute `material` allows you to specify a primitive's look (color, texture, etc)

NOTE: Any rotation on primitives directly affects the direction in which the scale - X, Y, Z - value faces

 * The example has a rotation of `"-90 0 0"`

   * Only the x-axis is rotated by -90 degrees, so as a result:

      * Scale values - `x = x`, `y = z`, `z = y`

* Applied an image to `<a-plane>`, `<a-box>`, `<a-sphere>`, and `<a-cylinder>`
``` HTML
<a-assets>
  <img src="img/grass_1.png" id="h1">
</a-assets>
 <a-plane material="color: #53C532" scale="10 10 1" rotation="-90 0 0" src="#h1"></a-plane>
```

* Added a 360° image within the `<a-assets>` and `<a-scene>` tag to represent the sky -->

```HTML
<a-assets>
      <img src="img/grass_1.png" id="h1">
      <img src="img/cloud_3.jpg" id="h2">
      <img src="img/8ball2.jpg" id="h3">
      <img src="img/gradient.avif" id="h4">
      <img src="img/steel.jpg" id="h5">
    </a-assets>
<a-scene>
    <a-sky src="#h2"></a-sky>
    <a-box src="#h4" position="-30 1 -10" scale="10 10 10"></a-box>
    <a-sphere src="#h3" position="-5 1 -5" scale="4 4 4"><a-sphere>
    <a-cylinder src="#h5" position="8 -1 -5" scale="1.5 4 2"></a-cylinder>
</a-scene>
```
* Included the `radius` attribute to the `<a-sky>` and  tag

```HTML
<a-scene>
<a-sky radius="100" src="#h2">
</a-sky>
</a-scene>
```

NOTE #2:  The `radius` attribute is similar to the `border-radius` in CSS. Both of the `radius` makes an item more round.

Goal for next time: Learn more about primitives and continue to explore attributes

---

**3/11/24**

Goal: To continue enhancing my knowledge of A-Frame

* Look over A-Frame documentations for attributes of primitives.
  * Continued to watch [A-Frame playlist](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) for 15 minutes
* Added `<a-entity>` - with attributes - and `<a-camera>` to my existing scene
  *  I also added atrributes to the `<a-entity>` tag, specifically `position` and `camera-active`
```HTML
<a-entity position= "0 0 10" camera="active: true">
    <a-camera></a-camera>
    </a-entity>
```
* NOTE: `<a-entity>` is similar to a `div` - any element within the tag when there is a class or attribute applied will also be affected
* Tested the `repeat`, `normal-map`, and `normal-map-repeat` attribute toward my `<a-plane>` tag:
```HTML
<a-assets>
<img src="img/wooden-floor.jpg" id="h8">
</a-assets>
<a-scene>
  <a-plane
    material= "repeat: 5 5;
    normal-map: #h9;
    normal-map-repeat: 5 5;"
    scale="35 35 1"
    rotation="-90 0 0"
    position="0 -3 0"
    src="#h8">
    </a-plane>
</a-scene>
```

* NOTE #2: The `repeat` attribute purpose is in its name. The attribute "repeats" a texture based on the X and Y axis as in the format (x y) - must be inside `material`

  * The `normal-map` and `normal-map-repeat` attributes combined with `repeat` is mainly served to make realistic grounds - high detail.
* Utilized the `metalness` attribute on my `a-sphere` primitives:

``` HTML
 <a-sphere src="#h3" position="10 2 0" scale="2 2 2" metalness="1"></a-sphere>
 <a-sphere src="#h6" position="0 2 0" scale="2 2 2" metalness="1"></a-sphere>
 <a-sphere src="#h7" position="-10 2 0" scale="2 2 2" metalness="1"></a-sphere>
```
* NOTE #3: The `metalness` attribute gives a tint to the spheres as the value increases. This is to make the primitives look more of a metal texture as the function is stated by its name.
* I also tried out the `fog` attribute on `<a-scene>` using this code:
``` HTML
<a-scene fog="true"></a-scene>
```
* NOTE #4: `fog` applies smoke to a given scene.
  * The attribute can also be adjusted with distance, controlling the visibility.
* Next steps:
  * Continue to watch the [A-Frame](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) playlist as I move to focus on other concepts (possibly video and sound)
  * Keep up with my tinkering process

---
**3/22/24**

Aim: Practice more A-Frame conceptions, specifically learning about implementing video and audios

* Continue to watch [A-Frame](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) playlist, primarily focusing on the video and audio videos
* Imported a video file through GitHub and inserted in `<a-assets>`
  * Added an `autoplay loop` attribute and set it to "true", making the visual repeat on its own

```HTML
<a-assets>
<video id="hi" src="video/3d-monochrome-abstract-art-video-animation-featuring-a-surreal-chrome-sphere-c-SBV-348789757-preview.mp4" autoplay loop="true"></video>
</a-assets>
```
* Created a video in my `<a-scene>` using the `<a-video>` tag and adjusted the size following with position using the `width`, `height`, and `position` attribute:

``` HTML
 <a-video src="#hi" width="8" height="4.5" position="0 10 0">
    </a-video>
```
* Subsequently, I added another video following the same process. I aligned the two panels side-by-side.
  * NOTE #1: JavaScript can also be applied for videos if you choose to use play and pause buttons.
``` HTML
<a-assets>
<video id="hi2" src="video/shapes-moving-synergy-texture-abstract-animated-background-with-moving-geometr-SBV-348787527-preview.mp4" autoplay loop="true"></video>
</a-assets>
```
* I tested out the audio portion of A-Frame by uploading sound files first
  * I used this line of code to make an audio functionable:

``` HTML
 <a-sound src="src: url(video/sound1.wav)" autoplay="true" loop="true" position="0 2 5"></a-sound>

```
* `src` was the most promienent tag for this moment. The label allowed my sound file to exist.
   * Included `loop="true"` to make the sound repeat itself, similar to my videos
* NOTE #2: Audio can be used in a diverse amount of ways. Primitives can also use the tag to display a sound when clicked on.
* NOTE #3: Any audio can be adjusted using the `volume` and `on` attributes.

Goal for next time:

* Continue to tinker and enhance my knowledge of A-Frame
* Introduction to new topics (likely collisions and physics)
---
**3/25/24**

Aim: To focus on the Physics and Collisions topic of A-Frame

* Watched a [Physics and Collisions](https://www.youtube.com/watch?v=CsXNfoXEJ2w) lesson video
* Looked over the [Physics system page](https://github.com/c-frame/aframe-physics-system) on GitHub provided by A-Frame
* Imported extra scripts that allows for a physics package to be installed

``` HTML
<script src="https://cdn.jsdelivr.net/gh/MozillaReality/ammo.js@8bbc0ea/builds/ammo.wasm.js"></script>
<script src="https://cdn.jsdelivr.net/gh/c-frame/aframe-physics-system@v4.2.2/dist/aframe-physics-system.js"></script>
```

* The first script in the code snippet is the `ammo engine` - it includes JavaScript that supports physics.
* Classified the engine I am using for physics and collisions in my `a-scene` tag using this code:
  * Additionally added `debug` to `<a-scene>`
``` HTML
<a-scene physics="driver: ammo; debug:true;"></a-scene>
```
* NOTE #1: `debug` creates a wireframe for all entities
* Started testing the features out on a few primitives: three `<a-sphere>`. I applied various classes in the process:

```HTML
<a-sphere src="#h3" position="10 5 0" scale="2 2 2" ammo-body="type: dynamic;" ammo-shape="type:sphere">
    </a-sphere>
    <a-sphere src="#h6" position="0 5 0" scale="2 2 2" ammo-body="type: dynamic;" ammo-shape="type:sphere"></a-sphere>
    <a-sphere src="#h7" position="-10 5 0" scale="2 2 2" ammo-body="type: static;" ammo-shape="type:sphere"></a-sphere>
```
* NOTE #2: A primitive with the `dynamic` class will typically move during a collision, and is usually affected by gravity.
  * NOTE #3: A entity with the `static` class will not move when another object strikes, nor is it affected by gravity.
* Added the `static` class towards my `<a-plane>` so the sphere primitives would not fall through the floor and instead stop on the platform.

  * This code helped with the process:
``` HTML
<a-plane ammo-body="type: static" ammo-shape="type:box"></a-plane>
```
* Lastly, included the `restitution` class to the `<a-scene>` tag to increase bounciness of the `<a-sphere>` primitives:
```HTML
<a-scene physics="driver: ammo; restitution: 1">
```
* NOTE #4: The `restitution` class must be set to a value above 0 to work. As the number increases higher, the primitive will bounce more. 

For next time:
- Learn to import 3D models into A-Frame
- Continue to tinker along with videos
<!--

X/X/X:
* Text

* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next





- mainly Camera Primitive
-->

