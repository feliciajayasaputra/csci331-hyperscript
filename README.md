# CSCI 331 Project - Hyperscript
## Group Members: Felicia Jayasaputra and Mico Monks

## Introduction

Our group discusses about Hyperscript Programming Language.....

## Features of Hyperscript:

1. Filter
This filter feature that let you look/search things you want from the list. It uses "show" and "when" to filter things which we can only write it in 2 lines of codes. After the code is done, we can start by typing one letter in the search bar, and this will show the match things in te list.

Example code:
```
<input _="on keyup show <li/> in #color-list
                   when it's innerHTML contains my value">
```

2. Intersection
Intersection feature brings animation to your design. When at least half of the image comes into view, it will become visible. This can be done with the intersecting property and the threshold amount. For example, If it has a threshold of 0.5, its opacity will transition to 1 (visible) when 50% of it is in view. If less than 50% of the image is in view, it does not meet the 0.5 threshold, and its opacity will be 0 (invisible).

Example code:
```
 <img _="on intersection(intersecting) having threshold 0.5
    if intersecting transition opacity to 1
    else transition opacity to 0 " src="styles/fox.jpg" alt="fox">
```

3. "Go" Command
This allows you to navigate the browser to a new location like locally or to new URLs, depending on how it is used. This "Go" command can be used in many things that helps you move stuff. 

Example code:
```
 <button _="on click
    go to the top of the body smoothly
    wait 2s
    go to the bottom of me smoothly">
    Take A Trip
    </button>
```

4. Increment Button
The code for the incrememnt button allows us to add if statements, and increment variables. In the example, we are incrementing x. Once x is greater than 10, we are setting it back to 0. In either case, we will display x in the output below with "put".

Example code:
```
<button _="on click increment :x
                if :x > 10
                    set :x to 0
                    put :x into the next <output/>
                else
                    put :x into the next <output/>
                end">
            Click Me
            </button>
```

5. Countdown and Waiting
This allows you to add time to events and control what happens when. In this simple countdown demo I have made, it utilizes waiting as well as functions such as repeat, hide, and show.

Example code:

```
<button _="on click put 'Started...' into the next <output/>
                hide me
                repeat for x in [3, 2, 1]
                    put x into the next <output/>
                    wait 1s
                end
                put '' into the next <output/>
                show me
    ">
        Start
    </button>
```

6. Color Changing
For the first example, we can change the color of a button on click, without the use of an event handler. As long as we have the id ".red" defined in css, we can toggle it on and off.

Example Code:
```
<button script="on click toggle .red on me">
                Click Me
            </button>
```

WE can also change the color of the entire div. All we're doing here is adding a few lines of Hyperscript to the div that all the text is in, and it changes the background color of everything inside the div. Also note how we can replace "script" with "_".

Example code:
```
<div _="on pointerdown
                            repeat until event pointerup
                                set rand to Math.random() * 360
                                transition
                                    *background-color
                                    to `hsl($rand 100% 90%)`
                                    over 50ms
                            end">
```





URL Link(s)

Group 16
