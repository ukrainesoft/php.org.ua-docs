Eio Функції

-   [« Примеры](eio.examples.html)
    
-   [eio\_busy »](function.eio-busy.html)
    
-   [PHP Manual](index.html)
    
-   [Eio](book.eio.html)
    
-   Eio Функції
    

# Eio Функції

## Зміст

-   [eio\_busy](function.eio-busy.html) — Штучно збільшує навантаження. Може бути корисним при тестуванні, вивченні продуктивності
-   [eio\_cancel](function.eio-cancel.html) — Скасує запит
-   [eio\_chmod](function.eio-chmod.html) — Змінює права доступу до файлу/директорії
-   [eio\_chown](function.eio-chown.html) — Змінює права доступу до файлу/директорії
-   [eio\_close](function.eio-close.html) - Закрити файл
-   [eio\_custom](function.eio-custom.html) — Виконує запит користувача як будь-який інший eio виклик
-   [eio\_dup2](function.eio-dup2.html) - Створює дублікат дескриптора файлу
-   [eio\_event\_loop](function.eio-event-loop.html) — Взаємодіє з libeio доти, доки всі запити не будуть виконані
-   [eio\_fallocate](function.eio-fallocate.html) — Дозволяє безпосередньо керувати розміром дискового простору, що використовується для файлу.
-   [eio\_fchmod](function.eio-fchmod.html) — Змінює права доступу до файлу
-   [eio\_fchown](function.eio-fchown.html) - Змінює власника файлу
-   [eio\_fdatasync](function.eio-fdatasync.html) — Синхронізує поточний стан файлу із фізичним пристроєм
-   [eio\_fstat](function.eio-fstat.html) — Повертає статус файлу
-   [eio\_fstatvfs](function.eio-fstatvfs.html) — Повертає статистику файлової системи
-   [eio\_fsync](function.eio-fsync.html) — Синхронізує поточний стан файлу із фізичним пристроєм
-   [eio\_ftruncate](function.eio-ftruncate.html) - Урізує розмір файлу
-   [eio\_futime](function.eio-futime.html) — Змінює дату та час останньої модифікації та доступу до файлу
-   [eio\_get\_event\_stream](function.eio-get-event-stream.html) — Повертає потік, що відображає змінну, що використовується при взаємодії з libeio
-   [eio\_get\_last\_error](function.eio-get-last-error.html) — Повертає останню помилку, пов'язану із вказівником на ресурс
-   [eio\_grp\_add](function.eio-grp-add.html) — Додає запит до групи запитів
-   [eio\_grp\_cancel](function.eio-grp-cancel.html) — Скасує групу запитів
-   [eio\_grp\_limit](function.eio-grp-limit.html) — Встановлює граничну кількість запитів у групі
-   [eio\_grp](function.eio-grp.html) — Створює групу запитів
-   [eio\_init](function.eio-init.html) - (Не-) ініціалізує Eio
-   [eio\_link](function.eio-link.html) - Створює жорстке посилання на файл
-   [eio\_lstat](function.eio-lstat.html) — Повертає статус файлу
-   [eio\_mkdir](function.eio-mkdir.html) - Створення директорії
-   [eio\_mknod](function.eio-mknod.html) — Створює спеціальний чи звичайний файл
-   [eio\_nop](function.eio-nop.html) - Прохід по циклу запиту, не здійснюючи жодних операцій
-   [eio\_npending](function.eio-npending.html) — Повертає кількість завершених, але необроблених процесів
-   [eio\_nready](function.eio-nready.html) — Повертає кількість ще не опрацьованих запитів
-   [eio\_nreqs](function.eio-nreqs.html) — Повертає кількість запитів, які потрібно виконати
-   [eio\_nthreads](function.eio-nthreads.html) — Повертає кількість потоків, що використовуються в даний момент.
-   [eio\_open](function.eio-open.html) - Відкриває файл
-   [eio\_poll](function.eio-poll.html) — Може бути викликана коли є запити, які очікують на виконання
-   [eio\_read](function.eio-read.html) — Читає дані з файлу, починаючи із заданого усунення
-   [eio\_readahead](function.eio-readahead.html) — Поміщає дані з файлу до кешу сторінки
-   [eio\_readdir](function.eio-readdir.html) — Читає вміст директорії
-   [eio\_readlink](function.eio-readlink.html) — Читає значення символічного посилання
-   [eio\_realpath](function.eio-realpath.html) — Отримує абсолютний приведений до канонічного виду шлях
-   [eio\_rename](function.eio-rename.html) — Змінює ім'я або переміщує файл
-   [eio\_rmdir](function.eio-rmdir.html) - Видаляє директорію
-   [eio\_seek](function.eio-seek.html) — Переміщує файловий покажчик файлу fd на число байт offset відповідно до директиви whence
-   [eio\_sendfile](function.eio-sendfile.html) — Переміщує дані між файлами
-   [eio\_set\_max\_idle](function.eio-set-max-idle.html) — Встановлює максимальну кількість потоків, що очікують.
-   [eio\_set\_max\_parallel](function.eio-set-max-parallel.html) — Встановлює максимальну кількість паралельних потоків
-   [eio\_set\_max\_poll\_reqs](function.eio-set-max-poll-reqs.html) — Встановлює максимальну кількість запитів, що обробляються.
-   [eio\_set\_max\_poll\_time](function.eio-set-max-poll-time.html) - Встановлює максимальний час виконання
-   [eio\_set\_min\_parallel](function.eio-set-min-parallel.html) — Встановлює мінімальну кількість паралельних потоків
-   [eio\_stat](function.eio-stat.html) — Повертає статус файлу
-   [eio\_statvfs](function.eio-statvfs.html) — Повертає статистику файлової системи
-   [eio\_symlink](function.eio-symlink.html) - Створює символічне посилання
-   [eio\_sync\_file\_range](function.eio-sync-file-range.html) — Синхронізує сегмент файлу із даними файлу на зовнішньому сховищі
-   [eio\_sync](function.eio-sync.html) — Записує кеш із буфера на диск
-   [eio\_syncfs](function.eio-syncfs.html) — Викликає системний syncfs у Linux, якщо це доступно
-   [eio\_truncate](function.eio-truncate.html) - Урізує розмір файлу
-   [eio\_unlink](function.eio-unlink.html) — Видаляє файл або одне із жорстких посилань на нього
-   [eio\_utime](function.eio-utime.html) — Змінює дату та час останньої модифікації та доступу до файлу
-   [eio\_write](function.eio-write.html) - Запис у файл