## Very simple and powerful LESS GRID.
### Don't like 12 or 16 column grids? Need custom grid with e.g. 11 columns? No problem.

***

1. Open mx-grid.less
2. Choose number of columns (@grid_num)
3. If using fixed-width grid, enter width of the single column (@item_width)
4. Set margin and padding.

...and compile.

Compiled css will have set of fluid classes: e.g. **@grid_num=11**  =>  **.mx-box1 - .mx-box11**, where **.mx-box1** is **1/11** of the container width and **.mx-box11** is **full width** element.

Also, there will be same classes with fixed width in **.mx-container-fix**, where **.mx-box1 = @item_width** and **.mx-box11 = 11 * @item_width.**

Margin and padding are working flawlessly.

Possible nesting.

**.mx-line** is one-line container class, that removes left margin of the first-child, and the right margin of the last-child.


html example:

```
<div class="mx-container">
    <div class="mx-box2">hello</div>
    <div class="mx-box6">World</div>
    <div class="mx-box3">!</div>
    <div class="mx-box11"></div>
</div>
<div class="mx-container">
    <div class="mx-line">
        <div class="mx-box4">4</div>
        <div class="mx-box7">7</div>
    </div>
    <div class="mx-line">
        <div class="mx-box6">6</div>
        <div class="mx-box5">5</div>
    </div>
</div>
<div class="mx-container-fix">
    <div class="mx-box7">hello</div>
    <div class="mx-box4">World</div>
    <div class="mx-line">
        <div class="mx-box1">1</div>
        <div class="mx-box4">4</div>
        <div class="mx-box1">1</div>
        <div class="mx-box4">4</div>
        <div class="mx-box1">1</div>
    </div>
</div>
```