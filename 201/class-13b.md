**transforms:** The transform property comes in two different settings, two-dimensional and three-dimensional.<br>
Each of these come with their own individual properties and values.

**2D Translate**
The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions <br>
without interrupting the normal flow of the document. Using the translateX value will change the position of an element on <br>
the horizontal axis while using the translateY value will change the position of an element on the vertical axis.<br>

**2D Skew**
The last transform value in the group, skew, is used to distort elements on the horizontal axis, vertical axis, or both.<br>

**3D Rotate**
So far we’ve discussed how to rotate an object either clockwise or counterclockwise on a flat plane. With three-dimensional <br>
transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, <br>
and rotateZ.

With hover you can do a change a lot of things when you hover over the stuff that you made , like color , size and background.<br>

**Transitions**
As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified <br>
for each state. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active,` <br>
and `:target` `pseudo-classes`.

For example :`.box:hover {background: #ff7b29;border-radius: 50%;}` when you hover over the box it will turn into circle.<br>

**Animation Duration, Timing Function, & Delay**
Once you have declared the animation-name property on an element, animations behave similarly to transitions. They include a <br>
duration, timing function, and delay if desired.<br>
