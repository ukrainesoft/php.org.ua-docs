---
navigation:
  - mysql-xdevapi.requirements.md: « Вимоги
  - mysql-xdevapi.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - mysql-xdevapi.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Цей модуль [» PECL](https://pecl.php.net/)не поставляется вместе с PHP.

Приклад процедури встановлення на Ubuntu 18.04 з PHP 7.2:

```
// Зависимости
$ apt install build-essential libprotobuf-dev libboost-dev openssl protobuf-compiler liblz4-tool zstd

// PHP с нужными модулями; php7.2-dev, необходимым для компиляции
$ apt install php7.2-cli php7.2-dev php7.2-mysql php7.2-pdo php7.2-xml

// Компиляция модуля
$ pecl install mysql_xdevapi
```

Команда`pecl install` не включає модулі PHP (за замовчуванням), включення модулів PHP може бути зроблено кількома способами. Інший приклад PHP 7.2 в Ubuntu 18.04:

```
// Создание собственного ini файла
$ echo "extension=mysql_xdevapi.so" > /etc/php/7.2/mods-available/mysql_xdevapi.ini

// Использование команды 'phpenmod' (примечание: это применимо для Debian/Ubuntu)
$ phpenmod -v 7.2 -s ALL mysql_xdevapi

// Альтернативой 'phpenmod' является создание символической ссылки
// $ ln -s /etc/php/7.2/mods-available/mysql_xdevapi.ini /etc/php/7.2/cli/conf.d/20-mysql_xdevapi.ini

// Давайте посмотрим, какие модули MySQL сейчас включены
$ php -m |grep mysql

mysql_xdevapi
mysqli
mysqlnd
pdo_mysql
```

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Встановлення PECL модулів](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/mysql\_xdevapi](https://pecl.php.net/package/mysql_xdevapi)
