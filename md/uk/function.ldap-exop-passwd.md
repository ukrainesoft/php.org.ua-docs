---
navigation:
  - function.ldap-escape.md: « ldapescape
  - function.ldap-exop-refresh.md: ldapexoprefresh »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapexoppasswd
---
# ldapexoppasswd

(PHP 7> = 7.2.0, PHP 8)

ldapexoppasswd — Обгортка для розширеної операції PASSWD

### Опис

```methodsynopsis
ldap_exop_passwd(    LDAP\Connection $ldap,    string $user = "",    string $old_password = "",    string $new_password = "",    array &$controls = null): string|bool
```

Виконує розширену операцію PASSWD.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`user`

Унікальне ім'я (DN) користувача, для якого змінюється пароль.

`old_password`

Старий пароль. Залежно від конфігурації можна опустити.

`new_password`

Новий пароль. Може бути опущений або заданий порожнім для автогенерації пароля.

`controls`

Якщо задано, то із запитом буде передано запит парольної політики і це поле буде заповнено масивом [управляющих констант LDAP](ldap.controls.md), повернутим запитом.

### Значення, що повертаються

Повертає новий пароль, якщо параметр `new_password` не заданий, або заданий порожнім. Інакше повертає **`true`** або **`false`**, Залежно від успішності виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Приклади

**Приклад #1 Розширена операція PASSWD**

```php
<?php
$ds = ldap_connect("localhost");  // предположим, что сервер LDAP запущен локально

if ($ds) {
    // Привязываемся к нужному DN
    $bind = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");
    if (!$bind) {
      echo "Невозможно осуществить привязку LDAP";
      exit;
    }

    // Используем PASSWD EXOP для смены пароля пользователя на новый случайный
    $genpw = ldap_exop_passwd($ds, "cn=root, o=My Company, c=US", "secret");
    if ($genpw) {
      // Используем для привязки новый пароль
      $bind = ldap_bind($ds, "cn=root, o=My Company, c=US", $genpw);
    }

    // Возвращаем старый пароль "secret"
    ldap_exop_passwd($ds, "cn=root, o=My Company, c=US", $genpw, "secret");

    ldap_close($ds);
} else {
    echo "Невозможно соединиться с сервером LDAP";
}
?>
```

### Дивіться також

-   [ldapexop()](function.ldap-exop.md) - Виконує розширену операцію
-   [ldapparseexop()](function.ldap-parse-exop.md) - Розбір результуючого об'єкта виконання розширеної операції LDAP
