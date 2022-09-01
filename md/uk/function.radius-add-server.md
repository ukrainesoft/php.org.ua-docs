---
navigation:
  - function.radius-acct-open.html: « radiusacctopen
  - function.radius-auth-open.html: radiusauthopen »
  - index.html: PHP Manual
  - ref.radius.html: Функции Radius
title: radiusaddserver
---
# radiusaddserver

(PECL radius >= 1.1.0)

radiusaddserver — Додає сервер

### Опис

```methodsynopsis
radius_add_server(    resource $radius_handle,    string $hostname,    int $port,    string $secret,    int $timeout,    int $max_tries): bool
```

**radiusaddserver()** може викликатися кілька разів і може використовуватися разом з [radiusconfig()](function.radius-config.html). Можна вказати не більше 10 серверів. Коли задано кілька серверів, вони перевіряються циклічно, доки не буде отримано дійсну відповідь або доки не буде досягнуто межі `max_tries` для кожного сервера.

### Список параметрів

`radius_handle`

`hostname`

Параметр `hostname` вказує хост сервера у вигляді повного доменного імені або IP-адреси, розділеної крапками, у текстовому вигляді.

`port`

`port` вказує UDP-порт для зв'язку на сервері. Якщо порт задан як 0, бібліотека шукає сервіс `radius/udp` або `radacct/udp` базі даних мережевих сервісів, і використовує знайдений там порт. Якщо запис не знайдено, бібліотека використовує стандартні порти Radius, 1812 для автентифікації та 1813 для обліку.

`secret`

Загальний секрет для хоста сервера передається у параметрі `secret`. Протокол Radius ігнорує все, окрім перших 128 байтів загального секрету.

`timeout`

Час очікування відповідей від сервера передається у параметрі `timeout` за секунди.

`max_tries`

Максимальна кількість повторних запитів, які потрібно зробити перед відмовою, передається у `max_tries`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radiusaddserver()****

```php
<?php
if (!radius_add_server($res, 'radius.example.com', 1812, 'testing123', 3, 3)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br>";
    exit;
}
?>
```

### Дивіться також

-   [radiusconfig()](function.radius-config.html) - Примушує бібліотеку читати цей файл конфігурації
