Додає вузол градієнта

-   [« UIDrawBrushGradient](class.ui-draw-brush-gradient.html)
    
-   [ОЙDrawBrushGradient::delStop »](ui-draw-brush-gradient.delstop.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙDrawBrushGradient](class.ui-draw-brush-gradient.html)
    
-   Додає вузол градієнта
    

# ОЙDrawBrushGradient::addStop

(UI 2.0.0)

ОЙDrawBrushGradient::addStop — Додає вузол градієнта

### Опис

```methodsynopsis
public UI\Draw\Brush\Gradient::addStop(float $position, UI\Draw\Color $color): int
```

```methodsynopsis
public UI\Draw\Brush\Gradient::addStop(float $position, int $color): int
```

Додає вузол градієнта заданого кольору заданої позиції.

### Список параметрів

`position`

Позиція нового вузла.

`color`

Колір для нового вузла, можливо UIDrawColor або RRGGBBAA.

### Значення, що повертаються

Загальна кількість вузлів.