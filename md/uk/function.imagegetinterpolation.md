Отримує метод інтерполяції

-   [« imagegetclip](function.imagegetclip.html)
    
-   [imagegif »](function.imagegif.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
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

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Значення, що повертаються

Повертає метод інтерполяції.

### список змін

| Версия | Описание                                                                                          |
|--------|---------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [imagesetinterpolation()](function.imagesetinterpolation.html) - встановлює метод інтерполяції