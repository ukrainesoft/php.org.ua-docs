---
navigation:
  - function.pspell-config-create.md: « pspellconfigcreate
  - function.pspell-config-dict-dir.md: pspellconfigdictdir »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellconfigdatadir
---
# pspellconfigdatadir

(PHP 5, PHP 7, PHP 8)

pspellconfigdatadir — Розташування файлів із мовними даними

### Опис

```methodsynopsis
pspell_config_data_dir(PSpell\Config $config, string $directory): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
