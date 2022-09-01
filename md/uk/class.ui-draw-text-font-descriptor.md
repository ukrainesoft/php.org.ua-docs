---
navigation:
  - ui-draw-text-font.getunderlinethickness.html: '« UIDrawTextFont::getUnderlineThickness'
  - ui-draw-text-font-descriptor.construct.html: 'ОЙDrawTextFontDescriptor::construct »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Дескриптор шрифту
---
# Дескриптор шрифту

(UI 0.9.9)

## Вступ

Описує шрифт

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Text\Font\Descriptor
     
     {


    /* Конструктор */
    
   public __construct(    string $family,    float $size,    int $weight = UI\Draw\Text\Font\Weight::Normal,    int $italic = UI\Draw\Text\Font\Italic::Normal,    int $stretch = UI\Draw\Text\Font\Stretch::Normal)


    /* Методы */
    public getFamily(): string
public getItalic(): int
public getSize(): float
public getStretch(): int
public getWeight(): int



   }
```

## Зміст

-   [ОЙDrawTextFontDescriptor::construct](ui-draw-text-font-descriptor.construct.html) - Конструктор класу Font Descriptor
-   [ОЙDrawTextFontDescriptor::getFamily](ui-draw-text-font-descriptor.getfamily.html) — Отримує сімейство шрифтів
-   [ОЙDrawTextFontDescriptor::getItalic](ui-draw-text-font-descriptor.getitalic.html) — Визначення стилю
-   [ОЙDrawTextFontDescriptor::getSize](ui-draw-text-font-descriptor.getsize.html) - Визначення розміру
-   [ОЙDrawTextFontDescriptor::getStretch](ui-draw-text-font-descriptor.getstretch.html) — Визначення стилю
-   [ОЙDrawTextFontDescriptor::getWeight](ui-draw-text-font-descriptor.getweight.html) — Визначення насиченості
