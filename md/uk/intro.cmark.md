Вступ

-   [« CommonMark](book.cmark.html)
    
-   [Установка и настройка »](cmark.setup.html)
    
-   [PHP Manual](index.html)
    
-   [CommonMark](book.cmark.html)
    
-   Вступ
    

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

Модуль CommonMark реалізує переміщення для об'єктів CommonMarkNode:

```methodsynopsis
public CommonMark\Node::accept(CommonMark\Interfaces\IVisitor $visitor): void
```

##### CQL:

Модуль CommonMark надає інтерфейс для CQL, CommonMark Query Language:

public [CommonMarkCQL::construct](commonmark-cql.construct.html)(string `$query`