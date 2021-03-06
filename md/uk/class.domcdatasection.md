- [« DOMAttr::isId](domattr.isid.md)
- [DOMCdataSection::\_\_construct »](domcdatasection.construct.md)

- [PHP Manual](index.md)
- [DOM](book.dom.md)
- Клас DOMCdataSection

# Клас DOMCdataSection

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **DOMCdataSection** успадковується від [DOMText](class.domtext.md)
для текстового представлення конструкцій CData

## Огляд класів

class **DOMCdataSection** extends [DOMText](class.domtext.md) {

/\* Наслідувані властивості \*/

public readonly string `$wholeText`;

public string `$data`;

public readonly int `$length`;

public readonly ?[DOMElement](class.domelement.md)
`$previousElementSibling`;

public readonly ?[DOMElement](class.domelement.md)
`$nextElementSibling`;

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

public [\_\_construct](domcdatasection.construct.md)(string `$data`)

/\* Наслідувані методи \*/

public
[DOMText::isElementContentWhitespace](domtext.iselementcontentwhitespace.md)():
bool

public
[DOMText::isWhitespaceInElementContent](domtext.iswhitespaceinelementcontent.md)():
bool

public [DOMText::splitText](domtext.splittext.md)(int `$offset`):
[DOMText](class.domtext.md)\|false

public
[DOMCharacterData::appendData](domcharacterdata.appenddata.md)(string
`$data`): bool

public
[DOMCharacterData::deleteData](domcharacterdata.deletedata.md)(int
`$offset`, int `$count`): bool

public
[DOMCharacterData::insertData](domcharacterdata.insertdata.md)(int
`$offset`, string `$data`): bool

public
[DOMCharacterData::replaceData](domcharacterdata.replacedata.md)(int
`$offset`, int `$count`, string `$data`): bool

public
[DOMCharacterData::substringData](domcharacterdata.substringdata.md)(int
`$offset`, int `$count`): string\|false

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

## Зміст

- [DOMCdataSection::\_\_construct](domcdatasection.construct.md) -
Створює новий екземпляр класу DOMCdataSection
