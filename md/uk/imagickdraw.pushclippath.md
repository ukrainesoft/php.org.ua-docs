Запускає визначення шляху відсічного контуру

-   [« ImagickDraw::push](imagickdraw.push.html)
    
-   [ImagickDraw::pushDefs »](imagickdraw.pushdefs.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Запускає визначення шляху відсічного контуру
    

# ImagickDraw::pushClipPath

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pushClipPath — Запускає визначення шляху відсічного контуру

### Опис

```methodsynopsis
public ImagickDraw::pushClipPath(string $clip_mask_id): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Запускає визначення шляху відсічного контуру, який складається з будь-якої кількості команд малювання та завершується командою [ImagickDraw::popClipPath()](imagickdraw.popclippath.html)

### Список параметрів

`clip_mask_id`

Ідентифікатор маски відсічного контуру

### Значення, що повертаються

Функція не повертає значення після виконання.