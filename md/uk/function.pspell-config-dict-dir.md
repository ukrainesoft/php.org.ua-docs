---
navigation:
  - function.pspell-config-data-dir.html: « pspellconfigdatadir
  - function.pspell-config-ignore.html: pspellconfigignore »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellconfigdictdir
---
# pspellconfigdictdir

(PHP 5, PHP 7, PHP 8)

pspellconfigdictdir — Розташування основного списку слів

### Опис

```methodsynopsis
pspell_config_dict_dir(PSpell\Config $config, string $directory): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
