# Entry 4
##### 2/13/24

### Context

After spending time finishing Part A and B of the Freedom Project in the past few weeks, I reached a new stage - to choose a tool that I will include in my future webpage.

### Choosing A Tool

Reaching the tool selection portion of the Freedom Project, I made a list of the desirable ones I wanted to use. As for choosing a specific tool to find out which one was the best fit for me, I had to tinker along with them. The top three tools I chose were: A-Frame, Skeleton, and SASS.

To begin with my selection process, I started tinkering with SASS first. For the tool, I used a [coding playground](https://www.codingame.com/playgrounds/166/sass) to gain a better knowledge of. The page included to-be completed assignments with instructions provided, as well as the option to create own examples given the code boxes.

For my part, I mainly focused on the given assignments first before making a commitment to go deeper into the learning process. This was because I wanted to get a reaction prior, as I was still unfamiliar with the tool.

I began by reading all of the instructions for each task. After a while, I managed to complete all of the tasks by switching back and forth to the details provided for each concept and working in the coding box. Here is one assignment (Variable Topic) I completed:

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

The assignment above required me to make the first two paragraphs equal to `50px`in terms of height. I was given information for the concept behind variables, specifically as in the syntax `$name: value;`. To do this task, I created a new variable, `$height` and defined it with `50px`. After that, I checked the HTML portion of the files and found that the two paragraphs are assigned the classes `p-border` and `p-background`, so I went back to CSS and inserted height to both of them, defining the variable in the process. I executed the task, and it was completed.

Overall, my experiment with the SASS assignments left me with a mixed feeling about the tool. I wasn't particularly that interested when learning the resource as I was tinkering, so I didn't dive any deeper. This thought helped shape my list, as I knew SASS wasn't going to be the top choice for me.

The next tool I tested out was Skeleton. The way I tinkered for Skeleton was in my CS50 IDE. This time when I looked over the tool page, however, I noticed that there wasn't a side-by-side tutorial. Skeleton specifically only lists its CSS elements on its page.


For an ideal beginner's lesson on the tool, I followed a [Pythonology video](https://www.youtube.com/watch?v=v4UC9emY9KA). I used the video to my advantage and grabbed key information occasionally. After a while of learning Skeleton, I was able to implement my twists and create an example with Skeleton. 


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
