---
navigation:
  - function.ldap-add-ext.md: « ldap\_add\_ext
  - function.ldap-bind-ext.md: ldap\_bind\_ext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_add

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_add — Додати запис до LDAP директорії

### Опис

```methodsynopsis
ldap_add(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Додає запис до LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Масив, який визначає інформацію про запис. Значення запису індексуються індивідуальними атрибутами. У разі множинних значень для атрибуту вони індексуються з використанням цілих чисел, починаючи з 0.

```php
<?php
$entry["attribute1"] = "value";
$entry["attribute2"][0] = "value1";
$entry["attribute2"][1] = "value2";
?>
```

`controls`

Массив[керуючих констант LDAP](ldap.controls.md)для отправки в запросе.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Приклади

**Приклад #1 Повний приклад з автентичністю прив'язки**

```php
<?php
$ds = ldap_connect("localhost");  // предположим, что сервер LDAP находится тут

if ($ds) {
    // привязка к соответствующему dn для возможности обновления
    $r = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");

    // подготовить данные
    $info["cn"] = "John Jones";
    $info["sn"] = "Jones";
    $info["objectclass"] = "person";

    // добавить данные
    $r = ldap_add($ds, "cn=John Jones, o=My Company, c=US", $info);

    ldap_close($ds);
} else {
    echo "Невозможно соединиться с сервером LDAP";
}
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldap\_add\_ext()](function.ldap-add-ext.md) \- Додати записи до каталогу LDAP
-   [ldap\_delete()](function.ldap-delete.md) \- Видаляє запис із директорії LDAP
