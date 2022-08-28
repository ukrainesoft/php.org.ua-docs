Видалити значення атрибута з поточних атрибутів

-   [« ldap\_mod\_del\_ext](function.ldap-mod_del-ext.html)
    
-   [ldap\_mod\_replace\_ext »](function.ldap-mod_replace-ext.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Видалити значення атрибута з поточних атрибутів
    

# ldapmoddel

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapmoddel — Видалити атрибути з поточних атрибутів.

### Опис

```methodsynopsis
ldap_mod_del(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Видаляє один або більше атрибутів із зазначеного `dn`. Видалення об'єктів здійснюється функцією [ldap\_delete()](function.ldap-delete.html)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

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

### Дивіться також

-   [ldap\_mod\_del\_ext()](function.ldap-mod_del-ext.html) - Видалити значення атрибутів із поточних атрибутів
-   [ldap\_mod\_add()](function.ldap-mod-add.html) - Додати значення атрибуту до поточних атрибутів
-   [ldap\_mod\_replace()](function.ldap-mod-replace.html) - Замінити значення атрибутів на нові
-   [ldap\_modify\_batch()](function.ldap-modify-batch.html) - Формування та запуск пакетної зміни запису LDAP