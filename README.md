# Yeet

*Still very much in experimental, early stage!*

__*The lord Yeethed and the Lord Yoinked away*__  
Abstraction messaging layer, using custom event triggers in a (mostly) Pub/Sub pattern to make 121 or 12M communications easier  
Uses the build in event and messaging queu to transport events over to elements.  
Heavily inspired by the angular two way binding where components react to eachothers updates

### What is it and what does it do
An abstraction layer which takes away the burden of tracking where bindings are and reflecting state to other components. It creates an easy way for elements or the environment to communicate and react to eachother by providing an interface to bind actions to rather than the elements itself, thus decoupling sender/receiver

__Why not Observables, Proxies, MutationObservers or Promises?__

> Well because:  
a) Observables are (at this time) not native avaible for JS, but could prove to be a worthy successor to this project.  
b) Promises are a pretty much one use only, not much use if you want to distribute non direct messages  
c) Proxies are not supported in IE (and this is still a big marketshare unfortunatly) and are not globally implemented (i.e. no central global mediator, nodes needs to know eachother)  
d) MutationsObservers havbe a limited scope of mutations they can watch, do not support binding to external events directly 

__Pros__  
- Not a framework, not even a library, so implementations can be done however you want it to be done
- Central global mediator
- Asynchronious behavior

__Cons__
- Not yet fully (not even half to be honest) tested so use with caution
- Possible performance hit when overused due to very much not optimized code
- Relies on prototype extending of Element prototype, if you're not into that (like a lot of people are) I'm sorry

### What's to come  
- Fully functional and tested 'library'
- Support for observables to throw yoinks
- Build in donut pause
- Refine some methods as they are quite crude at the moment
- Better integration into elements
- ...
- Whatever else I can think off while I'm developing 

### *Use with caution!*
