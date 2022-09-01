---
navigation:
  - function.imagecreatefromstring.md: « imagecreatefromstring
  - function.imagecreatefromwbmp.md: imagecreatefromwbmp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromtga
---
# imagecreatefromtga

(PHP 7> = 7.4.0, PHP 8)

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

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс ([resource](language.types.resource.md) |
