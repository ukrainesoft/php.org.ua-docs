---
navigation:
  - function.scandir.md: « scandir
  - intro.fileinfo.md: Введение »
  - index.md: PHP Manual
  - refs.fileprocess.file.md: Модулі для роботи з файловою системою
title: Інформація про файл
---
# Інформація про файл

-   [Введение](intro.fileinfo.md)
-   [Встановлення та налаштування](fileinfo.setup.md)
    -   [Вимоги](fileinfo.requirements.md)
    -   [Установка](fileinfo.installation.md)
    -   [Налаштування під час виконання](fileinfo.configuration.md)
    -   [Типи ресурсів](fileinfo.resources.md)
-   [Обумовлені константи](fileinfo.constants.md)
-   [Функции модуля Fileinfo](ref.fileinfo.md)
    -   [finfobuffer](function.finfo-buffer.md) — Повертає інформацію про рядок буфера
    -   [finfoclose](function.finfo-close.md) - Закриває екземпляр finfo
    -   [finfofile](function.finfo-file.md) — Повертає інформацію про файл
    -   [finfoopen](function.finfo-open.md) - Створює екземпляр finfo
    -   [finfosetflags](function.finfo-set-flags.md) — Встановлює параметри конфігурації libmagic
    -   [mimecontenttype](function.mime-content-type.md) - Визначає MIME-тип вмісту файлу
-   [finfo](class.finfo.md) - Клас finfo
    -   [finfo::buffer](finfo.buffer.md) - Псевдонім finfobuffer()
    -   [finfo::construct](finfo.construct.md) - Псевдонім finfoopen
    -   [finfo::file](finfo.file.md) - Псевдонім finfofile()
    -   [finfo::setflags](finfo.set-flags.md) - Псевдонім finfosetflags()
