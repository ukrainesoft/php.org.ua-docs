---
navigation:
  - function.pspell-config-create.html: « pspellconfigcreate
  - function.pspell-config-dict-dir.html: pspellconfigdictdir »
  - index.html: PHP Manual
  - ref.pspell.html: Функции Pspell
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
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
