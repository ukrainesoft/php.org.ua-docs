Задає кодовий набір тексту

-   [« ImagickDraw::setTextDecoration](imagickdraw.settextdecoration.html)
    
-   [ImagickDraw::setTextInterlineSpacing »](imagickdraw.settextinterlinespacing.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Задає кодовий набір тексту
    

# ImagickDraw::setTextEncoding

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextEncoding — Задає кодовий набір тексту

### Опис

```methodsynopsis
public ImagickDraw::setTextEncoding(string $encoding): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Задає кодовий набір, який використовуватиметься для текстових анотацій. Єдине кодування символів, яке може бути вказане в даний час, це "UTF-8" для представлення Unicode як послідовності байтів. Вкажіть порожній рядок, щоб встановити кодування тексту за промовчанням у системі. Для успішного анотування тексту з Unicode можуть знадобитися шрифти, які підтримують Unicode.

### Список параметрів

`encoding`

Ім'я кодування.

### Значення, що повертаються

Функція не повертає значення після виконання.