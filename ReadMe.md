Greensock's TweenLite updated to work with Titanium Mobile.

Android animation on Titanium frankly, sucks. Hit areas don't move to where an item is animated and the easing function, while accessible, doesn't have any effect. This library solves that problem, albeit at not quite the same performance as views animated with native animations. 

Anway, if you don't know how to use Tweenlite, head on over to http://www.greensock.com/tweenlite/


Animating an item is pretty straightforward.

require("TweenLite");

Alloy.Globals.Tweenlite.to(yourView, timeInSeconds, { param1:value1, param2:value2, onComplete:someFunction, onCompleteParams:[someArray], ease:SomeEaseFunction(optiona)});


So to animate an item to left 100, in 1/2 a second.

Alloy.Globals.Tweenlite.to(yourView, .5, { left: 100 });

Please make sure to read the GreenSock license @ http://www.greensock.com/licensing/ to make sure you are using the library under the correct License.

