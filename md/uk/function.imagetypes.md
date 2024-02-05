---
navigation:
  - function.imagettftext.md: « imagettftext
  - function.imagewbmp.md: imagewbmp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagetypes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagetypes

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

imagetypes — Повертає список типів зображень, які підтримує PHP збірка

### Опис

```methodsynopsis
imagetypes(): int
```

Повертає типи зображень, що підтримуються поточною збіркою PHP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає бітове поле, що відповідає форматам зображень, які підтримуються поточною версією GD прилінкованою до PHP. Повертаються такі біти: **`IMG_AVIF`** **`IMG_BMP`** **`IMG_GIF`** **`IMG_JPG`** **`IMG_PNG`** **`IMG_WBMP`** **`IMG_XPM`** **`IMG_WEBP`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Добавлена константа\*\*`IMG_AVIF`\*\* |
| 7.2.0 | Добавлена константа\*\*`IMG_BMP`\*\* |
| 7.0.10 | Добавлена константа\*\*`IMG_WEBP`\*\* |

### Приклади

**Приклад #1 Перевірка підтримки PNG**

```php
<?php
if (imagetypes() & IMG_PNG) {
    echo "Поддержка PNG включена";
}
?>
```

### Дивіться також

-   [gd\_info()](function.gd-info.md) \- Виведення інформації про поточну встановлену GD бібліотеку
