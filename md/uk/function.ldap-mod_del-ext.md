Видалити значення атрибутів із поточних атрибутів

-   [« ldapmodadd](function.ldap-mod-add.html)
    
-   [ldapmoddel »](function.ldap-mod-del.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Видалити значення атрибутів із поточних атрибутів
    

# ldapmoddelext

(PHP 7> = 7.3.0, PHP 8)

ldapmoddelext — Видалити значення атрибутів із поточних атрибутів.

### Опис

```methodsynopsis
ldap_mod_del_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapmoddel()](function.ldap-mod-del.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldapmoddel()](function.ldap-mod-del.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Дивіться також

-   [ldapmoddel()](function.ldap-mod-del.html) - Видалити значення атрибута із поточних атрибутів
-   [ldapparseresult()](function.ldap-parse-result.html) - Витягти інформацію з результату