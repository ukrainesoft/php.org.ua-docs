---
navigation:
  - function.imagecreatefromstring.md: « imagecreatefromstring
  - function.imagecreatefromwbmp.md: imagecreatefromwbmp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromtga
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromtga

(PHP 7 >= 7.4.0, PHP 8)

imagecreatefromtga — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromtga(string $filename): GdImage|false
```

**imagecreatefromtga()** повертає об'єкт зображення, що представляє зображення, одержане з цього імені файлу.

### Список параметрів

`filename`

Шлях до зображення Truevision TGA.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс ([resource](language.types.resource.md) |
