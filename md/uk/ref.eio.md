Eio Функції

-   [« Приклади](eio.examples.html)
    
-   [eiobusy »](function.eio-busy.html)
    
-   [PHP Manual](index.html)
    
-   [Eio](book.eio.html)
    
-   Eio Функції
    

# Eio Функції

## Зміст

-   [eiobusy](function.eio-busy.html) — Штучно збільшує навантаження. Може бути корисним при тестуванні, вивченні продуктивності
-   [eiocancel](function.eio-cancel.html) — Скасує запит
-   [eiochmod](function.eio-chmod.html) — Змінює права доступу до файлу/директорії
-   [eiochown](function.eio-chown.html) — Змінює права доступу до файлу/директорії
-   [eioclose](function.eio-close.html) - Закрити файл
-   [eiocustom](function.eio-custom.html) — Виконує запит користувача як будь-який інший eio виклик
-   [eiodup2](function.eio-dup2.html) - Створює дублікат дескриптора файлу
-   [eioeventloop](function.eio-event-loop.html) — Взаємодіє з libeio доти, доки всі запити не будуть виконані
-   [eiofallocate](function.eio-fallocate.html) — Дозволяє безпосередньо керувати розміром дискового простору, що використовується для файлу.
-   [eiofchmod](function.eio-fchmod.html) — Змінює права доступу до файлу
-   [eiofchown](function.eio-fchown.html) - Змінює власника файлу
-   [eiofdatasync](function.eio-fdatasync.html) — Синхронізує поточний стан файлу із фізичним пристроєм
-   [eiofstat](function.eio-fstat.html) — Повертає статус файлу
-   [eiofstatvfs](function.eio-fstatvfs.html) — Повертає статистику файлової системи
-   [eiofsync](function.eio-fsync.html) — Синхронізує поточний стан файлу із фізичним пристроєм
-   [eioftruncate](function.eio-ftruncate.html) - Урізує розмір файлу
-   [eiofutime](function.eio-futime.html) — Змінює дату та час останньої модифікації та доступу до файлу
-   [eiogeteventstream](function.eio-get-event-stream.html) — Повертає потік, що відображає змінну, що використовується при взаємодії з libeio
-   [eiogetlasterror](function.eio-get-last-error.html) — Повертає останню помилку, пов'язану із вказівником на ресурс
-   [eiogrpadd](function.eio-grp-add.html) — Додає запит до групи запитів
-   [eiogrpcancel](function.eio-grp-cancel.html) — Скасує групу запитів
-   [eiogrplimit](function.eio-grp-limit.html) — Встановлює граничну кількість запитів у групі
-   [eiogrp](function.eio-grp.html) — Створює групу запитів
-   [eioinit](function.eio-init.html) - (Не-) ініціалізує Eio
-   [eiolink](function.eio-link.html) - Створює жорстке посилання на файл
-   [eiolstat](function.eio-lstat.html) — Повертає статус файлу
-   [eiomkdir](function.eio-mkdir.html) - Створення директорії
-   [eiomknod](function.eio-mknod.html) — Створює спеціальний чи звичайний файл
-   [eionop](function.eio-nop.html) - Прохід по циклу запиту, не здійснюючи жодних операцій
-   [eionpending](function.eio-npending.html) — Повертає кількість завершених, але необроблених процесів
-   [eionready](function.eio-nready.html) — Повертає кількість ще не опрацьованих запитів
-   [eionreqs](function.eio-nreqs.html) — Повертає кількість запитів, які потрібно виконати
-   [eionthreads](function.eio-nthreads.html) — Повертає кількість потоків, що використовуються в даний момент.
-   [eioopen](function.eio-open.html) - Відкриває файл
-   [eiopoll](function.eio-poll.html) — Може бути викликана коли є запити, які очікують на виконання
-   [eioread](function.eio-read.html) — Читає дані з файлу, починаючи із заданого усунення
-   [eioreadahead](function.eio-readahead.html) — Поміщає дані з файлу до кешу сторінки
-   [eioreaddir](function.eio-readdir.html) — Читає вміст директорії
-   [eioreadlink](function.eio-readlink.html) — Читає значення символічного посилання
-   [eiorealpath](function.eio-realpath.html) — Отримує абсолютний приведений до канонічного виду шлях
-   [eiorename](function.eio-rename.html) — Змінює ім'я або переміщує файл
-   [eiormdir](function.eio-rmdir.html) - Видаляє директорію
-   [eioseek](function.eio-seek.html) — Переміщує файловий покажчик файлу fd на число байт offset відповідно до директиви whence
-   [eiosendfile](function.eio-sendfile.html) — Переміщує дані між файлами
-   [eiosetmaxidle](function.eio-set-max-idle.html) — Встановлює максимальну кількість потоків, що очікують.
-   [eiosetmaxparallel](function.eio-set-max-parallel.html) — Встановлює максимальну кількість паралельних потоків
-   [eiosetmaxpollreqs](function.eio-set-max-poll-reqs.html) — Встановлює максимальну кількість запитів, що обробляються.
-   [eiosetmaxpolltime](function.eio-set-max-poll-time.html) - Встановлює максимальний час виконання
-   [eiosetminparallel](function.eio-set-min-parallel.html) — Встановлює мінімальну кількість паралельних потоків
-   [eiostat](function.eio-stat.html) — Повертає статус файлу
-   [eiostatvfs](function.eio-statvfs.html) — Повертає статистику файлової системи
-   [eiosymlink](function.eio-symlink.html) - Створює символічне посилання
-   [eiosyncfilerange](function.eio-sync-file-range.html) — Синхронізує сегмент файлу із даними файлу на зовнішньому сховищі
-   [eiosync](function.eio-sync.html) — Записує кеш із буфера на диск
-   [eiosyncfs](function.eio-syncfs.html) — Викликає системний syncfs у Linux, якщо це доступно
-   [eiotruncate](function.eio-truncate.html) - Урізує розмір файлу
-   [eiounlink](function.eio-unlink.html) — Видаляє файл або одне із жорстких посилань на нього
-   [eioutime](function.eio-utime.html) — Змінює дату та час останньої модифікації та доступу до файлу
-   [eiowrite](function.eio-write.html) - Запис у файл