flexbox tutorial: 


video1: 

https://www.youtube.com/watch?v=hwbqquXww-U&list=PL4-IK0AVhVjMSb9c06AjRlTpvxL3otpUd&ab_channel=KevinPowell

4:05 Flex Direction
5:24 Flex Wrap
6:45 Setting nowrap will ignore width of item
7:50 Flex-flow = flex-direction+flex-wrap
9:33 Flex justify-content
11:09 align-items defaults is "strech"
11:43 align-items works as cross axis (if you are column then it row)
13:06 align-items Baseline align text same level
15:58 align-contents align all content in flex

--------------------------------------------------------------------
Flexbox Tutorial - Flexbox containers
- flexbox has replaced floats and clears 


--------------------------------------------------------------------
Flex Direction
--------------------------------------------------------------------
 - options: row (default) | row-reverse | column | column-reverse

  display: flex;
  flex-direction: row;

https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction
--------------------------------------------------------------------
Flex-wrap
--------------------------------------------------------------------
 - options: nowrap (default) | wrap | wrap-reverse 
 - Having the default, nowrap, the items inside the flex is possible to spill outside 
 - use wrap so flex will re-organize to make it fit nicely inside the container
 - nowrap, will cancel out the width of your items 
	- ex: width: 25% will not work, will still try to fit everything 
 - width: will become more or less a max-width if you use a large number 
	- ex: 1000px -> 100%, will just have 1 item per row or column 

--------------------------------------------------------------------
flex-flow: row nowrap; 
--------------------------------------------------------------------
 - shorten version of: 
	flex-direciton: row
	flex-wrap: nowrap 
 - Flex-flow = flex-direction+flex-wrap

--------------------------------------------------------------------
justify-content: flex-start (default) 
--------------------------------------------------------------------
 - justifiy content in the main-axis (row/column)  

formal syntax: 

normal | <content-distribution> | <overflow-position>? [ <content-position> | left | right ]

where 
<content-distribution> = space-between | space-around | space-evenly | stretch
<overflow-position> = unsafe | safe
<content-position> = center | start | end | flex-start | flex-end

https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content
--------------------------------------------------------------------
align-items: stretch (default) 
--------------------------------------------------------------------
 - works on the cross axis (perpendicular to the main axis) 
 - will align per row/column 

normal | stretch (default) | <baseline-position> | [ <overflow-position>? <self-position> ]
where 
<baseline-position> = [ first | last ]? baseline
<overflow-position> = unsafe | safe
<self-position> = center | start | end | self-start | self-end | flex-start | flex-end

https://developer.mozilla.org/en-US/docs/Web/CSS/align-items
--------------------------------------------------------------------
align-content: 
--------------------------------------------------------------------
 - conflicts with align-items
 - only works with more than 1 row/column of items 
 - will align everything (all rows/column) 

--------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
--------------------------------------------------------------------
Flexbox Tutorial - Flexbox items: 

https://www.youtube.com/watch?v=4Oi5xpjoCRk&list=PL4-IK0AVhVjMSb9c06AjRlTpvxL3otpUd&index=2&ab_channel=KevinPowell

- flex items, everything inside a flex box 

different-properties: 
flex-grow: 0 (default) - unitless numbers 
	- the rate it will grow compared to other items
 
flex-shrink: 0 (default) 
 	- the rate it will shrink compared to other items 

flex-basis = how much room can it take up if it's available 
	- max width, ideal width 

flex = flex-grow + flex-shrink + flex-basis (short hand) 
	-ex: flex: 0 1 250px
		flex-grow: 0 
		flex-shrink: 1
		flex-basis: 250px 
flex: 250px (will assume grow/srhink is 0 or take other assigned properties) 

--------------------------------------------------------------------
for single items: 

align-self
 - will align a single flex item 
 - ex: align-self: center | flex-start/end | etc

order
 - will change the order of the flex items
 - order of 1 = beginning 
 - order: -1 = before start (will supercede order of 1) 
 - order: 0 (default) 

 - having only 1 flex-item with order does nothing 
 	- all items must have order, unless you do order: -1; 

--------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
--------------------------------------------------------------------
Flexbox Tutorial - Building a simple layout with flexbox 


https://www.youtube.com/watch?v=JqJNhM8i-nc&list=PL4-IK0AVhVjMSb9c06AjRlTpvxL3otpUd&index=3&ab_channel=KevinPowell


.class{
 flex-direction: column;
}

@media (min-width: 40rem){
 flex-direction: row; 
} 

min-width (will change when the min-width becomes 40rem = 40x16 = 640px) 

















