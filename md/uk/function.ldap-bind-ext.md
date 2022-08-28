Прив'язати до директорії LDAP

-   [« ldap\_add](function.ldap-add.html)
    
-   [ldap\_bind »](function.ldap-bind.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Прив'язати до директорії LDAP
    

# ldapbindext

(PHP 7> = 7.3.0, PHP 8)

ldapbindext — Прив'язати до директорії LDAP

### Опис

```methodsynopsis
ldap_bind_ext(    LDAP\Connection $ldap,    ?string $dn = null,    ?string $password = null,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_bind()](function.ldap-bind.html), але повертає екземпляр [LDAP\\Result](class.ldap-result.html) для розбору за допомогою [ldap\_parse\_result()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldap\_bind()](function.ldap-bind.html)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Повертає екземпляр [LDAP\\Result](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html)                            |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                        |

### Дивіться також

-   [ldap\_bind()](function.ldap-bind.html) - Прив'язати до LDAP директорії
-   [ldap\_parse\_result()](function.ldap-parse-result.html) - Витягти інформацію з результату