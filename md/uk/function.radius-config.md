---
navigation:
  - function.radius-close.md: « radiusclose
  - function.radius-create-request.md: radiuscreaterequest »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusconfig
---
# radiusconfig

(PECL radius >= 1.1.0)

radiusconfig — Примушує бібліотеку читати файл конфігурації

### Опис

```methodsynopsis
radius_config(resource $radius_handle, string $file): bool
```

Перед виконанням будь-яких запитів Radius бібліотека повинна бути поінформована про сервери, з якими вона може зв'язатися. Найпростіший спосіб налаштувати бібліотеку - викликати **radiusconfig()**. . **radiusconfig()** змушує бібліотеку читати файл конфігурації, формат якого описаний у [» radius.conf](http://www.freebsd.org/cgi/man.cgi?query=radius.conf)

### Список параметрів

`radius_handle`

`file`

Шлях до файлу конфігурації передається як аргумент файлу в **radiusconfig()**. Бібліотека також може бути налаштована програмно за допомогою дзвінка [radiusaddserver()](function.radius-add-server.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [radiusaddserver()](function.radius-add-server.md) - Додає сервер
