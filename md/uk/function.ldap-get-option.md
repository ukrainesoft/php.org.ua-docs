---
navigation:
  - function.ldap-get-entries.md: « ldap\_get\_entries
  - function.ldap-get-values-len.md: ldap\_get\_values\_len »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_get\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_get\_option

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

ldap\_get\_option — Отримати поточне значення цієї опції

### Опис

```methodsynopsis
ldap_get_option(LDAP\Connection $ldap, int $option, array|string|int &$value = null): bool
```

Устанавливает`value` значення зазначеної опції.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`option`

Опция`option` може бути однією з:

| Опция | Тип | Начиная с версии |
| --- | --- | --- |
| **`LDAP_OPT_DEREF`** | int |  |
| **`LDAP_OPT_SIZELIMIT`** | int |  |
| **`LDAP_OPT_TIMELIMIT`** | int |  |
| **`LDAP_OPT_NETWORK_TIMEOUT`** | int |  |
| **`LDAP_OPT_PROTOCOL_VERSION`** | int |  |
| **`LDAP_OPT_ERROR_NUMBER`** | int |  |
| **`LDAP_OPT_DIAGNOSTIC_MESSAGE`** | string |  |
| **`LDAP_OPT_REFERRALS`** | int |  |
| **`LDAP_OPT_RESTART`** | int |  |
| **`LDAP_OPT_HOST_NAME`** | string |  |
| **`LDAP_OPT_ERROR_STRING`** | string |  |
| **`LDAP_OPT_MATCHED_DN`** | string |  |
| **`LDAP_OPT_SERVER_CONTROLS`** | array |  |
| **`LDAP_OPT_CLIENT_CONTROLS`** | array |  |
| **`LDAP_OPT_X_KEEPALIVE_IDLE`** | int | 7.1 |
| **`LDAP_OPT_X_KEEPALIVE_PROBES`** | int | 7.1 |
| **`LDAP_OPT_X_KEEPALIVE_INTERVAL`** | int | 7.1 |
| **`LDAP_OPT_X_TLS_CACERTDIR`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_CACERTFILE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_CERTFILE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_CIPHER_SUITE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_CRLCHECK`** | int | 7.1 |
| **`LDAP_OPT_X_TLS_CRL_NONE`** | int | 7.1 |
| **`LDAP_OPT_X_TLS_CRL_PEER`** | int | 7.1 |
| **`LDAP_OPT_X_TLS_CRL_ALL`** | int | 7.1 |
| **`LDAP_OPT_X_TLS_CRLFILE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_DHFILE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_KEYFILE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_PACKAGE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_PROTOCOL_MIN`** | int | 7.1 |
| **`LDAP_OPT_X_TLS_RANDOM_FILE`** | string | 7.1 |
| **`LDAP_OPT_X_TLS_REQUIRE_CERT`** | int |  |

`value`

Буде встановлено значення опції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |

### Приклади

**Приклад #1 Перевірка версії протоколу**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection
if (ldap_get_option($ds, LDAP_OPT_PROTOCOL_VERSION, $version)) {
    echo "Используется версия протокола $version\n";
} else {
    echo "Невозможно определить версию протокола\n";
}
?>
```

### Примітки

> **Зауваження** :
> 
> Ця функція доступна лише при використанні OpenLDAP 2.x.x або Netscape Directory SDK x.x.

### Дивіться також

-   [ldap\_set\_option()](function.ldap-set-option.md) \- Встановити значення цієї опції
