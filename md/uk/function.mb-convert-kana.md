Перетворення кодувань "kana" з одного в інше ("zen-kaku", "han-kaku" та інші)

-   [« mbconvertencoding](function.mb-convert-encoding.html)
    
-   [мбconvertvariables »](function.mb-convert-variables.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
    
-   Перетворення кодувань "kana" з одного в інше ("zen-kaku", "han-kaku" та інші)
    

# мбconvertkana

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбconvertkana - Перетворення кодувань "kana" з одного в інше ("zen-kaku", "han-kaku" та інші)

### Опис

```methodsynopsis
mb_convert_kana(string $string, string $mode = "KV", ?string $encoding = null): string
```

Здійснює перетворення "han-kaku" - "zen-kaku" для рядкового аргументу `string`. Ця функція може бути корисною лише для японської мови.

### Список параметрів

`string`

Початковий рядок (string).

`mode`

Налаштування конвертації.

Задається комбінацією наступних опцій.

**Можливі налаштування перетворення**

| Настройка | Описание |
| --- | --- |
| `r` | Перетворення "zen-kaku" букв на "han-kaku" |
| `R` | Перетворення "han-kaku" букв на "zen-kaku" |
| `n` | Перетворення "zen-kaku" чисел на "han-kaku" |
| `N` | Перетворення "han-kaku" чисел на "zen-kaku" |
| `a` | Перетворення "zen-kaku" букв і чисел на "han-kaku" |
| `A` | Перетворення "han-kaku" букв і чисел на "zen-kaku" (Для налаштувань "a", "A" символи беруться з діапазону U+0021 - U+007E, крім U+0022, U+0027, U+005C, U+007E) |
| `s` | Перетворення "zen-kaku" пропуску в "han-kaku" (U+3000 -> U+0020) |
| `S` | Перетворення "han-kaku" пропуску в "zen-kaku" (U+0020 -> U+3000) |
| `k` | Перетворення "zen-kaku kata-kana" на "han-kaku kata-kana" |
| `K` | Перетворення "han-kaku kata-kana" на "zen-kaku kata-kana" |
| `h` | Перетворення "zen-kaku hiragana" на "han-kaku katakana" |
| `H` | Перетворення "han-kaku katakana" на "zen-kaku hiragana" |
| `c` | Перетворення "zen-kaku katakana" на "zen-kaku hiragana" |
| `C` | Перетворення "zen-kaku hiragana" на "zen-kaku katakana" |
| `V` | Виготовляє згортку фонем і перетворює їх на символ. Використовується з "K", "H" |

`encoding`

Параметр `encoding` є символьним кодуванням. Якщо він опущений або дорівнює **`null`**, замість нього буде використано значення внутрішнього кодування.

### Значення, що повертаються

Перетворений рядок (string).

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **мбconvertkana()****

```php
<?php
/* Преобразование всех символов "kana" в "zen-kaku" "kata-kana" */
$str = mb_convert_kana($str, "KVC");

/* Преобразование "han-kaku" "kata-kana" в "zen-kaku" "kata-kana"
   и "zen-kaku" буквенно-цифровых символов в "han-kaku" */
$str = mb_convert_kana($str, "KVa");
?>
```