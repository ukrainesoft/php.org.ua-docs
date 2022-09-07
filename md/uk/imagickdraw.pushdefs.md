---
navigation:
  - imagickdraw.pushclippath.md: '« ImagickDraw::pushClipPath'
  - imagickdraw.pushpattern.md: 'ImagickDraw::pushPattern »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pushDefs'
---
# ImagickDraw::pushDefs

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pushDefs — Вказує, що наступні команди створюють іменовані елементи для ранньої обробки

### Опис

```methodsynopsis
public ImagickDraw::pushDefs(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Вказує, що команди аж до завершальної команди [ImagickDraw::popDefs()](imagickdraw.popdefs.md) створюють іменовані елементи (наприклад, шляхи відсічного контуру, текстури тощо), які можуть безпечно оброблятися раніше для підвищення ефективності.

### Значення, що повертаються

Функція не повертає значення після виконання.
