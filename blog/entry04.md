# Entry 4
##### 2/13/24

### Update/Context

In the past few weeks, I spent time finishing Parts A and B of the Freedom Project. Eventually, I reached a new stage - to choose a tool that I would include in my future webpage - where I would conduct more research.

### Choosing A Tool

Reaching the tool selection portion of the Freedom Project, I made a list of the desirable ones I wanted to use. As for choosing a specific tool to find out which one was the best fit for me, I had to tinker along with them. The top three tools I chose were: A-Frame, Skeleton, and SASS.

To begin with my selection process, I started tinkering with [SASS](https://sass-lang.com/). For the tool, I used a [coding playground](https://www.codingame.com/playgrounds/166/sass) to play around and gain a better knowledge of it. The playground included to-be-completed assignments with instructions provided, as well as the option to create own examples given the code boxes.

For my part, I mainly focused on the assignments first before committing to go deeper into the learning process. This was because I wanted to get a reaction prior, as I was still unfamiliar with the tool. I began by reading all of the instructions for each task. I also reviewed the syntax of the custom codes and tried to see how it functioned. After a while, I managed to complete all of the tasks by switching back and forth between the details provided for each concept and working in the coding box.

Here is one assignment (Variable Topic) I completed:

``` CSS & HTML
// Define variables
$height: 50px;


.wrap p {
	padding: $space;
	margin: $space * 2;
}

.p-border {
	border: dotted 3px $myColor;
	height:$height;
}

.p-background {
	background: rgba($myColor, 0.3);
	height:$height;
}

*HTML*

    <link rel="stylesheet" href="variables.css"/>
<div class="wrap">
	<p class="p-border">A p with a border!</p>
	<p class="p-background">A p with a background!</p>
</div>
}
```

The assignment above required me to make the first two paragraphs equal to `50px` in terms of height. I was given information about the concept behind variables, specifically as in the syntax `$name: value;`. To do this task, I created a new variable, `$height` and defined it with `50px`. After that, I checked the HTML portion of the files and found that the two paragraphs are assigned the classes `p-border` and `p-background`, so I went back to CSS and inserted height to both of them, defining the variable in the process. I executed the task, and it was completed.

My overall experiment with the [SASS](https://sass-lang.com/) assignments left me with a mixed feeling about the tool. **I wasn't particularly that interested** when learning the resource as I was tinkering, so I didn't dive any deeper. This thought helped shape my list, as I knew [SASS](https://sass-lang.com/) wasn't going to be the top choice for me.

Moving forward with the decision, the next tool I tested out was [Skeleton](http://getskeleton.com/). Beginning with my [Skeleton](http://getskeleton.com/) tinkering process, I looked closely at the webpage provided by the developers. This time when I observed over the tool page, however, I noticed that there wasn't a side-by-side playground for a tutorial. [Skeleton](http://getskeleton.com/) only list its CSS elements in brief detail and a download button on its page.

For a beginner's lesson on the tool, I followed a [Pythonology video](https://www.youtube.com/watch?v=v4UC9emY9KA). I used the video to my advantage, occasionally grabbing information that were important. While listening to the video and constantly engaged, I was gradually able to use some of the topics mentioned and implement my twists and create an about me page with [Skeleton](http://getskeleton.com/) on CS50. Here is a visual:

![Untitled drawing (6)](https://github.com/joez2450/sep10-freedom-project/assets/146861465/3757f136-68fc-4040-8261-a16b998e5f91)

In the page I created, I first created a repository and inputted the CDN for Skeleton in my HTML file, then used a variety of `divs` to create a container and rows. After that, I added an `h3` element with the text "About Me" into the second `div` element, holding the class "row nav". I later included a "row" class into the third `div` and subsequently added two more `div` with the class "six columns" to make separate columns that each take up half of the space in the container. Afterward, I created a `p`, `ul`, and `li` elements, and typed in my basic information. Once that was done, I created a form using the `form`,   `label`, `option`, and `button` elements. I included the placeholder text in the form and also went to the CSS file and added `padding` along with `font-size` to specific elements so I could adjust the positioning and size of them. During the process, I constantly used `http-server` to see my changes. For the final step, I added a `@media` query, so that when a smaller device views the page, everything will be responsive.


In my experience with Skeleton, **I was more satisfied with the tool compared to SASS**. However, **I will not be using it for my Freedom Project as it is relatively similar to BootStrap** - another tool dedicated to web design which I will use already, with the features only being a miniature version.

[A-Frame](https://aframe.io/) was the last tool to be tested. For [A-Frame](https://aframe.io/), I first checked their webpage for additional information, similar to my approach for [Skeleton](http://getskeleton.com/). The page included documentation and a tutorial for beginners. The tool also had multiple alternatives to be inputted through its script, one being Jsbin. My initial reaction to the tool was off to a positive start, as the basic information was brief.

On my end, to start with my [A-Frame](https://aframe.io/) tinkering, I set up my workplace in my CS50 IDE, creating a new HTML in my `tool-practice` repository and importing the CDN link through the `script` tag. My next step involved carefully reading the Introduction portion of the website, subsequently looking at the "Building a Basic Scene". As I continued to take in the large amount of provided information, I started to gain more knowledge of the custom elements of [A-Frame](https://aframe.io/). Eventually, I was able to create simple examples that I desired. Here is one example I created:

![Untitled drawing (5)](https://github.com/joez2450/sep10-freedom-project/assets/146861465/9ef23a9b-2637-49ec-9684-677a276b312d)

For my example, I wanted a square with a space in the middle that is surrounded by a forest environment with a template text beside it. To begin coding, I first used the `<a-box>` element repeatedly and created eight boxes. I gave each `<a-box>` element a style class of different colors to make all of the box's appearance different. The positioning section was relatively difficult. I didn't understand the concept behind positioning, however, I returned to the "Build a Basic Scene" section of the A-Frame website and reviewed it eventually learning that `x = extends right`, `y = extends up`, and `z = extends forward`. I began trial and error and got the positioning correct after some time. I then used the `<a-entity>` element and included the environment class of forest and dressing amount of one hundred to display a large number of trees. In the end, I used the `<a-text>` element to put a template message beside my creation, additionally using `<a-camera>` to adjust the frame view.


My experience with [A-Frame](https://aframe.io/) was delightful. The tool was pleasant to use and some of the challenges I faced were fun to solve along my way of tinkering. As for my tool selection, **I will be using A-Frame**.

### Skills
My process for choosing a specific tool to use for my Freedom Project helped me learn new skills while also enhancing my previous ones. These include:

#### Decision-Making/Analysis
 During this stage of the Freedom Project, I had three tools that I wanted to use. However, I could only use one of the three tools, meaning I had to reduce the number that I had down to a single one. I was able to achieve a singular tool through a process of deep analysis - tinkering and finding every small aspect of each tool to see which one best fit me. The entire procedure enhanced my decision-making skills and also helped me learn how to analyze specific objects.

#### Time Management
Time management was a skill that I learned progressively throughout my process of choosing a permanent tool for the Freedom Project. At the very beginning of the stage, I had three tools to tinker with. There was an immense amount of testing to do. As a solution, I developed a method to gain an initial reaction to certain tools before deciding to continue. This allowed me to see which tools were more desirable for me and the ones that were not in a efficient time manner.



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
