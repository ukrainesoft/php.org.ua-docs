Вступ

-   [« Inotify](book.inotify.html)
    
-   [Установка и настройка »](inotify.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Inotify](book.inotify.html)
    
-   Вступ
    

# Вступ

Модуль inotify надає функції [inotifyinit()](function.inotify-init.html) [inotifyaddwatch()](function.inotify-add-watch.html) і [inotifyрмwatch()](function.inotify-rm-watch.html)

У той час як функція мови C [inotifyinit()](function.inotify-init.html) повертає дескриптор файлу, функція [inotifyinit()](function.inotify-init.html) PHP повертає потоковий ресурс, який можна використовувати в стандартних функціях, наприклад, [streamselect()](function.stream-select.html) [streamsetblocking()](function.stream-set-blocking.html) і [fclose()](function.fclose.html). Функція [inotifyread()](function.inotify-read.html) замінює спосіб читання подій inotify в C.