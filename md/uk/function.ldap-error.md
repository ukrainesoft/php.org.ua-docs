---
navigation:
  - function.ldap-errno.html: « ldaperrno
  - function.ldap-escape.html: ldapescape »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldaperror
---
# ldaperror

(PHP 4, PHP 5, PHP 7, PHP 8)

ldaperror — Повернути повідомлення про помилку LDAP останньої команди

### Опис

```methodsynopsis
ldap_error(LDAP\Connection $ldap): string
```

Повертає рядкове повідомлення про помилку, пояснюючи помилку, згенеровану останньою командою LDAP для цього ідентифікатора з'єднання `ldap`. У той час як LDAP errno числа стандартизовані, різні бібліотеки повертають різний або навіть локалізовані текстові повідомлення про помилки. Ніколи не перевіряйте повідомлення про помилку на певний текст, завжди використовуйте коди помилок для перевірки.

Якщо ви не знизите достатньо попереджень у php.ini, або префікс ваших LDAP-команд не буде з символом @ для придушення виведення попереджень, генеровані помилки будуть також відображатися у вашому HTML виводі.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

### Значення, що повертаються

Повертає повідомлення помилки у вигляді рядка.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldaperr2str()](function.ldap-err2str.html) - Перетворити код помилки LDAP на рядкове повідомлення про помилку
-   [ldaperrno()](function.ldap-errno.html) - Повернути номер помилки LDAP останньої команди
