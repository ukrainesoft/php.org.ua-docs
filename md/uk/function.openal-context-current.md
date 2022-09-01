---
navigation:
  - function.openal-context-create.html: « openalcontextcreate
  - function.openal-context-destroy.html: openalcontextdestroy »
  - index.html: PHP Manual
  - ref.openal.html: Функции OpenAL
title: openalcontextcurrent
---
# openalcontextcurrent

(PECL openal >= 0.1.0)

openalcontextcurrent — Зробити вказаний контекст поточним

### Опис

```methodsynopsis
openal_context_current(resource $context): bool
```

### Список параметрів

`context`

Ресурс [Open AL(Context)](openal.resources.html) (Створений раніше за допомогою [openalcontextcreate()](function.openal-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalcontextcreate()](function.openal-context-create.md) - Створити контекст обробки звуку
