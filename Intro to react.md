**1. In your own words, explain React's Virtual DOM. What gives React its fast performance?**

DOM maniupulation in most javascript frameworks involves rebuilding the entire DOM from scratch after a single change. A good example is a checklist with 10 items.  Normal Javascript would rebuild the entire list if you only checked one item, which is slow.  In React, the Virtual DOM contains a representation of each and every DOM object.  The virtuall DOM is much faster than updating the regular DOM, as nothing is drawn onscreen, which is the slow part.  

When it is time to render an element, every single object in the virtual DOM gets updated.  This might sound ineffecient, but the virtual DOM is so much faster that it really doesn't matter.  once the virtual DOM is updated, React compares the update to a snapshot it took right before the update, and uses this comparison to figure out exactly which virtual DOM objects have changed.  At this point, React is ready to change the updated virtual DOM objects in the real DOM, and only those objects actually get updated.  To use the example from before, React is smart enough to only update the one item that got checked, and leave the rest of the list alone.  

**2. In your own words, describe React's core concept of uni-directional data flow. Draw diagrams to illustrate. Discuss the answer with your mentor in your next session.**

Unidirectional data flow means that data only goes in one direction.  For comparison, Angular has two-way data binding that basically means data can go in two directions when it needs to.  Many developers feel this makes react easier to debug, since if something goes wrong, the error can only go down one path, instead of doubling back and going up or down either way.   

Since data can only go in one direction, is is possible for data to go back up the path to update previous components?  Yes, kinda.  If you define a callback function in the parent component, it will be passed down from component to component along with everything else. the callback can then be executed in a child component to send the data back up to the parent, which then invokes the corresponding method within the parent.  

Diagram showing unidirectional data flow: https://i.imgur.com/fwnZvos.png