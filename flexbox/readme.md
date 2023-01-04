# Flexbox
---
Flexbox uses two types of boxes “flex containers” and “flex items”. The job of a flex container is to group a bunch of flex items together and define how they’re positioned. Every HTML element that’s a direct child of a flex container is an “item”.

## Flexbox container
---
By giving display a value of flex, we’re telling the browser that everything in the box should be rendered with flexbox instead of the default box model.
`display:flex`

### Aligning a flex item
---
The justify-content property is for the horizontal alignment of flex container.
`justify-content:center`

This has the same effect as adding a `margin: 0 auto` declaration to the .menu element.
Other values for justify-content are shown below:

* center
* flex-start
* flex-end
* space-around
* space-between
* space evenly

### Distributing multiple flex items
---
The justify-content property also lets you distribute items equally inside a container.
`justify-content: space-between`

## Cross Axis(Vertical) Alignment
---
Flex containers can also define the vertical alignment of their items. This is something that’s simply not possible with floats. Vertical alignment is defined by adding an align-items property to a flex container.
`align-items: center`

The available options for align-items is similar to justify-content:

* center
* flex-start   (top)
* flex-end      (bottom)
* stretch
* baseline

The stretch option lets you display the background of each element. The box for each item extends the full height of the flex container, regardless of how much content it contains. A common use case for this behavior is creating equal-height columns with a variable amount of content in each one—something very difficult to do with floats.

## Wrapping flex items

To create a grid, we need the flex-wrap property. Adding the following flex-wrap property forces items that don’t fit to get bumped down to the next row.
`flex-wrap: wrap`

## Flex container direction
---
One of the most amazing things about flexbox is its ability to transform rows into columns using only a single line of CSS.
`flex-direction: column`

Most mobile layouts are a single column, while most desktop layouts stack elements horizontally. You can imagine how useful flex-direction is going to become once we start building responsive layouts.

### Alignment Consideration

When you rotate the direction of a container, you also rotate the direction of the justify-content property. It now refers to the container’s vertical alignment—not its horizontal alignment. To horizontally center our column, we need to define an align-items property.

## Flex container order
---
The flex-direction property also offers you control over the order in which items appear via the row-reverse and column-reverse properties.

## Flex item order
---
It’s also possible to manipulate individual items. Adding an order property to a flex item defines its order in the container without affecting surrounding items. Its default value is 0, and increasing or decreasing it from there moves the item to the right or left, respectively.

## Flex item alignment
---
We can do the same thing with vertical alignment. You can align elements in other ways using the same values as the align-items property

## Flexible items
---
Flex items are flexible: they can shrink and stretch to match the width of their containers. The flex property defines the width of individual items in a flex container. Or, more accurately, it allows them to have flexible widths.
`flex: 1;` line tells the items to stretch to match the width of parent container.

### Static item width

We can even mix-and-match flexible boxes with fixed-width ones. `flex: initial` falls back to the item’s explicit width property. This lets us combine static and flexible boxes in complex ways.

## Flex Items and Auto Margins
---
Auto-margins in flexbox are special. They can be used as an alternative to an extra <div> when trying to align a group of items to the left/right of a container. Think of auto-margins as a “divider” for flex items in the same container.


