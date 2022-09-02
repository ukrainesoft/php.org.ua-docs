---
navigation:
  - function.openal-context-current.md: « openalcontextcurrent
  - function.openal-context-process.md: openalcontextprocess »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalcontextdestroy
---
# openalcontextdestroy

(PECL openal >= 0.1.0)

openalcontextdestroy — Знищує контекст

### Опис

```methodsynopsis
openal_context_destroy(resource $context): bool
```

### Список параметрів

`context`

Ресурс [Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openalcontextcreate()](function.openal-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalcontextcreate()](function.openal-context-create.md) - Створити контекст обробки звуку
