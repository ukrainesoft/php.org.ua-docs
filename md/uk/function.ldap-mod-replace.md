Замінити значення атрибутів на нові

-   [« ldap\_mod\_replace\_ext](function.ldap-mod_replace-ext.html)
    
-   [ldap\_modify\_batch »](function.ldap-modify-batch.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Замінити значення атрибутів на нові
    

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

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Асоціативний масив зі списком атрибутів, що замінюються. Якщо встановити порожній масив, то атрибут буде видалений. Якщо якийсь атрибут відсутній, він буде доданий.

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

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldap\_mod\_replace\_ext()](function.ldap-mod_replace-ext.html) - Замінити значення атрибута на нові
-   [ldap\_mod\_del()](function.ldap-mod-del.html) - Видалити значення атрибута із поточних атрибутів
-   [ldap\_mod\_add()](function.ldap-mod-add.html) - Додати значення атрибуту до поточних атрибутів
-   [ldap\_modify\_batch()](function.ldap-modify-batch.html) - Формування та запуск пакетної зміни запису LDAP