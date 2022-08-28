Отримання висоти шрифту

-   [« imageflip](function.imageflip.html)
    
-   [imagefontwidth »](function.imagefontwidth.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Отримання висоти шрифту
    

# imagefontheight

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefontheight — Отримання висоти шрифту

### Опис

```methodsynopsis
imagefontheight(GdFont|int $font): int
```

Повертає висоту пікселів символу заданого шрифту.

### Список параметрів

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.html), що повертається функцією [imageloadfont()](function.imageloadfont.html)

### Значення, що повертаються

Повертає висоту у пікселах.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `font` тепер приймає як екземпляр [GdFont](class.gdfont.html), і ціле число (int); раніше приймалося лише ціле число (int). |

### Приклади

**Приклад #1 Приклад використання **imagefontheight()** на вбудованих шрифтах**

```php
<?php
echo 'Font height: ' . imagefontheight(4);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Font height: 16
```

**Приклад #2 Використання **imagefontheight()** разом з [imageloadfont()](function.imageloadfont.html)**

```php
<?php
// загрузка .gdf шрифта
$font = imageloadfont('anonymous.gdf');

echo 'Высота шрифта: ' . imagefontheight($font);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Font height: 43
```

### Дивіться також

-   [imagefontwidth()](function.imagefontwidth.html) - Отримання ширини шрифту
-   [imageloadfont()](function.imageloadfont.html) - Завантаження шрифту