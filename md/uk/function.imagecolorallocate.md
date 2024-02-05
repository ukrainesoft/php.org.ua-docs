---
navigation:
  - function.imagecharup.md: « imagecharup
  - function.imagecolorallocatealpha.md: imagecolorallocatealpha »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorallocate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorallocate

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorallocate — Створення кольору зображення

### Опис

```methodsynopsis
imagecolorallocate(    GdImage $image,    int $red,    int $green,    int $blue): int|false
```

Повертає ідентифікатор кольору відповідно до заданих компонентів RGB.

**imagecolorallocate()** має викликатись для створення кожного кольору, який буде використовуватися у зображенні `image`

> **Зауваження** :
> 
> Перший виклик **imagecolorallocate()** задає колір фону у півлітрових зображеннях - зображеннях, створених функцією [imagecreate()](function.imagecreate.md)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

Ці аргументи можуть приймати або цілочисленні значення від 0 до 255, або шістнадцяткові в діапазоні від 0x00 до 0xFF.

### Значення, що повертаються

Ідентифікатор кольору, або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagecolorallocate()\*\*\*\*

```php
<?php

$im = imagecreate(100, 100);

// делаем фон красным
$background = imagecolorallocate($im, 255, 0, 0);

// создадим несколько цветов
$white = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// шестнадцатеричный способ
$white = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);
$black = imagecolorallocate($im, 0x00, 0x00, 0x00);

?>
```

### Дивіться також

-   [imagecolorallocatealpha()](function.imagecolorallocatealpha.md) \- Створення кольору для зображення
-   [imagecolordeallocate()](function.imagecolordeallocate.md) \- Розрив асоціації змінної із кольором для заданого зображення
