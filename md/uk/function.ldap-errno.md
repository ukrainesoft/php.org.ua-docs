- [« ldap_err2str](function.ldap-err2str.md)
- [ldap_error »](function.ldap-error.md)

- [PHP Manual](index.md)
- [Функції LDAP](ref.ldap.md)
- Повернути номер помилки LDAP останньої команди

#ldap_errno

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap_errno — Повернути номер помилки LDAP останньої команди

### Опис

**ldap_errno**([LDAP\Connection](class.ldap-connection.md) `$ldap`):
int

Повертає стандартизований код помилки, повернутий останньою
командою LDAP. Це число може бути перетворено на текстове повідомлення
про помилку, використовуючи [ldap_err2str()](function.ldap-err2str.md).

### Список параметрів

`ldap`
Примірник [LDAP\Connection](class.ldap-connection.md), що повертається
функцією [ldap_connect()](function.ldap-connect.md).

### Значення, що повертаються

Повертає код помилки LDAP останньої команди для цього посилання.

### Список змін

| Версія | Опис                                                                                                                                                    |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.1.0  | Параметр ldap тепер очікує на екземпляр [LDAP\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |

### Приклади

Якщо ви не знизите достатньо попереджень в `php.ini`, або
префікс ваших LDAP-команд не буде із символом @ для придушення виводу
попереджень, що генеруються помилки будуть також відображатися у вашому
HTML висновку.

**Приклад #1 Генерування та фіксація помилки**

` <?php// Цей приклад містить помилку, ми спіймаємо$ld = ldap_connect("localhost");$bind = ldap_bind($ld);// синтаксічна помилка в | objectclass=*" для того, щоб це працювало.$res =  @ldap_search($ld, "o=Myorg, c=DE", "objectclass");if (!$res) {    echo ". ldap_errno($ld) . "<br />
";   echo "LDAP-Error: " . ldap_error($ld) . "<br />
";   die("Argh!<br />
");}$info = ldap_get_entries($ld, $res);echo $info["count"] . " підходящих записів.<br />
";?> `

### Дивіться також

- [ldap_err2str()](function.ldap-err2str.md) - Перетворити код
помилки LDAP у рядкове повідомлення про помилку
- [ldap_error()](function.ldap-error.md) - Повернути повідомлення про
помилка LDAP останньої команди
