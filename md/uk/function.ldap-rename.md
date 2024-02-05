---
navigation:
  - function.ldap-rename-ext.md: « ldap\_rename\_ext
  - function.ldap-sasl-bind.md: ldap\_sasl\_bind »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_rename

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

ldap\_rename — Змінити ім'я запису

### Опис

```methodsynopsis
ldap_rename(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): bool
```

Перейменування/переміщення запису, визначеного `dn`

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`new_rdn`

Новий RDN.

`new_parent`

Новий батьківський/переважаючий запис.

`delete_old_rdn`

Якщо **`true`**, старі значення RDN видаляються, інакше старі значення RDN зберігаються як унікальні значення запису.

`controls`

Массив[керуючих констант LDAP](ldap.controls.md)для отправки в запросе.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Примітки

> **Зауваження** :
> 
> Ця функція працює лише з LDAPv3. Можливо, вам доведеться використати [ldap\_set\_option()](function.ldap-set-option.md) перед прив'язкою за допомогою LDAPv3. Ця функція доступна лише під час використання OpenLDAP 2.xx або Netscape Directory SDK x.x.

### Дивіться також

-   [ldap\_rename\_ext()](function.ldap-rename-ext.md) \- Модифікувати назву запису
-   [ldap\_modify()](function.ldap-modify.md) \- Псевдонім ldap\_mod\_replace
