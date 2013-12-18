Greensock's TweenLite updated to work with Titanium Mobile.

I developed this approach to solve Android animation issues:

1. Hit areas don't move with the animated view. 
2. Easing functions, while accessible (eg Ti.Android.R.anim.linear_interpolator), don't have any effect. 

This library solves both of these issues (albeit at not quite the same performance as views animated natively) and is also compatible Mobile Web and IOS.

There is currently an dependency on Alloy. I'll remove this if there is enough interest.

Animating an item is pretty straightforward.

require("TweenLite");

Alloy.Globals.Tweenlite.to(yourView, timeInSeconds, { param1:value1, param2:value2, onComplete:someFunction, onCompleteParams:[someArray], ease:SomeEaseFunction(optiona)});

To animate an item to left: 100, in 1/2 a second.

Alloy.Globals.Tweenlite.to(yourView, .5, { left: 100 });


Same thing, but call some function when finished

Alloy.Globals.Tweenlite.to(yourView, .5, { left: 100, onComplete:animComplete });

function animComplete() {
 alert("Animation Finished!");
}


Full documentation for TweenLite can be found @ http://www.greensock.com/tweenlite/


Please make sure to read the GreenSock license @ http://www.greensock.com/licensing/ to make sure you are using the library under the correct License.
