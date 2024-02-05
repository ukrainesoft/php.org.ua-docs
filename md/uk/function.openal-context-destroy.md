---
navigation:
  - function.openal-context-current.md: « openal\_context\_current
  - function.openal-context-process.md: openal\_context\_process »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_context\_destroy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_context\_destroy

(PECL openal >= 0.1.0)

openal\_context\_destroy — Знищує контекст

### Опис

```methodsynopsis
openal_context_destroy(resource $context): bool
```

### Список параметрів

`context`

Ресурс[Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openal\_context\_create()](function.openal-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_context\_create()](function.openal-context-create.md) \- Створити контекст обробки звуку
