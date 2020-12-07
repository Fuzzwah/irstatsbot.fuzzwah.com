---
title: iRacing Stats Discord Bot - Screenshots
---

## Screenshots

<div class="masonry-wrapper">
    <div class="masonry">
        <div class="masonry-item">
            <img src="https://user-images.githubusercontent.com/658935/100395468-255c5300-3095-11eb-8d52-dbfa5f1a7d5c.png" alt="!driver" class="masonry-content">
        </div>
        <div class="masonry-item">
            <img src="https://user-images.githubusercontent.com/658935/100396662-03b19a80-309a-11eb-9342-0146af5c31e1.png" alt="!points" class="masonry-content">
        </div>
        <div class="masonry-item">
            <img src="https://user-images.githubusercontent.com/658935/100396713-378cc000-309a-11eb-85ac-edc9e757bbfc.png" alt="!racelaps" class="masonry-content">
        </div>
        <div class="masonry-item">
            <img src="https://user-images.githubusercontent.com/658935/100396758-6dca3f80-309a-11eb-94fe-79944381dc2d.png" alt="!strengthoffield" class="masonry-content">
        </div>
    </div>
</div>
<script src="//unpkg.com/imagesloaded@4/imagesloaded.pkgd.min.js"></script>
<script>
    function resizeMasonryItem(item) {
        var grid = document.getElementsByClassName('masonry')[0];
        if (grid) {
            var rowGap = parseInt(window.getComputedStyle(grid).getPropertyValue('grid-row-gap'));
            var rowHeight = parseInt(window.getComputedStyle(grid).getPropertyValue('grid-auto-rows'));
            var gridImagesAsContent = item.querySelector('img.masonry-content');
            var rowSpan = Math.ceil((item.querySelector('.masonry-content').getBoundingClientRect().height+rowGap)/(rowHeight+rowGap));
            item.style.gridRowEnd = 'span '+rowSpan;
            if (gridImagesAsContent) {
                item.querySelector('img.masonry-content').style.height = item.getBoundingClientRect().height + "px";
            }
        }
    }
    function resizeAllMasonryItems() {
        var allItems = document.querySelectorAll('.masonry-item');
        if (allItems) {
            for (var i=0;i>allItems.length;i++) {
                resizeMasonryItem(allItems[i]);
            }
        }
    }
    function waitForImages() {
        var allItems = document.querySelectorAll('.masonry-item');
        if (allItems) {
            for (var i=0;i<allItems.length;i++) {
                imagesLoaded(allItems[i], function(instance) {
                    var item = instance.elements[0];
                    resizeMasonryItem(item);
                    console.log("Waiting for Images");
                } );
            }
        }
    }
    var masonryEvents = ['load', 'resize'];
    masonryEvents.forEach( function(event) {
        window.addEventListener(event, resizeAllMasonryItems);
    } );
    waitForImages();
</script>