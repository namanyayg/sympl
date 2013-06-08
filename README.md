## What is Sympl.css?

Sympl.css is a extremely simple stylesheet for starting projects, that contains a easy-to-use and fully responsive grid; useful defaults; empty classes; and sets typography.

Sympl.css' grid is a flexible and fully responsible grid, which has separate styles for large, medium, and small sized screens&mdash;all this while being easy to use and understand. 

Sympl.css sets the font sizes, margins, and line heights for all the headings, and sets uniform font settings on all elements. 

Sympl.css' defaults relate to having empty declarations for anchors and form elements&mdash;You just write styles, and you're done. 

Developed by [Namanyay Goel](http://namanyayg.com/).

### The grid

All grid items are to be enclosed in a class of `stack`. Two classes can be added for different results, example, use `stack-sympl` to give space (`1.5em`) to the bottom, and `stack-clean` to give a space at the top, and each `sympl` item to have a bottom padding of `1.5em`.

Inside a stack, all elements which need to follow the grid should have the class of `sympl`, along with grid class(es). Grid classes follow a similar structure, which goes `[l|m|s]-(size)(s)`. An example would be `l-onethird`, which gives the element a width of `33.333333%` on viewport sizes equal to or less than `60em`. Another would be `m-fourfifths`, which gives the element a width of `80%` on viewport sizes equal to or less than `45em`.

Class names are descriptive, and easy to understand. The major class names and their widths are below.

	.half, .twoquarters, .threesixths { width: 50%; }

	.onethird, .twosixths { width: 33.333333%; }
	.twothirds, .foursixths { width: 66.666666%; }

	.quarter { width: 25%; }
	.three-quarters { width: 75%; }

	.onefifth { width: 20%; }
	.twofifths { width: 40%; }
	.threefifths { width: 60%; }
	.fourfifths { width: 80%; }

	.onesixth { width: 16.666666%; }
	.fivesixths { width: 83.333333%; }

These classes can be clubbed together to give different widths to different sizes. Example:

    <div class="sympl quarter l-onethird m-half s-half">
    Content goes here.
    </div>

Classes with the prefix `l-` get applied on equal to or less than `60em` viewport width, `m-` on `45em`, and `s-` on `30em`. Each sympl item gets a width of `100%` on size `s`, that is, on less than or equal to `30em`. This can be changed by adding a `s-` class, like `s-half`, as illustrated in the above example.

Sympl also has visibility classes. You can hide/show an element based on the viewport size. All hide/show classes follow the pattern of `hide-size-and-below` or `show-size-and-below`, where size can be `l`, `m`, or `s`. Another is `hide-on-size` and `show-on-size`, which hides/shows only on the specific size.

### Typography

Sympl declares the margins of paragraphs. Paragraphs have no margin of their own, unless the are preceeded by another paragraph. In that case, the paragraphs have a margin of `1.5em` between them.

All sizes, line heights, and margins of headings are declared as well. These follow vertical rhythm of `1.5`.


### Empty declarations

There are a few empty declarations, and some defaults set, example, anchor colors, anchor transitions. Empty declarations are for inputs, anchor hovers, buttons, etc. A normalize/reset **isn't included**, but it is recommended to use one, like [normalize.css](http://necolas.github.com/normalize.css/).

Sympl uses `box-sizing: border-box;` which isn't supported IE7 and below. 

