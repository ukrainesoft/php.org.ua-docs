---
navigation:
  - function.session-reset.md: « sessionreset
  - function.session-set-cookie-params.md: sessionsetcookieparams »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionsavepath
---
# sessionsavepath

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionsavepath — Отримує та/або встановлює шлях збереження сесії

### Опис

```methodsynopsis
session_save_path(?string $path = null): string|false
```

**sessionsavepath()** повертає шлях поточної директорії, що використовується для збереження даних сесії.

### Список параметрів

`path`

Шлях для даних сесії. Якщо вказано і не дорівнює **`null`**, то шлях, куди зберігаються дані, буде змінено. Для цієї мети **sessionsavepath()** слід викликати перед [sessionstart()](function.session-start.md)

> **Зауваження**
> 
> У деяких операційних системах можна вказати шлях у файловій системі, яка ефективно обробляє велику кількість невеликих файлів. Наприклад, у Linux файлова система reiserfs може забезпечити кращу продуктивність, ніж ext2fs.

### Значення, що повертаються

Повертає шлях поточної директорії, що використовується для зберігання даних сесії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `path` тепер може бути **`null`** |

### Дивіться також

-   [session.savepath](session.configuration.md#ini.session.save-path)
