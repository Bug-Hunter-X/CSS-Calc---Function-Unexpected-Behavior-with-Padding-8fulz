# CSS Calc() Function Unexpected Behavior with Padding

This repository demonstrates an unexpected behavior with the `calc()` function in CSS when calculating the width of an element that has padding.

## Bug Description

The `calc()` function is used to calculate the width of a div element. The calculation is `100% - 20px`, and a padding of `10px` is applied.  The expected behavior is for the element's width to be 80% of the parent container's width. However, the padding is added to the calculated width, resulting in a total width greater than 100% and causing layout issues.

## Solution

The solution involves adjusting the calculation within the `calc()` function to account for the padding. By subtracting the horizontal padding (twice the padding value, as it's applied to both sides) from the width, we correctly calculate the appropriate size.