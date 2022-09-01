---
navigation:
  - function.openal-context-destroy.html: « openalcontextdestroy
  - function.openal-context-suspend.html: openalcontextsuspend »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalcontextprocess
---
# openalcontextprocess

(PECL openal >= 0.1.0)

openalcontextprocess — Обробити вказаний контекст

### Опис

```methodsynopsis
openal_context_process(resource $context): bool
```

### Список параметрів

`context`

Ресурс [Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openalcontextcreate()](function.openal-context-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalcontextcreate()](function.openal-context-create.html) - Створити контекст обробки звуку
-   [openalcontextcurrent()](function.openal-context-current.html) - Зробити вказаний контекст поточним
-   [openalcontextsuspend()](function.openal-context-suspend.html) - призупинити зазначений контекст
