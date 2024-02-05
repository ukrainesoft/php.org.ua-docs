---
navigation:
  - function.ldap-errno.md: « ldap\_errno
  - function.ldap-escape.md: ldap\_escape »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_error

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_error — Повернути повідомлення про помилку LDAP останньої команди

### Опис

```methodsynopsis
ldap_error(LDAP\Connection $ldap): string
```

Повертає рядкове повідомлення про помилку, пояснюючи помилку, згенеровану останньою командою LDAP для цього ідентифікатора з'єднання `ldap`. У той час як LDAP errno числа стандартизовані, різні бібліотеки повертають різний або навіть локалізовані текстові повідомлення про помилки. Ніколи не перевіряйте повідомлення про помилку на певний текст, завжди використовуйте коди помилок для перевірки.

Якщо ви не знизите достатньо попереджень у php.ini, або префікс ваших LDAP-команд не буде з символом @ для придушення виведення попереджень, генеровані помилки будуть також відображатися у вашому HTML виводі.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

### Значення, що повертаються

Повертає повідомлення помилки у вигляді рядка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |

### Дивіться також

-   [ldap\_err2str()](function.ldap-err2str.md) \- Перетворити код помилки LDAP на рядкове повідомлення про помилку
-   [ldap\_errno()](function.ldap-errno.md) \- Повернути номер помилки LDAP останньої команди
