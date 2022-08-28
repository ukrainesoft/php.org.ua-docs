Закриває екземпляр finfo

-   [« finfo\_buffer](function.finfo-buffer.html)
    
-   [finfo\_file »](function.finfo-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции модуля Fileinfo](ref.fileinfo.html)
    
-   Закриває екземпляр finfo
    

# finfoclose

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfoclose — Закриває екземпляр finfo

### Опис

```methodsynopsis
finfo_close(finfo $finfo): bool
```

Функція закриває екземпляр, який було відкрито функцією [finfo\_open()](function.finfo-open.html)

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.html), що повертається функцією [finfo\_open()](function.finfo-open.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                             |
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `finfo` тепер чекає екземпляр [finfo](class.finfo.html); раніше очікувався ресурс ([resource](language.types.resource.html) |