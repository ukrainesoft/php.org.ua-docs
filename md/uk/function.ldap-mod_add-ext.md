Додати значення атрибуту до поточних атрибутів

-   [« ldap\_list](function.ldap-list.html)
    
-   [ldap\_mod\_add »](function.ldap-mod-add.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Додати значення атрибуту до поточних атрибутів
    

# ldapmodaddext

(PHP 7> = 7.3.0, PHP 8)

ldapmodaddext — Додати значення атрибуту до поточних атрибутів

### Опис

```methodsynopsis
ldap_mod_add_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_mod\_add()](function.ldap-mod-add.html), але повертає екземпляр [LDAP\\Result](class.ldap-result.html) для розбору за допомогою [ldap\_parse\_result()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldap\_mod\_add()](function.ldap-mod-add.html)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Повертає екземпляр [LDAP\\Result](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldap\_mod\_add()](function.ldap-mod-add.html) - Додати значення атрибуту до поточних атрибутів
-   [ldap\_parse\_result()](function.ldap-parse-result.html) - Витягти інформацію з результату