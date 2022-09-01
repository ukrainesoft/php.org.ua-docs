---
navigation:
  - function.openal-context-process.html: « openalcontextprocess
  - function.openal-device-close.html: openaldeviceclose »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalcontextsuspend
---
# openalcontextsuspend

(PECL openal >= 0.1.0)

openalcontextsuspend — Зупинити вказаний контекст

### Опис

```methodsynopsis
openal_context_suspend(resource $context): bool
```

### Список параметрів

`context`

Ресурс [Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openalcontextcreate()](function.openal-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalcontextcreate()](function.openal-context-create.md) - Створити контекст обробки звуку
-   [openalcontextcurrent()](function.openal-context-current.md) - Зробити вказаний контекст поточним
-   [openalcontextprocess()](function.openal-context-process.md) - опрацювати зазначений контекст
