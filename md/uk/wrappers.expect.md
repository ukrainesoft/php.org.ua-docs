---
navigation:
  - wrappers.audio.md: '« ogg://'
  - security.md: Безпека »
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'expect://'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# expect://

expect:// - Потоки для взаємодії з процесами

### Опис

Потоки, відкриті за допомогою обгортки expect://, надають доступ до процесів stdio, stdout та stderr через PTY.

> **Зауваження** **Ця обгортка вимкнена за умовчанням**  
> Для того щоб використовувати обгортку expect://, необхідно встановити модуль [» Expect](https://pecl.php.net/package/expect), доступний у репозиторії [» PECL](https://pecl.php.net/)

expect:// (PECL)

### Використання

-   expect://command

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allow\_url\_fopen](filesystem.configuration.md#ini.allow-url-fopen) | Ні |
| Читання | Так |
| Запис | Так |
| Додавання | Так |
| Одночасне читання та запис | Ні |
| Поддержка[stat()](function.stat.md) | Ні |
| Поддержка[unlink()](function.unlink.md) | Ні |
| Поддержка[rename()](function.rename.md) | Ні |
| Поддержка[mkdir()](function.mkdir.md) | Ні |
| Поддержка[rmdir()](function.rmdir.md) | Ні |

### Приклади
