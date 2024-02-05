---
navigation:
  - function.openal-buffer-loadwav.md: « openal\_buffer\_loadwav
  - function.openal-context-current.md: openal\_context\_current »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_context\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_context\_create

(PECL openal >= 0.1.0)

openal\_context\_create — Створити контекст обробки звуку

### Опис

```methodsynopsis
openal_context_create(resource $device): resource
```

### Список параметрів

`device`

Ресурс[Open AL(Device)](openal.resources.md) (Створений раніше за допомогою **openal\_device\_create()**

### Значення, що повертаються

Повертає ресурс [Open AL(Context)](openal.resources.md) у разі успішного виконання, \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_device\_open()](function.openal-device-open.md) \- Ініціалізувати звуковий рівень OpenAL
-   [openal\_context\_destroy()](function.openal-context-destroy.md) \- Знищує контекст
