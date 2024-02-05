---
navigation:
  - function.php-ini-scanned-files.md: « php\_ini\_scanned\_files
  - function.php-uname.md: php\_uname »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: php\_sapi\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_sapi\_name

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

php\_sapi\_name — Повертає тип інтерфейсу між веб-сервером та PHP

### Опис

```methodsynopsis
php_sapi_name(): string|false
```

Повертає рядок у нижньому регістрі, який містить опис типу інтерфейсу (Server API, SAPI), який використовує PHP. Наприклад, у CLI PHP цей рядок буде "cli", тоді як з Apache може бути кілька різних значень залежно від конкретного SAPI. Можливі значення наведено нижче.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тип інтерфейсу у вигляді рядка в нижньому регістрі або \*\*`false`\*\*в случае возникновения ошибки.

Можливі значення, що повертаються (список може бути неповним): `apache` `apache2handler` `cgi`(до PHP 5.3),`cgi-fcgi` `cli` `cli-server` `embed` `fpm-fcgi` `litespeed` `phpdbg`

### Приклади

**Приклад #1 Приклад використання** php\_sapi\_name()\*\*\*\*

У цьому прикладі перевіряється підрядок `cgi`, так як це також може бути `cgi-fcgi`

```php
<?php
$sapi_type = php_sapi_name();
if (substr($sapi_type, 0, 3) == 'cgi') {
    echo "Вы используете CGI PHP\n";
} else {
    echo "Вы используете не CGI PHP\n";
}
?>
```

### Примітки

> **Зауваження** **Альтернативний варіант**
> 
> Константа PHP\*\*`PHP_SAPI`\*\* зберігає те саме значення, що і **php\_sapi\_name()**

**Підказка**

# Важливий аспект

Ім'я SAPI може визначитися неточно, тому що, наприклад, у випадку з `apache` інтерфейс може бути визначений як `apache2handler`

### Дивіться також

-   [PHP\_SAPI](reserved.constants.md#reserved.constants.core)
