---
navigation:
  - function.radius-acct-open.md: « radius\_acct\_open
  - function.radius-auth-open.md: radius\_auth\_open »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_add\_server
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_add\_server

(PECL radius >= 1.1.0)

radius\_add\_server — Додає сервер

### Опис

```methodsynopsis
radius_add_server(    resource $radius_handle,    string $hostname,    int $port,    string $secret,    int $timeout,    int $max_tries): bool
```

**radius\_add\_server()** може викликатися кілька разів і може використовуватися разом з [radius\_config()](function.radius-config.md). Можна вказати не більше 10 серверів. Коли задано кілька серверів, вони перевіряються циклічно, доки не буде отримано дійсну відповідь або доки не буде досягнуто межі `max_tries` для кожного сервера.

### Список параметрів

`radius_handle`

`hostname`

Параметр`hostname` вказує хост сервера у вигляді повного доменне ім'я або IP-адреси, розділеної крапками, у текстовому вигляді.

`port`

`port` вказує UDP-порт для зв'язку на сервері. Якщо порт задан як 0, бібліотека шукає сервіс `radius/udp`или`radacct/udp` базі даних мережевих сервісів, і використовує знайдений там порт. Якщо запис не знайдено, бібліотека використовує стандартні порти Radius, 1812 для автентифікації та 1813 для обліку.

`secret`

Загальний секрет для хоста сервера передається у параметрі `secret`. Протокол Radius ігнорує все, окрім перших 128 байтів загального секрету.

`timeout`

Час очікування відповідей від сервера передається у параметрі `timeout` за секунди.

`max_tries`

Максимальна кількість повторних запитів, які потрібно зробити перед відмовою, передається у `max_tries`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**radius\_add\_server()\*\*\*\*

```php
<?php
if (!radius_add_server($res, 'radius.example.com', 1812, 'testing123', 3, 3)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br>";
    exit;
}
?>
```

### Дивіться також

-   [radius\_config()](function.radius-config.md) \- Примушує бібліотеку читати цей файл конфігурації
