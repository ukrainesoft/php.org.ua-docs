---
navigation:
  - function.pspell-new-personal.md: « pspell\_new\_personal
  - function.pspell-save-wordlist.md: pspell\_save\_wordlist »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_new
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_new

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_new — Завантажує новий словник

### Опис

```methodsynopsis
pspell_new(    string $language,    string $spelling = "",    string $jargon = "",    string $encoding = "",    int $mode = 0): PSpell\Dictionary|false
```

**pspell\_new()** відкриває новий словник та повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md)для использования в других функциях pspell.

Більш детальну інформацію та приклади можна знайти у посібнику з pspell на сайті:[» http://aspell.net/](http://aspell.net/)

### Список параметрів

`language`

Параметр language - це код мови, який складається з дволітерного коду мови за стандартом ISO 639 та необов'язкового дволітерного коду країни за стандартом ISO 3166 після тире або підкреслення.

`spelling`

Параметр spelling визначає варіант перевірки орфографії для мов із більш ніж одним варіантом правопису, таких як англійська. Відомі значення: 'american', 'british', і 'canadian'.

`jargon`

Параметр jargon містить додаткову інформацію для розрізнення двох різних списків слів, що мають однакові параметри language та spelling.

`encoding`

Параметр encoding - це кодування, в якому, як очікується, дано слова. Допустимі значення: 'utf-8', 'iso8859-\*', 'koi8-r', 'viscii', 'cp1252', 'machine unsigned 16', 'machine unsigned 32'. Цей параметр ще не перевірено досить добре, тому будьте обережні під час його використання.

`mode`

Параметр mode - це режим, у якому працюватиме перевірка орфографії. Доступно кілька режимів:

-   \*\*`PSPELL_FAST`\*\*- Швидкий режим (найменше варіантів виправлення)
-   \*\*`PSPELL_NORMAL`\*\*- Нормальний режим (більше варіантів виправлення)
-   \*\*`PSPELL_BAD_SPELLERS`\*\*- Повільний режим (багато варіантів виправлення)
-   **`PSPELL_RUN_TOGETHER`** - Розглядає об'єднані слова як правильні складні слова. Тобто "thecat" буде вважатися правильним складним словом, хоча між артиклем і словом має бути пробіл. Зміна цієї установки впливає лише на результати, що повертаються функцією [pspell\_check()](function.pspell-check.md) [pspell\_suggest()](function.pspell-suggest.md) продовжуватиме видавати варіанти виправлення.

Mode - це бітова маска, сконструйована з перелічених вище констант. Однак, **`PSPELL_FAST`** **`PSPELL_NORMAL`** і **`PSPELL_BAD_SPELLERS`** є взаємовиключними, тому ви повинні вибрати тільки одну з них.

### Значення, що повертаються

Повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pspell\_new()\*\*\*\*

```php
<?php
$pspell = pspell_new("en", "", "", "",
                           (PSPELL_FAST|PSPELL_RUN_TOGETHER));
?>
```
