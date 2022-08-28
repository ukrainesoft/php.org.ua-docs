Закрити дескриптор директорії

-   [« streamWrapper::\_\_destruct](streamwrapper.destruct.html)
    
-   [streamWrapper::dir\_opendir »](streamwrapper.dir-opendir.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Закрити дескриптор директорії
    

# streamWrapper::dirclosedir

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dirclosedir — Закрити дескриптор директорії

### Опис

```methodsynopsis
public streamWrapper::dir_closedir(): bool
```

Цей метод викликається у процесі виконання [closedir()](function.closedir.html)

Усі ресурси, заблоковані або виділені під час відкриття та використання потоку директорії, необхідно звільнити.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [closedir()](function.closedir.html) - Закриває дескриптор каталогу
-   [streamWrapper::dir\_opendir()](streamwrapper.dir-opendir.html) - відкрити дескриптор директорії