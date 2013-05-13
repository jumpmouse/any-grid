Very simple and powerful LESS GRID.
Don't like 12 or 16 column grids? Need custom grid with e.g. 11 columns? No problem.

***

1. Open mx-grid.less
2. Choose number of columns (**@grid_num**)
3. If using fixed-width grid, enter width of the single column (**@item_width**)
4. Set margin and padding.

...and compile.

Compiled css will have set of fluid classes: **.mx-box1 - .mx-box11**, where **.mx-box1** is 1/11 of the container width and **.mx-box11** is full width element.
Also, there will be same classes with fixed width in **.mx-container-fix**, where .mx-box1 = @item_width and .mx-box11 = 11 * @item width.
margin and padding are working flawlessly.
.mx-line is one-line container class, that removes left margin of the first-child, and the right margin of the last-child.


html markup
`//fluid grid
<div class="container">
    <div class="mx-box2">hello</div> // 2/11 of the container width
    <div class="mx-box6">World</div> // 6/11 of the container width
    <div class="mx-box3">!</div> // 3/11 of the container width
    <div class="mx-box11"></div>
</div>
<div class="container">
    <div class="mx-line">            // removes margins from the first and the last child element.
        <div class="mx-box1">1</div>
        <div class="mx-box4">4</div>
        <div class="mx-box1">1</div>
        <div class="mx-box4">4</div>
        <div class="mx-box1">1</div>
    </div>
    <div class="mx-line">
        <div class="mx-box6">6</div>
        <div class="mx-box5">5</div>
    </div>
    <div class="mx-line">
        <div class="mx-box">6</div>
        <div class="mx-box5">5</div>
    </div>

</div>
//fixed box width
<div class="container-fix">          // fixed item width container
    <div class="mx-box7">hello</div> // 7/11 of the container width
    <div class="mx-box4">World</div> // 4/11 of the container width
    <div class="mx-line">            // removes margins from the first and the last child element.
        <div class="mx-box1">1</div>
        <div class="mx-box4">4</div>
        <div class="mx-box1">1</div>
        <div class="mx-box4">4</div>
        <div class="mx-box1">1</div>
    </div>
</div>

`