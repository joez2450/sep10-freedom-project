# Entry 6
##### 5/1/24

### Update/Context
Following the last blog, I have progressed even more in my Freedom Project. I created multiple wireframes for my Freedom Project. Subsequently, I started the coding portion with my peer, Jimmy, and worked to design a minimal viable product.

### Constructing a MVP for my Freedom Project
Starting the process for building a Travel webpage, my peer and I split the coding sections into various responsibilities. Through our planning, we both split the CSS into two, and I focused on the cards, whereas Jimmy placed more emphasis on the Navbar design. In addition, I was also given the task of making a A-Frame embbeded view.

I first imported CDN links from Bootstrap - CSS and Javascript - and started working on the basic portion of the webpage next. As for the overview, I created a `section` element, followed with `div` including a container, row, and column class. Inside the `div` with the column class, I added a `p` and `h1` element to create a title and mini-context. Afterwards, I moved into making the cards. I wanted the display cards to be both informative and good-looking. So, as I imported the codes for them on Bootstrap, I changed all of the placeholder text, using a prep document made earlier in the year, and fit all of the software and hardware innovations information in it. Along the process, Jimmy and I added commented titles to help guide us through the code later on.

A challenge, however, that came along was the size proportions. Since some cards had more information than the others, the height differences were prominent on the default screen size. This caused the content to be funky in terms of looks. I called my peer for help and after countless solutions, we watched a tutorial and deleted the `style` inline that came along with the imported code. In an instant, the card sizes were equal in length. A visual of the set-code:

``` HTML
 style="width: 30rem;">
```
As the cards were created, I moved onto the background image. I wanted a visual regarding travel such as a destination to be the first sight on the website. To do this, I went into the CSS file and created a new class called `background` and added properties such as `background-image`, `background-repeat`, `background-size`, `height`, and `width`. I added values to all of the CSS properties, inputting the URL towards the `background-image`, a value of cover to `background-size`, no-repeat to `background-repeat`, and set the `height` to 750px with the `width` being auto. I also added various `div` to display the CSS. The image was completed with the codes. A visual of the code:

```CSS & HTML
  <section>
  <div class="background width" id="Home">
    <div class="container">
      <div class="row">
        <div class="col">
          <p style="font-size:110px; text-align:center; color:white; padding-top:230px;">Travel </p>
        </div>
      </div>
    </div>
  </div>
  </section>

.background {
    background-image: url(img/sunset.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height:750px;
    width:auto;
}

```

Reaching the A-Frame section, my peer and I desired to make a VR-scene directly on our webpage. As this goal was planned, I didn't have prior knowledge to reach our satisfication. I used [W3schools](https://www.w3schools.com/tags/tag_iframe.ASP) and found a section regarding the specific topic. I looked over the details provided and later on, created my own example. I created a `iframe` element in my HTML file and added `style` inline including `padding` and within CSS, media queries to make it responsive. Here is a overview of the code I created:


``` HTML
<section class="white">
<h1 style="text-align:center; padding-top:50px;">A-Frame Model (our visual):</h1>
<iframe src="model.html" title="Visual"></iframe>
</section>
 ```
After the cards and A-Frame embedded were completed, Jimmy and I both focused on decorating the website. Choosing a color scheme was difficult, however, my peer eventually used a linear gradient of two colors: white and light brown. In addition, I added more `margin` and `padding` to specific elements for proper spacing and a better visual of the content. At last, we finished designing a MVP.


### EDP
In the Engineering Design Process, I am at the fifth stage: Create a Prototype. I have already designed a viable webpage with my peer for the Freedom Project. In the future, I will move onto the sixth and seventh stages, where further improvements and testing are made. These specifically include the responsiveness of the website, as some content are in undesirable spots within different screen sizes.

### Skills
I learned two primary skills with my partner while constructing our first website prototype. These include:

#### Organization
Throughout the course of the coding process, I learned to be organized with my peer. Given there were many lines of codes, various BootStrap components imported, and constant flows of merging, it was easy to get lost in the HTML file. We stayed arranged by using the comment (`<!-->`) feature and adding names within them.

#### Creative-Thinking
As my peer and I were coding especially in the decoration process, we needed to find a color scheme that was fit towards our webpage. We struggled to find one that was good-looking with our content. However, after countless attempts, Jimmy eventually brainstormed to use a brigther layout.


[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)



<!--
accumulated my initial move was to delete the `style` inline that placed a set-width.>
