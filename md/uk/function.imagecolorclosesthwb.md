Отримання індексу кольору, що має заданий тон, білизну та затемнення

-   [« imagecolorclosestalpha](function.imagecolorclosestalpha.html)
    
-   [imagecolordeallocate »](function.imagecolordeallocate.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Отримання індексу кольору, що має заданий тон, білизну та затемнення
    

# imagecolorclosesthwb

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagecolorclosesthwb — Отримання індексу кольору, що має заданий тон, білизну та затемнення

### Опис

```methodsynopsis
imagecolorclosesthwb(    GdImage $image,    int $red,    int $green,    int $blue): int
```

Отримання індексу кольору, що має значення тону, білизни та затемнення найбільш близькі до заданого кольору.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

### Значення, що повертаються

Повертає цілий індекс кольору, що має значення тону, білизни і затемнення найбільш близькі до заданого кольору.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolorclosesthwb()****

```php
<?php
$im = imagecreatefromgif('php.gif');

echo 'HWB: ' . imagecolorclosesthwb($im, 116, 115, 152);

imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
HWB: 33
```

### Дивіться також

-   [imagecolorclosest()](function.imagecolorclosest.html) - Отримання індексу кольору найближчого до заданого