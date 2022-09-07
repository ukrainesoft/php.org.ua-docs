---
navigation:
  - domcomment.construct.md: '« DOMComment::construct'
  - domdocument.construct.md: 'DOMDocument::construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMDocument
---
# Клас DOMDocument

(PHP 5, PHP 7, PHP 8)

## Вступ

Надає весь вміст HTML- або XML-документа; служить коренем дерева документа.

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMDocument
     

     
      extends
       DOMNode
     

     implements 
       DOMParentNode {

    /* Свойства */
    
     public
     readonly
     ?DOMDocumentType
      $doctype;

    public
     readonly
     DOMImplementation
      $implementation;

    public
     readonly
     ?DOMElement
      $documentElement;

    public
     readonly
     ?string
      $actualEncoding;

    public
     ?string
      $encoding;

    public
     readonly
     ?string
      $xmlEncoding;

    public
     bool
      $standalone;

    public
     bool
      $xmlStandalone;

    public
     ?string
      $version;

    public
     ?string
      $xmlVersion;

    public
     bool
      $strictErrorChecking;

    public
     ?string
      $documentURI;

    public
     readonly
     mixed
      $config = null;

    public
     bool
      $formatOutput;

    public
     bool
      $validateOnParse;

    public
     bool
      $resolveExternals;

    public
     bool
      $preserveWhiteSpace;

    public
     bool
      $recover;

    public
     bool
      $substituteEntities;

    public
     readonly
     ?DOMElement
      $firstElementChild;

    public
     readonly
     ?DOMElement
      $lastElementChild;

    public
     readonly
     int
      $childElementCount;


    /* Наследуемые свойства */
    public
     readonly
     string
      $nodeName;
public
     ?string
      $nodeValue;
public
     readonly
     int
      $nodeType;
public
     readonly
     ?DOMNode
      $parentNode;
public
     readonly
     DOMNodeList
      $childNodes;
public
     readonly
     ?DOMNode
      $firstChild;
public
     readonly
     ?DOMNode
      $lastChild;
public
     readonly
     ?DOMNode
      $previousSibling;
public
     readonly
     ?DOMNode
      $nextSibling;
public
     readonly
     ?DOMNamedNodeMap
      $attributes;
public
     readonly
     ?DOMDocument
      $ownerDocument;
public
     readonly
     ?string
      $namespaceURI;
public
     string
      $prefix;
public
     readonly
     ?string
      $localName;
public
     readonly
     ?string
      $baseURI;
public
     string
      $textContent;


    /* Методы */
    
   public __construct(string $version = "1.0", string $encoding = "")

    public createAttribute(string $localName): DOMAttr|false
public createAttributeNS(?string $namespace, string $qualifiedName): DOMAttr|false
public createCDATASection(string $data): DOMCdataSection|false
public createComment(string $data): DOMComment
public createDocumentFragment(): DOMDocumentFragment
public createElement(string $localName, string $value = ""): DOMElement|false
public createElementNS(?string $namespace, string $qualifiedName, string $value = ""): DOMElement|false
public createEntityReference(string $name): DOMEntityReference|false
public createProcessingInstruction(string $target, string $data = ""): DOMProcessingInstruction|false
public createTextNode(string $data): DOMText
public getElementById(string $elementId): ?DOMElement
public getElementsByTagName(string $qualifiedName): DOMNodeList
public getElementsByTagNameNS(?string $namespace, string $localName): DOMNodeList
public importNode(DOMNode $node, bool $deep = false): DOMNode|false
public load(string $filename, int $options = 0): DOMDocument|bool
public loadHTML(string $source, int $options = 0): DOMDocument|bool
public loadHTMLFile(string $filename, int $options = 0): DOMDocument|bool
public loadXML(string $source, int $options = 0): DOMDocument|bool
public normalizeDocument(): void
public registerNodeClass(string $baseClass, ?string $extendedClass): bool
public relaxNGValidate(string $filename): bool
public relaxNGValidateSource(string $source): bool
public save(string $filename, int $options = 0): int|false
public saveHTML(?DOMNode $node = null): string|false
public saveHTMLFile(string $filename): int|false
public saveXML(?DOMNode $node = null, int $options = 0): string|false
public schemaValidate(string $filename, int $flags = 0): bool
public schemaValidateSource(string $source, int $flags = 0): bool
public validate(): bool
public xinclude(int $options = 0): int|false


    /* Наследуемые методы */
    public DOMNode::appendChild(DOMNode $node): DOMNode|false
public DOMNode::C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
public DOMNode::cloneNode(bool $deep = false): DOMNode|false
public DOMNode::getLineNo(): int
public DOMNode::getNodePath(): ?string
public DOMNode::hasAttributes(): bool
public DOMNode::hasChildNodes(): bool
public DOMNode::insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
public DOMNode::isDefaultNamespace(string $namespace): bool
public DOMNode::isSameNode(DOMNode $otherNode): bool
public DOMNode::isSupported(string $feature, string $version): bool
public DOMNode::lookupNamespaceUri(string $prefix): string
public DOMNode::lookupPrefix(string $namespace): ?string
public DOMNode::normalize(): void
public DOMNode::removeChild(DOMNode $child): DOMNode|false
public DOMNode::replaceChild(DOMNode $node, DOMNode $child): DOMNode|false

   }
```

## Властивості

actualEncoding

*Застаріло*. Кодування документа є доступним тільки для читання еквівалентом encoding.

childElementCount

Кількість дочірніх елементів.

config

*Застаріло*. Конфігурація, яка використовується під час виклику [DOMDocument::normalizeDocument()](domdocument.normalizedocument.md)

doctype

Оголошення типу документа, що відповідає цьому документу.

documentElement

Об'єкт [DOMElement](class.domelement.md)який є першим елементом документа. Якщо не знайдено, оцінюється як **`null`**. Зручний атрибут, що надає прямий доступ до дочірнього вузла як елемент документа . \*\*`null`\*\*якщо не існує.

documentURI

Розташування документа або \*\*`null`\*\*якщо воно не визначено.

encoding

Кодування документа, як зазначено у оголошенні XML. Цей атрибут відсутній в останній специфікації DOM Level 3, але єдиний спосіб маніпулювання кодуванням XML-документа в цій реалізації.

першийЕlementChild

Перший дочірній елемент або **`null`**

formatOutput

Форматує висновок, додаючи відступи та додаткові прогалини. Не працює, якщо документ був завантажений з увімкненим параметром preserveWhitespace.

implementation

Об'єкт класу [DOMImplementation](class.domimplementation.md), що обробляє цей документ.

останнійеlementChild

Останній дочірній елемент або **`null`**

preserveWhiteSpace

Вказівка ​​не прибирати зайві прогалини та відступи. За замовчуванням **`true`**. Встановлення цього значення на **`false`** має той самий ефект, що і передача **`LIBXML_NOBLANKS`** в якості `option` в [DOMDocument::load()](domdocument.load.md) і т.д.

recover

*Пропрієтарна властивість*. Включає режим відновлення, тобто намагається розібрати некоректно складені документи. Цей атрибут не є частиною специфікації DOM і є специфічним для libxml.

resolveExternals

Встановіть у **`true`** для завантаження зовнішніх елементів із оголошення типу документа. Може бути корисним при включенні елементів із символьними даними у документ XML.

standalone

*Застаріло*. Вказує, що документ не залежить від інших документів XML. Це можна визначити з оголошення XML. Властивість пов'язана з xmlStandalone.

strictErrorChecking

Викидає виняток [DOMException](class.domexception.md) у разі виникнення помилок. За замовчуванням **`true`**

substituteEntities

*Патентована властивість*. Вказує, чи замінювати елементи документа. Цей атрибут не є частиною специфікації DOM і є специфічним для libxml.

**Застереження**

Увімкнення заміщення об'єкта може полегшити атаки на зовнішній об'єкт XML (XXE).

validateOnParse

Завантажує DTD та перевіряє документ на відповідність. За замовчуванням **`false`**

version

*Застаріло*. Версія XML відповідає xmlVersion.

xmlEncoding

Атрибут, що визначає, як частина XML-оголошення, кодування цього документа. Має значення **`null`** у разі, коли атрибут не заданий, або значення невідоме, якщо, наприклад, документ створено пам'яті.

xmlStandalone

Атрибут визначає як частину XML-оголошення, що документ є автономним. Приймає значення **`false`**, якщо не вказано.

xmlVersion

Атрибут, який визначає, як частину XML-оголошення, номер версії цього документа. Якщо оголошення немає, але є підтримка всіх особливостей "XML", значення дорівнює "1.0".

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **DOMDocument** тепер реалізує інтерфейс [DOMParentNode](class.domparentnode.md) |
|  | Нереалізований метод **DOMDocument::renameNode()** був видалений. |

## Примітки

> **Зауваження**
> 
> Модуль DOM використовує кодування UTF-8. Використовуйте [мбconvertencoding()](function.mb-convert-encoding.md) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md) для роботи з іншими кодуванням.

> **Зауваження**
> 
> При використанні [jsonencode()](function.json-encode.md) для об'єкту **DOMDocument** буде отримано результат кодування порожнього об'єкта.

## Дивіться також

-   [» Спецификация W3C для Document](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.md#core-i-Document)

## Зміст

-   [DOMDocument::construct](domdocument.construct.md) — Створює новий об'єкт DOMDocument
-   [DOMDocument::createAttribute](domdocument.createattribute.md) - Створити новий атрибут
-   [DOMDocument::createAttributeNS](domdocument.createattributens.md) — Створює новий атрибут вузла із відповідним простором імен
-   [DOMDocument::createCDATASection](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createComment](domdocument.createcomment.md) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment](domdocument.createdocumentfragment.md) - Створити новий фрагмент документа
-   [DOMDocument::createElement](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createElementNS](domdocument.createelementns.md) — Створити новий вузол елемента із відповідним простором імен
-   [DOMDocument::createEntityReference](domdocument.createentityreference.md) - Створити новий вузол посилання на сутність
-   [DOMDocument::createProcessingInstruction](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode](domdocument.createtextnode.md) - Створити новий текстовий вузол
-   [DOMDocument::getElementById](domdocument.getelementbyid.md) — Шукає елемент із певним ідентифікатором
-   [DOMDocument::getElementsByTagName](domdocument.getelementsbytagname.md) — Шукає всі елементи із заданим локальним ім'ям
-   [DOMDocument::getElementsByTagNameNS](domdocument.getelementsbytagnamens.md) — Шукає всі елементи із заданим ім'ям у вказаному просторі імен
-   [DOMDocument::importNode](domdocument.importnode.md) — Імпортувати вузол у поточний документ
-   [DOMDocument::load](domdocument.load.md) — Завантаження XML із файлу
-   [DOMDocument::loadHTML](domdocument.loadhtml.md) — Завантаження HTML із рядка
-   [DOMDocument::loadHTMLFile](domdocument.loadhtmlfile.md) — Завантаження HTML із файлу
-   [DOMDocument::loadXML](domdocument.loadxml.md) — Завантаження XML із рядка
-   [DOMDocument::normalizeDocument](domdocument.normalizedocument.md) - Нормалізує документ
-   [DOMDocument::registerNodeClass](domdocument.registernodeclass.md) — Реєстрація розширеного класу, який використовується для створення типу базового вузла
-   [DOMDocument::relaxNGValidate](domdocument.relaxngvalidate.md) - Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource](domdocument.relaxngvalidatesource.md) - Перевіряє документ за допомогою relaxNG
-   [DOMDocument::save](domdocument.save.md) — Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveHTML](domdocument.savehtml.md) — Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
-   [DOMDocument::saveHTMLFile](domdocument.savehtmlfile.md) — Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML
-   [DOMDocument::saveXML](domdocument.savexml.md) — Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
-   [DOMDocument::schemaValidate](domdocument.schemavalidate.md) — Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::schemaValidateSource](domdocument.schemavalidatesource.md) — Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::validate](domdocument.validate.md) — Перевіряє документ на відповідність його DTD
-   [DOMDocument::xinclude](domdocument.xinclude.md) — Вставляє XInclude в об'єкті DOMDocument.
