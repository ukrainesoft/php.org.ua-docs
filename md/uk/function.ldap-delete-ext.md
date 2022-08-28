Видалити запис із директорії

-   [« ldap\_count\_references](function.ldap-count-references.html)
    
-   [ldap\_delete »](function.ldap-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Видалити запис із директорії
    

# ldapdeleteext

(PHP 7> = 7.3.0, PHP 8)

ldapdeleteext — Видалити запис із директорії

### Опис

```methodsynopsis
ldap_delete_ext(LDAP\Connection $ldap, string $dn, ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_delete()](function.ldap-delete.html), але повертає екземпляр [LDAP\\Result](class.ldap-result.html) для розбору за допомогою [ldap\_parse\_result()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldap\_delete()](function.ldap-delete.html)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Повертає екземпляр [LDAP\\Result](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |

### Дивіться також

-   [ldap\_delete()](function.ldap-delete.html) - Видаляє запис із директорії LDAP
-   [ldap\_parse\_result()](function.ldap-parse-result.html) - Витягти інформацію з результату