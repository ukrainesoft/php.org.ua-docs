---
navigation:
  - function.openal-device-close.md: « openal\_device\_close
  - function.openal-listener-get.md: openal\_listener\_get »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_device\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_device\_open

(PECL openal >= 0.1.0)

openal\_device\_open — Ініціалізувати звуковий рівень OpenAL

### Опис

```methodsynopsis
openal_device_open(string $device_desc = ?): resource
```

### Список параметрів

`device_desc`

При необхідності відкрити аудіопристрій, вказавши значення параметра `device_desc`. Якщо `device_desc` не вказано, буде використано перший аудіопристрій.

### Значення, що повертаються

Повертає ресурс [Open AL(Device)](openal.resources.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_device\_close()](function.openal-device-close.md) \- Закрити пристрій OpenAL
-   [openal\_context\_create()](function.openal-context-create.md) \- Створити контекст обробки звуку
