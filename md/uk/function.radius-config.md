Примушує бібліотеку читати цей файл конфігурації

-   [« radius\_close](function.radius-close.html)
    
-   [radius\_create\_request »](function.radius-create-request.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Примушує бібліотеку читати цей файл конфігурації
    

# radiusconfig

(PECL radius >= 1.1.0)

radiusconfig — Примушує бібліотеку читати файл конфігурації

### Опис

```methodsynopsis
radius_config(resource $radius_handle, string $file): bool
```

Перед виконанням будь-яких запитів Radius бібліотека повинна бути поінформована про сервери, з якими вона може зв'язатися. Найпростіший спосіб налаштувати бібліотеку - викликати **radiusconfig()**. . **radiusconfig()** змушує бібліотеку читати файл конфігурації, формат якого описаний у [» radius.conf](http://www.freebsd.org/cgi/man.cgi?query=radius.conf)

### Список параметрів

`radius_handle`

`file`

Шлях до файлу конфігурації передається як аргумент файлу в **radiusconfig()**. Бібліотека також може бути налаштована програмно за допомогою дзвінка [radius\_add\_server()](function.radius-add-server.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [radius\_add\_server()](function.radius-add-server.html) - Додає сервер