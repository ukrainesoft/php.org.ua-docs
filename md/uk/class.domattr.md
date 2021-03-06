- [« Приклади](dom.examples.md)
- [DOMAttr::\_\_construct »](domattr.construct.md)

- [PHP Manual](index.md)
- [DOM](book.dom.md)
- Клас DOMAttr

# Клас [DOMAttr](class.domattr.md)

(PHP 5, PHP 7, PHP 8)

## Вступ

**DOMAttr** надає атрибут в об'єкті
[DOMElement](class.domelement.md).

## Огляд класів

class **DOMAttr** extends [DOMNode](class.domnode.md) {

/\* Властивості \*/

public readonly string `$name`;

public readonly bool `$specified` = true;

public string `$value`;

public readonly ?[DOMElement](class.domelement.md) `$ownerElement`;

public readonly
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$schemaTypeInfo` = null;

/\* Наслідувані властивості \*/

public readonly string `$nodeName`;

public ?string `$nodeValue`;

public readonly int `$nodeType`;

public readonly ?[DOMNode](class.domnode.md) `$parentNode`;

public readonly [DOMNodeList](class.domnodelist.md) `$childNodes`;

public readonly ?[DOMNode](class.domnode.md) `$firstChild`;

public readonly ?[DOMNode](class.domnode.md) `$lastChild`;

public readonly ?[DOMNode](class.domnode.md) `$previousSibling`;

public readonly ?[DOMNode](class.domnode.md) `$nextSibling`;

public readonly ?[DOMNamedNodeMap](class.domnamednodemap.md)
`$attributes`;

public readonly ?[DOMDocument](class.domdocument.md) `$ownerDocument`;

public readonly ?string `$namespaceURI`;

public string `$prefix`;

public readonly ?string `$localName`;

public readonly ?string `$baseURI`;

public string `$textContent`;

/\* Методи \*/

public [\_\_construct](domattr.construct.md)(string `$name`, string
`$value` = "")

public [isId](domattr.isid.md)(): bool

/\* Наслідувані методи \*/

public
[DOMNode::appendChild](domnode.appendchild.md)([DOMNode](class.domnode.md)
`$node`): [DOMNode](class.domnode.md)\|false

public [DOMNode::C14N](domnode.c14n.md)(
bool `$exclusive` = **`false`**,
bool `$withComments` = **`false`**,
?array `$xpath` = **`null`**,
?array `$nsPrefixes` = **`null`**
): string\|false

public [DOMNode::C14NFile](domnode.c14nfile.md)(
string `$uri`,
bool `$exclusive` = **`false`**,
bool `$withComments` = **`false`**,
?array `$xpath` = **`null`**,
?array `$nsPrefixes` = **`null`**
): int\|false

public [DOMNode::cloneNode](domnode.clonenode.md)(bool `$deep` =
**`false`**): [DOMNode](class.domnode.md)\|false

public [DOMNode::getLineNo](domnode.getlineno.md)(): int

public [DOMNode::getNodePath](domnode.getnodepath.md)(): ?string

public [DOMNode::hasAttributes](domnode.hasattributes.md)(): bool

public [DOMNode::hasChildNodes](domnode.haschildnodes.md)(): bool

public
[DOMNode::insertBefore](domnode.insertbefore.md)([DOMNode](class.domnode.md)
`$node`, ?[DOMNode](class.domnode.md) `$child` = **`null`**):
[DOMNode](class.domnode.md)\|false

public
[DOMNode::isDefaultNamespace](domnode.isdefaultnamespace.md)(string
`$namespace`): bool

public
[DOMNode::isSameNode](domnode.issamenode.md)([DOMNode](class.domnode.md)
`$otherNode`): bool

public [DOMNode::isSupported](domnode.issupported.md)(string
`$feature`, string `$version`): bool

public
[DOMNode::lookupNamespaceUri](domnode.lookupnamespaceuri.md)(string
`$prefix`): string

public [DOMNode::lookupPrefix](domnode.lookupprefix.md)(string
`$namespace`): ?string

public [DOMNode::normalize](domnode.normalize.md)(): void

public
[DOMNode::removeChild](domnode.removechild.md)([DOMNode](class.domnode.md)
`$child`): [DOMNode](class.domnode.md)\|false

public
[DOMNode::replaceChild](domnode.replacechild.md)([DOMNode](class.domnode.md)
`$node`, [DOMNode](class.domnode.md) `$child`):
[DOMNode](class.domnode.md)\|false

}

## Властивості

`name`
Назва атрибута.

`ownerElement`
Елемент, який містить атрибут або **`null`**.

`schemaTypeInfo`
Ще не реалізовано, повертає **`null`**.

`specified`
Ще не реалізовано, повертає **`null`**.

`value`
Значення атрибуту.

## Дивіться також

- [» Специфікація W3C для Attr](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.md#core-ID-637646024)

## Зміст

- [DOMAttr::\_\_construct](domattr.construct.md) - Створює екземпляр
класу DOMAttr
- [DOMAttr::isId](domattr.isid.md) — Перевіряє, чи є атрибут
певним ідентифікатором
