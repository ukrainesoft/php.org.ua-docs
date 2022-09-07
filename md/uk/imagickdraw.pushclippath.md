---
navigation:
  - imagickdraw.push.md: '« ImagickDraw::push'
  - imagickdraw.pushdefs.md: 'ImagickDraw::pushDefs »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pushClipPath'
---
# ImagickDraw::pushClipPath

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pushClipPath — Запускає визначення шляху відсічного контуру

### Опис

```methodsynopsis
public ImagickDraw::pushClipPath(string $clip_mask_id): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Запускає визначення шляху відсічного контуру, який складається з будь-якої кількості команд малювання та завершується командою [ImagickDraw::popClipPath()](imagickdraw.popclippath.md)

### Список параметрів

`clip_mask_id`

Ідентифікатор маски відсічного контуру

### Значення, що повертаються

Функція не повертає значення після виконання.
