Повертає поточне налаштування згладжування обведення

-   [« ImagickDraw::getGravity](imagickdraw.getgravity.html)
    
-   [ImagickDraw::getStrokeColor »](imagickdraw.getstrokecolor.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Повертає поточне налаштування згладжування обведення
    

# ImagickDraw::getStrokeAntialias

(PECL imagick 2, PECL imagick 3)

ImagickDraw::getStrokeAntialias — Повертає поточне налаштування згладжування обведення

### Опис

```methodsynopsis
public ImagickDraw::getStrokeAntialias(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає поточне налаштування згладжування обведення. За промовчанням обведені контури згладжуються. Коли згладжування вимкнено, для обведених пікселів встановлюється граничне значення, щоб визначити, чи слід використовувати колір обведення або базовий колір полотна.

### Значення, що повертаються

Повертає **`true`**, якщо згладжування увімкнено або **`false`**якщо вимкнено.