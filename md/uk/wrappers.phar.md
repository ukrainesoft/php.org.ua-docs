---
navigation:
  - wrappers.glob.md: '« glob://'
  - wrappers.ssh2.md: 'ssh2:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'phar://'
---
# phar://

phar:// - PHP-архів

### Опис

Обгортка потоку phar://. Дивіться розділ [Обёртка потока Phar](phar.using.stream.md) для детальнішого опису.

### Використання

-   phar://

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | Ні |
| Обмеження по [allowurlinclude](filesystem.configuration.md#ini.allow-url-include) | Ні |
| Читання | Так |
| Запис | Так |
| Додавання | Ні |
| Одночасне читання та запис | Так |
| Підтримка [stat()](function.stat.md) | Так |
| Підтримка [unlink()](function.unlink.md) | Так |
| Підтримка [rename()](function.rename.md) | Так |
| Підтримка [mkdir()](function.mkdir.md) | Так |
| Підтримка [rmdir()](function.rmdir.md) | Так |

### Дивіться також

-   [Контекстні опції Phar](context.phar.md)
