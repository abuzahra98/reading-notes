# MUSTACHE and FLEXBOX
2
***Javascript Templating***
3
JavaScript templating refers to the client side data binding method implemented with the JavaScript language. This approach became popular thanks to JavaScript’s increased use, its increase in client processing capabilities, and the trend to outsource calculus to the client’s web browser. Popular JavaScript templating libraries are AngularJS, Backbone.js, Ember.js, Handlebars.js, and Mustache.js.
@Dana-Kiswani
Create Read-03.md
5 months ago
4

@Dana-Kiswani
Update Read-03.md
5 months ago
5
The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.
6

7
***Mustache***
8

9
Mustache can be used for HTML, config files, source code - anything. It works by expanding tags in a template using values provided in a hash or object.
10

11
We call it "logic-less" because there are no if statements, else clauses, or for loops. Instead there are only tags. Some tags are replaced with a value, some nothing, and others a series of values. This document explains the different types of Mustache tags.
12

13
Tags are indicated by the double mustaches. {{person}} is a tag, as is {{#person}}. In both examples, we'd refer to person as the key or tag key.
14

15
If you intend you use mustache with Node and Express, you can use mustache-express. Mustache Express lets you use Mustache and Express together easily.
16

17
mustache.js is an implementation of the mustache template system in JavaScript. It is often considered the base for JavaScript templating.
18

19
***Flexbox***
20

21
Flexbox is a one-dimensional layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces. In other words, Flexbox Layout aims at providing a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic.
22

23
<hr>
24

25
***Properties for the Parent (flex container)***
26
* display.
27

28
*This defines the parent as a flex container*
29

30
``` ruby
31
.container {
32
     display: flex; /* or inline-flex */
33
 }
34
```
35
36
* ***flex-direction*** To establishe the main-axis.
37
38
``` ruby 
39
.container {
40
   flex-direction: row | row-reverse | column | column-reverse;
41
 }
42
 ```
43
@Dana-Kiswani
Update Read-03.md
5 months ago
44
-row (default): left to right in ltr; right to left in rtl
45
-row-reverse: right to left in ltr; left to right in rtl
46
-column: same as row but top to bottom
47
-column-reverse: same as row-reverse but bottom to top
@Dana-Kiswani
Update Read-03.md
5 months ago
48
49
* flex-wrap
50
By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.
51
52
``` ruby 
53
 .container {
54
    flex-wrap: nowrap | wrap | wrap-reverse;
55
  }
56
  ```
57
  
@Dana-Kiswani
Update Read-03.md
5 months ago
58
-nowrap (default): all flex items will be on one line
59
-wrap: flex items will wrap onto multiple lines, from top to bottom.
60
-wrap-reverse: flex items will wrap onto multiple lines from bottom to top.
@Dana-Kiswani
Update Read-03.md
5 months ago
61
62
* flex-flow
63
64
This is a shorthand for the flex-direction and flex-wrap properties, which together define the flex container’s main and cross axes. The default value is row nowrap.
65
66
``` ruby
67
.container {
68
   flex-flow: column wrap;
69
 }
70
 ```
71
 <hr>
72
 
73
***Properties for the Children (flex items)***
74
* ***order*** By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.
75
76
```ruby
77
.item {
78
  order: 5; /* default is 0 */
79
}
80
```
81
82
* flex-grow
83
84
This defines the ability for a flex item to grow if necessary. If all items have flex-grow set to 1, the remaining space in the container will be distributed equally to all children.
85
86
``` ruby
87
.item {
88
   flex-grow: 4; /* default 0 */
89
 }
90
 ```
91
 
92
* flex-shrink
93
94
This defines the ability for a flex item to shrink if necessary.
95
96
``` ruby
97
.item {
98
  flex-shrink: 3; /* default 1 */
99
}
100
```
101
102
* flex-basis
103
104
This defines the default size of an element before the remaining space is distributed. The auto keyword means “look at my width or height property”:
105
106
``` ruby
107
.item {
108
   flex-basis:  | auto; /* default auto */
109
 }
110
 ```
111
 
112
* flex
113
114
This is the shorthand for flex-grow, flex-shrink and flex-basis combined. The second and third parameters (flex-shrink and flex-basis) are optional. The default is 0 1 auto, but if you set it with a single number value, it’s like 1 0.
115
116
``` ruby
117
.item {
118
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
119
}
120
```