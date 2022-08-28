Модифікувати назву запису

-   [« ldap\_read](function.ldap-read.html)
    
-   [ldap\_rename »](function.ldap-rename.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Модифікувати назву запису
    

# ldaprenameext

(PHP 7> = 7.3.0, PHP 8)

ldaprenameext — Модифікувати назву запису

### Опис

```methodsynopsis
ldap_rename_ext(    LDAP\Connection $ldap,    string $dn,    string $new_rdn,    string $new_parent,    bool $delete_old_rdn,    ?array $controls = null): LDAP\Result|false
```

Робить те саме, що й [ldap\_rename()](function.ldap-rename.html), але повертає екземпляр [LDAP\\Result](class.ldap-result.html) для розбору за допомогою [ldap\_parse\_result()](function.ldap-parse-result.html)

### Список параметрів

Дивіться [ldap\_rename()](function.ldap-rename.html)

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

-   [ldap\_rename()](function.ldap-rename.html) - Змінити ім'я запису
-   [ldap\_parse\_result()](function.ldap-parse-result.html) - Витягти інформацію з результату