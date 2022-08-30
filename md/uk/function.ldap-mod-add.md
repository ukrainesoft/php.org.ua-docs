Додати значення атрибуту до поточних атрибутів

-   [« ldapmodaddext](function.ldap-mod_add-ext.html)
    
-   [ldapmoddelext »](function.ldap-mod_del-ext.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Додати значення атрибуту до поточних атрибутів
    

# ldapmodadd

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapmodadd — Додати значення атрибуту до поточних атрибутів

### Опис

```methodsynopsis
ldap_mod_add(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Додає один або більше атрибутів до зазначеного `dn`. Щоб додати повноцінний новий об'єкт, використовуйте [ldapadd()](function.ldap-add.html)

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Асоціативний масив зі списком значень атрибутів, що додаються. Якщо атрибут ще не існує, то він буде доданий. Якщо атрибут вже існує, ви можете лише додати до нього значення, якщо він підтримує множинні значення.

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                      |
|        | Додано підтримку параметра `controls`                                                                                                                  |

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldapmodaddext()](function.ldap-mod_add-ext.html) - Додати значення атрибуту до поточних атрибутів
-   [ldapmoddel()](function.ldap-mod-del.html) - Видалити значення атрибута із поточних атрибутів
-   [ldapmodreplace()](function.ldap-mod-replace.html) - Замінити значення атрибутів на нові
-   [ldapmodifybatch()](function.ldap-modify-batch.html) - Формування та запуск пакетної зміни запису LDAP