---
navigation:
  - function.ldap-add-ext.html: « ldapaddext
  - function.ldap-bind-ext.html: ldapbindext »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
title: ldapadd
---
# ldapadd

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapadd — Додати запис до LDAP директорії

### Опис

```methodsynopsis
ldap_add(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Додає запис до LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Масив, який визначає інформацію про запис. Значення запису індексуються індивідуальними атрибутами. У разі множинних значень для атрибуту вони індексуються з використанням цілих чисел, починаючи з 0.

```php
<?php
$entry["attribute1"] = "value";
$entry["attribute2"][0] = "value1";
$entry["attribute2"][1] = "value2";
?>
```

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
|  | Додано підтримку параметра `controls` |

### Приклади

**Приклад #1 Повний приклад з автентичністю прив'язки**

```php
<?php
$ds = ldap_connect("localhost");  // предположим, что сервер LDAP находится тут

if ($ds) {
    // привязка к соответствующему dn для возможности обновления
    $r = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");

    // подготовить данные
    $info["cn"] = "John Jones";
    $info["sn"] = "Jones";
    $info["objectclass"] = "person";

    // добавить данные
    $r = ldap_add($ds, "cn=John Jones, o=My Company, c=US", $info);

    ldap_close($ds);
} else {
    echo "Невозможно соединиться с сервером LDAP";
}
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldapaddext()](function.ldap-add-ext.html) - Додати записи до каталогу LDAP
-   [ldapdelete()](function.ldap-delete.html) - Видаляє запис із директорії LDAP
