- [« Встановлення Nginx 1.4.x на систему Unix](install.unix.nginx.md)
- [Веб-сервер LiteSpeed/OpenLiteSpeed на системах Unix »](install.unix.litespeed.md)

- [PHP Manual](index.md)
- [Установка для Unix-системи](install.unix.md)
- Установка PHP на Lighttpd 1.4 на Unix-системах

## Встановлення PHP на Lighttpd 1.4 на Unix-системах

Цей розділ містить інформацію про встановлення PHP на Unix-системи з
сервером Lighttpd 1.4.

Прочитайте, будь ласка, інструкції зі встановлення Lighttpd в
[» документації по Lighttpd](http://trac.lighttpd.net/trac/) перед
установкою PHP.

FastCGI - інтерфейс для зв'язку PHP і Lighttpd. FastCGI
доступний за замовчуванням у php-cgi.

### Управління процесами php через Lighttpd

Для налаштування Lighttpd на з'єднання з PHP та породження процесів
FastCGI необхідно відредагувати конфігураційний файл
`lighttpd.conf`. Переважно підключатися до процесів FastCGI
використовуючи Unix-сокети.

**Приклад #1 Приклад частини файлу lighttpd.conf**

server.modules += ( "mod_fastcgi")

fastcgi.server = (".php" =>
((
"socket" => "/tmp/php.socket",
"bin-path" => "/usr/local/bin/php-cgi",
"bin-environment" => (
"PHP_FCGI_CHILDREN" => "16",
"PHP_FCGI_MAX_REQUESTS" => "10000"
),
"min-procs" => 1,
"max-procs" => 1,
"idle-timeout" => 20
))
)

Директива `bin-path` дозволяє lighttpd динамічно запускати процеси
FastCGI. Lighttpd буде динамічно створювати дочірні процеси php,
відповідно до змінної оточення `PHP_FCGI_CHILDREN`. Директива
`bin-environment` задає установки для дочірніх процесів.
`PHP_FCGI_MAX_REQUESTS` визначає поріг, при досягненні якого PHP
завершить дочірній процес Директив `min-procs` та `max-procs` зазвичай
варто уникати. PHP керує лише своїми дочірніми процесами, та
інструменти кешування в байт-код (наприклад, APC) будуть використовуватися
лише у цих дочірніх процесах. Якщо значення `min-procs` встановлено
більше `1`, загальна кількість процесів, що обробляють запити, буде
одно `PHP_FCGI_CHILDREN` \ * min-procs.

### Управління процесами за допомогою spawn-fcgi

Lighttpd надає програму spawn-fcgi для полегшення управління
дочірніми процесами FastCGI.

### Управління процесами за допомогою php-cgi

Керувати процесами можна і без spawn-fcgi, але це вимагатиме деяких
доробок. Змінна оточення `PHP_FCGI_CHILDREN` вказує кількість
дочірніх процесів, які запускаються PHP для обробки вхідних запитів.
Змінна `PHP_FCGI_MAX_REQUESTS` відповідає за кількість запитів,
які обробить один процес. Нижче наведений простий bash-скрипт,
що полегшує створення дочірніх процесів.

**Приклад #2 Створення FastCGI-обробників**

#!/bin/sh

# Розташування бінарного файлу php-cgi
PHP=/usr/local/bin/php-cgi

# Розташування PID-файлу
PHP_PID=/tmp/php.pid

# Прив'язка до адреси
#FCGI_BIND_ADDRESS=10.0.1.1:10000
# Прив'язка до сокету
FCGI_BIND_ADDRESS=/tmp/php.sock

PHP_FCGI_CHILDREN=16
PHP_FCGI_MAX_REQUESTS=10000

env -i PHP_FCGI_CHILDREN=$PHP_FCGI_CHILDREN \
PHP_FCGI_MAX_REQUESTS=$PHP_FCGI_MAX_REQUESTS \
$PHP -b $FCGI_BIND_ADDRESS &

echo $! > "$PHP_PID"

### Підключення до віддалених процесів FCGI

Обробники FastCGI можуть перебувати на кількох окремих машинах
масштабування навантаження.

**Приклад #3 Підключення до віддалених процесів fastcgi**

fastcgi.server = (".php" =>
(( "host" => "10.0.0.2", "port" => 1030 ),
( "host" => "10.0.0.3", "port" => 1030))
)
