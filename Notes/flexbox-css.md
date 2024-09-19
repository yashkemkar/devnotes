#Flexbox CSS

##HOW IT WORKS

In a container there are two axes. 
Main Axis: Horizontal (elements are individual columns in 1 row)
Cross Axis: Vertical (elements are individual rows in 1 column)

### creating a flex-box
- The code below creates a flexible display
```
.container {
    display: flex;
}
```

- The default orientation of children in a flex display box is in a **row**. If we want a **column**:
```
.container {
    display: flex;
    flex-direction: column;
}
```

- The flexible property is a very useful property as most websites are just layers of flex displays - combinations of nested columns and rows to create a layout.

### styling a flex-box (only along main axis) with justify-content: (insert below item);
- flex-end - aligns all the elements to the end of the main axis
- flex-start - aligns all the elements to the start of the main axis
- center - places all the elements in the center of the main axis
- space-around - creates an even space around (in the main axis direction) each element (it will be twice as big in between two elements as on the side of a single one)
- space-between - creates an equal space in between each element

### styling a flex-box (only along cross axis) with align-items: (insert below item);
- flex-end - aligns all the elements to the end of the cross axis
- flex-start - aligns all the elements to the start of the cross axis
- center - places all the elements in the center of the cross axis
- stretch - stretches elements along the whole cross axis

### styling a flex-box with large elements that push others outside the page using flex-wrap:
```
.container {
display: flex;
flex-wrap: (insert here);
}
```
- no-wrap (default value) - no wrap for the elements in the flex box (they will overflow)
- wrap - elements that would overflow are now be bumped down to comfortably fit on a secondary main axis

### styling a flex-box with gap:
```
.container {
    display: flex;
    gap: vertical horizontal;
}
```
The gap function takes two values, if you provide only one it will assume vertical.
You can still create gaps between any differently styled elements using gap.

### styling an element in a flex-box with flex-grow:
```
.item1 {
   flex-grow: 1;
}
```
This is useful when the screen size increases and we need to tell the children elements how to behave. By default this value is assigned to all children elements as 0. So if we assign one with a higher value it will be greedy with the space available. This function would relative/proportional with the values assigned to other elements. 1 is infinitely greater than 0, therefore it would take all the space. But if 1 element was 1 and another was 2, then 1 would take 1/3 of the space and 2 would take 2/3 of the space.

### styling an element in a flex-box with flex-shrink:
This is useful when the screen size decreases and we need to tell the children elements how to behave. By default this value is assigned to all children elements as 0. So if we assign one with a higher value it will be starved of the space available. This function would relative/proportional with the values assigned to other elements. 1 is infinitely greater than 0, therefore it would shrink to 0. But if 1 element was 1 and another was 2, then 1 would shrink 1/3 of the reduced space and 2 would shrink 2/3 of the reduced space.

### styling an element in a flex-box with flex-basis:
```
.item1 {
   flex-basis:200px;
}
```
This is useful when you need to set a particular size in the main axis dimension from the start. Then any functions applied to the element in the flex-box will follow from the starting dimensions.

### styling an element in a flex-box with flex:
It is uncommon for an element in a flex-box to be stylised with each individual function as we just did above, instead we can use just *flex:* as shown below with values in the order of flex: flex-grow flex-shrink flex-basis:
```
.item1 {
   flex: 1 0 200px;
}
```
### styling an element in a flex-box with align-self:
```
.item1 {
   align-self:(same values as align-contents);
}
```
Align-self allows a child element to disobey the parent element functions and align itself how it wants. It uses the same values as align-contents above.
There are two additional values however:
- self-start - aligns the items to be flush with the edge of the alignment container corresponding to the items start side in the cross axis. Ie it stays in its original position on the main axis, but is placed either at the start of the cross axis. 
- self-end - same as above, but at the end of the cross axis.

### styling an element in a flex-box with order:
```
.item1 {
   order:(position along main axis);
}
```
This is a very simple function, just pick the location you want it to be in. For example if you have 4 boxes, and you want box 1 to be in position just order: 3;