---
navigation:
  - function.svn-add.md: « svn\_add
  - function.svn-auth-set-parameter.md: svn\_auth\_set\_parameter »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_auth\_get\_parameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_auth\_get\_parameter

(PECL svn >= 0.1.0)

svn\_auth\_get\_parameter — Повертає параметр автентифікації

### Опис

```methodsynopsis
svn_auth_get_parameter(string $key): string
```

Повертає параметр аутентифікації за ключем `key`. Список можливих ключів та їх значень доступний у [списку констант аутентифікації](svn.constants.md#svn.constants.auth)

### Список параметрів

`key`

Ім'я ключа (рядок). Щоб вказати ключ, використовуйте [список констант аутентифікації](svn.constants.md#svn.constants.auth), Визначений даним модулем.

### Значення, що повертаються

Возвращает значение параметра по ключу`key` у вигляді рядка, або \*\*`null`\*\*якщо параметр не існує.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

-   [svn\_auth\_set\_parameter()](function.svn-auth-set-parameter.md) \- Встановлює параметр автентифікації
-   [Константи аутентифікації](svn.constants.md#svn.constants.auth)
