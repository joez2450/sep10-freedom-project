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
* Adding primitives inside `a-scene` tags -->
```HTML
<a-box></a-box>
<a-sphere><a-sphere>
<a-cylinder></a-cylinder>
```
* Adjusting primitives with color, [positioning](https://aframe.io/docs/1.5.0/components/position.html), [scale](https://aframe.io/docs/1.5.0/components/scale.html), and [rotation](https://aframe.io/docs/1.5.0/components/rotation.html) attributes
    * X-value = left and right, Y-value = up and down, Z-value = front and back

```HTML
  <a-scene>
    <a-box color="red" rotation="10 10 35" position="0 0 -10" scale="2 2 2"></a-box>
    <a-sphere color="green" position="-7 0.5 -10" scale="2 2 2"><a-sphere>
    <a-cylinder color="orange" position="8 -1 0" scale="1.5 2 2"></a-cylinder>
  </a-scene>
```
* Positioning was relatively difficult for me. I specifically didn't understand the function of the z-value.

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

----------------------------------------------------------------------------

**3/3/24**

Goal: To learn more about A-Frame attributes and general concepts
* Continue to watch [A-Frame tutorial playlist](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) for 15 minutes
* Adding a green platform (ground component) to my existing A-Frame scene

   ```HTML
   <a-plane material="color: #53C532" scale="10 10 1" rotation="-90 0 0"></a-plane>
   ```

     * The attribute `material` allows you to specify a primitive's look (color, texture, etc)

NOTE: Any rotation on primitives directly affects the direction in which the scale - X, Y, Z - value faces

 * The example I created has a rotation of `"-90 0 0"`

   * Only the x-axis is rotated by -90 degrees, so as a result:

      * Scale values - `x = x`, `y = z`, `z = y`

* Applying an image to `<a-plane>`, `<a-box>`, `<a-sphere>`, and `<a-cylinder>`
``` HTML
<a-assets>
  <img src="img/grass_1.png" id="h1">
</a-assets>
 <a-plane material="color: #53C532" scale="10 10 1" rotation="-90 0 0" src="#h1"></a-plane>
```

* Adding a 360° image within the `<a-assets>` and `<a-scene>` tag to represent the sky -->

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

NOTE:  The `radius` attribute is similar to the `border-radius` in CSS. Both of the `radius` makes an item more round.

Goal for next time: Learn more about primitives and continue to explore attributes
<!--X/X/X:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->

