---
navigation:
  - swoole.installation.md: « Установка
  - swoole.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - swoole.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Swoole**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [swoole.aiothreadnum](swoole.configuration.md#ini.swoole.aio-thread-num) |  | PHPINIALL |  |
| [swoole.displayerrors](swoole.configuration.md#ini.swoole.display-errors) | Він | PHPINIALL |  |
| [swoole.fastserialize](swoole.configuration.md#ini.swoole.fast-serialize) | Off | PHPINIALL |  |
| [swoole.unixsockbuffersize](swoole.configuration.md#ini.swoole.unixsock-buffer-size) |  | PHPINIALL |  |
| [swoole.usenamespace](swoole.configuration.md#ini.swoole.use-namespace) | Він | PHPINISYSTEM |  |
| [swoole.enablecoroutine](swoole.configuration.md#ini.swoole.enable-coroutine) | Він | PHPINIALL | Доступно, починаючи з swoole 4.0.0 |
| [swoole.useshortname](swoole.configuration.md#ini.swoole.use-shortname) | Він | PHPINIALL | Доступно, починаючи з swoole 4.0.0 |
| [swoole.enablepreemptivescheduler](swoole.configuration.md#ini.swoole.enable-preemptive-scheduler) | Off | PHPINIALL | Доступно, починаючи з swoole 4.4.0 |
| [swoole.enablelibrary](swoole.configuration.md#ini.swoole.enable-library) | Він | PHPINIALL | Доступно, починаючи з swoole 4.0.0 |

Коротке пояснення конфігураційних директив.

`swoole.aio_thread_num` int

Номер потоку асинхронного введення/виводу POSIX

`swoole.display_errors` string

Визначає, чи помилки Swoole повинні виводитися на екран.

`swoole.fast_serialize` string

Визначає, чи включати Swoole fastserialize.

`swoole.unixsock_buffer_size` int

Розмір буфера сокету Unix

`swoole.use_namespace` string

Визначає, чи використовувати простір імен PHP.

`swoole.enable_coroutine` string

Визначає, чи включати співпрограму

`swoole.use_shortname` string

Визначає, чи включати короткі псевдоніми

`swoole.enable_preemptive_scheduler` string

Визначає, чи включати витісняючий планувальник

`swoole.enable_library` string

Визначає, чи включати бібліотеку
