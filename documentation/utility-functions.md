---
layout: documentation
title: Utility functions
---

Knockout provides a small collection of useful utility functions for manipulating arrays, elements, and bindings. These can come in handy especially if you are not using jQuery on your project.

 
* `ko.utils.arrayForEach(array, function(item, index) { ... })` iterates over an array just like a regular for loop. 
* `ko.utils.arrayMap(array, function(item, index) {... return item; })` iterates over an array, replacing each item with the value returned from the callback function. **Note:** This function cannot remove an item from the array altogether. 
* `ko.utils.arrayFirst(array, function(item, index) {... return item; })` iterates over an array, returning the first item for which callback returns a truthy value.
* `ko.utils.arrayIndexOf(array, item)` Returns the index of the first array item matching 'item'. Most suitable with primitive values. <br>*Example:* `ko.utils.arrayIndexOf(['John','Mitch','Powell','Donna'], function(item) { return item.indexOf('n'); }) // returns 'John'`
* `ko.utils.arrayFilter(array, function(item) { ... return item; })` Returns an array containing only items that pass the truth test in callback. <br>*Example:* `ko.utils.arrayFilter([1,2,3,4,5], function(i) { return i > 2 }) // returns [3,4,5]`
