---
layout: documentation
title: Utility functions
---

Knockout provides a small collection of useful utility functions for manipulating arrays, elements, and bindings. These can come in handy especially if you are not using jQuery on your project.

#Manipulating arrays
* `ko.utils.arrayForEach(array, function(item, index) { ... })` iterates over an array just like a regular for loop.  <br>*Example:* `var count = 0; ko.utils.arrayForEach([10,25,20], function(item, index) { count += item; }) //count === 55`
* `ko.utils.arrayMap(array, function(item, index) {... return item; })` replaces each item in the original array with the value returned from the callback function. **Note:** This function cannot remove an item from the array altogether. <br>*Example:* `ko.utils.arrayMap([1,2,3], function(item, index) { return item*5; }) // returns [5,10,15]`
* `ko.utils.arrayFirst(array, function(item, index) {... return item; })` returns the first item for which callback returns a truthy value.<br>*Example:* `ko.utils.arrayFirst(['John','Mitch','Powell','Donna'], function(item) { return item.indexOf('on'); }) // returns 'Donna'`
* `ko.utils.arrayIndexOf(array, item)` returns the index of the first array item matching item. Most suitable with primitive values. <br>*Example:* `ko.utils.arrayIndexOf(['John','Mitch','Powell','Donna'], function(item) { return item.indexOf('on'); }) // returns 3`
* `ko.utils.arrayFilter(array, function(item) { ... return item; })` Returns an array containing only items that pass the truth test in callback. <br>*Example:* `ko.utils.arrayFilter([1,2,3,4,5], function(i) { return i > 2 }) // returns [3,4,5]`
* `ko.utils.arrayGetDistinctValues(array)` Returns an array containing only **unique** items. <br>*Example:* `ko.utils.arrayGetDistinctValues([5,3,2,5,2]) // returns [5,3,2]`

#Manipulating DOM nodes

