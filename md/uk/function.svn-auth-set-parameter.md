---
navigation:
  - function.svn-auth-get-parameter.md: « svn\_auth\_get\_parameter
  - function.svn-blame.md: svn\_blame »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_auth\_set\_parameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_auth\_set\_parameter

(PECL svn >= 0.1.0)

svn\_auth\_set\_parameter — Встановлює параметр автентифікації

### Опис

```methodsynopsis
svn_auth_set_parameter(string $key, string $value): void
```

Встановлює параметр аутентифікації на значення `value`по ключу`key`. Список можливих ключів та їх значень доступний у [списку констант аутентифікації](svn.constants.md#svn.constants.auth)

### Список параметрів

`key`

Ім'я ключа (Рядок). Щоб вказати ключ, використовуйте [список констант аутентифікації](svn.constants.md#svn.constants.auth), Визначений цим модулем.

`value`

Строкове значення параметра, що встановлюється за ключом. Формат значень може змінюватись в залежності від параметра.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Простий приклад автентифікації**

Цей приклад показує як налаштувати SVN, щоб ім'я користувача за промовчанням було 'Bob', а пароль за умовчанням - 'abc123':

```php
<?php
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_USERNAME, 'Bob');
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_PASSWORD, 'abc123');
?>
```

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

-   [svn\_auth\_get\_parameter()](function.svn-auth-get-parameter.md) \- Повертає параметр автентифікації
-   [Константи аутентифікації](svn.constants.md#svn.constants.auth)
