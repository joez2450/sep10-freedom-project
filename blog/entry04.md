# Entry 4
##### 2/13/24

### Context

After spending time finishing Part A and B of the Freedom Project in the past few weeks, I reached a new stage - to choose a tool that I will include in my future webpage.

### Choosing A Tool

Reaching the tool selection portion of the Freedom Project, I made a list of the desirable ones I wanted to use. As for choosing a specific tool to find out which one was the best fit for me, I had to tinker along with them. The top three tools I chose were: A-Frame, Skeleton, and SASS.

To begin with my selection process, I started tinkering with [SASS]() first. For the tool, I used a [coding playground](https://www.codingame.com/playgrounds/166/sass) to gain a better knowledge of it. The page included to-be-completed assignments with instructions provided, as well as the option to create your examples given the code boxes.

For my part, I mainly focused on the assignments first before committing to go deeper into the learning process. This was because I wanted to get a reaction prior, as I was still unfamiliar with the tool. I began by reading all of the instructions for each task. I also reviewed the syntax of the custom codes and tried to see how it functioned. After a while, I managed to complete all of the tasks by switching back and forth between the details provided for each concept and working in the coding box. Here is one assignment (Variable Topic) I completed:

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

 My experiment with the SASS assignments left me with a mixed feeling about the tool. **I wasn't particularly that interested** when learning the resource as I was tinkering, so I didn't dive any deeper. This thought helped shape my list, as I knew SASS wasn't going to be the top choice for me.

Moving forward with the decision, the next tool I tested out was [Skeleton](http://getskeleton.com/). Beginning with my Skeleton tinkering process, I looked closely at the webpage provided by the developers. This time when I looked over the tool page, however, I noticed that there wasn't a side-by-side playground for a tutorial. Skeleton only lists its CSS elements in brief detail and a download button on its page.

For an ideal beginner's lesson on the tool, I followed a [Pythonology video](https://www.youtube.com/watch?v=v4UC9emY9KA). I used the video to my advantage, as I specifically grabbed key information occasionally. While listening to the video and constantly learning, I was able to implement my twists and create an About Me page with Skeleton on CS50. Here is a visual:

![Untitled drawing (3)](https://github.com/joez2450/sep10-freedom-project/assets/146861465/2adcd319-d413-4eb4-9643-7a8c12ee709b)


In the example I created, I first inputted the CDN for Skeleton in my HTML file and then used a variety of `divs` to create a container and rows. After that, I added an `h3` element with the text "About Me" into the second `div` element, holding the class "row nav". I later included a "row" class into the third `div` and subsequently added two more `div` with the class "six columns" to make separate columns that each take up half of the space in the container. Afterward, I created a `p`, `ul`, and `li` elements, and typed in my basic information. Once that was done, I created a form using the `form`,   `label`, `option`, and `button` elements. I included the placeholder text in the form and also went to the CSS file and added `padding` along with `font-size` to specific elements so I could adjust the positioning and size of them. During the process, I constantly used `http-server` to see my changes. For the final step, I added a `@media` query, so that when a smaller device views the page, everything will be responsive.


For my experience with Skeleton, **I was more satisfied with the tool compared to SASS**. However, **I will not be using it for my Freedom Project, as it is similar to BootStrap**, another tool dedicated to web design, which I will use already.





[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
