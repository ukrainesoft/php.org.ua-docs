---
navigation:
  - domcomment.construct.md: '« DOMComment::\_\_construct'
  - domdocument.adoptnode.md: 'DOMDocument::adoptNode »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMDocument
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMDocument

(PHP 5, PHP 7, PHP 8)

## Вступ

Подає весь HTML- або XML-документ; корінь дерева документа.

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
      $config;

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
     ?DOMElement
      $parentElement;
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
     bool
      $isConnected;
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

    public adoptNode(DOMNode $node): DOMNode|false
public append(DOMNode|string ...$nodes): void
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
public load(string $filename, int $options = 0): bool
public loadHTML(string $source, int $options = 0): bool
public loadHTMLFile(string $filename, int $options = 0): bool
public loadXML(string $source, int $options = 0): bool
public normalizeDocument(): void
public prepend(DOMNode|string ...$nodes): void
public registerNodeClass(string $baseClass, ?string $extendedClass): bool
public relaxNGValidate(string $filename): bool
public relaxNGValidateSource(string $source): bool
public replaceChildren(DOMNode|string ...$nodes): void
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
public DOMNode::C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
public DOMNode::cloneNode(bool $deep = false): DOMNode|false
public DOMNode::contains(DOMNode|DOMNameSpaceNode|null $other): bool
public DOMNode::getLineNo(): int
public DOMNode::getNodePath(): ?string
public DOMNode::getRootNode(array $options = null): DOMNode
public DOMNode::hasAttributes(): bool
public DOMNode::hasChildNodes(): bool
public DOMNode::insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
public DOMNode::isDefaultNamespace(string $namespace): bool
public DOMNode::isEqualNode(?DOMNode $otherNode): bool
public DOMNode::isSameNode(DOMNode $otherNode): bool
public DOMNode::isSupported(string $feature, string $version): bool
public DOMNode::lookupNamespaceURI(?string $prefix): ?string
public DOMNode::lookupPrefix(string $namespace): ?string
public DOMNode::normalize(): void
public DOMNode::removeChild(DOMNode $child): DOMNode|false
public DOMNode::replaceChild(DOMNode $node, DOMNode $child): DOMNode|false

   }
```

## Властивості

actualEncoding

*Застаріло*. Кодування документа – доступний лише для читання еквівалент якості encoding.

childElementCount

Кількість дочірніх елементів.

config

*Застаріло*. Конфігурація, яка буде використана під час виклику методу [DOMDocument::normalizeDocument()](domdocument.normalizedocument.md)

doctype

Оголошення типу документа, який відповідає цьому документу.

documentElement

Об'єкт [DOMElement](class.domelement.md) - Перший елемент документа. Якщо не знайдено, оцінюється як **`null`**. Зручний атрибут, який дає прямий доступ до дочірнього вузла як елемент документа. Значення \*\*`null`\*\*якщо не існує.

documentURI

Расположение документа или\*\*`null`\*\*якщо воно не визначено.

encoding

Кодування документа, як зазначено у оголошенні XML. Цього атрибуту немає в останній специфікації DOM Level 3, але він єдиний спосіб маніпулювання кодуванням XML-документа в цій реалізації.

firstElementChild

Перший дочірній елемент або **`null`**

formatOutput

Форматує висновок, додаючи відступи та додаткові прогалини. Не працює, якщо документ був завантажений з увімкненою властивістю preservewhitespace.

implementation

Об'єкт класу [DOMImplementation](class.domimplementation.md), що обробляє цей документ.

lastElementChild

Останній дочірній елемент або **`null`**

preserveWhiteSpace

Вказівка ​​не прибирати зайві прогалини та відступи. За замовчуванням **`true`**. Встановлення цього значення **`false`** дає той самий ефект, як і передача константи **`LIBXML_NOBLANKS`** як параметр `option`в метод[DOMDocument::load()](domdocument.load.md)и т. д.

recover

*Пропрієтарна властивість*. Включає режим відновлення, тобто намагається розібрати некоректно складені документи. Цей атрибут не входить до специфікації DOM і специфічний для модуля libxml.

resolveExternals

Устанавливают в\*\*`true`\*\* для завантаження зовнішніх елементів із оголошення типу документа. Корисний при включенні елементів із символьними даними у документ XML.

standalone

*Застаріло*. Вказівка, що документ не залежить від інших документів XML, як зазначено в декларації XML, відповідає властивості xmlStandalone.

strictErrorChecking

Викидає виняток [DOMException](class.domexception.md)в случае ошибок. По умолчанию\*\*`true`\*\*

substituteEntities

*Патентована властивість*. Вказує, чи замінювати елементи документа. Цей атрибут не входить до специфікації DOM і специфічний для модуля libxml. За замовчуванням **`false`**

**Застереження**

Увімкнення підміни сутностей сприяє атакам XML External Entity (XXE).

validateOnParse

Завантажує DTD та перевіряє документ на відповідність. За замовчуванням **`false`**

**Застереження**

Увімкнення перевірки DTD сприяє атакам XML External Entity (XXE).

version

*Застаріло*. Версія XML відповідає xmlVersion.

xmlEncoding

Атрибут визначає як частину XML-оголошення кодування документа. Значення дорівнює **`null`**, якщо вона не вказана або коли значення невідоме, наприклад, коли документ було створено у пам'яті.

xmlStandalone

Атрибут визначає як частину XML-оголошення, що документ автономний. Приймає значення **`false`**, якщо не вказано.

xmlVersion

Атрибут, який визначає як частину XML-оголошення номер версії цього документа. Якщо оголошення в документі немає, але є підтримка всіх особливостей XML, значення дорівнює 1.0.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**DOMDocument** тепер реалізує інтерфейс [DOMParentNode](class.domparentnode.md) |
| 8.0.0 | Нереалізований метод \*\*DOMDocument::renameNode()\*\*був видалений. |

## Примітки

> **Зауваження** :
> 
> Модуль DOM працює з кодуванням UTF-8. Для роботи з іншими кодуваннями користуються функціями [mb\_convert\_encoding()](function.mb-convert-encoding.md) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md)

> **Зауваження** :
> 
> При использовании[json\_encode()](function.json-encode.md) для об'єкту **DOMDocument** буде отримано результат кодування порожнього об'єкта.

## Дивіться також

-   [» Специфікація W3C для інтерфейсу Document](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.md#core-i-Document)

## Зміст

-   [DOMDocument::adoptNode](domdocument.adoptnode.md)— Переносить вузол із іншого документа
-   [DOMDocument::append](domdocument.append.md)— Додає вузли після останнього дочірнього вузла
-   [DOMDocument::\_\_construct](domdocument.construct.md)— Створює новий об'єкт DOMDocument
-   [DOMDocument::createAttribute](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createAttributeNS](domdocument.createattributens.md)— Створює новий атрибут вузла із відповідним простором імен
-   [DOMDocument::createCDATASection](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElement](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS](domdocument.createelementns.md)— Створити новий вузол елемента із відповідним простором імен
-   [DOMDocument::createEntityReference](domdocument.createentityreference.md) \- Створити новий вузол посилання на сутність
-   [DOMDocument::createProcessingInstruction](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode](domdocument.createtextnode.md) \- Створити новий текстовий вузол
-   [DOMDocument::getElementById](domdocument.getelementbyid.md)— Шукає елемент із певним ідентифікатором
-   [DOMDocument::getElementsByTagName](domdocument.getelementsbytagname.md)— Шукає всі елементи із заданим локальним ім'ям
-   [DOMDocument::getElementsByTagNameNS](domdocument.getelementsbytagnamens.md)— Шукає всі елементи із заданим ім'ям у вказаному просторі імен
-   [DOMDocument::importNode](domdocument.importnode.md)— Імпортувати вузол у поточний документ
-   [DOMDocument::load](domdocument.load.md)— Завантаження XML із файлу
-   [DOMDocument::loadHTML](domdocument.loadhtml.md)— Завантаження HTML із рядка
-   [DOMDocument::loadHTMLFile](domdocument.loadhtmlfile.md)— Завантаження HTML із файлу
-   [DOMDocument::loadXML](domdocument.loadxml.md)— Завантаження XML із рядка
-   [DOMDocument::normalizeDocument](domdocument.normalizedocument.md) \- Нормалізує документ
-   [DOMDocument::prepend](domdocument.prepend.md) \- Додає вузли перед першим дочірнім вузлом
-   [DOMDocument::registerNodeClass](domdocument.registernodeclass.md)— Реєстрація розширеного класу, який використовується для створення типу базового вузла
-   [DOMDocument::relaxNGValidate](domdocument.relaxngvalidate.md) \- Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource](domdocument.relaxngvalidatesource.md) \- Перевіряє документ за допомогою relaxNG
-   [DOMDocument::replaceChildren](domdocument.replacechildren.md)— Замінює дочірні вузли у документі
-   [DOMDocument::save](domdocument.save.md)— Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveHTML](domdocument.savehtml.md)— Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
-   [DOMDocument::saveHTMLFile](domdocument.savehtmlfile.md)— Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML
-   [DOMDocument::saveXML](domdocument.savexml.md)— Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
-   [DOMDocument::schemaValidate](domdocument.schemavalidate.md)— Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::schemaValidateSource](domdocument.schemavalidatesource.md)— Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::validate](domdocument.validate.md)— Перевіряє документ на відповідність його DTD
-   [DOMDocument::xinclude](domdocument.xinclude.md)— Вставляє XInclude в об'єкті DOMDocument.
