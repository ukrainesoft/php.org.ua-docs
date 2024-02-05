---
navigation:
  - ui-controls-box.setpadded.md: '« UI\\Controls\\Box::setPadded'
  - ui-draw-pen.clip.md: 'UI\\Draw\\Pen::clip »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Малювання за допомогою "Перо"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Draw\\Pen::clip](ui-draw-pen.clip.md) \- Обрізати шлях
-   [UI\\Draw\\Pen::fill](ui-draw-pen.fill.md) \- Залити шлях
-   [UI\\Draw\\Pen::restore](ui-draw-pen.restore.md) \- Відновити
-   [UI\\Draw\\Pen::save](ui-draw-pen.save.md) \- Зберегти
-   [UI\\Draw\\Pen::stroke](ui-draw-pen.stroke.md) \- Обвести шлях
-   [UI\\Draw\\Pen::transform](ui-draw-pen.transform.md) \- Перетворює матрицю
-   [UI\\Draw\\Pen::write](ui-draw-pen.write.md)— Намалювати текст у точці
