# Yeet

*Still very much in experimental, early stage!*

__*The lord Yeethed and the Lord Yoinked away*__  
Abstraction messaging layer, using custom event triggers in a (mostly) Pub/Sub pattern to make 121 or 12M communications easier  
Uses the build in event and messaging queu to transport events over to elements.

### What is it and what does it do
An abstraction layer which takes away the burden of tracking where bindings are and reflecting state to other components. It creates an easy way for elements or the environment to communicate and react to eachother by providing an interface to bind actions to rather than the elements itself, thus decoupling sender/receiver

__Why not observables or promises?__

> Well because a) observables are (at this time) not native avaible for JS and in my opinion quite cumbersome to use and b) Promises are a pretty much one use only, for each message you would have to create a new one and bind the promise to whatever you'd want to happen while event listeners remain for a long as you'd like and can be added/removed on the fly


__What is the goal of this.. thing...?__

> To make it easier for elements to respond to eachother or the enviroment or to directly communicate from one to another.  
  
For example, you want to change the title of the document to whatever a user is typing in an inputfield, fine you use a onChange binding and write a little function to change the title.  
Later you need to make the document background-color change depending on input, you extend your function a little.  
somewhile later on you need the input to also be given to another div as a welcome message, urgh fine you extend the function even more to do so.  
Even Later on someone tells you to make it happen not only for this one input, but for a shitload of inputs, and ah the background-color should also change when a user click a button, at this point you can start splitting the function and adding the correct functions to the correct event from different inputs and buttons and whatnot

__OR__

> You create a Yoink on the onChange of said input which is throwing the identifier 'InputChanged' together with it's new value and configure the title and div to listen for something yelling 'inputChanged' and retrieve the value, or to dance whatever floats your boat.  
  
  
In short; make it easier for elements to react to eachother by eliminating the need to know the other elements, all event go to/from a central mediator which takes care of it there, the retrieving object does not know who threw the event (unless you want it too) and the throwing element does not know which elements receive it's message, if any.  
Here both ends are totally decoupled and you can add/remove/modify as many input/outputs as you'd like without touching the core of the communication! Every input can send different values in and different outputs can react differently to whatever they receive

__Beware__
- Not yet fully (not even half to be honest) tested so use with caution
- Possible performance hit when overused due to very much not optimized code
- Asychronious behavior
- Relies on prototype extending of Element prototype, if you're not into that (like a lot of people are) I'm sorry
- Exposes the interface on the window, so it is globally avaible 

### What's to come  
- Fully functional and tested 'library'
- Support for observables to throw yoinks
- Build in donut pause
- Refine some methods as they are quite crude at the moment
- Better integration into elements
- ...
- Whatever else I can think off while I'm developing 

### *Use with caution!*
