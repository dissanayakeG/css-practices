CSS positioning
---------------

static: The default position of an element. 
   - No access to left/top/right/bottom properties and Z-index property.

relative: Similar to static but allows setting left/top/right/bottom properties.
   - Changes the position of the element relative to its normal position in the document flow.
   - Takes the element out of the document flow, potentially overlapping other elements when using left/top/right/bottom.
   - It is not common to use left/top/right/bottom with relative positioning.

absolute: The document completely ignores this element, as if it were deleted.
   - Other elements are rendered without considering the absolute-positioned element.
   - Used when you want to position something precisely without affecting the surrounding elements.
   - The left/top/right/bottom properties are positioned absolutely within the nearest positioned (non-static) ancestor.
   - Relative and absolute positioning can be used together, and often, absolute is used inside a relatively positioned element.

fixed: Similar to absolute, but ignores any nearest positioned ancestor and is fixed based on the entire HTML element.
   - The position remains fixed when scrolling.

sticky: Combines aspects of both relative and fixed positioning.
   - Initial appearance is like relative positioning; no effect until left/top/right/bottom properties are set.
   - Left/top/right/bottom properties work when the element hits the end of its container during scrolling.
   - Stays in the same position when scrolling.

Use relative when you want to keep your elements in the normal flow of the document.
Use absolute when you want to remove your element from the normal flow of the document and position it precisely.
Consider fixed for elements that should stay in a fixed position regardless of scrolling.
Sticky is useful when you want an element to behave like relative positioning but switch to fixed positioning when scrolling reaches a certain point.



Center a div
------------
container mx-auto

Flex
----
vertically (top to bottom) -> items-center
horizontally (left to right) -> justify-between

inline elements don't respond to width (w-) and height (h-) classes in the same way as block-level or inline-block elements.


YouTube
-------
 <script>
    // JavaScript to dynamically change the CSS variables
    document.documentElement.style.setProperty('--ytd-rich-grid-content-max-width', '300px');
    document.documentElement.style.setProperty('--ytd-rich-grid-item-margin', '20px');
  </script>
  
:root {
      --ytd-rich-grid-content-max-width: 300px;
      --ytd-rich-grid-item-margin: 20px;
    }

ytd-rich-grid-row #contents.ytd-rich-grid-row {
    width: 100%;
    max-width: calc(var(--ytd-rich-grid-content-max-width) + var(--ytd-rich-grid-item-margin));
    margin: 0 16px;
    display: flex;
}