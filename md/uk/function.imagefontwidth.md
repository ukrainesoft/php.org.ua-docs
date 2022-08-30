Отримання ширини шрифту

-   [« imagefontheight](function.imagefontheight.html)
    
-   [imageftbbox »](function.imageftbbox.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Отримання ширини шрифту
    

# imagefontwidth

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefontwidth — Отримання ширини шрифту

### Опис

```methodsynopsis
imagefontwidth(GdFont|int $font): int
```

Повертає ширину символу шрифту.

### Список параметрів

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.html), що повертається функцією [imageloadfont()](function.imageloadfont.html)

### Значення, що повертаються

Повертає ширину у пікселах

### список змін

| Версия | Описание                                                                                                                             |
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `font` тепер приймає як екземпляр [GdFont](class.gdfont.html), і ціле число (int); раніше приймалося лише ціле число (int). |

### Приклади

**Приклад #1 Використання **imagefontwidth()** на вбудованих шрифтах**

```php
<?php
echo 'Ширина шрифта: ' . imagefontwidth(4);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Font width: 8
```

**Приклад #2 Використання **imagefontwidth()** разом з [imageloadfont()](function.imageloadfont.html)**

```php
<?php
// загрузка .gdf шрифта
$font = imageloadfont('anonymous.gdf');

echo 'Ширина шрифта: ' . imagefontwidth($font);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Font width: 23
```

### Дивіться також

-   [imagefontheight()](function.imagefontheight.html) - Отримання висоти шрифту
-   [imageloadfont()](function.imageloadfont.html) - Завантаження шрифту