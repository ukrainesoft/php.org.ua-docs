---
navigation:
  - function.ldap-mod_del-ext.md: « ldapmoddelext
  - function.ldap-mod_replace-ext.md: ldapmodreplaceext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapmoddel
---
# ldapmoddel

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapmoddel — Видалити атрибути з поточних атрибутів.

### Опис

```methodsynopsis
ldap_mod_del(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Видаляє один або більше атрибутів із зазначеного `dn`. Видалення об'єктів здійснюється функцією [ldapdelete()](function.ldap-delete.md)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

`controls`

Масив [управляющих констант LDAP](ldap.controls.md) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldapmoddelext()](function.ldap-mod_del-ext.md) - Видалити значення атрибутів із поточних атрибутів
-   [ldapmodadd()](function.ldap-mod-add.md) - Додати значення атрибуту до поточних атрибутів
-   [ldapmodreplace()](function.ldap-mod-replace.md) - Замінити значення атрибутів на нові
-   [ldapmodifybatch()](function.ldap-modify-batch.md) - Формування та запуск пакетної зміни запису LDAP
