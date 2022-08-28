Перелік послідовностей символів Unicode згрупованих за ними категоріями

-   [« IntlChar::enumCharNames](intlchar.enumcharnames.html)
    
-   [IntlChar::foldCase »](intlchar.foldcase.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перелік послідовностей символів Unicode згрупованих за ними категоріями
    

# IntlChar::enumCharTypes

(PHP 7, PHP 8)

IntlChar::enumCharTypes — Перелік послідовностей символів Unicode згрупованих за ними.

### Опис

```methodsynopsis
public static IntlChar::enumCharTypes(callable $callback): void
```

Перелік послідовностей символів Unicode згрупованих за ними категоріями. Корисно при побудові структур даних, для перебору всіх кодів символів і т.д.

Для кожного безперервного діапазону символів з однією категорією буде викликано функцію `callback`. Сусідні діапазони мають різні категорії. Стандарти Unicode гарантують числові значення від 0 до 31.

### Список параметрів

`callback`

Функція, яка буде викликана кожної безперервної послідовності з однаковою категорією. До неї будуть передані такі параметри:

-   int `$start` - Початковий символ діапазону
-   int `$end` - Кінцевий символ діапазону
-   int `$name` - Категорія символів (одна з констант `IntlChar::CHAR_CATEGORY_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Перелік діапазонів категорій символів**

```php
<?php
IntlChar::enumCharTypes(function($start, $end, $type) {
    printf("U+%04x through U+%04x are in category %d\n", $start, $end, $type);
});
?>
```

Результат виконання цього прикладу:

```
U+0000 through U+0020 are in category 15
U+0020 through U+0021 are in category 12
U+0021 through U+0024 are in category 23
U+0024 through U+0025 are in category 25
U+0025 through U+0028 are in category 23
U+0028 through U+0029 are in category 20
U+0029 through U+002a are in category 21
U+002a through U+002b are in category 23
U+002b through U+002c are in category 24
U+002c through U+002d are in category 23
U+002d through U+002e are in category 19
U+002e through U+0030 are in category 23
U+0030 through U+003a are in category 9
...
```