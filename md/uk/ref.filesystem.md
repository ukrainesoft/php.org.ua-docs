Функції файлової системи

-   [« Предопределённые константы](filesystem.constants.html)
    
-   [basename »](function.basename.html)
    
-   [PHP Manual](index.html)
    
-   [Файловая система](book.filesystem.html)
    
-   Функції файлової системи
    

# Функції файлової системи

# Дивіться також

Опис родинних функцій ви зможете знайти у розділах [Каталоги](ref.dir.html) і [Выполнение программ](ref.exec.html)

За списком обгорток URL для роботи з віддаленими файлами та поясненнями зверніться до розділу [Поддерживаемые протоколы и обёртки](wrappers.html)

## Зміст

-   [basename](function.basename.html) — Повертає останній компонент імені із зазначеного шляху
-   [chgrp](function.chgrp.html) — Змінює групу файлу
-   [chmod](function.chmod.html) — Змінює режим доступу до файлу
-   [chown](function.chown.html) - Змінює власника файлу
-   [clearstatcache](function.clearstatcache.html) — Очищує кеш файлів
-   [copy](function.copy.html) - Копіює файл
-   [delete](function.delete.html) — Дивіться опис функції unlink або unset
-   [dirname](function.dirname.html) — Повертає ім'я батьківського каталогу із зазначеного шляху
-   [disk\_free\_space](function.disk-free-space.html) — Повертає розмір доступного простору в каталозі чи файловій системі
-   [disk\_total\_space](function.disk-total-space.html) — Повертає загальний розмір файлової системи або розділу диска
-   [diskfreespace](function.diskfreespace.html) - Псевдонім diskfreespace
-   [fclose](function.fclose.html) — Закриває відкритий дескриптор файлу
-   [fdatasync](function.fdatasync.html) — Синхронізує дані (але не метадані) із файлом
-   [feof](function.feof.html) — Перевіряє, чи кінець файлу досягнуто.
-   [fflush](function.fflush.html) — Скидає буфер виводу у файл
-   [fgetc](function.fgetc.html) — Зчитує символ із файлу
-   [fgetcsv](function.fgetcsv.html) — Читає рядок із файлу та проводить розбір даних CSV
-   [fgets](function.fgets.html) — Читає рядок із файлу
-   [fgetss](function.fgetss.html) — Читає рядок із файлу та видаляє HTML-теги
-   [file\_exists](function.file-exists.html) — Перевіряє існування вказаного файлу чи каталогу
-   [file\_get\_contents](function.file-get-contents.html) — Читає вміст файлу в рядок
-   [file\_put\_contents](function.file-put-contents.html) - Пише дані у файл
-   [file](function.file.html) — Читає вміст файлу та поміщає його у масив
-   [fileatime](function.fileatime.html) — Повертає час останнього доступу до файлу
-   [filectime](function.filectime.html) — Повертає час зміни індексного дескриптора файлу
-   [filegroup](function.filegroup.html) — Отримує ідентифікатор групи файлів
-   [fileinode](function.fileinode.html) — Повертає індексний дескриптор файлу
-   [filemtime](function.filemtime.html) — Повертає час останньої зміни файлу
-   [fileowner](function.fileowner.html) — Повертає ідентифікатор власника файлу
-   [fileperms](function.fileperms.html) — Повертає інформацію про права на файл
-   [filesize](function.filesize.html) — Повертає розмір файлу
-   [filetype](function.filetype.html) — Повертає тип файлу
-   [flock](function.flock.html) — Портоване консультативне блокування файлів
-   [fnmatch](function.fnmatch.html) — Перевіряє збіг імені файлу із шаблоном
-   [fopen](function.fopen.html) — Відкриває файл чи URL
-   [fpassthru](function.fpassthru.html) — Виводить всі дані з файлового покажчика, що залишилися.
-   [fputcsv](function.fputcsv.html) — Форматує рядок у вигляді CSV і записує його у файловий покажчик
-   [fputs](function.fputs.html) - Псевдонім fwrite
-   [fread](function.fread.html) - Бінарно-безпечне читання файлу
-   [fscanf](function.fscanf.html) — Обробляє дані з файлу відповідно до формату
-   [fseek](function.fseek.html) — Встановлює зміщення у файловому покажчику
-   [fstat](function.fstat.html) — Отримує інформацію про файл, використовуючи відкритий файловий покажчик
-   [fsync](function.fsync.html) — Синхронізує зміни у файлі (включаючи метадані)
-   [ftell](function.ftell.html) — Повертає поточну позицію покажчика читання/запису файлу
-   [ftruncate](function.ftruncate.html) — Урізує файл до вказаної довжини
-   [fwrite](function.fwrite.html) - Бінарно-безпечний запис у файл
-   [glob](function.glob.html) — Знаходить файлові шляхи, що збігаються із шаблоном
-   [is\_dir](function.is-dir.html) — Визначає, чи ім'я файлу є директорією
-   [is\_executable](function.is-executable.html) — Визначає, чи файл виконуваний
-   [is\_file](function.is-file.html) — Визначає, чи файл є звичайним файлом
-   [is\_link](function.is-link.html) — Визначає, чи є файл символічним посиланням
-   [is\_readable](function.is-readable.html) — Визначає існування файлу і чи він доступний для читання
-   [is\_uploaded\_file](function.is-uploaded-file.html) — Визначає, чи файл завантажений за допомогою HTTP POST
-   [is\_writable](function.is-writable.html) — Визначає, чи є файл для запису.
-   [is\_writeable](function.is-writeable.html) - Псевдонім iswritable
-   [lchgrp](function.lchgrp.html) — Змінює групу, якій належить символічне посилання
-   [lchown](function.lchown.html) - Змінює власника символічного посилання
-   [link](function.link.html) - Створює жорстке посилання
-   [linkinfo](function.linkinfo.html) — Повертає інформацію про посилання
-   [lstat](function.lstat.html) — Повертає інформацію про файл або символічне посилання
-   [mkdir](function.mkdir.html) - Створює директорію
-   [move\_uploaded\_file](function.move-uploaded-file.html) — Переміщує завантажений файл у нове місце
-   [parse\_ini\_file](function.parse-ini-file.html) - Обробляє конфігураційний файл
-   [parse\_ini\_string](function.parse-ini-string.html) — Розбирає рядок конфігурації
-   [pathinfo](function.pathinfo.html) — Повертає інформацію про шлях до файлу
-   [pclose](function.pclose.html) — Закриває файловий покажчик процесу
-   [popen](function.popen.html) — Відкриває файловий покажчик процесу
-   [readfile](function.readfile.html) - Виводить файл
-   [readlink](function.readlink.html) — Повертає файл, на який вказує символічне посилання
-   [realpath\_cache\_get](function.realpath-cache-get.html) — Отримує записи з кеша realpath
-   [realpath\_cache\_size](function.realpath-cache-size.html) — Отримує розмір кеша realpath
-   [realpath](function.realpath.html) — Повертає абсолютний канонізований шлях до файлу
-   [rename](function.rename.html) — Перейменовує файл чи директорію
-   [rewind](function.rewind.html) — Скидає курсор файлового покажчика
-   [rmdir](function.rmdir.html) - Видаляє директорію
-   [set\_file\_buffer](function.set-file-buffer.html) - Псевдонім streamsetwritebuffer
-   [stat](function.stat.html) — Повертає інформацію про файл
-   [symlink](function.symlink.html) - Створює символічне посилання
-   [tempnam](function.tempnam.html) — Створює файл із унікальним ім'ям
-   [tmpfile](function.tmpfile.html) — Створює тимчасовий файл
-   [touch](function.touch.html) — Встановлює час доступу та модифікації файлу
-   [umask](function.umask.html) — Змінює поточну umask
-   [unlink](function.unlink.html) — Видаляє файл