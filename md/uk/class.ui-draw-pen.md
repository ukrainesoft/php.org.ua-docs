Малювання за допомогою "Перо"

-   [« UIControlsBox::setPadded](ui-controls-box.setpadded.html)
    
-   [ОЙDrawPen::clip »](ui-draw-pen.clip.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Малювання за допомогою "Перо"
    

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

-   [ОЙDrawPen::clip](ui-draw-pen.clip.html) - Обрізати шлях
-   [ОЙDrawPen::fill](ui-draw-pen.fill.html) - Залити шлях
-   [ОЙDrawPen::restore](ui-draw-pen.restore.html) - Відновити
-   [ОЙDrawPen::save](ui-draw-pen.save.html) - Зберегти
-   [ОЙDrawPen::stroke](ui-draw-pen.stroke.html) - Обвести шлях
-   [ОЙDrawPen::transform](ui-draw-pen.transform.html) - Перетворити матрицю
-   [ОЙDrawPen::write](ui-draw-pen.write.html) — Намалювати текст у точці