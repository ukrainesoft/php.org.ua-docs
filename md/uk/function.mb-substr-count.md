Повертає кількість входжень підрядка

-   [« mb\_substitute\_character](function.mb-substitute-character.html)
    
-   [mb\_substr »](function.mb-substr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Повертає кількість входжень підрядка
    

# мбsubstrcount

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

мбsubstrcount — Повертає кількість входжень підрядка

### Опис

```methodsynopsis
mb_substr_count(string $haystack, string $needle, ?string $encoding = null): int
```

Підраховує, скільки разів підрядок `needle` зустрічається у рядку `haystack`

### Список параметрів

`haystack`

Рядок (string) для перевірки

`needle`

Рядок (string) для пошуку

`encoding`

Параметр `encoding` є символьним кодуванням. Якщо він опущений або дорівнює **`null`**, замість нього буде використано значення внутрішнього кодування.

### Значення, що повертаються

Кількість входжень підрядка `needle` у рядок `haystack`

### список змін

| Версия | Описание                                                    |
|--------|-------------------------------------------------------------|
|        | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **мбsubstrcount()****

```php
<?php
echo mb_substr_count("Это просто проверка", "то"); // выведет на экран 2
?>
```

### Дивіться також

-   [mb\_strpos()](function.mb-strpos.html) - Пошук позиції першого входження одного рядка до іншого
-   [mb\_substr()](function.mb-substr.html) - Повертає частину рядка
-   [substr\_count()](function.substr-count.html) - Повертає кількість входжень підрядка