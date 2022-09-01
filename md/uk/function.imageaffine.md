---
navigation:
  - function.image2wbmp.md: « image2wbmp
  - function.imageaffinematrixconcat.md: imageaffinematrixconcat »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageaffine
---
# imageaffine

(PHP 5> = 5.5.0, PHP 7, PHP 8)

imageaffine — Повернути зображення, яке містить афінно-перетворене зображення src, використовуючи додаткову область обмеження

### Опис

```methodsynopsis
imageaffine(GdImage $image, array $affine, ?array $clip = null): GdImage|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`affine`

Масив із ключами від 0 до 5.

`clip`

Масив з ключами "x", "y", "width" та "height"; або **`null`**

### Значення, що повертаються

Повертає об'єкт із афінним зображенням у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `clip` тепер допускає значення null. |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |
