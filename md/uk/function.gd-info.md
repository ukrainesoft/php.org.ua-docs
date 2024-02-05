---
navigation:
  - ref.image.md: « Функції GD та функції для роботи із зображеннями
  - function.getimagesize.md: getimagesize »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: gd\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gd\_info

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

gd\_info — Виведення інформації про поточну встановлену GD бібліотеку

### Опис

```methodsynopsis
gd_info(): array
```

Отримує інформацію про версію та можливості встановленої GD бібліотеки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив.

**Елементи масиву, що повертається з **gd\_info()****

| Атрибут | Смысловое значение |
| --- | --- |
| GD Version | Рядок (string), що містить версію `libgd` |
| FreeType Support | bool значення. . **`true`**, якщо компонент FreeType Support встановлено. |
| FreeType Linkage | Рядок (string), що містить опис, яким чином підключений компонент FreeType. Очікувані значення: 'with freetype', 'with TTF library', 'with unknown library'. Цей елемент буде визначений лише якщо `FreeType Support`имеет значение\*\*`true`\*\* |
| GIF Read Support | bool значення. . **`true`**, якщо включена підтримка читання (*reading* `GIF` зображень. |
| GIF Create Support | bool значення. . **`true`**, якщо включена підтримка запису (*creating* `GIF` зображень. |
| JPEG Support | bool значення. . **`true`**, якщо включена підтримка `JPEG` |
| PNG Support | bool значення. . **`true`**, якщо включена підтримка `PNG` |
| WBMP Support | bool значення. . **`true`**, якщо включена підтримка `WBMP` |
| XBM Support | bool значення. . **`true`**, якщо включена підтримка `XBM` |
| WebP Support | bool значення. . **`true`**, якщо включена підтримка `WebP` |
| AVIF Support | bool значення. . **`true`**, якщо включена підтримка `AVIF`. Доступно з PHP 8.1.0. |

### Приклади

**Пример #1 Пример использования**gd\_info()\*\*\*\*

```php
<?php
var_dump(gd_info());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(10) {
  ["GD Version"]=>
  string(24) "bundled (2.1.0 compatible)"
  ["FreeType Support"]=>
  bool(false)
  ["GIF Read Support"]=>
  bool(true)
  ["GIF Create Support"]=>
  bool(false)
  ["JPEG Support"]=>
  bool(false)
  ["PNG Support"]=>
  bool(true)
  ["WBMP Support"]=>
  bool(true)
  ["XBM Support"]=>
  bool(false)
  ["WebP Support"]=>
  bool(false)
  ["AVIF Support"]=>
  bool(false)
}
```

### Дивіться також

-   [imagepng()](function.imagepng.md) \- Виведення PNG зображення у браузер або файл
-   [imagejpeg()](function.imagejpeg.md) \- Виводить зображення у браузер або пише у файл
-   [imagegif()](function.imagegif.md) \- Виводить зображення у браузер або пише у файл
-   [imagewbmp()](function.imagewbmp.md) \- Виводить зображення у браузер або пише у файл
-   [imagewebp()](function.imagewebp.md) \- Виведення зображення WebP у браузер або файл
-   [imageavif()](function.imageavif.md) \- Виводить зображення у браузер або пише у файл
-   [imagetypes()](function.imagetypes.md) \- Повертає список типів зображень, які підтримує PHP збірка
