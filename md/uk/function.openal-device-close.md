---
navigation:
  - function.openal-context-suspend.html: « openalcontextsuspend
  - function.openal-device-open.html: openaldeviceopen »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openaldeviceclose
---
# openaldeviceclose

(PECL openal >= 0.1.0)

openaldeviceclose — Закрити пристрій OpenAL

### Опис

```methodsynopsis
openal_device_close(resource $device): bool
```

### Список параметрів

`device`

Ресурс [Open AL(Device)](openal.resources.md) (Створений раніше за допомогою [openaldeviceopen()](function.openal-device-open.md)), який потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openaldeviceopen()](function.openal-device-open.md) - Ініціалізувати звуковий рівень OpenAL
