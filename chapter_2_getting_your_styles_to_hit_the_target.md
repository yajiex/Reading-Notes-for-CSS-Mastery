# Chapter 2: Getting Your Styles to Hit the Target
* Specificity is not calculated in base 10 but a high, unspecified, base number. This is to ensure that a highly specific selector, such as an ID selector, is never overridden by lots of less specific selectors, such as type selectors. However, if you have fewer than 10 selectors in a specific selector, you can calculate specificity in base 10 for simplicity's sake.
* The specificity of a selector is broken down into four constituent levels: a, b, c, and d.
  1. If the style is an inline style, a equals 1.
  2. b equals the total number of ID selectors.
  3. c equals the number of class, pseudo-class, and attribute selectors.
  4. d equals the number of type selectors and pseudo-element selectors.
* Certain properties, such as color or font size, are inherited by the descendants of the elements those styles are applied to.
* Any style applied directly to an element will always override an inherited style. This is because inherited styles have a null specificity.
* Importing style sheets can be slower than linking to them.
* 

