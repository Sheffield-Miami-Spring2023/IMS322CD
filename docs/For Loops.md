---
title: IMS322 Documentation - Spring 2023
---

# For Loops

[Home](index)
<br><br>
Often, you will find that you need to run very similar code multiple times. Let's say that you need to draw 5 shapes that span the width of the canvas in p5. Normally, that might look something like this:
```
function draw() {
	circle(0, height/2, 50);
	circle(80, height/2, 50);
	circle(160, height/2, 50);
	circle(240, height/2, 50);
	circle(320, height/2, 50);
}
```
With a for loop, that can be written more flexibly and efficiently and like so:
```
function draw() {
	for(let i=0; i<5; i++) {
		circle(i*80, height/2, 50);
	}
}
```
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="QWVrpOy" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/QWVrpOy">
  IMS322-ForLoop1</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

The construction of a for loop follows this format:
```
for (counter, condition, increment) {
	// do this multiple times
}
```

The *counter* is a variable that keeps track of how many times the loop has been run. It is conventionally almost always declared as `let i = 0` and incremented by 1 each time through the loop. As you saw in the circle example above, this counter variable can also be used within the loop itself for calculations. That is how we spread the circle position across the canvas - by multiplying `i` with 80.

The *condition* determines how many times you would like to run the loop. Again, this is conventionally almost always declared as `i < x` where `x` is the number of times the loop will run. Remember that `i` increments each time through the loop, so the loop continues as long as `i` is less than `x`.

Finally, the *increment* determines how `i` changes each time through the loop. Most of the time, `i++` will be the most suitable option (increasing `i` by only 1 each time), though occasinally you may come across instances where you would like `i` to increase by a larger amount.

The `i` counter variable can also be used as a way to efficiently read through each index in an array. Notice that the `array.length` property can ensure that the for loop only runs for the length of the array - in this case, `myData.length` is equal to 4 since the array contains 4 values.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="qBMYrMy" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBMYrMy">
  IMS322-ForLoop2</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Finally, here is an example of performing other calculations inside of a for loop - in this case, I am testing to see whether my cursor is hovering over one of the squares and, if it is, temporarily changing the fill color to red.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="BaOxWbo" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BaOxWbo">
  IMS322-ForLoop3</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

