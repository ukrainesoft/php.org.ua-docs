---
navigation:
  - ui-draw-text-font.getunderlinethickness.md: '« UI\\Draw\\Text\\Font::getUnderlineThickness'
  - ui-draw-text-font-descriptor.construct.md: 'UI\\Draw\\Text\\Font\\Descriptor::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Дескриптор шрифту
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Draw\\Text\\Font\\Descriptor::\_\_construct](ui-draw-text-font-descriptor.construct.md) \- Конструктор класу Font Descriptor
-   [UI\\Draw\\Text\\Font\\Descriptor::getFamily](ui-draw-text-font-descriptor.getfamily.md)— Отримує сімейство шрифтів
-   [UI\\Draw\\Text\\Font\\Descriptor::getItalic](ui-draw-text-font-descriptor.getitalic.md)— Визначення стилю
-   [UI\\Draw\\Text\\Font\\Descriptor::getSize](ui-draw-text-font-descriptor.getsize.md) \- Визначення розміру
-   [UI\\Draw\\Text\\Font\\Descriptor::getStretch](ui-draw-text-font-descriptor.getstretch.md)— Визначення стилю
-   [UI\\Draw\\Text\\Font\\Descriptor::getWeight](ui-draw-text-font-descriptor.getweight.md)— Визначення насиченості
