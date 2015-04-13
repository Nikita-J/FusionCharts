---
permalink: usage-guide/annotations/creating-annotations/introduction.html
title: Introduction
chartPresent: false
---

## Prerequisites

* [Creating a simple chart using FusionCharts Suite XT]{% linkTo tutorials/getting-started/your-first-charts/building-your-first-chart.md %}

* [Introduction to annotations]{% linkTo tutorials/annotations/introduction.md %}

FusionCharts Suite XT includes a wide range of [charts, gauges, and maps](http://www.fusioncharts.com/charts/) that you can use to plot static as well as real-time data. Annotations, a compelling feature of the product, lets you make your charts self-descriptive and visually engaging.

This article:

* Tells you about the different types of annotation items available

* Describes the objects used to create annotations

## Annotation Items

Annotations are graphical elements-text, images, shapes-that you can use to customize your chart.

You can add the following types of annotations to your chart:

* Text (custom notes, labels, or paragraphs of text)

* Image (external images)

* Shapes (rectangle, polygon, circle, arc, and line)

* Path connectors (free-form arrows, connectors, callouts, and so on)

The image of a chart rendered with different types of annotations items is shown below:

![image alt text]({{ site.baseurl }}assets/images/advanced-charting-annotations-creating-annotations-image-1.jpg)

The basic JSON structure to create annotations is shown below:

{% highlight javascript lineanchors %}{% raw %}
{
    "chart": {
        ...
    },
    "annotations": {
        "groups": [{
        		//Annotation group 1
            	//Define a unique identification string for the group.
                "items": [
                	//Define individual annotation items.
                    {//Annotation Item 1},
                    {//Annotation Item 2},
                    ...
                    {//Annotation Item *n*}
                ]
            }, {
            	//Annotation group 2
            	//Define a unique identification string for the group.
                "items": [
                	//Define individual annotation items.
                	{//Annotation Item 1},
                	{//Annotation Item 2},
                	...
                    {//Annotation Item *n*}
                ]
            },
            ...
             {
            	//Annotation group *n*
            	//Define a unique identification string for the group.
                "items": [
                	//Define individual annotation items.
                    {//Annotation Item 1},
                    {//Annotation Item 2},
                    ...
                    {//Annotation Item *n*}
                ]
            },
        ]
    }
}
{% endraw %}{% endhighlight %}

## Objects Used to Create Annotations

The `annotations`, `groups`, and `items` objects are used to create annotations.

A brief description of these objects is given in the table below:

<table>
  <tr>
    <th>Object</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>`annotations`</td>
    <td>An object that encompasses all the code for generating annotations.</td>
  </tr>
  <tr>
    <td>`groups`</td>
    <td>An object array that consolidates multiple annotations into one group. You can create multiple annotation groups for one chart. Grouping annotations is useful when a complex graphic is created using individual annotation items.

This is covered in detail in the subsequent articles.</td>
  </tr>
  <tr>
    <td>`items`</td>
    <td>An object array that defines individual annotation items that will be contained in one annotation group.</td>
  </tr>
</table>


To know how to create the different types of annotations, refer the following articles:

* [Creating Text Annotations]{% linkTo tutorials/annotations/creating-annotations/creating-text-annotations.md %}

* [Creating Image Annotations]{% linkTo tutorials/annotations/creating-annotations/creating-image-annotations.md %}

* [Creating Shape Annotations]{% linkTo tutorials/annotations/creating-annotations/creating-shape-annotations.md %}

* [Creating Path Annotations]{% linkTo tutorials/annotations/creating-annotations/creating-path-annotations.md %}

