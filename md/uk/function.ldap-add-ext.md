Додати записи до каталогу LDAP

-   [« ldap\_8859\_to\_t61](function.ldap-8859-to-t61.html)
    
-   [ldap\_add »](function.ldap-add.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Додати записи до каталогу LDAP
    

# ldapaddext

(PHP 7> = 7.3.0, PHP 8)

ldapaddext — Додати записи до каталогу LDAP

### Опис

```methodsynopsis
ldap_add_ext(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_add()](function.ldap-add.html), але повертає екземпляр [LDAP\\Result](class.ldap-result.html) для розбору за допомогою [ldap\_parse\_result()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldap\_add()](function.ldap-add.html)

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Повертає екземпляр [LDAP\\Result](class.ldap-result.html); раніше повертався ресурс ([resource](language.types.resource.html)                            |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                        |

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldap\_add()](function.ldap-add.html) - Додати запис до LDAP директорії
-   [ldap\_parse\_result()](function.ldap-parse-result.html) - Витягти інформацію з результату