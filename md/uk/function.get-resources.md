---
navigation:
  - function.get-required-files.md: « getrequiredfiles
  - function.getenv.md: getenv »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getresources
---
# getresources

(PHP 7, PHP 8)

getresources — Повертає активні ресурси

### Опис

```methodsynopsis
get_resources(?string $type = null): array
```

Повертає масив усіх поточних активних ресурсів, опціонально відфільтрований за типом ресурсу.

> **Зауваження**: Функція призначена для налагодження та тестування. Функцію не слід використовувати в робочому оточенні, особливо для доступу або навіть управління ресурсами, які зазвичай недоступні (наприклад, базовий ресурс потоку екземплярів [SplFileObject](class.splfileobject.md)

### Список параметрів

`type`

Якщо поставлено, то **getresources()** поверне лише ресурси зазначеного типу . [Список доступних типів ресурсів.](resource.md)

Якщо як тип заданий рядок `Unknown`, то будуть повернуті лише ресурси невідомого типу.

Якщо не задано, то буде повернено всі ресурси.

### Значення, що повертаються

Повертає масив поточних активних ресурсів, проіндексованих за номером ресурсу.

### список змін

| Версия | Описание |
| --- | --- |
|  | `type` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **getresources()****

```php
<?php
$fp = tmpfile();
var_dump(get_resources());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [1]=>
  resource(1) of type (stream)
}
```

**Приклад #2 Приклад використання **getresources()** з фільтрацією**

```php
<?php
$fp = tmpfile();
var_dump(get_resources('stream'));
var_dump(get_resources('curl'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [1]=>
  resource(1) of type (stream)
}
array(0) {
}
```

### Дивіться також

-   [getloadedextensions()](function.get-loaded-extensions.md) - Повертає масив імен усіх скомпілованих та завантажених модулів
-   [getdefinedconstants()](function.get-defined-constants.md) - Повертає асоціативний масив з іменами всіх констант та їх значень
-   [getdefinedfunctions()](function.get-defined-functions.md) - Повертає масив усіх певних функцій
-   [getdefinedvars()](function.get-defined-vars.md) - Повертає масив усіх певних змінних
