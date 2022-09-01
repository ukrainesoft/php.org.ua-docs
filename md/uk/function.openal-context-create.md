---
navigation:
  - function.openal-buffer-loadwav.html: « openalbufferloadwav
  - function.openal-context-current.html: openalcontextcurrent »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalcontextcreate
---
# openalcontextcreate

(PECL openal >= 0.1.0)

openalcontextcreate — Створити контекст обробки звуку

### Опис

```methodsynopsis
openal_context_create(resource $device): resource
```

### Список параметрів

`device`

Ресурс [Open AL(Device)](openal.resources.md) (Створений раніше за допомогою **openaldevicecreate()**

### Значення, що повертаються

Повертає ресурс [Open AL(Context)](openal.resources.md) у разі успішного виконання, **`false`** у разі виникнення помилки.

### Дивіться також

-   [openaldeviceopen()](function.openal-device-open.html) - Ініціалізувати звуковий рівень OpenAL
-   [openalcontextdestroy()](function.openal-context-destroy.html) - Знищує контекст
