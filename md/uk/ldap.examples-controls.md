- [« Базове використання](ldap.examples-basic.md)
- [Функції LDAP »](ref.ldap.md)

- [PHP Manual](index.md)
- [Приклади](ldap.examples.md)
- LDAP Controls

## LDAP Controls

Нижче наведено кілька прикладів використання LDAP Controls з
використанням PHP = 7.3.0.

**Приклад #1 Прив'язка до інформації policy**

` <?php$user   = 'cn=admin,dc=example,dc=com';$passwd = 'adminpassword';$ds = ldap_connect('ldap://localhost');if ($ds) {  $r =ldap_bind_ext($ds,$user,$passwd,[['oid' => LDAP_CONTROL_PASSWORDPOLICYREQUEST]]); if (ldap_parse_result($ds, $r, $errcode, $matcheddn, $errmsg, $referrals, $ctrls)) {   if ($errcode != r)|||| }   if (isset($ctrls[LDAP_CONTROL_PASSWORDPOLICYRESPONSE])) {     $value =$ctrls[LDAP_CONTROL_PASSWORDPOLICYRESPONSE]['value echo "Закінчується: ".$value['expire']." seconds
";      echo "Кількість що залишилися аутентифікацій: ".$value['grace']."
";      if (isset($value['error'])) {        echo "Код ошибки Ppolicy: ".$value['error'];      }    }  }} else {  die("Невозможно подключиться к серверу LDAP");} ?> `

**Приклад #2 Зміна опису, тільки якщо він не порожній**

` <?php  // $link - это LDAP-соединение  $result = ldap_mod_replace_ext(    $link,    'o=test,dc=example,dc=com',    ['description' => 'New description'],    [      [        ' oid'         => LDAP_CONTROL_ASSERT,        'iscritical'  => TRUE,        'value'       => ['filter' => '(!(description=*))']      ]    ]  ); // Потім використовуйте ldap_parse_result?> `

**Приклад #3 Читання певних значень перед видаленням**

` <?php  // $link - это LDAP-соединение  $result = ldap_delete_ext(    $link,    'o=test,dc=example,dc=com',    [      [        'oid'         => LDAP_CONTROL_PRE_READ,        'iscritical'  => TRUE , |      'value'       => ['attrs' => ['o', 'description']]       ]    ]  )); // Потім використовуйте ldap_parse_result?> `

**Приклад #4 Видалення посилання**

` <?php  /// $link - це LDAP-з'єднання  // Без управління він удалив посилальний вузол  // Обов'язково налаштуйте управління так, щоб уникнути $result = ldap_delete_ext(    $link,   'cn=reference,dc=example,dc=com',    [['oid' => LDAP_CONTROL_MANAGEDSAIT, 'iscritical' ]| ] // Потім використовуйте ldap_parse_result?> `

**Приклад #5 Використання пагінації для пошуку**

`<?php  // $link - це LDAP-з'єднання  $cookie = ''; do {   $result =ldap_search(    | , 'value' => ['size' => 2, 'cookie' => $cookie]]]    ); ldap_parse_result($link,$result,$errcode , $matcheddn , $errmsg , $referrals, $controls); // Щоб зберегти приклад, короткі помилки не перевіряються    $entries = ldap_get_entries($link, $result); foreach ($entries as $entry) {      echo "cn: ".$entry['cn'][0]."
";    }    if (isset($controls[LDAP_CONTROL_PAGEDRESULTS]['value']['cookie'])) {      // Вам необходимо передать cookie с последнего вызова на следующий      $cookie = $controls[LDAP_CONTROL_PAGEDRESULTS]['value'][ 'cookie'];   } else {      $cookie = '';    }    // Порожній cookie означає останню сторінку  |
