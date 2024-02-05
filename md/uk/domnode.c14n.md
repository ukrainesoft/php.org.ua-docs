---
navigation:
  - domnode.appendchild.md: '« DOMNode::appendChild'
  - domnode.c14nfile.md: 'DOMNode::C14NFile »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::C14N'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::C14N

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DOMNode::C14N — Канонізувати вузли в рядок

### Опис

```methodsynopsis
public DOMNode::C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
```

Канонізувати вузли в рядок

### Список параметрів

`exclusive`

Включити ексклюзивний розбір лише тих вузлів, які збігаються з наданими xpath або ns\_prefixes.

`withComments`

Зберігати коментарі у висновку.

`xpath`

Массив`xpath` для фільтрації вузлів.

`nsPrefixes`

Масив префіксів просторів імен фільтрації вузлів.

### Значення, що повертаються

Повертає канонізовані вузли у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки

### Дивіться також

-   [DOMNode::C14NFile()](domnode.c14nfile.md) \- Канонізувати вузли у файл
