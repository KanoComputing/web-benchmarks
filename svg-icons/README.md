# SVG Icons benchmark

This benchmark compares 3 different ways to render SVG icons.
All benchmark runs the same task 1000 times with an svg string whose fill is randomised to simulate different icons.
Using the DevTools' Performance tab, the time to load is recorded.
Using a simple console.time wrapping the run loop, the time blocking the main thread is recorded.

## CSS

Creates a `div` and sets its `background-image` to a dataURI of the svg icon string.
Main thread: 82ms
Time to load: 5560ms

## DOM

Inline the svg element directly in the DOM tree.
Main thread: 97ms
Time to load: 894ms

## IMG

Creates a `img` and sets its `src` to a dataURI of the svg icon string.
Main thread: 167ms
Time to load: 6500ms
