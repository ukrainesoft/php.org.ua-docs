Виконує розширену операцію

-   [« ldap\_exop\_whoami](function.ldap-exop-whoami.html)
    
-   [ldap\_explode\_dn »](function.ldap-explode-dn.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Виконує розширену операцію
    

# ldapexop

(PHP 7> = 7.2.0, PHP 8)

ldapexop — Виконує розширену операцію

### Опис

```methodsynopsis
ldap_exop(    LDAP\Connection $ldap,    string $request_oid,    string $request_data = null,    array $controls = null,    string &$response_data = ?,    string &$response_oid = ?): mixed
```

Виконує розширену операцію для заданого з'єднання `ldap` з OID операції `request_oid` та даними `request_data`

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.html), що повертається функцією [ldap\_connect()](function.ldap-connect.html)

`request_oid`

Ідентифікатор розширеної операції OID. Можна використовувати одну з констант **`LDAP_EXOP_START_TLS`** **`LDAP_EXOP_MODIFY_PASSWD`** **`LDAP_EXOP_REFRESH`** **`LDAP_EXOP_WHO_AM_I`** **`LDAP_EXOP_TURN`** або рядок з OID необхідної операції.

`request_data`

Дані для запиту на розширену операцію. Може бути **`null`** для операцій типу **`LDAP_EXOP_WHO_AM_I`**. Може знадобитися закодувати BER.

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для посилки у запиті.

`response_data`

Якщо встановлено, то буде заповнено даними, отриманими в результаті виконання операції. Якщо не встановлено, то для отримання даних можна використовувати ldapparseexop для одержаного об'єкта.

`retoid`

Якщо встановлено, то буде заповнено OID відповіді. Зазвичай збігається з запитом OID.

### Значення, що повертаються

Якщо використовується з `response_data`, то повертає **`true`** або **`false`**. Якщо використовується без `response_data`, то повертає ідентифікатор ресурсу або **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Додана підтримка `controls` |

### Приклади

**Приклад #1 Розширена операція Whoami**

```php
<?php
$ds = ldap_connect("localhost");   // предположим, что сервер LDAP запущен локально

if ($ds) {
    // Привязываемся к нужному DN
    $bind = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");
    if (!$bind) {
     echo "Невозможно осуществить привязку LDAP";
      exit;
    }

    // Вызываем WHOAMI EXOP
    $r = ldap_exop($ds, LDAP_EXOP_WHO_AM_I);

    // Разбираем полученный ответ
    ldap_parse_exop($ds, $r, $response_data);
    // Вывод: string(31) "dn:cn=root, o=My Company, c=US"
    var_dump($response_data);

    // То же самое, но с параметром $response_data
    $success = ldap_exop($ds, LDAP_EXOP_WHO_AM_I, NULL, NULL, $response_data, $retoid);
    if ($success) {
      var_dump($response_data);
    }

    ldap_close($ds);
} else {
    echo "Невозможно соединиться с сервером LDAP";
}
?>
```

### Дивіться також

-   [ldap\_parse\_result()](function.ldap-parse-result.html) - Витягти інформацію з результату
-   [ldap\_parse\_exop()](function.ldap-parse-exop.html) - Розбір результуючого об'єкта виконання розширеної операції LDAP
-   [ldap\_exop\_whoami()](function.ldap-exop-whoami.html) - Обгортка для розширеної операції WHOAMI
-   [ldap\_exop\_refresh()](function.ldap-exop-refresh.html) - Обгортка для розширеної операції Refresh
-   [ldap\_exop\_passwd()](function.ldap-exop-passwd.html) - Обгортка для розширеної операції PASSWD