HTTP-автентифікація в PHP

-   [" Відмітні особливості](features.html)
    
-   [Cookies »](features.cookies.html)
    
-   [PHP Manual](index.html)
    
-   [Відмітні особливості](features.html)
    
-   HTTP-автентифікація в PHP
    

# HTTP-автентифікація в PHP

Можливо використовувати функцію [header()](function.header.html) для надсилання повідомлення `"Authentication Required"` браузеру, змусивши його показати віконце для введення логіну та пароля. Як тільки користувач заповнить логін і пароль, посилання, що містить PHP-скрипт буде викликане ще раз [предопределёнными переменными](reserved.variables.html) PHPAUTHUSER, PHPAUTHPW та AUTHTYPE, встановленими в логін, пароль та тип аутентифікації відповідно. Ці зумовлені змінні зберігаються у масиві [SERVER](reserved.variables.server.html). Підтримуються *тільки*: "Basic" та "Digest". Докладніше дивіться функцію [header()](function.header.html)

Приклад фрагмента скрипта, який змушує клієнта авторизуватись для перегляду сторінки:

**Приклад #1 Приклад Basic HTTP-автентифікації**

```php
<?php
if (!isset($_SERVER['PHP_AUTH_USER'])) {
    header('WWW-Authenticate: Basic realm="My Realm"');
    header('HTTP/1.0 401 Unauthorized');
    echo 'Текст, отправляемый в том случае,
    если пользователь нажал кнопку Cancel';
    exit;
} else {
    echo "<p>Hello {$_SERVER['PHP_AUTH_USER']}.</p>";
    echo "<p>Вы ввели пароль {$_SERVER['PHP_AUTH_PW']}.</p>";
}
?>
```

**Приклад #2 Приклад Digest HTTP-автентифікації**

Це приклад реалізації простого скрипту Digest HTTP аутентифікації. За подробицями звертайтесь до [» RFC 2617](http://www.faqs.org/rfcs/rfc2617)

```php
<?php
$realm = 'Запретная зона';

//user => password
$users = array('admin' => 'mypass', 'guest' => 'guest');


if (empty($_SERVER['PHP_AUTH_DIGEST'])) {
    header('HTTP/1.1 401 Unauthorized');
    header('WWW-Authenticate: Digest realm="'.$realm.
           '",qop="auth",nonce="'.uniqid().'",opaque="'.md5($realm).'"');

    die('Текст, отправляемый в том случае, если пользователь нажал кнопку Cancel');
}


// анализируем переменную PHP_AUTH_DIGEST
if (!($data = http_digest_parse($_SERVER['PHP_AUTH_DIGEST'])) ||
    !isset($users[$data['username']]))
    die('Неправильные данные!');


// генерируем корректный ответ
$A1 = md5($data['username'] . ':' . $realm . ':' . $users[$data['username']]);
$A2 = md5($_SERVER['REQUEST_METHOD'].':'.$data['uri']);
$valid_response = md5($A1.':'.$data['nonce'].':'.$data['nc'].':'.$data['cnonce'].':'.$data['qop'].':'.$A2);

if ($data['response'] != $valid_response)
    die('Неправильные данные!');

// все хорошо, логин и пароль верны
echo 'Вы вошли как: ' . $data['username'];


// функция разбора заголовка http auth
function http_digest_parse($txt)
{
    // защита от отсутствующих данных
    $needed_parts = array('nonce'=>1, 'nc'=>1, 'cnonce'=>1, 'qop'=>1, 'username'=>1, 'uri'=>1, 'response'=>1);
    $data = array();
    $keys = implode('|', array_keys($needed_parts));

    preg_match_all('@(' . $keys . ')=(?:([\'"])([^\2]+?)\2|([^\s,]+))@', $txt, $matches, PREG_SET_ORDER);

    foreach ($matches as $m) {
        $data[$m[1]] = $m[3] ? $m[3] : $m[4];
        unset($needed_parts[$m[1]]);
    }

    return $needed_parts ? false : $data;
}
?>
```

> **Зауваження** **Зауваження щодо сумісності**
> 
> Будьте особливо уважні при вказівці заголовків HTTP. Для того, щоб гарантувати максимальну сумісність з найбільшою кількістю різних клієнтів, слово "Basic" має бути написане з великої літери "B", регіон (realm) повинен бути взятий у подвійні (не одинарні!) лапки, і рівно один пробіл повинен передувати коду у заголовку *HTTP/1.0 401*. Параметри автентифікації повинні розділятися комами, як це було показано у прикладі Digest автентифікації вище.

Замість простого відображення на екрані змінних PHPAUTHUSER та PHPAUTHPW, вам, можливо, знадобиться перевірити їхню коректність. Використовуйте для цього запит до бази даних або пошук користувача в файлі dbm.

Ви можете переглянути особливості роботи браузера Internet Explorer. Він дуже вимогливий до параметра заголовків, що передаються. Трюк із зазначенням заголовка *WWW-Authenticate* перед відправкою статусу `HTTP/1.0 401` поки що працює для нього.

> **Зауваження** **Примітка щодо конфігурації**
> 
> PHP використовує вказівку директиви `AuthType` для вказівки того, використовується зовнішня автентифікація чи ні.

Слід зазначити, що все сказане вище не запобігає викрадання паролів до сторінок, що вимагають авторизацію, будь-ким, хто контролює сторінки без авторизації, розташовані на тому ж сервері.

І Netscape Navigator та Internet Explorer очищають кеш аутентифікації поточного вікна для заданого регіону (realm) при отриманні від сервера статусу 401. Це може використовуватися для реалізації примусового виходу користувача та повторного відображення діалогового вікна для введення імені користувача та пароля. Деякі розробники використовують це для обмеження авторизації за часом або надання кнопки "Вихід".

**Приклад #3 Приклад HTTP-автентифікації з введенням нової пари логін/пароль**

```php
<?php
function authenticate() {
    header('WWW-Authenticate: Basic realm="Test Authentication System"');
    header('HTTP/1.0 401 Unauthorized');
    echo "Вы должны ввести корректный логин и пароль для получения доступа к ресурсу \n";
    exit;
}

if (!isset($_SERVER['PHP_AUTH_USER']) ||
    ($_POST['SeenBefore'] == 1 && $_POST['OldAuth'] == $_SERVER['PHP_AUTH_USER'])) {
    authenticate();
} else {
    echo "<p>Добро пожаловать: " . htmlspecialchars($_SERVER['PHP_AUTH_USER']) . "<br />";
    echo "Предыдущий логин: " . htmlspecialchars($_REQUEST['OldAuth']);
    echo "<form action='' method='post'>\n";
    echo "<input type='hidden' name='SeenBefore' value='1' />\n";
    echo "<input type='hidden' name='OldAuth' value=\"" . htmlspecialchars($_SERVER['PHP_AUTH_USER']) . "\" />\n";
    echo "<input type='submit' value='Авторизоваться повторно' />\n";
    echo "</form></p>\n";
}
?>
```

Ця поведінка не регламентується стандартами `HTTP Basic`аутентифікації, отже, ви не повинні залежати від цього. Тестування браузера `Lynx` показало, що `Lynx` не очищає кеш авторизації при отриманні від сервера статусу 401, і, натиснувши послідовно "Back", а потім "Forward" можна відкрити таку сторінку, за умови, що потрібні атрибути авторизації не змінилися. Однак користувач може натиснути клавішу `'_'` для очищення кешу аутентифікації.

Для того, щоб досягти коректної роботи HTTP-аутентифікації в IIS сервері з CGI версією PHP, ви повинні відредагувати конфігураційне налаштування IIS під назвою "`Directory Security`". Клацніть на написи"`Edit`" та встановіть опцію "`Anonymous Access`"Всі інші поля повинні залишитися невідзначеними.

> **Зауваження** **Примітка щодо IIS:**  
> Для того, щоб HTTP-автентифікація коректно працювала в IIS, у конфігурації PHP-опція [cgi.rfc2616headers](ini.core.html#ini.cgi.rfc2616-headers) має бути встановлена ​​значенням `0` (значення за замовчуванням).