---
navigation:
  - function.openal-source-create.md: « openal\_source\_create
  - function.openal-source-get.md: openal\_source\_get »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_source\_destroy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_source\_destroy

(PECL openal >= 0.1.0)

openal\_source\_destroy - Знищення ресурсу джерела

### Опис

```methodsynopsis
openal_source_destroy(resource $source): bool
```

### Список параметрів

`source`

Ресурс[Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openal\_source\_create()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_source\_create()](function.openal-source-create.md) \- Згенерувати джерело ресурсу
