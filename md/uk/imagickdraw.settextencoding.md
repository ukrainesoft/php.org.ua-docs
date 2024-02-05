---
navigation:
  - imagickdraw.settextdecoration.md: '« ImagickDraw::setTextDecoration'
  - imagickdraw.settextinterlinespacing.md: 'ImagickDraw::setTextInterlineSpacing »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setTextEncoding'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setTextEncoding

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextEncoding — Задає кодовий набір тексту

### Опис

```methodsynopsis
public ImagickDraw::setTextEncoding(string $encoding): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Задає кодовий набір, який використовуватиметься для текстових анотацій. Єдине кодування символів, яке може бути вказане в даний час, це "UTF-8" для представлення Unicode як послідовності байтів. Вкажіть порожній рядок, щоб встановити кодування тексту за промовчанням у системі. Для успішного анотування тексту з Unicode можуть знадобитися шрифти, які підтримують Unicode.

### Список параметрів

`encoding`

Ім'я кодування.

### Значення, що повертаються

Функція не повертає значення після виконання.
