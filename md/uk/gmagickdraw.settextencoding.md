---
navigation:
  - gmagickdraw.settextdecoration.md: '« GmagickDraw::settextdecoration'
  - class.gmagickpixel.md: GmagickPixel »
  - index.md: PHP Manual
  - class.gmagickdraw.md: GmagickDraw
title: 'GmagickDraw::settextencoding'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Об'єкт [Gmagick](class.gmagick.md)
