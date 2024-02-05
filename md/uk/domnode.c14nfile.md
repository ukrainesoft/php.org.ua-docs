---
navigation:
  - domnode.c14n.md: '« DOMNode::C14N'
  - domnode.clonenode.md: 'DOMNode::cloneNode »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::C14NFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::C14NFile

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DOMNode::C14NFile — Канонізувати вузли у файл

### Опис

```methodsynopsis
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
```

Канонізувати вузли у файл.

### Список параметрів

`uri`

Шлях для запису виводу.

`exclusive`

Включити ексклюзивний розбір лише тих вузлів, які збігаються з наданими xpath або ns\_prefixes.

`withComments`

Зберігати коментарі у висновку.

`xpath`

Массив`xpath` для фільтрації вузлів.

`nsPrefixes`

Масив префіксів просторів імен фільтрації вузлів.

### Значення, що повертаються

Кількість записаних байт або \*\*`false`\*\*в случае возникновения ошибки

### Дивіться також

-   [DOMNode::C14N()](domnode.c14n.md) \- Канонізувати вузли в рядок
