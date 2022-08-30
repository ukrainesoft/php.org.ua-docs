Отримує метод інтерполяції

-   [« imagegetclip](function.imagegetclip.md)
    
-   [imagegif »](function.imagegif.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Отримує метод інтерполяції
    

# imagegetinterpolation

(PHP 8)

imagegetinterpolation — Отримує метод інтерполяції

### Опис

```methodsynopsis
imagegetinterpolation(GdImage $image): int
```

Отримує встановлений метод інтерполяції. `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає метод інтерполяції.

### список змін

| Версия | Описание                                                                                        |
|--------|-------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [imagesetinterpolation()](function.imagesetinterpolation.md) - встановлює метод інтерполяції