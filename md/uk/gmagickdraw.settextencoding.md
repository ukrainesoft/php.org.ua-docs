Задає кодовий набір тексту

-   [« GmagickDraw::settextdecoration](gmagickdraw.settextdecoration.html)
    
-   [GmagickPixel »](class.gmagickpixel.html)
    
-   [PHP Manual](index.html)
    
-   [GmagickDraw](class.gmagickdraw.html)
    
-   Задає кодовий набір тексту
    

# GmagickDraw::settextencoding

(PECL gmagick >= Unknown)

GmagickDraw::settextencoding — Задає кодовий набір тексту

### Опис

```methodsynopsis
public GmagickDraw::settextencoding(string $encoding): GmagickDraw
```

Задає кодовий набір, який використовуватиметься для текстових анотацій. Єдине кодування символів, яке може бути вказане в даний час, це "UTF-8" для представлення Unicode як послідовності байтів. Вкажіть порожній рядок, щоб встановити кодування тексту за промовчанням у системі. Для успішного анотування тексту з Unicode можуть знадобитися шрифти, які підтримують Unicode.

### Список параметрів

`encoding`

Рядок символів, що визначає кодування тексту.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html)