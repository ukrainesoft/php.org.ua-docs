---
navigation:
  - function.get-required-files.md: « get\_required\_files
  - function.getenv.md: getenv »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_resources
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_resources

(PHP 7, PHP 8)

get\_resources — Повертає активні ресурси

### Опис

```methodsynopsis
get_resources(?string $type = null): array
```

Повертає масив усіх поточних активних ресурсів, опціонально відфільтрований за типом ресурсу.

> **Зауваження**: Функція призначена для налагодження та тестування. Функцію не слід використовувати в робочому оточенні, особливо для доступу або навіть управління ресурсами, які зазвичай недоступні (наприклад, базовий ресурс потоку екземплярів [SplFileObject](class.splfileobject.md)

### Список параметрів

`type`

Якщо поставлено, то **get\_resources()** поверне лише ресурси зазначеного типу . [Список доступних типів ресурсів.](resource.md)

Якщо як тип заданий рядок `Unknown`, то будуть повернуті лише ресурси невідомого типу.

Якщо не задано, то буде повернено всі ресурси.

### Значення, що повертаються

Повертає масив поточних активних ресурсів, проіндексованих за номером ресурсу.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `type` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** get\_resources()\*\*\*\*

```php
<?php
$fp = tmpfile();
var_dump(get_resources());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [1]=>
  resource(1) of type (stream)
}
```

**Приклад #2 Приклад використання** get\_resources()\*\* з фільтрацією\*\*

```php
<?php
$fp = tmpfile();
var_dump(get_resources('stream'));
var_dump(get_resources('curl'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [1]=>
  resource(1) of type (stream)
}
array(0) {
}
```

### Дивіться також

-   [get\_loaded\_extensions()](function.get-loaded-extensions.md) \- Повертає масив імен усіх скомпілованих та завантажених модулів
-   [get\_defined\_constants()](function.get-defined-constants.md) \- Повертає асоціативний масив з іменами всіх констант та їх значень
-   [get\_defined\_functions()](function.get-defined-functions.md) \- Повертає масив усіх певних функцій
-   [get\_defined\_vars()](function.get-defined-vars.md) \- Повертає масив усіх певних змінних
