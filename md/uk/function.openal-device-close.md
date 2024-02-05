---
navigation:
  - function.openal-context-suspend.md: « openal\_context\_suspend
  - function.openal-device-open.md: openal\_device\_open »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_device\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_device\_close

(PECL openal >= 0.1.0)

openal\_device\_close — Закрити пристрій OpenAL

### Опис

```methodsynopsis
openal_device_close(resource $device): bool
```

### Список параметрів

`device`

Ресурс[Open AL(Device)](openal.resources.md) (Створений раніше за допомогою [openal\_device\_open()](function.openal-device-open.md)), який потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_device\_open()](function.openal-device-open.md) \- Ініціалізувати звуковий рівень OpenAL
