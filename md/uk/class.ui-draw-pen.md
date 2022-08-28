Малювання за допомогою "Перо"

-   [« UI\\Controls\\Box::setPadded](ui-controls-box.setpadded.html)
    
-   [UI\\Draw\\Pen::clip »](ui-draw-pen.clip.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
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

-   [UI\\Draw\\Pen::clip](ui-draw-pen.clip.html) - Обрізати шлях
-   [UI\\Draw\\Pen::fill](ui-draw-pen.fill.html) - Залити шлях
-   [UI\\Draw\\Pen::restore](ui-draw-pen.restore.html) - Відновити
-   [UI\\Draw\\Pen::save](ui-draw-pen.save.html) - Зберегти
-   [UI\\Draw\\Pen::stroke](ui-draw-pen.stroke.html) - Обвести шлях
-   [UI\\Draw\\Pen::transform](ui-draw-pen.transform.html) - Перетворити матрицю
-   [UI\\Draw\\Pen::write](ui-draw-pen.write.html) — Намалювати текст у точці