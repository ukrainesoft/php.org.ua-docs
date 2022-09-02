---
navigation:
  - wrappers.audio.md: '« ogg://'
  - security.md: Безпека »
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'expect://'
---
# expect://

expect:// - Потоки для взаємодії з процесами

### Опис

Потоки, відкриті за допомогою обгортки expect://, надають доступ до процесів stdio, stdout та stderr через PTY.

> **Зауваження** **Ця обгортка вимкнена за умовчанням**  
> Для того щоб використовувати обгортку expect://, необхідно встановити модуль [» Expect](https://pecl.php.net/package/expect), доступний у [» PECL](https://pecl.php.net/)

expect:// (PECL)

### Використання

-   expect://command

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | Ні |
| Читання | Так |
| Запис | Так |
| Додавання | Так |
| Одночасне читання та запис | Ні |
| Підтримка [stat()](function.stat.md) | Ні |
| Підтримка [unlink()](function.unlink.md) | Ні |
| Підтримка [rename()](function.rename.md) | Ні |
| Підтримка [mkdir()](function.mkdir.md) | Ні |
| Підтримка [rmdir()](function.rmdir.md) | Ні |

### Приклади
