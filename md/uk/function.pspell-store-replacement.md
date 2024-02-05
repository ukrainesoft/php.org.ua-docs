---
navigation:
  - function.pspell-save-wordlist.md: « pspell\_save\_wordlist
  - function.pspell-suggest.md: pspell\_suggest »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_store\_replacement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_store\_replacement

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_store\_replacement — Зберігає заміщувальну пару для слова

### Опис

```methodsynopsis
pspell_store_replacement(PSpell\Dictionary $dictionary, string $misspelled, string $correct): bool
```

**pspell\_store\_replacement()** зберігає заміщувальну пару для слова, так що заміна пізніше може бути повернена функцією [pspell\_suggest()](function.pspell-suggest.md). Щоб використати переваги цієї функції, слід відкрити словник за допомогою [pspell\_new\_personal()](function.pspell-new-personal.md). Щоб назавжди зберегти пару, що заміщає, необхідно використовувати [pspell\_config\_personal()](function.pspell-config-personal.md) і [pspell\_config\_repl()](function.pspell-config-repl.md) для того, щоб вказати шлях, куди зберегти списки слів, а потім скористатися [pspell\_save\_wordlist()](function.pspell-save-wordlist.md)для записи изменений на диск.

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md)

`misspelled`

Слово з помилкою.

`correct`

Виправлене написання для слова з помилкою (`misspelled`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_store\_replacement()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_config($pspell_config);

pspell_store_replacement($pspell, $misspelled, $correct);
pspell_save_wordlist($pspell);
?>
```

### Примітки

> **Зауваження** :
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
