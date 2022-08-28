Отримати властивість FCNFKCClosure для символу

-   [« IntlChar::getCombiningClass](intlchar.getcombiningclass.html)
    
-   [IntlChar::getIntPropertyMaxValue »](intlchar.getintpropertymaxvalue.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Отримати властивість FCNFKCClosure для символу
    

# IntlChar::getFCNFKCClosure

(PHP 7, PHP 8)

IntlChar::getFCNFKCClosure — Отримати властивість FCNFKCClosure для символу

### Опис

```methodsynopsis
public static IntlChar::getFC_NFKC_Closure(int|string $codepoint): string|false|null
```

Отримує властивість FCNFKCClosure для символу.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає властивість FCNFKCClosure для `codepoint` у вигляді рядка або порожній рядок, якщо його немає. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::getFC_NFKC_Closure("\u{2121}"));
var_dump(IntlChar::getFC_NFKC_Closure("\u{1D2D}"));
?>
```

Результат виконання цього прикладу:

```
string(3) "tel"
string(2) "æ"
```