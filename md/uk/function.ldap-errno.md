---
navigation:
  - function.ldap-err2str.html: « ldaperr2str
  - function.ldap-error.html: ldaperror »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldaperrno
---
# ldaperrno

(PHP 4, PHP 5, PHP 7, PHP 8)

ldaperrno — Повернути номер помилки LDAP останньої команди

### Опис

```methodsynopsis
ldap_errno(LDAP\Connection $ldap): int
```

Повертає стандартизований код помилки, повернутий останньою командою LDAP. Це число може бути перетворено на текстове повідомлення про помилку, використовуючи [ldaperr2str()](function.ldap-err2str.md)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.md)

### Значення, що повертаються

Повертає код помилки LDAP останньої команди для цього посилання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

Якщо ви не знизите достатньо попереджень у php.ini, або префікс ваших LDAP-команд не буде з символом @ для придушення виведення попереджень, генеровані помилки будуть також відображатися у вашому HTML виводі.

**Приклад #1 Генерування та фіксація помилки**

```php
<?php
// Этот пример содержит ошибку, которую мы поймаем
$ld = ldap_connect("localhost");
$bind = ldap_bind($ld);
// синтаксическая ошибка в выражении фильтра (errno 87),
// должно быть "objectclass=*" для того, чтобы это работало.
$res =  @ldap_search($ld, "o=Myorg, c=DE", "objectclass");
if (!$res) {
    echo "LDAP-Errno: " . ldap_errno($ld) . "<br />\n";
    echo "LDAP-Error: " . ldap_error($ld) . "<br />\n";
    die("Argh!<br />\n");
}
$info = ldap_get_entries($ld, $res);
echo $info["count"] . " подходящих записей.<br />\n";
?>
```

### Дивіться також

-   [ldaperr2str()](function.ldap-err2str.md) - Перетворити код помилки LDAP на рядкове повідомлення про помилку
-   [ldaperror()](function.ldap-error.md) - Повернути повідомлення про помилку LDAP останньої команди
