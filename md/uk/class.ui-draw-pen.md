---
navigation:
  - ui-controls-box.setpadded.md: '« UIControlsBox::setPadded'
  - ui-draw-pen.clip.md: 'ОЙDrawPen::clip »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Малювання за допомогою "Перо"
---
# Малювання за допомогою "Перо"

(UI 0.9.9)

## Вступ

Перо передається обробнику події "малювання області" (Area Draw), він використовується для обрізання, заповнення, обведення та запису в "шляху малювання" (Draw Paths).

## Огляд класів

```classsynopsis



    
     
      final
      class UI\Draw\Pen
     
     {


    /* Методы */
    
   public clip(UI\Draw\Path $path)
public fill(UI\Draw\Path $path, UI\Draw\Brush $with)
public fill(UI\Draw\Path $path, UI\Draw\Color $with)
public fill(UI\Draw\Path $path, int $with)
public restore()
public save()
public stroke(UI\Draw\Path $path, UI\Draw\Brush $with, UI\Draw\Stroke $stroke)
public stroke(UI\Draw\Path $path, UI\Draw\Color $with, UI\Draw\Stroke $stroke)
public stroke(UI\Draw\Path $path, int $with, UI\Draw\Stroke $stroke)
public transform(UI\Draw\Matrix $matrix)
public write(UI\Point $point, UI\Draw\Text\Layout $layout)

   }
```

## Зміст

-   [ОЙDrawPen::clip](ui-draw-pen.clip.md) - Обрізати шлях
-   [ОЙDrawPen::fill](ui-draw-pen.fill.md) - Залити шлях
-   [ОЙDrawPen::restore](ui-draw-pen.restore.md) - Відновити
-   [ОЙDrawPen::save](ui-draw-pen.save.md) - Зберегти
-   [ОЙDrawPen::stroke](ui-draw-pen.stroke.md) - Обвести шлях
-   [ОЙDrawPen::transform](ui-draw-pen.transform.md) - Перетворити матрицю
-   [ОЙDrawPen::write](ui-draw-pen.write.md) — Намалювати текст у точці
