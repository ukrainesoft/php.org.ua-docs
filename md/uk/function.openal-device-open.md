---
navigation:
  - function.openal-device-close.html: « openaldeviceclose
  - function.openal-listener-get.html: openallistenerget »
  - index.html: PHP Manual
  - ref.openal.html: Функции OpenAL
title: openaldeviceopen
---
# openaldeviceopen

(PECL openal >= 0.1.0)

openaldeviceopen — Ініціалізувати звуковий рівень OpenAL

### Опис

```methodsynopsis
openal_device_open(string $device_desc = ?): resource
```

### Список параметрів

`device_desc`

При необхідності відкрити аудіопристрій, вказавши значення параметра `device_desc`. Якщо `device_desc` не вказано, буде використано перший аудіопристрій.

### Значення, що повертаються

Повертає ресурс [Open AL(Device)](openal.resources.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openaldeviceclose()](function.openal-device-close.html) - Закрити пристрій OpenAL
-   [openalcontextcreate()](function.openal-context-create.html) - Створити контекст обробки звуку
