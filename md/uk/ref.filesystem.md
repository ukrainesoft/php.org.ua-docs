---
navigation:
  - filesystem.constants.md: « Зумовлені константи
  - function.basename.md: basename »
  - index.md: PHP Manual
  - book.filesystem.md: Файлова система
title: Функції файлової системи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції файлової системи

# Дивіться також

Опис родинних функцій ви зможете знайти у розділах [Каталоги](ref.dir.md) і [Виконання програм](ref.exec.md)

За списком обгорток URL для роботи з віддаленими файлами та поясненнями зверніться до розділу [Підтримувані протоколи та обгортки](wrappers.md)

## Зміст

-   [basename](function.basename.md)— Повертає останній компонент імені із зазначеного шляху
-   [chgrp](function.chgrp.md)— Змінює групу файлу
-   [chmod](function.chmod.md)— Змінює режим доступу до файлу
-   [chown](function.chown.md) \- Змінює власника файлу
-   [clearstatcache](function.clearstatcache.md)— Очищує кеш файлів
-   [copy](function.copy.md) \- Копіює файл
-   [delete](function.delete.md)— Дивіться опис функції unlink або unset
-   [dirname](function.dirname.md)— Повертає ім'я батьківського каталогу із зазначеного шляху
-   [disk\_free\_space](function.disk-free-space.md)— Повертає розмір доступного простору в каталозі чи файловій системі
-   [disk\_total\_space](function.disk-total-space.md)— Повертає загальний розмір файлової системи або розділу диска
-   [diskfreespace](function.diskfreespace.md) \- Псевдонім disk\_free\_space
-   [fclose](function.fclose.md)— Закриває відкритий дескриптор файлу
-   [fdatasync](function.fdatasync.md)— Синхронізує дані (але не метадані) із файлом
-   [feof](function.feof.md)— Перевіряє, чи кінець файлу досягнуто.
-   [fflush](function.fflush.md)— Скидає буфер виводу у файл
-   [fgetc](function.fgetc.md)— Зчитує символ із файлу
-   [fgetcsv](function.fgetcsv.md)— Читає рядок із файлу та проводить розбір даних CSV
-   [fgets](function.fgets.md)— Читає рядок із файлу
-   [fgetss](function.fgetss.md)— Читає рядок із файлу та видаляє HTML-теги
-   [file\_exists](function.file-exists.md)— Перевіряє існування вказаного файлу чи каталогу
-   [file\_get\_contents](function.file-get-contents.md)— Читає вміст файлу в рядок
-   [file\_put\_contents](function.file-put-contents.md) \- Пише дані у файл
-   [file](function.file.md)— Читає вміст файлу та поміщає його у масив
-   [fileatime](function.fileatime.md)— Повертає час останнього доступу до файлу
-   [filectime](function.filectime.md)— Повертає час зміни індексного дескриптора файлу
-   [filegroup](function.filegroup.md)— Отримує ідентифікатор групи файлу
-   [fileinode](function.fileinode.md)— Повертає індексний дескриптор файлу
-   [filemtime](function.filemtime.md)— Повертає час останньої зміни файлу
-   [fileowner](function.fileowner.md)— Повертає ідентифікатор власника файлу
-   [fileperms](function.fileperms.md)— Повертає інформацію про права на файл
-   [filesize](function.filesize.md)— Повертає розмір файлу
-   [filetype](function.filetype.md)— Повертає тип файлу
-   [flock](function.flock.md)— Портоване консультативне блокування файлів
-   [fnmatch](function.fnmatch.md)— Перевіряє збіг імені файлу із шаблоном
-   [fopen](function.fopen.md)— Відкриває файл чи URL
-   [fpassthru](function.fpassthru.md)— Виводить всі дані з файлового покажчика, що залишилися.
-   [fputcsv](function.fputcsv.md)— Форматує рядок у вигляді CSV і записує його у файловий покажчик
-   [fputs](function.fputs.md) \- Псевдонім fwrite
-   [fread](function.fread.md) \- Бінарно-безпечне читання файлу
-   [fscanf](function.fscanf.md)— Обробляє дані з файлу відповідно до формату
-   [fseek](function.fseek.md)— Встановлює зміщення у файловому покажчику
-   [fstat](function.fstat.md)— Отримує інформацію про файл, використовуючи відкритий файловий покажчик
-   [fsync](function.fsync.md)— Синхронізує зміни у файлі (включаючи метадані)
-   [ftell](function.ftell.md)— Повертає поточну позицію покажчика читання/запису файлу
-   [ftruncate](function.ftruncate.md)— Урізує файл до вказаної довжини
-   [fwrite](function.fwrite.md) \- Бінарно-безпечний запис у файл
-   [glob](function.glob.md)— Знаходить файлові шляхи, що збігаються із шаблоном
-   [is\_dir](function.is-dir.md)— Визначає, чи ім'я файлу є директорією
-   [is\_executable](function.is-executable.md)— Визначає, чи файл виконуваний
-   [is\_file](function.is-file.md)— Визначає, чи файл є звичайним файлом
-   [is\_link](function.is-link.md)— Визначає, чи є файл символічним посиланням
-   [is\_readable](function.is-readable.md)— Визначає існування файлу і чи він доступний для читання
-   [is\_uploaded\_file](function.is-uploaded-file.md)— Визначає, чи файл завантажений за допомогою HTTP POST
-   [is\_writable](function.is-writable.md)— Визначає, чи є файл для запису.
-   [is\_writeable](function.is-writeable.md) \- Псевдонім is\_writable
-   [lchgrp](function.lchgrp.md)— Змінює групу, якій належить символічне посилання
-   [lchown](function.lchown.md)— Змінює власника символічного посилання
-   [link](function.link.md) \- Створює жорстке посилання
-   [linkinfo](function.linkinfo.md)— Повертає інформацію про посилання
-   [lstat](function.lstat.md)— Повертає інформацію про файл або символічне посилання
-   [mkdir](function.mkdir.md) \- Створює директорію
-   [move\_uploaded\_file](function.move-uploaded-file.md)— Переміщує завантажений файл у нове місце
-   [parse\_ini\_file](function.parse-ini-file.md) \- Обробляє конфігураційний файл
-   [parse\_ini\_string](function.parse-ini-string.md)— Розбирає рядок конфігурації
-   [pathinfo](function.pathinfo.md)— Повертає інформацію про шлях до файлу
-   [pclose](function.pclose.md)— Закриває файловий покажчик процесу
-   [popen](function.popen.md)— Відкриває файловий покажчик процесу
-   [readfile](function.readfile.md) \- Виводить файл
-   [readlink](function.readlink.md)— Повертає файл, на який вказує символічне посилання
-   [realpath\_cache\_get](function.realpath-cache-get.md)— Отримує записи з кеша realpath
-   [realpath\_cache\_size](function.realpath-cache-size.md)— Отримує розмір кеша realpath
-   [realpath](function.realpath.md)— Повертає абсолютний канонізований шлях до файлу
-   [rename](function.rename.md)— Перейменовує файл чи директорію
-   [rewind](function.rewind.md) \- Скидає курсор файлового покажчика
-   [rmdir](function.rmdir.md) \- Видаляє директорію
-   [set\_file\_buffer](function.set-file-buffer.md) \- Псевдонім stream\_set\_write\_buffer
-   [stat](function.stat.md)— Повертає інформацію про файл
-   [symlink](function.symlink.md) \- Створює символічне посилання
-   [tempnam](function.tempnam.md)— Створює файл із унікальним ім'ям
-   [tmpfile](function.tmpfile.md)— Створює тимчасовий файл
-   [touch](function.touch.md)— Встановлює час доступу та модифікації файлу
-   [umask](function.umask.md)— Змінює поточну маску прав доступу для новостворених файлів та каталогів (umask)
-   [unlink](function.unlink.md)— Видаляє файл
