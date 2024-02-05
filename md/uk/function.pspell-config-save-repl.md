---
navigation:
  - function.pspell-config-runtogether.md: « pspell\_config\_runtogether
  - function.pspell-new-config.md: pspell\_new\_config »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_save\_repl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_save\_repl

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_config\_save\_repl — Визначає, чи зберігати список заміщуваних пар разом зі списком слів

### Опис

```methodsynopsis
pspell_config_save_repl(PSpell\Config $config, bool $save): bool
```

**pspell\_config\_save\_repl()** визначає, чи буде [pspell\_save\_wordlist()](function.pspell-save-wordlist.md) зберігати пари разом зі списком слів. Зазвичай немає необхідності використовувати цю функцію, оскільки, якщо використовується [pspell\_config\_repl()](function.pspell-config-repl.md), заміщуючі пари будуть збережені [pspell\_save\_wordlist()](function.pspell-save-wordlist.md) у будь-якому випадку, і, якщо вона не використовується, заміщувальні пари не зберігатимуться.

**pspell\_config\_save\_repl()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.md)

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.md)

`save`

**`true`**, якщо заміщувальні пари повинні зберігатися, **`false`** в іншому випадку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

> **Зауваження** :
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
