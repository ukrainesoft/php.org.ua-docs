---
navigation:
  - function.ldap-mod_replace-ext.md: « ldapmodreplaceext
  - function.ldap-modify-batch.md: ldapmodifybatch »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapmodreplace
---
# ldapmodreplace

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapmodreplace — Замінити значення атрибутів на нові

### Опис

```methodsynopsis
ldap_mod_replace(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Замінює один або більше атрибутів із зазначеного `dn`. Також її можна використовувати для видалення чи додавання атрибутів.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Асоціативний масив зі списком атрибутів, що замінюються. Якщо встановити порожній масив, то атрибут буде видалений. Якщо якийсь атрибут відсутній, він буде доданий.

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

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldapmodreplaceext()](function.ldap-mod_replace-ext.md) - Замінити значення атрибута на нові
-   [ldapmoddel()](function.ldap-mod-del.md) - Видалити значення атрибута із поточних атрибутів
-   [ldapmodadd()](function.ldap-mod-add.md) - Додати значення атрибуту до поточних атрибутів
-   [ldapmodifybatch()](function.ldap-modify-batch.md) - Формування та запуск пакетної зміни запису LDAP
