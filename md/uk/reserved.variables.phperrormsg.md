---
navigation:
  - reserved.variables.cookies.md: « $\_COOKIE
  - reserved.variables.httpresponseheader.md: $http\_response\_header »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $php\_errormsg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $php\_errormsg

(PHP 4, PHP 5, PHP 7)

$php\_errormsg — Попереднє повідомлення про помилку

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 7.2.0 і її украй не рекомендується використовувати.

Используйте функцию[error\_get\_last()](function.error-get-last.md)

### Опис

$php\_errormsg є змінною, що містить текст останньої помилки, згенерованої PHP. Ця змінна буде доступна тільки в блоці коду, в якому трапилася помилка, і лише якщо увімкнено конфігураційну опцію [track\_errors](errorfunc.configuration.md#ini.track-errors)(по умолчанию отключена).

**Увага**

Якщо налаштовано користувальницький обробник помилок ([set\_error\_handler()](function.set-error-handler.md)), то $php\_errormsg встановлюється лише в тому випадку, якщо обробник помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Директива[track\_errors](errorfunc.configuration.md#ini.track-errors), через яку стає доступним $php\_errormsg була видалена. |
| 7.2.0 | Директива[track\_errors](errorfunc.configuration.md#ini.track-errors), через яку стає доступним $php\_errormsg, була оголошена застарілою. |

### Приклади

**Приклад #1 Приклад використання $php\_errormsg**

```php
<?php
@strpos();
echo $php_errormsg;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Wrong parameter count for strpos()
```

### Дивіться також

-   [error\_get\_last()](function.error-get-last.md) \- Отримання інформації про останню помилку
