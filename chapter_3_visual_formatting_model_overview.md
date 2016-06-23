# Chapter 3: Visual Formatting Model Overview
* If you add a `background` to an element, it will be applied to the area formed by the content and padding.
* CSS 2.1 also contains the `outline` property. Unlike the border property, outlines are drawn over the top of an element's box, so they don't affect its size or positioning. Because of this, outlines can be useful when fixing bugs, because they won't alter the layout of your page.
* Margin collapsing => when two or more vertical margins meet, they will collapse to form a single margin. The height of this margin will equal the height of the larger of the two collapsed margins.
* When one element is contained within another element, assuming there is no padding or border separating margins, their top and/or bottom margins will also collapse together
* Margins can even collapse on themselves. Say you have an empty element with a margin but no border or padding. In this situation, the top margin is touching the bottom margin, and they collapse together
* If this margin is touching the margin of another element, it will itself collapse
* Margin collapsing only happens with the vertical margins of block boxes in the normal flow of the document. Margins between inline boxes, floated, or absolutely positioned boxes never collapse.
* There is one situation where a block-level element is created even if it has not been explicitly defined—when you add some text at the start of a block-level element like a div. Even though you have not defined the text as a block-level element, it is treated as such
* With relative positioning, the element continues to occupy the original space, whether or not it is offset. As such, offsetting the element can cause it to overlap other boxes.
* Absolute positioning takes the element out of the flow of the document, thus taking up no space. Other elements in the normal flow of the document will act as though the absolutely positioned element was never there
* A floated box can either be shifted to the left or the right until its outer edge touches the edge of its containing box or another floated box.
* If the floated elements have different heights, it is possible for floats to get "stuck" on other floats when they drop down.
* If a floated element is followed by an element in the flow of the document, the element's box will behave as if the float didn't exist. However, the textural content of the box retains some memory of the floated element and moves out of the way to make room. In technical terms, a line box next to a floated element is shortened to make room for the floated element, thereby flowing around the floated box. In fact, floats were created to allow text to flow around images
* The `clear` property can be left, right, both, or none, and it indicates which side of the box should not be next to a floated box. When you clear an element, the browser adds enough margin to the top of the element to push the element's top border edge vertically down, past the float
* The `overflow` property defines how an element is supposed to behave if the enclosed content is too big for the stated dimensions. By default the content will spill out of the box, overflowing into the neighboring space. One useful side-effect of applying an overflow property of hidden or auto is that it will automatically clear any floats contained within. So this can be a useful way of clearing an element without adding any extra markup. This method is not appropriate in all situations, since setting the box's overflow property will affect how it behaves. More specifically, this method can force scroll bars or clip content under certain circumstances.
* `:after` clear `float`     
      .clear:after {
         content: ".";
         height: 0;
         visibility: hidden;
         display: block;
         clear: both;
       }
