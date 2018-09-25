---
layout:     post
title:      Intro to Processing
date:       2018-09-28
summary:    Setting up and using processing for the first time.
categories: cst
---

## The Processing Environment
To learn the fundamentals of programming we will be using Processing, a scripting langauge which uses Java as its backbone. If you download Processing, you will download both the required environment for Processing and an editor,
so you will not need to install a seperate editor/IDE (Integrated Development Environment). Processing uses files called 'sketches' that use save to a directory called your 'sketchbook'. Each program rquires its own folder, 
so programs with multiple files will be be located all in one folder.

## Setting Up Your First Program
When launching Processing, the file will either be empty or it will already have some code written. Either way we want to start with this basic format:
```processing
void setup()
{
}

void draw()
{
}
```
A Processing program has two parts as seen above: a 'setup' part and a 'draw' part. The 'setup' part is only executed once, so most of your initializations will go there. The 'draw' part is executed as a loop,
so it runs multiple times each second. Here, data can be changed over time based on different conditions, and all drawing code should be placed here.

## Processing Syntax
The syntax for Processing is similar to many other languages, but if you have never programmed before, it may look weird. Here are some syntax rules to start with:
*A line of code ends with a semi-colon, similar to how sentences end with periods
*Using Processing functions, or tools, requires entering the tool keyword followed by open parentheses, our inputs, then closed parentheses. It should look like this: `tool(myInput);'
As we learn more, there will be more syntax rules to learn, but for now that is all you need to know.

## A Simple Program
We are going write a simple program that draws a red rectangle over a blue background. Our setup should look like this:
```processing
void setup()
{
	size(800, 600);
}
```
Nothing fancy there, just changing the window size to 800px by 600px. Next is the code for drawing:
```processing
void draw()
{
	background(0, 0, 255);
	fill(255, 0, 0);
	rect(100, 100, 200, 150);
}
```
The three parts to drawing our rectangle are setting the background color, setting the rectange color, and drawing the rectangle with a specified size at specified coordinates.
The `background` function accepts three comma seperated values for the background color in the format R,G,B (Red, Green, Blue). Each RGB value is limited to the range 0-255. 
Our input of (0, 0, 255) represents a blue color, since blue has the only and highest value.
The `fill` function also uses the RGB format as an input, but this function tells our program to fill the next shape with the specified color.
Finally we have the `rect` function to draw our rectangle. This function accepts 4 values: the x coordinate, the y coordinate, a width, and a height. 
**Important**: Processing does not use the standard cartesian coordinate system. Instead, lower values correspond to a position closer to the top-left, and higher values correspond to a position closer to the bottom-right. Our input was (100, 100, 200, 150),
so we are drawing a rectangle at (100, 100) with a width of 200px, and a height of 150px.
*Side Note*: `background`, `fill`, and `rect` are pieces fo code called functions. Functions are pieces of code that take inputs and use them to execute multiple lines of other code.
We will see that using these will help us write clean code and prevent unneccesary work.



