---
navigation:
  - function.ldap-mod-replace.md: « ldap\_mod\_replace
  - function.ldap-modify.md: ldap\_modify »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_modify\_batch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_modify\_batch

(PHP 5.4 >= 5.4.26, PHP 5.5 >= 5.5.10, PHP 5.6 >= 5.6.0, PHP 7, PHP 8)

ldap\_modify\_batch — Формування та запуск пакетної зміни запису LDAP

### Опис

```methodsynopsis
ldap_modify_batch(    LDAP\Connection $ldap,    string $dn,    array $modifications_info,    ?array $controls = null): bool
```

Модифікує існуючий запис у каталозі LDAP. Допустимо детальний опис модифікації.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Характерне ім'я об'єкта LDAP.

`modifications_info`

Масив, який описує необхідну модифікацію. Кожен запис цього масиву є асоціативним масивом з двома або трьома ключами: `attrib` задає ім'я атрибута для зміни, `modtype` задає тип модифікації та (залежно від типу модифікації) `values` задає масив значень атрибутів, що відповідає даній модифікації.

Допустимі значення для `modtype` :

**`LDAP_MODIFY_BATCH_ADD`**

Каждое значение заданное в`values`будет добавлено (как дополнительное значение) к атрибуту`attrib`

**`LDAP_MODIFY_BATCH_REMOVE`**

Каждое значение заданное в`values`будет удалено из атрибута заданного в`attrib`Ни одно значение не указанное в`values`не будет затронуто.

**`LDAP_MODIFY_BATCH_REMOVE_ALL`**

Усі значення будуть видалені у атрибуту `attrib`Параметр`values`не нужен.

**`LDAP_MODIFY_BATCH_REPLACE`**

Все существующие значения атрибута`attrib` будуть замінені значеннями зазначеними в `values`

Обратите внимание, что все значения`attrib` повинні бути рядками, всі значення `values` повинні бути масивами рядків та будь-які значення `modtype` повинні бути однією з констант LDAP\_MODIFY\_BATCH\_\*, Перерахованих вище.

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

**Приклад #1 Додавання контакту номера**

```php
<?php
$dn = "cn=John Smith,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "telephoneNumber",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => ["+1 555 555 1717"],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
?>
```

**Приклад #2 Перейменування користувача**

```php
<?php
$dn = "cn=John Smith,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "sn",
        "modtype" => LDAP_MODIFY_BATCH_REPLACE,
        "values"  => ["Smith-Jones"],
    ],
    [
        "attrib"  => "givenName",
        "modtype" => LDAP_MODIFY_BATCH_REPLACE,
        "values"  => ["Jack"],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
ldap_rename($connection, $dn, "cn=Jack Smith-Jones", NULL, TRUE);
?>
```

**Приклад #3 Додавання користувачу двох e-mail адрес**

```php
<?php
$dn = "cn=Jack Smith-Jones,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "mail",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => [
            "jack.smith@example.com",
            "jack.smith-jones@example.com",
        ],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
?>
```

**Приклад #4 Зміна пароля користувача**

```php
<?php
$dn = "cn=Jack Smith-Jones,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "userPassword",
        "modtype" => LDAP_MODIFY_BATCH_REMOVE,
        "values"  => ["Tr0ub4dor&3"],
    ],
    [
        "attrib"  => "userPassword",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => ["correct horse battery staple"],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
?>
```

**Приклад #5 Зміна пароля користувача (Active Directory)**

```php
<?php
function adifyPw($pw)
{
    return iconv("UTF-8", "UTF-16LE", '"' . $pw . '"');
}

$dn = "cn=Jack Smith-Jones,ou=Wizards,dc=ad,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "unicodePwd",
        "modtype" => LDAP_MODIFY_BATCH_REMOVE,
        "values"  => [adifyPw("Tr0ub4dor&3")],
    ],
    [
        "attrib"  => "unicodePwd",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => [adifyPw("correct horse battery staple")],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
```
