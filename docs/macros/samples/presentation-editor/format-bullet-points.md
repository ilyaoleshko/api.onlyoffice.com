---
hide_table_of_contents: true
description: Format bullet point styles on presentation slides.
tags: ["Docs", "Macros", "Presentations"]
---

import Video from '@site/src/components/Video/Video';

# Format bullet points

Applies consistent formatting to bullet points.

```ts
(function () {
    let presentation = Api.GetPresentation();
    let slideCount = presentation.GetSlidesCount();
    let bullet = Api.CreateBullet("-");

    for (let i = 0; i < slideCount; i++) {
        let slide = presentation.GetSlideByIndex(i);
        let shapes = slide.GetAllShapes();

        shapes.forEach(function (shape) {
            let docContent = shape.GetDocContent();
            let paragraphs = docContent.GetAllParagraphs();
            paragraphs.forEach(function (paragraph) {
                let paragraphProperties = paragraph.GetParaPr();
                let indentLeft = paragraphProperties.GetIndLeft();

                if (indentLeft !== 0) {
                    paragraph.SetBullet(bullet);
                    paragraph.SetHighlight("white");
                }
            });
        });
    }
})();
```

Methods used: [GetPresentation](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/GetPresentation.md), [GetSlidesCount](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiPresentation/Methods/GetSlidesCount.md), [CreateBullet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/CreateBullet.md), [GetSlideByIndex](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiPresentation/Methods/GetSlideByIndex.md), [GetAllShapes](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiSlide/Methods/GetAllShapes.md), [GetDocContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiShape/Methods/GetDocContent.md), [GetParaPr](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiParagraph/Methods/GetParaPr.md), [GetIndLeft](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiParaPr/Methods/GetIndLeft.md), [SetBullet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiParagraph/Methods/SetBullet.md), [SetHighlight](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiParagraph/Methods/SetHighlight.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/presentation-editor/format-bullet-points" dark />
