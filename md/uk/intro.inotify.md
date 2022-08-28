Вступ

-   [« Inotify](book.inotify.html)
    
-   [Установка и настройка »](inotify.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Inotify](book.inotify.html)
    
-   Вступ
    

# Вступ

Модуль inotify надає функції [inotify\_init()](function.inotify-init.html) [inotify\_add\_watch()](function.inotify-add-watch.html) і [inotify\_rm\_watch()](function.inotify-rm-watch.html)

У той час як функція мови C [inotify\_init()](function.inotify-init.html) повертає дескриптор файлу, функція [inotify\_init()](function.inotify-init.html) PHP повертає потоковий ресурс, який можна використовувати в стандартних функціях, наприклад, [stream\_select()](function.stream-select.html) [stream\_set\_blocking()](function.stream-set-blocking.html) і [fclose()](function.fclose.html). Функція [inotify\_read()](function.inotify-read.html) замінює спосіб читання подій inotify в C.