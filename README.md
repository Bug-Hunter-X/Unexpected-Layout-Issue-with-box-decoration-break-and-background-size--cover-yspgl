# Unexpected Layout Issue with box-decoration-break and background-size: cover

This repository demonstrates an uncommon CSS bug related to the interaction between the `box-decoration-break` property, `background-size: cover`, and the height of the element.  The issue manifests as unexpected image clipping or distortion across different browsers.

## Bug Description
The `box-decoration-break: clone;` property, while useful for multiline backgrounds, can interact unexpectedly with `background-size: cover`.  In some cases, particularly with smaller height elements, the image may not render as intended due to browser inconsistencies in how they handle the combination of these properties.

## Reproduction
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe the unexpected rendering of the background image.

## Solution
The solution involves avoiding the use of `box-decoration-break: clone;` in cases where `background-size: cover;` is also used and the element's height is relatively small.  Alternatively, adjust the height or the background image itself to alleviate the problem.  Refer to `bugSolution.css` for a corrected version.

## Contributing
Feel free to contribute to this repository by opening issues or pull requests.