- [« ldap_add_ext](function.ldap-add-ext.md)
- [ldap_bind_ext »](function.ldap-bind-ext.md)

- [PHP Manual](index.md)
- [Функції LDAP](ref.ldap.md)
- Додати запис до LDAP директорії

#ldap_add

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap_add — Додати запис до LDAP директорії

### Опис

**ldap_add**(
[LDAP\Connection](class.ldap-connection.md) `$ldap`,
string `$dn`,
array `$entry`,
?array `$controls` = **`null`**
): bool

Додає запис до LDAP-директорії.

### Список параметрів

`ldap`
Примірник [LDAP\Connection](class.ldap-connection.md), що повертається
функцією [ldap_connect()](function.ldap-connect.md).

`dn`
Відмінне ім'я об'єкта LDAP.

`entry`
Масив, який визначає інформацію про запис. Значення у записі
індексуються індивідуальними атрибутами. У разі множинних
значень для атрибуту, вони індексуються з використанням цілих чисел,
починаючи із 0.

` <?php$entry["attribute1"] = "value";$entry["attribute2"][0] = "value1";$entry["attribute2"][1] = "value2";?> `

`controls` Масив [керуючих констант LDAP](ldap.controls.md) для надсилання в
запит.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                                    |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.1.0  | Параметр ldap тепер очікує на екземпляр [LDAP\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |
| 8.0.0  | controls тепер припускає значення null; раніше значення за промовчанням було [].                                                                        |
| 7.3    | Додано підтримку параметра controls                                                                                                                     |

### Приклади

**Приклад #1 Повний приклад з автентичністю прив'язки**

`<?php$ds = ldap_connect("localhost"); // припустимо, що сервер LDAP знаходиться тутif ($ds) {    // прив'язка до відповідному dn для можливості оновлення s= ; // підготувати дані    $info["cn"] = "John Jones"; $info["sn"] = "Jones"; $info["objectclass"] = "person"; // додати дані    $r = ldap_add($ds, "cn=John Jones, o=My Company, c=US", $info); ldap_close($ds);} else {    echo "Неможливо з'єднатися з сервером LDAP";}?> `

### Примітки

> **Примітка**: Ця функція безпечна для обробки даних у двійковій
> Формі.

### Дивіться також

- [ldap_add_ext()](function.ldap-add-ext.md) - Додати записи до
каталог LDAP
- [ldap_delete()](function.ldap-delete.md) - Видаляє запис з
директорії LDAP
