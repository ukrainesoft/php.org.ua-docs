- [«CommonMark\Node\Item](class.commonmark-node-item.md)
- [CommonMark\Node\Text::\_\_construct »](commonmark-node-text.construct.md)

- [PHP Manual](index.md)
- [CommonMark](book.cmark.md)
- Text успадковує CommonMark\Node

# Text успадковує CommonMark\Node

(cmark \>= 1.0.0)

## Огляд класів

final class **CommonMark\Node\Text** extends
[CommonMark\Node](class.commonmark-node.md) implements
[CommonMark\Interfaces\IVisitable](class.commonmark-interfaces-ivisitable.md),
[Traversable](class.traversable.md) {

/\* Наслідувані властивості \*/

public readonly ?Node `$parent`;

public readonly ?Node `$previous`;

public readonly ?Node `$next`;

public readonly ?Node `$lastChild`;

public readonly ?Node `$firstChild`;

public readonly int `$startLine`;

public readonly int `$endLine`;

public readonly int `$startColumn`;

public readonly int `$endColumn`;

/\* Властивості \*/

public ?string `$literal`;

/\* Конструктор \*/

public [\_\_construct](commonmark-node-text.construct.md)()

public [\_\_construct](commonmark-node-text.construct.md)(string
`$literal`)

/\* Наслідувані методи \*/

public
[CommonMark\Node::appendChild](commonmark-node.appendchild.md)([CommonMark\Node](class.commonmark-node.md)
`$child`): [CommonMark\Node](class.commonmark-node.md)

public
[CommonMark\Node::prependChild](commonmark-node.prependchild.md)([CommonMark\Node](class.commonmark-node.md)
`$child`): [CommonMark\Node](class.commonmark-node.md)

public
[CommonMark\Node::insertAfter](commonmark-node.insertafter.md)([CommonMark\Node](class.commonmark-node.md)
`$sibling`): [CommonMark\Node](class.commonmark-node.md)

public
[CommonMark\Node::insertBefore](commonmark-node.insertbefore.md)([CommonMark\Node](class.commonmark-node.md)
`$sibling`): [CommonMark\Node](class.commonmark-node.md)

public
[CommonMark\Node::replace](commonmark-node.replace.md)([CommonMark\Node](class.commonmark-node.md)
`$target`): [CommonMark\Node](class.commonmark-node.md)

public [CommonMark\Node::unlink](commonmark-node.unlink.md)(): void

public
[CommonMark\Node::accept](commonmark-node.accept.md)([CommonMark\Interfaces\IVisitor](class.commonmark-interfaces-ivisitor.md)
`$visitor`): void

}

## Зміст

- [CommonMark\Node\Text::\_\_construct](commonmark-node-text.construct.md)
- Конструктор класу Text
