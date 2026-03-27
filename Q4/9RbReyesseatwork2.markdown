# Seatwork #2 – CSS Position and z-index  
**Name/s:** Avisha Reyes & Enzo Lustre
**Date:** March 27, 2026  

---

## Guided Questions

### Step 1: Static vs Relative

**Question:** What changed compared to the default static positioning?

**Answer:**  
With `position: relative`, the sidebar remains in its original place in the document flow, but it can now be moved using `top`, `left`, `right`, or `bottom`. In this case, `top: 20px` moves it downward and `left: 20px` moves it to the right.

In contrast, with the default `static` positioning, the `top` and `left` properties do not work.

Changing the values:
- Increasing `top` moves the element further down  
- Increasing `left` moves it further right  
- Using `bottom` moves it upward  
- Using `right` moves it left  

---

### Step 2: Fixed

**Question:** What happens when you scroll the page? Why does the footer behave differently from position relative?

**Answer:**  
When scrolling the page, the footer stays fixed at the bottom of the screen and does not move. This is because `position: fixed` attaches the element to the viewport.

This is different from `position: relative` because relatively positioned elements still move with the page and remain part of the normal document flow.

---

### Step 3: Absolute

**Question:** What is the effect of position: absolute on an element? How is it different from fixed?

**Answer:**  
`position: absolute` removes the element from the normal document flow and allows it to be placed at a specific location using `top`, `left`, `right`, or `bottom`.

It is different from `fixed` because:
- `absolute` is positioned relative to the nearest positioned parent element  
- `fixed` is positioned relative to the browser window and stays in place when scrolling  

---

### Step 4: Absolute + z-index

**Question:** Why does the notice appear on top of the content? What happens if you swap the z-index values?

**Answer:**  
The notice appears on top because it has a higher `z-index` value (`2`) compared to the content (`1`). Elements with higher `z-index` values are displayed in front.

If the values are swapped, the content will appear on top of the notice instead.

---

## Challenge

### 1. Position `.notice` at the top-right corner of `.content`

**HTML:**
```html
<div class="content">
  Main Content
  <div class="notice">Notice!</div>
</div>