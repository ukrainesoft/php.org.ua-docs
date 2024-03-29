---
navigation:
  - reserved.variables.globals.md: « $GLOBALS
  - reserved.variables.get.md: $\_GET »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $\_SERVER
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $\_SERVER

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_SERVER — Інформація про сервер та середовище виконання

### Опис

Змінна $\_SERVER - це масив (array), що містить таку інформацію, як заголовки, шляхи та розташування скриптів. Записи в цьому масиві створюються веб-сервером, тому немає гарантії, що кожен веб-сервер надаватиме будь-яку з цих змінних; сервери можуть опускати деякі з них або надавати інші, не вказані тут. Проте більшість із цих змінних враховано у специфікації [» CGI/1.1](http://www.faqs.org/rfcs/rfc3875) і, швидше за все, буде визначено.

> **Зауваження**: При запуске PHP в[командному рядку](features.commandline.md) більшість із цих записів будуть недоступні або не матимуть жодного значення.

На додаток до наведених нижче елементів, PHP буде створювати додаткові елементи зі значеннями із заголовків запитів. У елементів буде ім'я `HTTP_`, За яким слідує ім'я заголовка, написане з великої літери та з підкресленням замість дефісу. Наприклад, заголовок `Accept-Language`будет доступен как`$_SERVER['HTTP_ACCEPT_LANGUAGE']`

### Індекси

'PHP\_SELF'

Ім'я файлу скрипта, який зараз виконується, щодо кореня документів. Наприклад, $\_SERVER\['PHP\_SELF'\]в скрипте по адресу[http://example.com/foo/bar.php](http://example.com/foo/bar.php)будет /foo/bar.php. Константа[\_\_FILE\_\_](language.constants.predefined.md) містить повний шлях та ім'я файлу поточного (тобто підключеного) файлу. Якщо PHP запущено у командному рядку, ця змінна містить ім'я скрипта.

'[argv](reserved.variables.argv.md)'

Масив аргументів переданих скрипту. Коли скрипт запущено у командному рядку, це дає C-подібний доступ до параметрів командного рядка. Коли викликається через метод GET, цей масив міститиме рядок запиту.

'[argc](reserved.variables.argc.md)'

Містить кількість параметрів, переданих скрипту (якщо запуск здійснено в командному рядку).

'GATEWAY\_INTERFACE'

Містить версію специфікації CGI, що використовується сервером; наприклад `'CGI/1.1'` .. .

'SERVER\_ADDR'

IP-адреса сервера, на якому виконується поточний скрипт.

'SERVER\_NAME'

Ім'я хоста, де виконується поточний скрипт. Якщо скрипт виконується на віртуальному хості, тут буде міститись ім'я, визначене для цього віртуального хоста.

> **Зауваження**: В Apache 2 необходимо установить`UseCanonicalName = On`и`ServerName`. Інакше це значення відобразить ім'я хоста, надане клієнтом, яке можна підробити. Небезпечно покладатися на це значення в контексті, що потребує безпеки.

'SERVER\_SOFTWARE'

Рядок ідентифікації сервера, вказаний у заголовках, коли відбувається відповідь на запит.

'SERVER\_PROTOCOL'

Ім'я та версія інформаційного протоколу, через який було запрошено сторінку; наприклад `'HTTP/1.0'`

'REQUEST\_METHOD'

Який метод використали для запиту сторінки; наприклад `'GET'` `'HEAD'` `'POST'` `'PUT'`

> **Зауваження** :
> 
> PHP-скрипт завершується після надсилання заголовків (тобто після того, як здійснюється будь-який висновок без буферизації виводу), якщо метод запиту був `HEAD`

'REQUEST\_TIME'

Тимчасова позначка початку запиту.

'REQUEST\_TIME\_FLOAT'

Тимчасова позначка початку запиту з точністю до мікросекунд.

'QUERY\_STRING'

Рядок запиту, якщо є, через яку було відкрито сторінку.

'DOCUMENT\_ROOT'

Директорія кореня документів, в якій виконується поточний скрипт, точно та, що вказана в конфігураційному файлі сервера.

'HTTPS'

Приймає непусте значення, якщо запит було здійснено через протокол HTTPS.

'REMOTE\_ADDR'

IP-адреса, з якої користувач переглядає поточну сторінку.

'REMOTE\_HOST'

Віддалений хост, з якого користувач переглядає поточну сторінку. Зворотний пошук DNS базується на значенні змінної REMOTE\_ADDR.

> **Зауваження**: Сервер повинен бути налаштований, щоб створювати цю змінну. Наприклад, в Apache потрібна присутність директиви `HostnameLookups On` у файлі httpd.conf, щоб ця змінна створювалася. Дивіться також [gethostbyaddr()](function.gethostbyaddr.md)

'REMOTE\_PORT'

Порт на дистанційній машині, який використовується для зв'язку з сервером.

'REMOTE\_USER'

Автентифікований користувач.

'REDIRECT\_REMOTE\_USER'

Аутентифікований користувач, якщо запит перенаправлено зсередини.

'SCRIPT\_FILENAME'

Абсолютний шлях до скрипту.

> **Зауваження** :
> 
> Якщо скрипт запускається в командному рядку (CLI), використовуючи відносний шлях, такий як file.php або ../file.php, змінна $\_SERVER\['SCRIPT\_FILENAME'\] міститиме відносний шлях, вказаний користувачем.

'SERVER\_ADMIN'

Ця змінна набуває свого значення (для Apache) з директиви конфігураційного файлу сервера. Якщо скрипт запущено на віртуальному хості, це буде значення, визначене для цього віртуального хоста.

'SERVER\_PORT'

Порт на комп'ютері сервера, який використовує сервер для з'єднання. Для установок за замовчуванням, значення буде `'80'`; використовуючи SSL, наприклад, це значення буде таким, яке налаштовано для з'єднань безпечного HTTP.

> **Зауваження**: Щоб отримати фізичний (реальний) порт в Apache 2, необхідно встановити `UseCanonicalName = On`и`UseCanonicalPhysicalPort = On`, інакше це значення може бути підмінено і не повернути реальне значення фізичного порту. Покладатися на це значення є небезпечним у контексті додатків, що потребують посиленої безпеки.

'SERVER\_SIGNATURE'

Рядок, що містить версію сервера та ім'я віртуального хоста, які додаються до сторінок, що генеруються сервером, якщо включено.

'PATH\_TRANSLATED'

Шлях файлової системи (не document root) до поточного скрипту після того, як сервер виконав відображення virtual-to-real.

> **Зауваження**: Користувачі Apache 2 можуть використовувати директиву. `AcceptPathInfo = On` у конфігураційному файлі httpd.conf для завдання змінної PATH\_INFO.

'SCRIPT\_NAME'

Містить шлях до поточного виконуваного скрипту. Це корисно для сторінок, які повинні вказувати на себе. Константа [\_\_FILE\_\_](language.constants.predefined.md) містить повний шлях та ім'я поточного (тобто включеного) файлу.

'REQUEST\_URI'

URI, який було надано для доступу до цієї сторінки. Наприклад, '`/index.md`'.

'PHP\_AUTH\_DIGEST'

При виконанні аутентифікації HTTP Digest цій змінній надається заголовок 'Authorization', надісланий клієнтом (який потім слід використовувати для проведення відповідної перевірки).

'PHP\_AUTH\_USER'

При виконанні HTTP-автентифікації цієї змінної надається ім'я користувача, надане користувачем.

'PHP\_AUTH\_PW'

При виконанні HTTP-автентифікації цієї змінної надається пароль, наданий користувачем.

'AUTH\_TYPE'

При виконанні HTTP-автентифікації цій змінній надається тип автентифікації, який використовується.

'PATH\_INFO'

Містить будь-який наданий користувачем шлях, що міститься після імені скрипта, але до рядка запиту, якщо він є. Наприклад, якщо поточний скрипт запрошений на URL [http://www.example.com/php/path\\\_info.php/some/stuff?foo=bar](http://www.example.com/php/path%5C_info.php/some/stuff?foo=bar), то змінна $\_SERVER\['PATH\_INFO'\] міститиме `/some/stuff`

'ORIG\_PATH\_INFO'

Вихідне значення змінної 'PATH\_INFO' перед обробкою PHP.

### Приклади

**Приклад #1 Приклад використання $\_SERVER**

```php
<?php
echo $_SERVER['SERVER_NAME'];
?>
```

Висновок наведеного прикладу буде схожим на:

```
www.example.com
```

### Примітки

> **Зауваження** :
> 
> Це «суперглобальна» чи автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [Фільтрування даних](book.filter.md)
