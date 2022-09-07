---
navigation:
  - function.commonmark-parse.md: « CommonMarkParse
  - function.commonmark-render-html.md: CommonMarkRenderHTML »
  - index.md: PHP Manual
  - ref.cmark.md: Функции CommonMark
title: CommonMarkRender
---
# CommonMarkRender

(cmark >= 1.0.0)

CommonMarkRender — Відображення

### Опис

```methodsynopsis
CommonMark\Render(CommonMark\Node $node, int $options = ?, int $width = ?): string
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`node`

`options`

Маска з:

**`CommonMark\Render\Normal`** (int)

**`CommonMark\Render\SourcePos`** (int)

**`CommonMark\Render\HardBreaks`** (int)

**`CommonMark\Render\Safe`** (int)

**`CommonMark\Render\NoBreaks`** (int)

`width`

### Значення, що повертаються
