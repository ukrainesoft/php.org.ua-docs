Змінити ім'я запису

-   [« ldap\_rename\_ext](function.ldap-rename-ext.html)
    
-   [ldap\_sasl\_bind »](function.ldap-sasl-bind.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Змінити ім'я запису
    

# ldaprename

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

ldaprename — Змінити ім'я запису

### Опис

```methodsynopsis
ldap_rename(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): bool
```

Перейменування/переміщення запису, визначеного `dn`

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`new_rdn`

Новий RDN.

`new_parent`

Новий батьківський/переважаючий запис.

`delete_old_rdn`

Якщо **`true`**, старі значення RDN видаляються, інакше старі значення RDN зберігаються як унікальні значення запису.

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Примітки

> **Зауваження**
> 
> Ця функція працює лише з LDAPv3. Можливо, вам доведеться використати [ldap\_set\_option()](function.ldap-set-option.html) перед прив'язкою за допомогою LDAPv3. Ця функція доступна лише під час використання OpenLDAP 2.xx або Netscape Directory SDK x.x.

### Дивіться також

-   [ldap\_rename\_ext()](function.ldap-rename-ext.html) - Модифікувати назву запису
-   [ldap\_modify()](function.ldap-modify.html) - Псевдонім ldapmodreplace