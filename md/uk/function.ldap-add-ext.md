Додати записи до каталогу LDAP

-   [« ldapтоt61](function.ldap-8859-to-t61.html)
    
-   [ldapadd »](function.ldap-add.html)
    
-   [PHP Manual](index.md)
    
-   [Функції LDAP](ref.ldap.md)
    
-   Додати записи до каталогу LDAP
    

# ldapaddext

(PHP 7> = 7.3.0, PHP 8)

ldapaddext — Додати записи до каталогу LDAP

### Опис

```methodsynopsis
ldap_add_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldapadd()](function.ldap-add.html), але повертає екземпляр [LDAPResult](class.ldap-result.html) для розбору за допомогою [ldapparseresult()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldapadd()](function.ldap-add.html)

### Значення, що повертаються

Повертає екземпляр [LDAPResult](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Повертає екземпляр [LDAPResult](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldapadd()](function.ldap-add.html) - Додати запис до LDAP директорії
-   [ldapparseresult()](function.ldap-parse-result.html) - Витягти інформацію з результату