---
navigation:
  - reserved.variables.cookies.md: COOKIE
  - reserved.variables.httpresponseheader.md: $httpresponseheader »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $phperrormsg
---
# $phperrormsg

(PHP 4, PHP 5, PHP 7)

$phperrormsg — Попереднє повідомлення про помилку

**Увага**

Ця функціональність оголошена *застарілої*, починаючи з PHP 7.2.0 і її украй не рекомендується використовувати.

Використовуйте функцію [errorgetlast()](function.error-get-last.md)

### Опис

$phperrormsg є змінною, що містить текст останньої помилки, згенерованої PHP. Ця змінна буде доступна тільки в блоці коду, в якому трапилася помилка, і тільки якщо увімкнено конфігураційну опцію [trackerrors](errorfunc.configuration.html#ini.track-errors) (за замовчуванням вимкнено).

**Увага**

Якщо налаштовано користувальницький обробник помилок ([seterrorhandler()](function.set-error-handler.md)), то $phperrormsg встановлюється лише в тому випадку, якщо обробник помилки повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Директива [trackerrors](errorfunc.configuration.html#ini.track-errors), через яку стає доступним $phperrormsg була видалена. |
|  | Директива [trackerrors](errorfunc.configuration.html#ini.track-errors), через яку стає доступним $phperrormsg, була оголошена застарілою. |

### Приклади

**Приклад #1 Приклад використання $phperrormsg**

```php
<?php
@strpos();
echo $php_errormsg;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Wrong parameter count for strpos()
```

### Дивіться також

-   [errorgetlast()](function.error-get-last.md) - Отримання інформації про останню помилку
