---
navigation:
  - function.mb-convert-encoding.md: « mb\_convert\_encoding
  - function.mb-convert-variables.md: mb\_convert\_variables »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_convert\_kana
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_convert\_kana

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_convert\_kana - Перетворює одне кодування "kana" в інше ("zen-kaku", "han-kaku" та інші)

### Опис

```methodsynopsis
mb_convert_kana(string $string, string $mode = "KV", ?string $encoding = null): string
```

Перетворює "han-kaku" - "zen-kaku" для рядкового аргументу `string`. Ця функція може бути корисною лише для японської мови.

### Список параметрів

`string`

Початковий рядок (string).

`mode`

Налаштування конвертації.

Задається комбінацією наступних опцій.

**Можливі налаштування перетворення**

| Настройка | Опис |
| --- | --- |
| `r` | Перетворення «zen-kaku» літер на «han-kaku» |
| `R` | Перетворення «han-kaku» букв на «zen-kaku» |
| `n` | Перетворення «zen-kaku» чисел на «han-kaku» |
| `N` | Перетворення «han-kaku» чисел на «zen-kaku» |
| `a` | Перетворення «zen-kaku» букв і чисел на «han-kaku» |
| `A` | Перетворення «han-kaku» букв і чисел на «zen-kaku» (Для налаштувань «a», «A» символи беруться з діапазону U+0021 — U+007E, крім U+0022, U+0027, U+005C, U+007E) |
| `s` | Перетворення "zen-kaku" пропуску в "han-kaku" (U+3000 → U+0020) |
| `S` | Перетворення «han-kaku» пропуску на «zen-kaku» (U+0020 → U+3000) |
| `k` | Перетворення "zen-kaku kata-kana" на "han-kaku kata-kana" |
| `K` | Перетворення «han-kaku kata-kana» на «zen-kaku kata-kana» |
| `h` | Перетворення "zen-kaku hiragana" в "hd-kaku katakana" |
| `H` | Перетворення «hankaku katakana» на «zen-kaku hiragana» |
| `c` | Перетворення "zen-kaku katakana" в "zen-kaku hiragana" |
| `C` | Перетворення "zen-kaku hiragana" в "zen-kaku katakana" |
| `V` | Згортає фонеми і перетворює їх на символ. Вказується разом із «K», «H» |

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає перетворений рядок (string).

### Помилки

Буде викинуто виняток [ValueError](class.valueerror.md)якщо комбінація заданих у параметрі `mode`режимов недопустима. НаПриклад,`«sS»`

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тепер викидається виняток[ValueError](class.valueerror.md), якщо комбінація встановлених у параметрі `mode` режимів неприпустима. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання функції** mb\_convert\_kana()\*\*\*\*

```php
<?php
/* Преобразование всех символов «kana» в «zen-kaku» «kata-kana» */

$str = mb_convert_kana($str, "KVC");

/* Преобразование «han-kaku» «kata-kana» в «zen-kaku» «kata-kana»
   и «zen-kaku» буквенно-цифровых символов в «han-kaku» */
$str = mb_convert_kana($str, "KVa");
?>
```
