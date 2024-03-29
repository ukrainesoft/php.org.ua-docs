---
navigation:
  - install.unix.nginx.md: Встановлення Nginx 1.4.x на систему Unix
  - install.unix.litespeed.md: Веб-сервер LiteSpeed/OpenLiteSpeed ​​на системах Unix »
  - index.md: PHP Manual
  - install.unix.md: Встановлення на Unix-системи
title: Встановлення PHP на Lighttpd 1.4 на Unix-системах
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Встановлення PHP на Lighttpd 1.4 на Unix-системах

Цей розділ містить інформацію про встановлення PHP на Unix-системи з сервером Lighttpd 1.4.

Прочитайте, пожалуйста, инструкции по установке Lighttpd в[» документації по Lighttpd](http://trac.lighttpd.net/trac/)перед установкой PHP.

FastCGI - інтерфейс для зв'язку PHP і Lighttpd. FastCGI доступний за замовчуванням у php-cgi.

### Управління процесами php через Lighttpd

Для налаштування Lighttpd на з'єднання з PHP та створення процесів FastCGI необхідно відредагувати конфігураційний файл lighttpd.conf. Переважно підключатися до процесів FastCGI, використовуючи Unix-сокети.

**Приклад #1 Приклад частини файлу lighttpd.conf**

```
server.modules += ( "mod_fastcgi" )

fastcgi.server = ( ".php" =>
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
```

Директива bin-path дозволяє lighttpd динамічно запускати процеси FastCGI. Lighttpd буде динамічно створювати дочірні процеси php, відповідно до змінного оточення PHP\_FCGI\_CHILDREN. Директива`bin-environment` задає параметри для дочірніх процесів. PHP\_FCGI\_MAX\_REQUESTS визначає поріг, при досягненні якого PHP завершить дочірній процес. Директив `min-procs`и`max-procs` зазвичай варто уникати. PHP керує лише своїми дочірніми процесами, і інструменти кешування в байт-код (наприклад, APC) будуть використовуватися лише у цих дочірніх процесах. Якщо значення `min-procs`установлено больше , загальна кількість процесів, що обробляють запити, дорівнюватиме PHP\_FCGI\_CHILDREN\*min-procs.

### Управління процесами за допомогою spawn-fcgi

Lighttpd надає програму spawn-fcgi для полегшення керування дочірніми процесами FastCGI.

### Управління процесами за допомогою php-cgi

Керувати процесами можна і без spawn-fcgi, але це вимагатиме деяких доробок. Змінне оточення PHP\_FCGI\_CHILDREN вказує кількість дочірніх процесів, що запускаються PHP для обробки запитів. Змінна PHP\_FCGI\_MAX\_REQUESTS відповідає за кількість запитів, які опрацьовує один процес. Нижче наведено простий bash-скрипт, що полегшує створення дочірніх процесів.

**Приклад #2 Створення FastCGI-обробників**

```
#!/bin/sh

# Местоположение бинарного файла php-cgi
PHP=/usr/local/bin/php-cgi

# Местоположение PID-файла
PHP_PID=/tmp/php.pid

# Привязка к адресу
#FCGI_BIND_ADDRESS=10.0.1.1:10000
# Привязка к сокету
FCGI_BIND_ADDRESS=/tmp/php.sock

PHP_FCGI_CHILDREN=16
PHP_FCGI_MAX_REQUESTS=10000

env -i PHP_FCGI_CHILDREN=$PHP_FCGI_CHILDREN \
       PHP_FCGI_MAX_REQUESTS=$PHP_FCGI_MAX_REQUESTS \
       $PHP -b $FCGI_BIND_ADDRESS &

echo $! > "$PHP_PID"
```

### Підключення до віддалених процесів FCGI

Обробники FastCGI можуть бути на декількох окремих машинах для масштабування навантаження.

**Приклад #3 Підключення до віддалених процесів fastcgi**

```
fastcgi.server = ( ".php" =>
   (( "host" => "10.0.0.2", "port" => 1030 ),
    ( "host" => "10.0.0.3", "port" => 1030 ))
)
```
