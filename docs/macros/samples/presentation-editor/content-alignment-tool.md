---
hide_table_of_contents: true
description: Align text content within slide text boxes.
tags: ["Docs", "Macros", "Presentations"]
---

import Video from '@site/src/components/Video/Video';

# Content alignment tool

Consistently aligns text boxes and images throughout the entire presentation.

```ts
(function () {
    let presentation = Api.GetPresentation();

    // Configuration (values in EMU)
    let leftMargin = 10 * 36000;
    let topMargin = 15 * 36000;
    let verticalSpacing = 5 * 36000;

    for (let i = 0; i < presentation.GetSlidesCount(); i++) {
        let slide = presentation.GetSlideByIndex(i);
        let slideWidth = slide.GetWidth();
        let slideHeight = slide.GetHeight();

        let elements = slide.GetAllDrawings();
        if (!elements || !elements.length) {
            console.log("No items found on this slide");
            continue;
        }

        console.log("Number of items:", elements.length);

        let currentY = topMargin;

        elements.forEach(function (element, index) {
            let elementWidth = element.GetWidth();
            let elementHeight = element.GetHeight();

            element.SetPosition(leftMargin, currentY);
            console.log("Item " + (index + 1) + " placed: X=" + leftMargin + ", Y=" + currentY);

            currentY += elementHeight + verticalSpacing;
        });
    }

    console.log("Placement is complete!");
})();
```

Methods used: [GetPresentation](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/GetPresentation.md), [GetSlidesCount](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiPresentation/Methods/GetSlidesCount.md), [GetSlideByIndex](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiPresentation/Methods/GetSlideByIndex.md), [GetWidth](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiDrawing/Methods/GetWidth.md), [GetHeight](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiDrawing/Methods/GetHeight.md), [GetAllDrawings](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiSlide/Methods/GetAllDrawings.md), [GetWidth](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiSlide/Methods/GetWidth.md), [GetHeight](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiSlide/Methods/GetHeight.md), [SetPosition](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiDrawing/Methods/SetPosition.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/presentation-editor/content-alignment-tool" dark />
