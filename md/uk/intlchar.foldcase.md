Здійснює перетворення регістра заданого символу

-   [« IntlChar::enumCharTypes](intlchar.enumchartypes.html)
    
-   [IntlChar::forDigit »](intlchar.fordigit.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Здійснює перетворення регістра заданого символу
    

# IntlChar::foldCase

(PHP 7, PHP 8)

IntlChar::foldCase — Перетворює регістр заданого символу.

### Опис

```methodsynopsis
public static IntlChar::foldCase(int|string $codepoint, int $options = IntlChar::FOLD_CASE_DEFAULT): int|string|null
```

Повертає код символу в регістрі відмінному від регістра переданого символу. Якщо символ не має уявлення в іншому регістрі, то буде повернутий переданий символ.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

`options`

**`IntlChar::FOLD_CASE_DEFAULT`** (за замовчуванням) або **`IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I`**

### Значення, що повертаються

Повертає *SimpleCaseFolding* для символу, якщо він є. В іншому випадку - сам символ у разі успішного виконання або **`null`** у разі виникнення помилки.