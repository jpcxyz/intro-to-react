**1. In your own words, explain the essential differences between props and state in React. Which is immutable or read-only, and which changes? Discuss the answer with your mentor.**  
Props in React are "properties" of the component.  They hold information about the component.  They are externally controlled, which means the properties of the props are determined by that which renders the component.  Props should not change, and are considered immutable, despite past versions of React providing `setProps` and `replaceProps` which allowed Props to change.  These abilities have been deprecated and props should never change now.  The immutability of props allows them to have the same output for the same input each and every time, which really helps with testing.    
State in React also holds information about the component, but the kind of information is different, and it is handled in a different way.  Technically, States are optional, as components don't have them by default.  By adding them, a component gains the ability to keep track of information between renderings.  Since props cannot be changed, state is there for when you need to change stuff.  

**2. Read the React official documentation on components and props, and brush up on JavaScript ES6 *classes**

**3. Built upon your component from the assignment after checkpoint 3, add in state and props to make sure you have fully mastered these core React properties.**

See Github submission for this assignment.  
