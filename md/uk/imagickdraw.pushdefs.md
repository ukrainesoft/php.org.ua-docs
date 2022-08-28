Вказує, що наступні команди створюють іменовані елементи для ранньої обробки

-   [« ImagickDraw::pushClipPath](imagickdraw.pushclippath.html)
    
-   [ImagickDraw::pushPattern »](imagickdraw.pushpattern.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Вказує, що наступні команди створюють іменовані елементи для ранньої обробки
    

# ImagickDraw::pushDefs

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pushDefs — Вказує, що наступні команди створюють іменовані елементи для ранньої обробки

### Опис

```methodsynopsis
public ImagickDraw::pushDefs(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Вказує, що команди аж до завершальної команди [ImagickDraw::popDefs()](imagickdraw.popdefs.html) створюють іменовані елементи (наприклад, шляхи відсічного контуру, текстури тощо), які можуть безпечно оброблятися раніше для підвищення ефективності.

### Значення, що повертаються

Функція не повертає значення після виконання.