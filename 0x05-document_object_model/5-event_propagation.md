# Event Propagation

Refers to the way events flow through the DOM tree.

Event propagation is a way of defining the element order when an event occurs.

_If you have a paragraph element inside a div element, both with click events attached, the user clicks on the paragraph element; which element's click event should be handled first?

There are two ways of even propagation in the HTML DOM, **bubbling** and **capturing**.


**In bubbling, the innermost element's event is handled first and then the outer. The p element's click event will be handled first then the div element's click event**

**In capturing, the outermost element's event is handled first and then the inner, so the div element's click event will be handled first then the p element's click event.**

**With the addEventListener method, you can specify the propagation type by passing a third parameter called useCapture (true or false), false means bubbling will be used and true means capturing will be used. False is the default. We also make sure we have passed this parameter to both the div and the p element**

