

 # Transforms

 *The transform property* comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

 ``div {``
  ``-webkit-transform: scale(1.5);``
    `` -moz-transform: scale(1.5);``
       ``-o-transform: scale(1.5);``
          ``transform: scale(1.5);``

``}``

## 2D Transforms

Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. 

Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth.

- 2D Rotate
  
  he transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees.

  ``<figure class="box-1">Box 1</figure>``
  ``<figure class="box-2">Box 2</figure>``



``box-1 {``
 `` transform: rotate(20deg);``
``}``
``.box-2 {``
`  transform: rotate(-55deg);`
`}`

- Transform Origin

The transform-origin property can accept one or two values. When only one value is 

specified, that value is used for both the horizontal and vertical axes. If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.

``.box-1 {``
``  transform: rotate(15deg);``
``  transform-origin: 0 0;``
``}``
``.box-2 {``
 `` transform: scale(.5);``
 `` transform-origin: 100% 100%;``
``}``
``.box-3 {``
  ``transform: skewX(20deg);``
  ``transform-origin: top left;``
``}``
``.box-4 {``
``  transform: scale(.75) translate(-10px, -10px)``;
  `transform-origin: 20px 50px;`
``}``

## 3D Translate

Elements may also be translated on the z axis using the translateZ value. A negative value here will push an element further away on the z axis, resulting in a smaller element. Using a positive value will pull an element closer on the z axis, resulting in a larger element.

``.box-1 {``
  ``transform: perspective(200px) translateZ````(-50px);``
``}``
``.box-2 {``
``  transform: perspective(200px) translateZ````(50px);``
`}`

- Shorthand 3D Transforms
  As with combining two-dimensional transforms, there are also properties to write out shorthand three-dimensional 
  
  transforms. These properties include rotate3d, scale3d, transition3d, and matrix3d. These properties do require a bit more math, as well as a strong understanding of the matrices behind each transform.

  ``.rotate {``
``  transform: perspective(200px) rotateY(45deg);``
`}`
``.three-d {``
 `` transform-style: preserve-3d;``
``}``
``.box {``
  ``transform: rotateX(15deg) translateZ(20px);``
  ``transform-origin: 0 0;``
``}``

## Transitions & Animations


Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, `:focus`, `:active`, and `:target `pseudo-classes.


There are four transition related properties in total:

1- ransition-property, 
2- transition-duration 
3- transition-timing-function
4- transition-delay

`.box {`
`  background: #2db34a;`
 ` transition-property: background;`
 ` transition-duration: 1s;`
 ` transition-timing-function: linear;`
`}`
`.box:hover {`
`  background: #ff7b29;`
`}`

## Transitional Property

The transition-property property determines exactly what properties will be altered in conjunction with the other transitional 

properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.

If multiple properties need to be transitioned they may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of an element.

`.box {`
  `  background: #2db34a;`
 `   border-radius: 6px`
 `   transition-property: background, ` 
   ` transition-duration: 1s;`
    `transition-timing-function: linear;`
`  }`
  `.box:hover {`
    `background: #ff7b29;`
     `border-radius: 50%;`
`  }`

 ## Transition Duration

 he duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

` .box {`
`  background: #2db34a;`
`  border-radius: 6px;`
  `transition-property: background,` 
  `border-radius`;   
  `transition-duration: .2s, 1s;`
  `transition-timing-function: linear;`
`}`
`.box:hover {`
 ` background: #ff7b29;`
 ` border-radius: 50%;`
`}`

## Animations Keyframes

To set multiple points at which an element should undergo a transition, use the 

@keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

`@keyframes slide `{
`  0% {`
`    left: 0;`
   ` top: 0;`
 ` }`
`  50% {`
  `  left: 244px;`
    `top: 100px;`
  `}`
 ` 100% {`
    `left: 488px;`
    `top: 0;`
 ` }`
`}`

The @keyframes rule must be vendor prefixed, just like all of the other transition and animation properties. The vendor prefixes for the @keyframes rule look like the following:

@-moz-keyframes@-o-keyframes@-webkit-keyframes

- 
Lesson 8
Transitions & Animations
In this Lesson8
CSS
Transitions
Shorthand Transitions
Animations
Customizing Animations
Shorthand Animations
SHARE
Share on Twitter
 
Share on Facebook
 
Share on Google+
ads via Carbon
Learn to build web APIs and applications with Node.js by taking the Frontend Masters Node.js Path. Start now!
ads via Carbon
One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true.

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

Transitions
As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, with the first three are the most popular.

In the example below the box will change its background color over the course of 1 second in a linear fashion.

1
2
3
4
5
6
7
8
9
10
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}

              
Transition Demo

Vendor Prefixes
The code above, as with the rest of the code samples in this lesson, are not vendor prefixed. This is intentionally un-prefixed in the interest of keeping the code snippet small and comprehensible. For the best support across all browsers, use vendor prefixes.

For reference, the prefixed version of the code above would look like the following.


`.box {`
    ``background: #2db34a;``
    `-webkit-transition-property: background;`
     `-moz-transition-property: background;`
    ` -o-transition-property: background;`
    `transition-property: background;`
    `-webkit-transition-duration: 1s;`
    ``-moz-transition-duration: 1s;``
    `-o-transition-duration: 1s;`
     `transition-duration: 1s;`
  ` -webkit-transition-timing-function: ` `linear;`
    ``-moz-transition-timing-function: linear;``  
    ``-o-transition-timing-function: linear;``
   ` transition-timing-function: linear;`
`}`
`.box:hover {`
  `background: #ff7b29;`
`}`

                
- Transitional Property
The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.

In the example above, the background property is identified in the transition-property value. Here the background property is the only property that will change over the duration of 1 second in a linear fashion. Any other properties included when changing an element’s state, but not included within the transition-property value, will not receive the transition behaviors as set by the transition-duration or transition-timing-function properties.

If multiple properties need to be transitioned they may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of an element.

``.box {``
    ``background: #2db34a;``
  `  border-radius: 6px`
    ``transition-property: background, ``
   ` border-radius;`
   ` transition-duration: 1s;`
   ` transition-timing-function: linear;`
  `}`
`  .box:hover {`
 `   background: #ff7b29;`
   ` border-radius: 50%;`
 ` }`

              
- Transition Property Demo

Transitional Properties
It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint. A handful of the more popular transitional properties include the following.

background-colorbackground-positionborder-colorborder-widthborder-spacingbottomclipcolorcropfont-sizefont-weightheightleftletter-spacingline-heightmarginmax-heightmax-widthmin-heightmin-widthopacityoutline-coloroutline-offsetoutline-widthpaddingrighttext-indenttext-shadowtopvertical-alignvisibilitywidthword-spacingz-index
Transition Duration
The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

When transitioning multiple properties you can set multiple durations, one for each property. As with the transition-property property value, multiple durations can be declared using comma separated values. The order of these values when identifying individual properties and durations does matter. For example, the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth.

If multiple properties are being transitioned with only one duration value declared, that one value will be the duration of all the transitioned properties.


              
Transition Duration Demo

Transition Timing
The transition-timing-function property is used to set the speed in which a transition will move. Knowing the duration from the transition-duration property a transition can have multiple speeds within a single duration. A few of the more popular keyword values for the transition-timing-function property include linear, ease-in, ease-out, and ease-in-out.

The linear keyword value identifies a transition moving in a constant speed from one state to another. The ease-in value identifies a transition that starts slowly and speeds up throughout the transition, while the ease-out value identifies a transition that starts quickly and slows down throughout the transition. The ease-in-out value identifies a transition that starts slowly, speeds up in the middle, then slows down again before ending.

Each timing function has a cubic-bezier curve behind it, which can be specifically set using the cubic-bezier(x1, y1, x2, y2) value. Additional values include step-start, step-stop, and a uniquely identified steps(number_of_steps, direction) value.

When transitioning multiple properties, you can identify multiple timing functions. These timing function values, as with other transition property values, may be declared as comma separated values.


`.box {`
`  background: #2db34a;`
`  border-radius: 6px;`
  `transition-property: background, `
 ` border-radius;`
  `transition-duration: .2s, 1s;`
  `transition-timing-function: linear, ease-in;`
`}`
`.box:hover {`
  `background: #ff7b29;`
 ` border-radius: 50%;`
`}`

- Shorthand Animations
Fortunately animations, just like transitions, can be written out in a shorthand format. This is accomplished with one animation property, 

rather than multiple declarations. The order of values within the animation property should be animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode, and lastly animation-play-state.

``.stage:hover .ball {``
``  animation: slide 2s ease-in-out .5s infinite`` 
`alternate;`
``}``
`.stage:active .ball {`
``  animation-play-state: paused;``
``}``





              
Transition Timing Demo

Transition Delay
On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property. The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing. As with all other transition properties, to delay numerous transitions, each delay can be declared as comma separated values.


              
Transition Delay Demo

Shorthand Transitions
Declaring every transition property individually can become quite intensive, especially with vendor prefixes. Fortunately there is a shorthand property, transition, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay. Do not use commas with these values unless you are identifying numerous transitions.

To set numerous transitions at once, set each individual group of transition values, then use a comma to separate each additional group of transition values.



                
Demo

Animations
Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.

Animations Keyframes
To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.


`@keyframes slide {`
`  0% {`
   ` left: 0;`
  `  top: 0;`
  `}`
  `50% {`
    `left: 244px;`
  `  top: 100px;`
`  }`
 ` 100% {`
    `left: 488px;`
   ` top: 0;`
  `}`
`}`

              
Vendor Prefixing the Keyframe Rule
The @keyframes rule must be vendor prefixed, just like all of the other transition and animation properties. The vendor prefixes for the @keyframes rule look like the following:

@-moz-keyframes@-o-keyframes@-webkit-keyframes
The animation above is named slide, stated directly after the opening @keyframes rule. The different keyframe breakpoints are set using percentages, starting at 0% and working to 100% with an intermediate breakpoint at 50%. The keywords from and to could be used in place of 0% and 100% if wished. Additional breakpoints, besides 50%, may also be stated. The element properties to be animated are listed inside each of the breakpoints, left and top in the example above.

It is important to note, as with transitions only individual properties may be animated. Consider how you might move an element from top to bottom for example. Trying to animate from top: 0; to bottom: 0; will not work, because animations can only apply a transition within a single property, not from one property to another. In this case, the element will need to be animated from top: 0; to top: 100%;.

Animations Keyframes Demo
Hover over the ball below to see the animation in action.


- Animation Name

Once the keyframes for an animation have been declared they need to be assigned to an element. To do so, the animation-name property is used with the animation name, identified from the @keyframes rule, as the property value. The animation-name declaration is applied to the element in which the animation is to be applied to.

- Animation Duration, Timing Function, & Delay

Once you have declared the animation-name property on an element, animations behave similarly to transitions. They include a duration, timing function, and delay if 

desired. To start, animations need a duration declared using the animation-duration property. As with transitions, the duration may be set in seconds or milliseconds.

``stage:hover .ball {``
``  animation-name: slide;``
 ` animation-duration: 2s;`
`}`




# 8 examples
1. Fade in

Having things fade in is a fairly common request from clients. It’s a great way to emphasize functionality or draw attention to a call to action.


``.fade``
``{``
       `` opacity:0.5;``
``}``
``.fade:hover``
``{``

2. Change color
   
`   .color:hover`
``{``
``        background:#53a7ea;``
``}``


3. Grow & Shrink

To grow an element, you used to have to use its width and height, or its padding.

`.grow:hover`
`{`
     `   -webkit-transform: scale(1.3);`
        `-ms-transform: scale(1.3);`
        `transform: scale(1.3);`
``}``

4. Rotate elements

CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element.

``.rotate:hover``
``{``
      ``  -webkit-transform: rotateZ(-30deg);``
        ``-ms-transform: rotateZ(-30deg);``
       `` transform: rotateZ(-30deg);``
`}`

5. Square to circle

A really popular effect at the moment is transitioning a square element into a round one, and vice versa. 

``.circle:hover``
``{``
      ``  border-radius:50%;``
``}``

6. 3D shadow

This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.

`.threed:hover`
`{`
     `   box-shadow:`
            `    1px 1px #53a7ea,`
               ` 2px 2px #53a7ea,`
               ` 3px 3px #53a7ea;`
        `-webkit-transform: translateX(-3px);`
        `transform: translateX(-3px);`
`}`


# What Google Learned From Its Quest to Build the Perfect Team

*A classmate* : that some students were putting together teams for ‘‘case competitions,’’ contests in which participants proposed solutions to real-world business problems that were evaluated by judges, who awarded trophies and cash. 

*The competitions were voluntary,*
 but the work wasn’t all that different from what Rozovsky did with her study group: conducting lots of research and financial analyses, writing reports and giving presentations. 
 
 project Aristotle’s researchers 
 reviewing a half-century of academic studies looking at how teams worked. Were the best teams made up of people with similar interests? Or did it matter more whether everyone was motivated by the same kinds of rewards? Based on those studies, 
 

## our data-saturated age

enables us to examine our work habits and office quirks with a scrutiny that our cubicle-bound forebears could only dream of. Today, on corporate campuses and within 

university laboratories, psychologists, sociologists and statisticians are devoting themselves to studying everything from team composition to email patterns in order to figure out how to make employees into faster, better and more productive versions of themselves. 

The company’s top executives long believed that building the best teams meant combining the best people.

## project Aristotle’s researchers 
No matter how researchers arranged the data, though, it was almost impossible to find patterns — or any evidence that the 

composition of a team made any difference. ‘‘We looked at 180 teams from all over the company,’’ Dubey said. ‘‘We had lots of data, 

but there was nothing showing that a mix of specific personality types or skills or backgrounds made any difference. The ‘who’ part of the equation didn’t seem to matter.’’

After looking at over a hundred groups for more than a year, Project Aristotle researchers concluded that understanding and 

influencing group norms were the keys to improving Google’s teams. But Rozovsky, now a lead researcher, needed to figure out which norms mattered most. Google’s research had identified dozens of behaviors that seemed important, except that sometimes the norms of one effective team contrasted sharply with those of another equally successful group.



 **imagine you have**

 been invited to join one of two groups.

Team A is composed of people who are all exceptionally smart and successful. When you watch a video of this group working, you see professionals who wait until a topic arises in which they are expert, and then they speak at length, explaining what the group ought to do. When someone makes a side comment, the speaker stops, reminds everyone of the agenda and pushes the meeting back on track. This team is efficient. There is no idle chitchat or long debates. The meeting ends as scheduled and disbands so everyone can get back to their desks.

What interested the researchers most, however, was that teams that did well on one assignment usually did well on all the others. Conversely, teams that failed at one 


thing seemed to fail at everything. The researchers eventually concluded that what distinguished the ‘‘good’’ teams from the dysfunctional groups was how teammates treated one another. The right norms, in other words, could raise a group’s collective intelligence, whereas the wrong norms could hobble a team, even if, individually, all the members were exceptionally bright.

##  the technology industry 
 
 not just one of the fastest growing parts of our economy; it is also increasingly the world’s dominant commercial culture. 
 The fact that these insights aren’t wholly original doesn’t mean Google’s contributions 
 
 aren’t valuable. In fact, in some ways, the ‘‘employee performance optimization’’ movement has given us a method for talking about our insecurities, fears and aspirations in more constructive ways. It also has given us the tools to quickly teach 
 
 lessons that once took managers decades to absorb. Google, in other words, in its race to build the perfect team, has perhaps unintentionally demonstrated the usefulness of imperfection and done what Silicon Valley does best: figure out how to create psychological safety faster, better and in more productive ways.

If this had happened earlier in Rozovsky’s life — if it had occurred while she was at Yale, for instance, in her study group — she 

**probably wouldn’t have known how to deal with** 

**those feelings. The email wasn’t a big enough**
**affront to justify a response. But all the**
**same, it really bothered her. It was**
**something she felt she needed to address.**






 
