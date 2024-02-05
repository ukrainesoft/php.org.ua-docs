---
navigation:
  - function.session-reset.md: « session\_reset
  - function.session-set-cookie-params.md: session\_set\_cookie\_params »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_save\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_save\_path

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_save\_path — Отримує та/або встановлює шлях збереження сесії

### Опис

```methodsynopsis
session_save_path(?string $path = null): string|false
```

**session\_save\_path()** повертає шлях поточної директорії, яка використовується для збереження сесії даних.

### Список параметрів

`path`

Шлях для даних сесії. Якщо вказано і не дорівнює **`null`**, то шлях, куди зберігаються дані, буде змінено. Для цієї мети **session\_save\_path()** слід викликати перед [session\_start()](function.session-start.md)

> **Зауваження** :
> 
> У деяких операційних системах можна вказати шлях у файловій системі, яка ефективно обробляє велику кількість невеликих файлів. Наприклад, у Linux файлова система reiserfs може забезпечити кращу продуктивність, ніж ext2fs.

### Значення, що повертаються

Повертає шлях поточної директорії, що використовується для зберігання даних сесії або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `path`тепер може бути\*\*`null`\*\* |

### Дивіться також

-   [session.save\_path](session.configuration.md#ini.session.save-path)
