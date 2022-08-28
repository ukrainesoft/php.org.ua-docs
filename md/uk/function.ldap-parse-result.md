Витягти інформацію з результату

-   [« ldap\_parse\_reference](function.ldap-parse-reference.html)
    
-   [ldap\_read »](function.ldap-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Витягти інформацію з результату
    

# ldapparseresult

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

ldapparseresult — Витягти інформацію з результату

### Опис

```methodsynopsis
ldap_parse_result(    LDAP\Connection $ldap,    LDAP\Result $result,    int &$error_code,    string &$matched_dn = null,    string &$error_message = null,    array &$referrals = null,    array &$controls = null): bool
```

Обробляє результат пошуку LDAP.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.html), що повертається [ldap\_list()](function.ldap-list.html) або [ldap\_search()](function.ldap-search.html)

`error_code`

Посилання на змінну, якій надається код помилки LDAP, або `0`якщо немає помилки.

`matched_dn`

Посилання на змінну, якій надається знайдений DN, якщо він визначається в запиті, інакше присвоюється **`null`**

`error_message`

Посилання на змінну, якій присвоюється повідомлення про помилку LDAP, або порожній рядок, якщо немає помилки.

`referrals`

Посилання на змінну, якій присвоюється масив (array) з усіма посиланнями (referral) як рядків, чи порожній масив, якщо вони повернули.

`controls`

Масив (array) LDAP Controls, які були відправлені замість відповіді.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Параметр `result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Додано підтримку параметра `controls` |

### Приклади

**Приклад #1 Приклад використання **ldapparseresult()****

```php
<?php
$result = ldap_search($ldap, "cn=userref,dc=my-domain,dc=com", "(cn=user*)");
$errcode = $dn = $errmsg = $refs =  null;
if (ldap_parse_result($ldap, $result, $errcode, $dn, $errmsg, $refs)) {
    // различные операции с $errcode, $dn, $errmsg и $refs
}
?>
```