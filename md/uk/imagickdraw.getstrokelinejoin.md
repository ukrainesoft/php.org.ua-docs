Повертає форму, яка використовуватиметься в кутах контурів під час їх обведення

-   [« ImagickDraw::getStrokeLineCap](imagickdraw.getstrokelinecap.html)
    
-   [ImagickDraw::getStrokeMiterLimit »](imagickdraw.getstrokemiterlimit.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Повертає форму, яка використовуватиметься в кутах контурів під час їх обведення
    

# ImagickDraw::getStrokeLineJoin

(PECL imagick 2, PECL imagick 3)

ImagickDraw::getStrokeLineJoin — Повертає форму, яка буде використовуватися в кутах контурів під час їх обведення

### Опис

```methodsynopsis
public ImagickDraw::getStrokeLineJoin(): int
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає фігуру, яка використовуватиметься в кутах контурів (або інших векторних фігур) під час їх обведення.

### Значення, що повертаються

Повертає одну з констант [LINEJOIN](imagick.constants.html#imagick.constants.linejoin) `imagick::LINEJOIN_*`) або 0, якщо з'єднання лінії обведення не встановлено.