# Entry 5
##### 4/8/24

### Update/Context
Since the last blog, I have achieved a margin of accomplishments in my Freedom Project. I tinkered with my selection of tools (Skeleton, A-Frame, and SASS) in various files by coding example templates. Based on my experimentations, I ended up choosing A-Frame as my permanent tool. Upon the decision, I had to familiarize myself of the engine.

### Tinkering
Beginning with my A-Frame tinkering process, I looked over the documentation provided by the software company. As I analyzed all of the concepts, the three main topics that interested me were importing 3D Models and Images, Physics and Collisions, and Video. But before I tested reached the subjects, I tested additional components for more context of how the tool functioned.

In my IDE, I began by importing the A-Frame CDN link for all of the features to work. I then pasted a skeleton base for A-Frame, which included the tags: `(html),(head),(body), and (a-scene)`. Afterwards, I watched a [introductory video](https://www.youtube.com/watch?v=j-dlO71Gsqk&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=3) about A-Frame placed the first primitives (shapes) into my VR scene using these lines of code: `<a-sphere position="10 2 0"></a-sphere> <a-box position="0 2 0"></a-box> <a-sphere
 position="-10 2 0"></a-sphere>`. At last, the next element I used was `<a-plane>` and `<a-sky>`. For this component I utilized the `rotation` property to make a platform. I added more touches using the `color` attribute, following with `scaling`.

 Once I learned the basics of A-Frame, I moved on to the more complex points. I first focused on importing images. I followed a [brief tutorial](https://www.youtube.com/watch?v=NYvYFtHReuE list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=8) made by a A-Frame expert. As I looked through the informative recording, certain points became more clear. I looked over multiple 8-ball image and downloaded all of the files. During this process, I ensured that the images would fully wrap around a sphere primitive to give a better view. After searching and finding suitable visuals, I imported the downloads into GitHub and used the same code in the video. I also added additional attributes to give the shapes a distint look:

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
As I learned how to put images in a VR scene, my next focus was on importing 3D models and installing videos. For this section, I mainly focused on two Youtube recordings: [Video](https://www.youtube.com/watch?v=5KjyTU07EHo&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=25&t=190s) and [Loading and Displaying 3D Models](https://www.youtube.com/watch?v=cS8uGfd_oG8&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=13). I watched the videos, and progressively, learned the methods for uploading videos and 3D models into GitHub. In my A-Frame scene, I created my own examples. Within the `<a-assets>` tag,






[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
