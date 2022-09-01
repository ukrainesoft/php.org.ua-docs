---
navigation:
  - function.ldap-search.html: « ldapsearch
  - function.ldap-set-rebind-proc.html: ldapsetrebindproc »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
title: ldapsetoption
---
# ldapsetoption

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

ldapsetoption — Встановити значення цієї опції

### Опис

```methodsynopsis
ldap_set_option(?LDAP\Connection $ldap, int $option, array|string|int|bool $value): bool
```

Встановлює значення вказаної опції в `value`

### Список параметрів

`ldap`

Або екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html) для встановлення опції для цього з'єднання, або **`null`** для встановлення опції глобально.

`option`

Опція `option` може бути однією з:

| Опция | Тип | Доступна с |
| --- | --- | --- |
| **`LDAP_OPT_DEREF`** | int |  |
| **`LDAP_OPT_SIZELIMIT`** | int |  |
| **`LDAP_OPT_TIMELIMIT`** | int |  |
| **`LDAP_OPT_NETWORK_TIMEOUT`** | int |  |
| **`LDAP_OPT_PROTOCOL_VERSION`** | int |  |
| **`LDAP_OPT_ERROR_NUMBER`** | int |  |
| **`LDAP_OPT_REFERRALS`** | bool |  |
| **`LDAP_OPT_RESTART`** | bool |  |
| **`LDAP_OPT_HOST_NAME`** | string |  |
| **`LDAP_OPT_ERROR_STRING`** | string |  |
| **`LDAP_OPT_DIAGNOSTIC_MESSAGE`** | string |  |
| **`LDAP_OPT_MATCHED_DN`** | string |  |
| **`LDAP_OPT_SERVER_CONTROLS`** | array |  |
| **`LDAP_OPT_CLIENT_CONTROLS`** | array |  |
| **`LDAP_OPT_X_KEEPALIVE_IDLE`** | int | PHP 7.1.0 |
| **`LDAP_OPT_X_KEEPALIVE_PROBES`** | int | PHP 7.1.0 |
| **`LDAP_OPT_X_KEEPALIVE_INTERVAL`** | int | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_CACERTDIR`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_CACERTFILE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_CERTFILE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_CIPHER_SUITE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_CRLCHECK`** | int | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_CRLFILE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_DHFILE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_KEYFILE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_PROTOCOL_MIN`** | int | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_RANDOM_FILE`** | string | PHP 7.1.0 |
| **`LDAP_OPT_X_TLS_REQUIRE_CERT`** | int | PHP 7.0.5 |

**`LDAP_OPT_SERVER_CONTROLS`** і **`LDAP_OPT_CLIENT_CONTROLS`** вимагають список елементів керування. Це означає, що значення має бути масивом елементів керування. Елемент управління складається з *oid*, що визначає елемент управління, опціонального *значення*, та додаткового прапора для *критичності*. У PHP елемент керування задається масивом, що містить елемент із ключем *oid* і рядковим значенням і двома необов'язковими елементами. Необов'язкові елементи є ключем *value* з рядковим значенням та ключем *iscritical* з логічним значенням . *iscritical* за замовчуванням встановлюється в ***`false`***, якщо не вказано. Для більш детальної інформації дивіться [» draft-ietf-ldapext-ldap-c-api-xx.txt](http://www.openldap.org/devel/cvsweb.cgi/~checkout~/doc/drafts/draft-ietf-ldapext-ldap-c-api-xx.txt). Дивіться також другий приклад, наведений нижче.

`value`

Нове значення для зазначеної `option` (Опції).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Встановлює версію протоколу**

```php
<?php
// $ds - действительный идентификатор связи с LDAP-сервером
if (ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3)) {
    echo "Используется LDAPv3";
} else {
    echo "Не удалось установить версию протокола в 3";
}
?>
```

**Приклад #2 Встановлює керування сервером**

```php
<?php
// $ds - действительный идентификатор связи с LDAP-сервером
// элемент управления с отсутствующим значением
$ctrl1 = array("oid" => "1.2.752.58.10.1", "iscritical" => true);
// iscritical по умолчанию FALSE
$ctrl2 = array("oid" => "1.2.752.58.1.10", "value" => "magic");
// попытка установить оба элемента управления
if (!ldap_set_option($ds, LDAP_OPT_SERVER_CONTROLS, array($ctrl1, $ctrl2))) {
    echo "Не удалось установить серверные элементы управления";
}
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція доступна лише при використанні OpenLDAP 2.x.x або Netscape Directory SDK x.x.

### Дивіться також

-   [ldapgetoption()](function.ldap-get-option.html) - Отримати поточне значення цієї опції
