---
hide_table_of_contents: true
description: Generate a presentation outline from slide titles.
tags: ["Docs", "Macros", "Presentations"]
---

import Video from '@site/src/components/Video/Video';

# Generate outline

Automatically generates a presentation outline based on titles.

```ts
(function()
{
    let presentation = Api.GetPresentation();
    let slides = presentation.GetAllSlides();
    let titles = [];
    
    slides.forEach(slide => {
        let titleShapes = slide.GetDrawingsByPlaceholderType("title");
        titleShapes.forEach(titleShape => {
            let docContent = titleShape.GetDocContent();
            let paragraphs = docContent.GetAllParagraphs();
            for (let paragraph of paragraphs) {
                titles.push(paragraph.GetText());
            }
        });
    });
    
    let slide = Api.CreateSlide();
    let shape = Api.CreateShape("rect", 100 * 36000, 50 * 36000);
    shape.SetPosition(608400, 1267200);
    
    let outlineTitle = Api.CreateParagraph();
    let outline = Api.CreateParagraph();
    outlineTitle.AddText("Outline");
    
    for (let title of titles) {
        outline.AddText(title);
    }

    outline.SetColor(0, 0, 0);
    outlineTitle.SetFontSize(48);
    outlineTitle.SetBold(true);
    outlineTitle.SetColor(0, 0, 0);
    
    let content = shape.GetDocContent();
    content.Push(outlineTitle);
    content.Push(outline);
    slide.AddObject(shape);
    presentation.AddSlide(slide);
})();
```

Methods used: [GetPresentation](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/GetPresentation.md), [GetAllSlides](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiPresentation/Methods/GetAllSlides.md), [GetDrawingsByPlaceholderType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiMaster/Methods/GetDrawingsByPlaceholderType.md), [GetDocContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiShape/Methods/GetDocContent.md), [CreateSlide](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/CreateSlide.md), [CreateShape](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/CreateShape.md), [SetPosition](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiDrawing/Methods/SetPosition.md), [CreateParagraph](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/Api/Methods/CreateParagraph.md), [AddText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiParagraph/Methods/AddText.md), [SetColor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiRun/Methods/SetColor.md), [SetFontSize](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiRun/Methods/SetFontSize.md), [SetBold](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiRun/Methods/SetBold.md), [Push](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiDocumentContent/Methods/Push.md), [AddObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiSlide/Methods/AddObject.md), [AddSlide](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/presentation-api/ApiPresentation/Methods/AddSlide.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/presentation-editor/generate-outline" dark />
