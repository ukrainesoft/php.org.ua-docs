Отримати всі бінарні значення із запису результату

-   [« ldap\_get\_option](function.ldap-get-option.html)
    
-   [ldap\_get\_values »](function.ldap-get-values.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Отримати всі бінарні значення із запису результату
    

# ldapgetvalueslen

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapgetvalueslen — Отримати всі бінарні значення із запису результату

### Опис

```methodsynopsis
ldap_get_values_len(LDAP\Connection $ldap, LDAP\ResultEntry $entry, string $attribute): array|false
```

Читає всі значення атрибута запису результату.

Ця функція використовується так само як і [ldap\_get\_values()](function.ldap-get-values.html) за винятком того, що обробляє двійкові дані, а не рядкові.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html)

`attribute`

### Значення, що повертаються

Повертає масив значень для атрибуту у разі успішного виконання та **`false`** у разі виникнення помилки. Окремі значення доступні за цілим індексом в масиві. Перший індекс 0. Число значень може бути знайдено за індексом "count" у результуючому масиві.

### список змін

| Версия | Описание                                                                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html)     |
|        | Параметр `entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [ldap\_get\_values()](function.ldap-get-values.html) - Отримує всі значення із запису результату