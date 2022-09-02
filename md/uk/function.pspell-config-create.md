---
navigation:
  - function.pspell-clear-session.md: « pspellclearsession
  - function.pspell-config-data-dir.md: pspellconfigdatadir »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellconfigcreate
---
# pspellconfigcreate

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigcreate — Створює конфігурацію, яка використовується для відкриття словника

### Опис

```methodsynopsis
pspell_config_create(    string $language,    string $spelling = "",    string $jargon = "",    string $encoding = ""): PSpell\Config
```

Створює конфігурацію для відкриття словника.

**pspellconfigcreate()** має синтаксис, дуже схожий на синтаксис [pspellnew()](function.pspell-new.md). Фактично використання **pspellconfigcreate()** відразу після [pspellnewconfig()](function.pspell-new-config.md) дасть такий самий результат. Однак після створення нової конфігурації також можна використовувати функції **pspellconfig** до виклику [pspellnewconfig()](function.pspell-new-config.md) для здобуття переваг від деякої додаткової функціональності.

Більш детальну інформацію та приклади можна знайти у посібнику з pspell на сайті:[» http://aspell.net/](http://aspell.net/)

### Список параметрів

`language`

Параметр language - це код мови, який складається з дволітерного коду мови за стандартом ISO 639 та необов'язкового дволітерного коду країни за стандартом ISO 3166 після тире або підкреслення.

`spelling`

Параметр spelling визначає варіант перевірки орфографії для мов із більш ніж одним варіантом правопису, таких як англійська. Відомі значення: 'american', 'british', і 'canadian'.

`jargon`

Параметр jargon містить додаткову інформацію для розрізнення двох різних списків слів, що мають однакові параметри language та spelling.

`encoding`

Параметр encoding - це кодування, у якому, як очікується, дано слова. Допустимі значення: 'utf-8', 'iso8859-', 'koi8-r', 'viscii', 'cp1252', 'machine unsigned 16', 'machine unsigned 32'. Цей параметр ще не перевірено досить добре, тому будьте обережні під час його використання.

### Значення, що повертаються

Повертає екземпляр [PSpellConfig](class.pspell-config.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PSpellConfig](class.pspell-config.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellconfigcreate()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_personal($pspell_config, "en");
?>
```
