---
navigation:
  - ldap.examples-basic.html: « Базовое использование
  - ref.ldap.md: Функції LDAP »
  - index.md: PHP Manual
  - ldap.examples.md: Приклади
title: LDAP Controls
---
## LDAP Controls

Нижче наведено кілька прикладів використання LDAP Controls з використанням PHP >= 7.3.0.

**Приклад #1 Прив'язка до інформації policy**

```php
<?php

$user   = 'cn=admin,dc=example,dc=com';
$passwd = 'adminpassword';

$ds = ldap_connect('ldap://localhost');

if ($ds) {
  $r = ldap_bind_ext($ds, $user, $passwd, [['oid' => LDAP_CONTROL_PASSWORDPOLICYREQUEST]]);

  if (ldap_parse_result($ds, $r, $errcode, $matcheddn, $errmsg, $referrals, $ctrls)) {
    if ($errcode != 0) {
      die("Ошибки: $errmsg ($errcode)");
    }
    if (isset($ctrls[LDAP_CONTROL_PASSWORDPOLICYRESPONSE])) {
      $value = $ctrls[LDAP_CONTROL_PASSWORDPOLICYRESPONSE]['value'];
      echo "Истекает: ".$value['expire']." seconds\n";
      echo "Количество оставшихся аутентификаций: ".$value['grace']."\n";
      if (isset($value['error'])) {
        echo "Код ошибки Ppolicy: ".$value['error'];
      }
    }
  }
} else {
  die("Невозможно подключиться к серверу LDAP");
}
?>
```

**Приклад #2 Зміна опису, якщо воно не порожнє**

```php
<?php
  // $link - это LDAP-соединение

  $result = ldap_mod_replace_ext(
    $link,
    'o=test,dc=example,dc=com',
    ['description' => 'New description'],
    [
      [
        'oid'         => LDAP_CONTROL_ASSERT,
        'iscritical'  => TRUE,
        'value'       => ['filter' => '(!(description=*))']
      ]
    ]
  );

  // Затем используйте ldap_parse_result
?>
```

**Приклад #3 Читання певних значень перед видаленням**

```php
<?php
  // $link - это LDAP-соединение

  $result = ldap_delete_ext(
    $link,
    'o=test,dc=example,dc=com',
    [
      [
        'oid'         => LDAP_CONTROL_PRE_READ,
        'iscritical'  => TRUE,
        'value'       => ['attrs' => ['o', 'description']]
      ]
    ]
  );

  // Затем используйте ldap_parse_result
?>
```

**Приклад #4 Видалення посилання**

```php
<?php
  // $link - это LDAP-соединение

  // Без управления он удалит ссылочный узел
  // Обязательно настройте управление так, чтобы избежать этого.
  $result = ldap_delete_ext(
    $link,
    'cn=reference,dc=example,dc=com',
    [['oid' => LDAP_CONTROL_MANAGEDSAIT, 'iscritical' => TRUE]]
  );

  // Затем используйте ldap_parse_result
?>
```

**Приклад #5 Використання пагінації для пошуку**

```php
<?php
  // $link - это LDAP-соединение

  $cookie = '';

  do {
    $result = ldap_search(
      $link, 'dc=example,dc=base', '(cn=*)', ['cn'], 0, 0, 0, LDAP_DEREF_NEVER,
      [['oid' => LDAP_CONTROL_PAGEDRESULTS, 'value' => ['size' => 2, 'cookie' => $cookie]]]
    );
    ldap_parse_result($link, $result, $errcode , $matcheddn , $errmsg , $referrals, $controls);
    // Чтобы сохранить пример, короткие ошибки не проверяются
    $entries = ldap_get_entries($link, $result);
    foreach ($entries as $entry) {
      echo "cn: ".$entry['cn'][0]."\n";
    }
    if (isset($controls[LDAP_CONTROL_PAGEDRESULTS]['value']['cookie'])) {
      // Вам необходимо передать cookie с последнего вызова на следующий
      $cookie = $controls[LDAP_CONTROL_PAGEDRESULTS]['value']['cookie'];
    } else {
      $cookie = '';
    }
    // Пустой cookie означает последнюю страницу
  } while (!empty($cookie));
?>
```
