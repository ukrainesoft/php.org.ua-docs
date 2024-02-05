---
navigation:
  - function.mdentities.md: « htmlentities
  - function.mdspecialchars.md: htmlspecialchars »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: htmlspecialchars\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# htmlspecialchars\_decode

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

htmlspecialchars\_decode — Перетворює спеціальні HTML-сутності назад на символи

### Опис

```methodsynopsis
htmlspecialchars_decode(string $string, int $flags = ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401): string
```

Ця функція - антипод функції [htmlspecialchars()](function.mdspecialchars.md). Вона перетворює спеціальні HTML-сутності назад у символи.

Конвертовані сутності: `&amp;` `&quot;`(когда\*\*`ENT_NOQUOTES`**не установлена),`&#039;`(когда**`ENT_QUOTES`\*\*установлена),`&lt;`и`&gt;`

### Список параметрів

`string`

Рядок, який треба перетворити.

`flags`

Бітова маска з одного або декількох наступних прапорів, які вказують як обробляти лапки та які типи документів використовувати. Значення за умовчанням є `ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401`

**Доступні константи, які використовуються як параметр `flags`**

| Имя константы | Опис |
| --- | --- |
| **`ENT_COMPAT`** | Перетворює подвійні лапки та пропускає одинарні. |
| **`ENT_QUOTES`** | Перетворює і подвійні, і одинарні лапки. |
| **`ENT_NOQUOTES`** | Не перетворює ні подвійні, ні одинарні лапки. |
| **`ENT_SUBSTITUTE`** | Замінює некоректні кодові послідовності символом заміни Юнікоду U+FFFD у разі використання UTF-8 та &#FFFD; при використанні іншого кодування замість повернення порожнього рядка. |
| **`ENT_HTML401`** | Обробляти код як HTML 4.01. |
| **`ENT_XML1`** | Обробляти код як XML 1. |
| **`ENT_XHTML`** | Обробляти код як XHTML. |
| **`ENT_HTML5`** | Обробляти код, як HTML 5. |

### Значення, що повертаються

Повертає перетворений рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Значення за промовчанням `flags` змінено з **`ENT_COMPAT`**на**`ENT_QUOTES`** |

### Приклади

**Приклад #1 Приклад использования функции**htmlspecialchars\_decode()\*\*\*\*

```php
<?php
$str = "<p>this -&gt; &quot;</p>\n";

echo htmlspecialchars_decode($str);

// обратите внимание, что в данном случае кавычки не будут преобразованы
echo htmlspecialchars_decode($str, ENT_NOQUOTES);
?>
```

Результат виконання наведеного прикладу:

```
<p>this -> "</p>
<p>this -> &quot;</p>
```

### Дивіться також

-   [htmlspecialchars()](function.mdspecialchars.md) \- Перетворює спеціальні символи в HTML-сутності
-   [html\_entity\_decode()](function.md-entity-decode.md) \- Перетворює HTML-сутності на символи
-   [get\_html\_translation\_table()](function.get-html-translation-table.md) \- Повертає таблицю перетворень, використовувану функціями htmlspecialchars і htmlentities
