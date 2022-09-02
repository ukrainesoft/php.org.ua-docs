---
navigation:
  - function.ldap-mod_add-ext.md: « ldapmodaddext
  - function.ldap-mod_del-ext.md: ldapmoddelext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapmodadd
---
# ldapmodadd

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapmodadd — Додати значення атрибуту до поточних атрибутів

### Опис

```methodsynopsis
ldap_mod_add(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Додає один або більше атрибутів до зазначеного `dn`. Щоб додати повноцінний новий об'єкт, використовуйте [ldapadd()](function.ldap-add.md)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Асоціативний масив зі списком значень атрибутів, що додаються. Якщо атрибут ще не існує, то він буде доданий. Якщо атрибут вже існує, ви можете лише додати до нього значення, якщо він підтримує множинні значення.

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

-   [ldapmodaddext()](function.ldap-mod_add-ext.md) - Додати значення атрибуту до поточних атрибутів
-   [ldapmoddel()](function.ldap-mod-del.md) - Видалити значення атрибута із поточних атрибутів
-   [ldapmodreplace()](function.ldap-mod-replace.md) - Замінити значення атрибутів на нові
-   [ldapmodifybatch()](function.ldap-modify-batch.md) - Формування та запуск пакетної зміни запису LDAP
