##xStateFlag

xStateFlag provides an array of divs whose classes change to indicate which of them is currently 'selected' - these can be styled with external CSS to create a typical 'n of m' illuminated dot 
indicator of state, as is often used in conjunction with a slide box.

###Use

One div is inserted for each state; the div corresponding to the active state has the class `selectedStateDiv`, and all other divs (corresponding to inactive states) have the class name `unselectedDiv`.  DIY CSS to give these the appearance you desire.

#Attributes
 - `nStates` sets the number of state flags to represent.
 - `gotoCallback` is a function fired at the end of the goto method.
 - `state` `read-only` returns the current state.  Setting this attribute will be ignored, use `goto(index)` method instead.

#Methods
 - `nextState()` advances to the next state
 - `previousState()` advances to the previous state
 - `goto(index)` advances to `<index> % nStates`

#Example

Declare a StateFlag with three states:

```
<x-StateFlag id='stateFlag' nStates='3'></x-StateFlag>
```
A simple StateFlag style:

```
x-StateFlag div{
	width:15px;
	height:15px;
	border-radius: 7.5px;
	background-color: #111111;
	margin:0.5em;
	cursor: pointer;
	-webkit-transition: background-color 0.3s ease, box-shadow 0.3s ease;
	-moz-transition: background-color 0.3s ease, box-shadow 0.3s ease;
	transition: background-color 0.3s ease, box-shadow 0.3s ease;
}

x-StateFlag div.selectedStateDiv{
	background-color: #EEEEEE;
	box-shadow: 0px 0px 5px #EEEEEE;

}
```