---
navigation:
  - function.pspell-config-create.md: « pspell\_config\_create
  - function.pspell-config-dict-dir.md: pspell\_config\_dict\_dir »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_data\_dir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_data\_dir

(PHP 5, PHP 7, PHP 8)

pspell\_config\_data\_dir — Розташування файлів із мовними даними

### Опис

```methodsynopsis
pspell_config_data_dir(PSpell\Config $config, string $directory): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
