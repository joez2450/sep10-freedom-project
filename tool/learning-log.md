# Tool Learning Log

Tool: **A-Frame**

---

2/26/24: **A-Frame Day 1**

Goal: To gain a better understanding of the basic A-Frame concepts

Steps:
* I followed an [A-Frame tutorial playlist](https://www.youtube.com/playlist?list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV) for roughly 25 minutes
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
* Positioning was relatively difficult for me. I specifically didn't understand the function of the z-value. To find out my misconception, I executed trial and errors processes in my IDE, along with looking at a visual diagram. Eventually, I learned that the z-value mainly applies to the viewer's perspective of "back and forth".

* I additionally learned the `<a-sky>` and `<a-entity>` element and used it in my example:
```HTML
<a-sky color="blue"></a-sky>
<a-entity environment="preset: forest; dressingAmount: 100"></a-entity> (Needs separate CDN link)
```
* `<a-entity>` is for background use and `<a-sky>`
is generally utilized for the change of atmosphere in the VR experience

NOTE: `<a-entity>` overides `<a-sky>` - for example, when both tags are used within `a-scene` only one result between the two will show up.


**Goal for next time:** Learn more attributes for tags

X/X/X:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
