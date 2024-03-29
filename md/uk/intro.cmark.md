---
navigation:
  - book.cmark.md: « CommonMark
  - cmark.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Модуль надає доступ до еталонної реалізації CommonMark, раціоналізованої версії синтаксису Markdown із специфікацією.

##### Розбір:

Модуль CommonMark надає простий API синтаксичного аналізу:

```methodsynopsis
CommonMark\Parse(string $content, int $options = ?): CommonMark\Node
```

##### Відображення:

Модуль CommonMark надає простий API відображення, який підтримує декілька форматів:

```methodsynopsis
CommonMark\Render(CommonMark\Node $node, int $options = ?, int $width = ?): string
```

```methodsynopsis
CommonMark\Render\HTML(CommonMark\Node $node, int $options = ?): string
```

```methodsynopsis
CommonMark\Render\XML(CommonMark\Node $node, int $options = ?): string
```

```methodsynopsis
CommonMark\Render\Man(CommonMark\Node $node, int $options = ?, int $width = ?): string
```

```methodsynopsis
CommonMark\Render\Latex(CommonMark\Node $node, int $options = ?, int $width = ?): string
```

##### AST:

Модуль CommonMark реалізує переміщення для об'єктів CommonMark\\Node:

```methodsynopsis
public CommonMark\Node::accept(CommonMark\Interfaces\IVisitor $visitor): void
```

##### CQL:

Модуль CommonMark надає інтерфейс для CQL, CommonMark Query Language:

public[CommonMark\\CQL::\_\_construct](commonmark-cql.construct.md)(string`$query`) .
