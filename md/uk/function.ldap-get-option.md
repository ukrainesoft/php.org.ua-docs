---
navigation:
  - function.ldap-get-entries.html: « ldapgetentries
  - function.ldap-get-values-len.html: ldapgetvalueslen »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapgetoption
---
# ldapgetoption

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

ldapgetoption — Отримати поточне значення цієї опції

### Опис

```methodsynopsis
ldap_get_option(LDAP\Connection $ldap, int $option, array|string|int &$value = null): bool
```

Встановлює `value` значення зазначеної опції.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`option`

Опція `option` може бути однією з:

| Опция | Тип | Начиная с версии |
| --- | --- | --- |
| **`LDAP_OPT_DEREF`** | int |  |
| **`LDAP_OPT_SIZELIMIT`** | int |  |
| **`LDAP_OPT_TIMELIMIT`** | int |  |
| **`LDAP_OPT_NETWORK_TIMEOUT`** | int |  |
| **`LDAP_OPT_PROTOCOL_VERSION`** | int |  |
| **`LDAP_OPT_ERROR_NUMBER`** | int |  |
| **`LDAP_OPT_DIAGNOSTIC_MESSAGE`** | int |  |
| **`LDAP_OPT_REFERRALS`** | int |  |
| **`LDAP_OPT_RESTART`** | int |  |
| **`LDAP_OPT_HOST_NAME`** | string |  |
| **`LDAP_OPT_ERROR_STRING`** | string |  |
| **`LDAP_OPT_MATCHED_DN`** | string |  |
| **`LDAP_OPT_SERVER_CONTROLS`** | array |  |
| **`LDAP_OPT_CLIENT_CONTROLS`** | array |  |
| **`LDAP_OPT_X_KEEPALIVE_IDLE`** | int |  |
| **`LDAP_OPT_X_KEEPALIVE_PROBES`** | int |  |
| **`LDAP_OPT_X_KEEPALIVE_INTERVAL`** | int |  |
| **`LDAP_OPT_X_TLS_CACERTDIR`** | string |  |
| **`LDAP_OPT_X_TLS_CACERTFILE`** | string |  |
| **`LDAP_OPT_X_TLS_CERTFILE`** | string |  |
| **`LDAP_OPT_X_TLS_CIPHER_SUITE`** | string |  |
| **`LDAP_OPT_X_TLS_CRLCHECK`** | int |  |
| **`LDAP_OPT_X_TLS_CRL_NONE`** | int |  |
| **`LDAP_OPT_X_TLS_CRL_PEER`** | int |  |
| **`LDAP_OPT_X_TLS_CRL_ALL`** | int |  |
| **`LDAP_OPT_X_TLS_CRLFILE`** | string |  |
| **`LDAP_OPT_X_TLS_DHFILE`** | string |  |
| **`LDAP_OPT_X_TLS_KEYFILE`** | string |  |
| **`LDAP_OPT_X_TLS_PACKAGE`** | string |  |
| **`LDAP_OPT_X_TLS_PROTOCOL_MIN`** | int |  |
| **`LDAP_OPT_X_TLS_RANDOM_FILE`** | string |  |
| **`LDAP_OPT_X_TLS_REQUIRE_CERT`** | int |  |

`value`

Буде встановлено значення опції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Перевірка версії протоколу**

```php
<?php
// $ds допустимый экземпляр LDAP\Connection
if (ldap_get_option($ds, LDAP_OPT_PROTOCOL_VERSION, $version)) {
    echo "Используется версия протокола $version\n";
} else {
    echo "Невозможно определить версию протокола\n";
}
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція доступна лише при використанні OpenLDAP 2.x.x або Netscape Directory SDK x.x.

### Дивіться також

-   [ldapsetoption()](function.ldap-set-option.md) - Встановити значення цієї опції
