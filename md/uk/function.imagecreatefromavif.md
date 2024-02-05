---
navigation:
  - function.imagecreate.md: « imagecreate
  - function.imagecreatefrombmp.md: imagecreatefrombmp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromavif
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromavif

(PHP 8 >= 8.1.0)

imagecreatefromavif — Створює нове зображення з файлу чи URL

### Опис

```methodsynopsis
imagecreatefromavif(string $filename): GdImage|false
```

**imagecreatefromavif()** повертає об'єкт зображення, що представляє зображення, одержане з цього імені файлу.

### Список параметрів

`filename`

Дорога до растрового зображення AVIF.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
