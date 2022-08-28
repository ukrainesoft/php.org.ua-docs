Малює дугу

-   [« GmagickDraw::annotate](gmagickdraw.annotate.html)
    
-   [GmagickDraw::bezier »](gmagickdraw.bezier.html)
    
-   [PHP Manual](index.html)
    
-   [GmagickDraw](class.gmagickdraw.html)
    
-   Малює дугу
    

# GmagickDraw::arc

(PECL gmagick >= Unknown)

GmagickDraw::arc — Малює дугу

### Опис

```methodsynopsis
public GmagickDraw::arc(    float $sx,    float $sy,    float $ex,    float $ey,    float $sd,    float $ed): GmagickDraw
```

Малює дугу, що знаходиться в межах прямокутника, що обмежує, на зображенні.

### Список параметрів

`sx`

Початкова координата x прямокутника, що обмежує.

`sy`

Початкова координата y обмежує прямокутника.

`ex`

Кінцева координата x прямокутника, що обмежує.

`ey`

Кінцева координата y обмежує прямокутника.

`sd`

Початковий градус повороту.

`ed`

Кінцевий градус повороту.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html)