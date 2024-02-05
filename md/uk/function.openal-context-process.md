---
navigation:
  - function.openal-context-destroy.md: « openal\_context\_destroy
  - function.openal-context-suspend.md: openal\_context\_suspend »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_context\_process
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_context\_process

(PECL openal >= 0.1.0)

openal\_context\_process — Обробити вказаний контекст

### Опис

```methodsynopsis
openal_context_process(resource $context): bool
```

### Список параметрів

`context`

Ресурс[Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openal\_context\_create()](function.openal-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_context\_create()](function.openal-context-create.md) \- Створити контекст обробки звуку
-   [openal\_context\_current()](function.openal-context-current.md) \- Зробити вказаний контекст поточним
-   [openal\_context\_suspend()](function.openal-context-suspend.md) \- призупинити зазначений контекст
