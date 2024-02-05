---
navigation:
  - swoole.installation.md: « Встановлення
  - swoole.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - swoole.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Swoole**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [swoole.aio\_thread\_num](swoole.configuration.md#ini.swoole.aio-thread-num) |  | **`INI_ALL`** |  |
| [swoole.display\_errors](swoole.configuration.md#ini.swoole.display-errors) | On | **`INI_ALL`** |  |
| [swoole.fast\_serialize](swoole.configuration.md#ini.swoole.fast-serialize) | Off | **`INI_ALL`** |  |
| [swoole.unixsock\_buffer\_size](swoole.configuration.md#ini.swoole.unixsock-buffer-size) | 8388608 | **`INI_ALL`** |  |
| [swoole.use\_namespace](swoole.configuration.md#ini.swoole.use-namespace) | On | **`INI_SYSTEM`** |  |
| [swoole.enable\_coroutine](swoole.configuration.md#ini.swoole.enable-coroutine) | On | **`INI_ALL`** | Доступно, починаючи з swoole 4.0.0 |
| [swoole.use\_shortname](swoole.configuration.md#ini.swoole.use-shortname) | On | **`INI_ALL`** | Доступно, починаючи з swoole 4.0.0 |
| [swoole.enable\_preemptive\_scheduler](swoole.configuration.md#ini.swoole.enable-preemptive-scheduler) | Off | **`INI_ALL`** | Доступно, починаючи з swoole 4.4.0 |
| [swoole.enable\_library](swoole.configuration.md#ini.swoole.enable-library) | On | **`INI_ALL`** | Доступно, починаючи з swoole 4.0.0 |

Коротке пояснення конфігураційних директив.

`swoole.aio_thread_num`int

Номер потоку асинхронного введення/виводу POSIX

`swoole.display_errors`string

Визначає, чи помилки Swoole повинні виводитися на екран.

`swoole.fast_serialize`string

Визначає, чи включати Swoole fast\_serialize.

`swoole.unixsock_buffer_size`int

Розмір буфера сокету Unix

`swoole.use_namespace`string

Визначає, чи використовувати простір імен PHP.

`swoole.enable_coroutine`string

Визначає, чи включати співпрограму

`swoole.use_shortname`string

Визначає, чи включати короткі псевдоніми

`swoole.enable_preemptive_scheduler`string

Визначає, чи включати витісняючий планувальник

`swoole.enable_library`string

Визначає, чи включати бібліотеку
