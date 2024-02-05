---
navigation:
  - wrappers.glob.md: '« glob://'
  - wrappers.ssh2.md: 'ssh2:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'phar://'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phar://

phar:// - PHP-архів

### Опис

Обгортка потоку phar://. Дивіться розділ [Обгортка потоку Phar](phar.using.stream.md) для детальнішого опису.

### Використання

-   phar://

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allow\_url\_fopen](filesystem.configuration.md#ini.allow-url-fopen) | Ні |
| Обмеження по [allow\_url\_include](filesystem.configuration.md#ini.allow-url-include) | Ні |
| Читання | Так |
| Запис | Так |
| Додавання | Ні |
| Одночасне читання та запис | Так |
| Поддержка[stat()](function.stat.md) | Так |
| Поддержка[unlink()](function.unlink.md) | Так |
| Поддержка[rename()](function.rename.md) | Так |
| Поддержка[mkdir()](function.mkdir.md) | Так |
| Поддержка[rmdir()](function.rmdir.md) | Так |

### Дивіться також

-   [Контекстні опції Phar](context.phar.md)
