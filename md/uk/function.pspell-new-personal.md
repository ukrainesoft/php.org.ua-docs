---
navigation:
  - function.pspell-new-config.html: « pspellnewconfig
  - function.pspell-new.html: pspellnew »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellnewpersonal
---
# pspellnewpersonal

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellnewpersonal — Завантажує новий словник із персональним списком слів

### Опис

```methodsynopsis
pspell_new_personal(    string $filename,    string $language,    string $spelling = "",    string $jargon = "",    string $encoding = "",    int $mode = 0): PSpell\Dictionary|false
```

**pspellnewpersonal()** відкриває новий словник із персональним списком слів. Список слів може бути модифікований та збережений функцією [pspellsavewordlist()](function.pspell-save-wordlist.html), якщо знадобиться. Однак пари, що заміщають, не зберігаються. Для збереження заміщувальної пари ви повинні створити конфігурацію, використовуючи [pspellconfigcreate()](function.pspell-config-create.html)встановити файл персонального списку слів функцією [pspellconfigpersonal()](function.pspell-config-personal.html), встановити файл для заміну пар функцією [pspellconfigrepl()](function.pspell-config-repl.html), і відкрити новий словник за допомогою [pspellnewconfig()](function.pspell-new-config.html)

Більш детальну інформацію та приклади можна знайти у посібнику з pspell на сайті:[» http://aspell.net/](http://aspell.net/)

### Список параметрів

`filename`

Файл, до якого будуть збережені слова, додані до персонального списку. Це має бути абсолютний шлях до файлу, що починається з '/', тому що інакше він буде відносним до $HOME, яким є "/root" для більшості систем, що, ймовірно, не те, що вам потрібно.

`language`

Код мови, який складається з дволітерного коду мови за стандартом ISO 639 та необов'язкового дволітерного коду країни за стандартом ISO 3166 після тире або підкреслення.

`spelling`

Визначає варіант перевірки орфографії для мов із більш ніж одним варіантом правопису, таких як англійська. Відомі значення: 'american', 'british', і 'canadian'.

`jargon`

Додаткова інформація для розрізнення двох різних списків слів, що мають однакові параметри language та spelling.

`encoding`

Кодування, в якому, як очікується, надано слова. Допустимі значення: `utf-8` `iso8859-*` `koi8-r` `viscii` `cp1252` `machine unsigned 16` `machine unsigned 32`

`mode`

Режим, у якому працюватиме перевірка орфографії. Доступно кілька режимів:

-   **`PSPELL_FAST`** - Швидкий режим (найменше варіантів виправлення)
-   **`PSPELL_NORMAL`** - Нормальний режим (більше варіантів виправлення)
-   **`PSPELL_BAD_SPELLERS`** - Повільний режим (багато варіантів виправлення)
-   **`PSPELL_RUN_TOGETHER`** - Розглядає об'єднані слова як правильні складні слова. Тобто "thecat" буде вважатися правильним складним словом, хоча між артиклем і словом має бути пробіл. Зміна цієї установки впливає лише на результати, що повертаються функцією [pspellcheck()](function.pspell-check.html) [pspellsuggest()](function.pspell-suggest.html) продовжуватиме видавати варіанти виправлення.

Mode - це бітова маска, сконструйована з перелічених вище констант. Проте, **`PSPELL_FAST`** **`PSPELL_NORMAL`** і **`PSPELL_BAD_SPELLERS`** є взаємовиключними, тому ви повинні вибрати тільки одну з них.

### Значення, що повертаються

Повертає екземпляр [PSpellDictionary](class.pspell-dictionary.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PSpellDictionary](class.pspell-dictionary.html); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellnewpersonal()****

```php
<?php
$pspell = pspell_new_personal ("/var/dictionaries/custom.pws",
        "en", "", "", "", PSPELL_FAST|PSPELL_RUN_TOGETHER);
?>
```
