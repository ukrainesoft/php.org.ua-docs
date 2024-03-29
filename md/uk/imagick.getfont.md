---
navigation:
  - imagick.getfilename.md: '« Imagick::getFilename'
  - imagick.getformat.md: 'Imagick::getFormat »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getFont'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getFont

(PECL imagick 2 >= 2.1.0, PECL imagick 3)

Imagick::getFont — Повертає назву шрифту

### Опис

```methodsynopsis
public Imagick::getFont(): string
```

Повертає значення шрифту об'єкта. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.7 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает строку, содержащую название шрифта или\*\*`false`\*\*якщо шрифт не встановлено.

### Дивіться також

-   [Imagick::setFont()](imagick.setfont.md) \- Встановлює шрифт
-   [ImagickDraw::setFont()](imagickdraw.setfont.md) \- Встановлює вказаний шрифт для використання під час анотування текстом
-   [ImagickDraw::getFont()](imagickdraw.getfont.md) \- Повертає шрифт
