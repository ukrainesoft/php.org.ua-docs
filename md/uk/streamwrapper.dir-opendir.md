Відкрити дескриптор директорії

-   [« streamWrapper::dirclosedir](streamwrapper.dir-closedir.html)
    
-   [streamWrapper::dirreaddir »](streamwrapper.dir-readdir.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Відкрити дескриптор директорії
    

# streamWrapper::diropendir

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::diropendir — Відкрити дескриптор директорії

### Опис

```methodsynopsis
public streamWrapper::dir_opendir(string $path, int $options): bool
```

Цей метод викликається у процесі виконання [opendir()](function.opendir.html)

### Список параметрів

`path`

Задає URL-адресу, яка була передана в [opendir()](function.opendir.html)

> **Зауваження**
> 
> URL можна розділити на частини за допомогою [parseurl()](function.parse-url.html)

`options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [opendir()](function.opendir.html) - Відкриває дескриптор каталогу
-   [streamWrapper::dirclosedir()](streamwrapper.dir-closedir.html) - Закрити дескриптор директорії
-   [parseurl()](function.parse-url.html) - Розбирає URL та повертає його компоненти