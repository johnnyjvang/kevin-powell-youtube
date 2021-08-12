html - css - core concept notes:
-------------------------------------------------------------------------
https://www.youtube.com/watch?v=c0kfcP_nD9E&list=PL4-IK0AVhVjP27yZLwW-gkPggRps0CCnP&ab_channel=KevinPowell
-------------------------------------------------------------------------
Specificity 

Specificity is the means by which browsers decide which CSS property values are the most relevant to an element and, therefore, will be applied.

Specificity is a weight that is applied to a given CSS declaration, determined by the number of each selector type in the matching selector. When multiple declarations have equal specificity, the last declaration found in the CSS is applied to the element. Specificity only applies when the same element is targeted by multiple declarations. As per CSS rules, directly targeted elements will always take precedence over rules which an element inherits from its ancestor.

- classes are more specific than tags 
- the more specific your css, the more "weight" it will have when applying the css


-------------------------------------------------------------------------
inline styles > IDS > Classes> Elements/tags  
-------------------------------------------------------------------------

- using id's for CSS is not prefered
- leave IDS for <anchor tags>, moving/navigating on page 

To Override the specificity of a css: 
	add (!important) 
		- PLEASE DO NOT USE 



-------------------------------------------------------------------------
Learn how to use CSS Media Queries in less than 5 minutes
-------------------------------------------------------------------------
https://www.youtube.com/watch?v=2KL-z9A56SQ&list=PL4-IK0AVhVjP27yZLwW-gkPggRps0CCnP&index=2&ab_channel=KevinPowell



@media (min-width: 600px){
 - mobile first
}

@media (max-width: 600px){
 - desktop first
}

@media (orientation: landscape){
}

@media (orientation: portrait){
}

@media screen and (...){
 - when someone is on a screen
}

@media print and (...){
 - when someone is printing off your screen 
}
-------------------------------------------------------------------------

CSS Positioning: Position absolute and relative explained

-------------------------------------------------------------------------
position: absolute (brings it out of the normal flow) 


.parent{
 position: relative (this acts as a wraper for the child) 
}

.child{
 position: absolute (absolute inside the parent) 
}


*Note: position aboslute will take what ever is relative to it prior. if there is no relative, it will be relative to the body 


z-index: 0 (note, item must have a position:relative/aboslute to the item) 

-------------------------------------------------------------------------

CSS em and rem explained

-------------------------------------------------------------------------
https://zellwk.com/blog/rem-vs-em/


An EM is a unit of typography, equal to the currently specified point-size


What it means is: 1em = 20px if a selector has a font-size of 20px.
h1 { font-size: 20px } /* 1em = 20px */
p { font-size: 16px } /* 1em = 16px */

html { font-size: 16px }
h1 { font-size: 2em } /* 16px * 2 = 32px */
html { font-size: 100% } /* This means 16px by default*/

-------------------------------------------------------------------------

rem means Root EM. It’s built to provide some relief the em computational problem that many faced.

is a unit of typography equal to the root font-size. This means 1rem is always equal to the font-size defined in <html>.

h1 {
  font-size: 2rem;
  margin-bottom: 1rem; /* 1rem = 16px */
}

p {
  font-size: 1rem;
  margin-bottom: 1rem; /* 1rem = 16px */
}

How? I have two simple rules:

1. Size in em if the property scales according to its font-size
2. Size everything else in rem.

-------------------------------------------------------------------------
improve your css by keepin' it dry 
-------------------------------------------------------------------------
https://www.youtube.com/watch?v=0px6YH-cauQ&list=PL4-IK0AVhVjP27yZLwW-gkPggRps0CCnP&index=5&ab_channel=KevinPowell
-------------------------------------------------------------------------


 













