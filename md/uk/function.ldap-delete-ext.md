Видалити запис із директорії

-   [« ldapcountreferences](function.ldap-count-references.html)
    
-   [ldapdelete »](function.ldap-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Видалити запис із директорії
    

# ldapdeleteext

(PHP 7> = 7.3.0, PHP 8)

ldapdeleteext — Видалити запис із директорії

### Опис

```methodsynopsis
ldap_delete_ext(LDAP\Connection $ldap, string $dn, ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapdelete()](function.ldap-delete.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldapdelete()](function.ldap-delete.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Повертає екземпляр [LDAPResult](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html)                            |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                      |

### Дивіться також

-   [ldapdelete()](function.ldap-delete.html) - Видаляє запис із директорії LDAP
-   [ldapparseresult()](function.ldap-parse-result.html) - Витягти інформацію з результату