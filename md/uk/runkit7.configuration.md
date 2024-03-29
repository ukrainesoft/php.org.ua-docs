---
navigation:
  - runkit7.installation.md: « Встановлення
  - runkit7.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - runkit7.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Runkit**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [runkit.superglobal](runkit7.configuration.md#ini.runkit7.superglobal) | "" | **`INI_PERDIR`** |  |
| [runkit.internal\_override](runkit7.configuration.md#ini.runkit7.internal-override) | "0" | **`INI_SYSTEM`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`runkit.superglobal`string

Розділений комами список імен змінних, які розглядатимуться як суперглобальні. Це значення має бути встановлене у загальносистемному файлі php.ini, але може працювати в контекстах конфігурації perdir залежно від вашого SAPI.

**Приклад #1 Користувальницькі суперглобальні файли з runkit.superglobal=\_FOO,\_BAR у php.ini**

```php
<?php
function show_values() {
  echo "Foo is $_FOO\n";
  echo "Bar is $_BAR\n";
  echo "Baz is $_BAZ\n";
}

$_FOO = 'foo';
$_BAR = 'bar';
$_BAZ = 'baz';

/* Отобразит foo и bar, но не baz */
show_values();
?>
```

`runkit.internal_override`bool

Дозволяє змінювати/перейменовувати/вилучати внутрішні функції.
