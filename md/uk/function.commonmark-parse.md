---
navigation:
  - ref.cmark.md: « Функції CommonMark
  - function.commonmark-render.md: CommonMark\\Render »
  - index.md: PHP Manual
  - ref.cmark.md: Функції CommonMark
title: CommonMark\\Parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CommonMark\\Parse

(cmark >= 1.0.0)

CommonMark\\Parse - Розбір

### Опис

```methodsynopsis
CommonMark\Parse(string $content, int $options = ?): CommonMark\Node
```

Розбирає `content`

### Список параметрів

`content`

Рядок markdown

`options`

Маска з:

**`CommonMark\Parser\Normal`**(int)

**`CommonMark\Parser\Normalize`**(int)

**`CommonMark\Parser\ValidateUTF8`**(int)

**`CommonMark\Parser\Smart`**(int)

### Значення, що повертаються

Поверне кореневий (root) вузол CommonMark\\Node
