# Chapter 5: Styling Links
* The `:link` pseudo-class selector is used to target links that have not been visited, and the `:visited` pseudo-class selector is used to target visited links.
* In the following example, the order of the selectors is very important. If the order is reversed, the hover and active styles won't work, the `:link` and `:visited` styles will override the `:hover` and `:active` styles
      a:link, a:visited {text-decoration: none;}
      a:hover, a:focus, a:active {text-decoration: underline;}
* If the page is quite busy, it is often difficult to tell to which element the link has sent you. To get around this problem, CSS 3 allows you to style the target element using the `target` pseudo-class.


