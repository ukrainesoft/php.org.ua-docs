- [«ldap_escape](function.ldap-escape.md)
- [ldap_exop_refresh »](function.ldap-exop-refresh.md)

- [PHP Manual](index.md)
- [Функції LDAP](ref.ldap.md)
- Обертка для розширеної операції PASSWD

#ldap_exop_passwd

(PHP 7 \>= 7.2.0, PHP 8)

ldap_exop_passwd — Обертка для розширеної операції PASSWD

### Опис

**ldap_exop_passwd**(
[LDAP\Connection](class.ldap-connection.md) `$ldap`,
string `$user` = "",
string `$old_password` = "",
string `$new_password` = "",
array `&$controls` = **`null`**
): string\|bool

Виконує розширену операцію PASSWD.

### Список параметрів

`ldap`
Примірник [LDAP\Connection](class.ldap-connection.md), що повертається
функцією [ldap_connect()](function.ldap-connect.md).

`user`
Унікальне ім'я користувача (DN), для якого змінюється пароль.

`old_password`
Старий пароль. Залежно від конфігурації можна опустити.

`new_password`
Новий пароль. Може бути опущений або заданий порожнім для автогенерації
пароля.

`controls`
Якщо задано, то із запитом буде передано запит парольної політики і це
поле буде заповнено масивом [керуючих констант LDAP](ldap.controls.md), повернутим запитом.

### Значення, що повертаються

Повертає новий пароль, якщо параметр `new_password` не заданий, або
заданий порожнім. Інакше повертає **`true`** або **`false`**, залежно
від успішності виконання.

### Список змін

| Версія | Опис                                                                                                                                                    |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.1.0  | Параметр ldap тепер очікує на екземпляр [LDAP\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |
| 8.0.0  | controls тепер припускає значення null; раніше значення за промовчанням було [].                                                                        |
| 7.3    | Додано підтримку параметра controls                                                                                                                     |

### Приклади

**Приклад #1 Розширена операція PASSWD**

`<?php$ds = ldap_connect("localhost"); // припустимо, що сервер LDAP запущено локальноif ($ds) {     // Прив'язуємось до потрібного DN   $bind = ldap_bind($ds, cn=s; if (!$bind) {      echo "Неможливо здійснити прив'язку LDAP"; exit; }    // Використовуємо PASSWD EXOP для зміни пароля користувача на новий випадковий    $genpw = ldap_exop_passwd($ds, cn=s c| if ($genpw) {       // Використовуємо для прив'язки новий пароль      $bind =ldap_bind($ds, "cn=root, o=My $; }    // Повертаємо старий пароль "secret"   ldap_exop_passwd($ds, "cn=root, o=My Company, c=US", $genpw, "secret"); ldap_close($ds);} else {    echo "Неможливо з'єднатися з сервером LDAP";}?> `

### Дивіться також

- [ldap_exop()](function.ldap-exop.md) - Виконати розширену
операцію
- [ldap_parse_exop()](function.ldap-parse-exop.md) - Розбір
результуючого об'єкта виконання розширеної операції LDAP
