##d3.layout.force3D with a proper third dimension

Import it to your project after d3.js and replace:
`d3.layout.force()` by `d3.layout.force3D()`` into your code.

The original API is unchanged except for :
 - `size()` that now takes an array of length 3 instead of 2. Default is now `.size([1, 1, 1])` .
 - `force.drag` **is not realy supported** because of the third dimention. You have to implement it yourself with unprojection techniques. The current `minimal-dirty-example.html` demo drag only on the `x` and `y` axes and ignore the `z` axis.


## Demo

[http://ggeoffrey.github.io](http://ggeoffrey.github.io)  
Implemented in ClojureScript with the d3.layout.force3D running in
a distinct webworker.
 
You can find dirty but working minimal code in the `minimal-dirty-example.html` file.

###Credits

Adapted from the original D3.js code and smart ideas and work from [@kalenedrael](https://github.com/kalenedrael).
I just extracted it, rewrote it, and exported it as a d3 plugin. So please give him the credits ;)

