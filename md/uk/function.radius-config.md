---
navigation:
  - function.radius-close.md: « radius\_close
  - function.radius-create-request.md: radius\_create\_request »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_config
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_config

(PECL radius >= 1.1.0)

radius\_config — Примушує бібліотеку читати файл конфігурації

### Опис

```methodsynopsis
radius_config(resource $radius_handle, string $file): bool
```

Перед виконанням будь-яких запитів Radius бібліотека повинна бути поінформована про сервери, з якими вона може зв'язатися. Найпростіший спосіб налаштувати бібліотеку - викликати **radius\_config()**. . **radius\_config()** змушує бібліотеку читати файл конфігурації, формат якого описаний у [» radius.conf](http://www.freebsd.org/cgi/man.cgi?query=radius.conf)

### Список параметрів

`radius_handle`

`file`

Шлях до файлу конфігурації передається як аргумент файлу в **radius\_config()**. Бібліотека також може бути налаштована програмно за допомогою дзвінка [radius\_add\_server()](function.radius-add-server.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [radius\_add\_server()](function.radius-add-server.md) \- Додає сервер
