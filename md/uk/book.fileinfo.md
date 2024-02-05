---
navigation:
  - function.scandir.md: « scandir
  - intro.fileinfo.md: Вступ "
  - index.md: PHP Manual
  - refs.fileprocess.file.md: Модулі для роботи з файловою системою
title: Інформація про файл
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інформація про файл

-   [Вступ](intro.fileinfo.md)
-   [Встановлення та налаштування](fileinfo.setup.md)
    -   [Вимоги](fileinfo.requirements.md)
    -   [Установка](fileinfo.installation.md)
    -   [Налаштування під час виконання](fileinfo.configuration.md)
    -   [Типи ресурсів](fileinfo.resources.md)
-   [Обумовлені константи](fileinfo.constants.md)
-   [Функції модуля Fileinfo](ref.fileinfo.md)
    -   [finfo\_buffer](function.finfo-buffer.md)— Повертає інформацію про рядок буфера
    -   [finfo\_close](function.finfo-close.md) \- Закриває екземпляр finfo
    -   [finfo\_file](function.finfo-file.md)— Повертає інформацію про файл
    -   [finfo\_open](function.finfo-open.md) \- Створює екземпляр finfo
    -   [finfo\_set\_flags](function.finfo-set-flags.md)— Встановлює параметри конфігурації libmagic
    -   [mime\_content\_type](function.mime-content-type.md) \- Визначає MIME-тип вмісту файлу
-   [finfo](class.finfo.md) \- Клас finfo
    -   [finfo::buffer](finfo.buffer.md) \- Псевдонім finfo\_buffer()
    -   [finfo::\_\_construct](finfo.construct.md) \- Псевдонім finfo\_open
    -   [finfo::file](finfo.file.md) \- Псевдонім finfo\_file()
    -   [finfo::set\_flags](finfo.set-flags.md) \- Псевдонім finfo\_set\_flags()
