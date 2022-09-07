---
navigation:
  - function.ldap-rename-ext.md: « ldaprenameext
  - function.ldap-sasl-bind.md: ldapsaslbind »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldaprename
---
# ldaprename

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

ldaprename — Змінити ім'я запису

### Опис

```methodsynopsis
ldap_rename(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): bool
```

Перейменування/переміщення запису, визначеного `dn`

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`new_rdn`

Новий RDN.

`new_parent`

Новий батьківський/переважаючий запис.

`delete_old_rdn`

Якщо **`true`**, старі значення RDN видаляються, інакше старі значення RDN зберігаються як унікальні значення запису.

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

### Примітки

> **Зауваження**
> 
> Ця функція працює лише з LDAPv3. Можливо, вам доведеться використати [ldapsetoption()](function.ldap-set-option.md) перед прив'язкою за допомогою LDAPv3. Ця функція доступна лише під час використання OpenLDAP 2.xx або Netscape Directory SDK x.x.

### Дивіться також

-   [ldaprenameext()](function.ldap-rename-ext.md) - Модифікувати назву запису
-   [ldapmodify()](function.ldap-modify.md) - Псевдонім ldapmodreplace
