---
navigation:
  - xmlreader.resources.md: « Типи ресурсів
  - xmlreader.close.md: 'XMLReader::close »'
  - index.md: PHP Manual
  - book.xmlreader.md: XMLReader
title: Клас XMLReader
---
# Клас XMLReader

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Модуль XMLReader – синтаксичний аналізатор XML. Клас-читач виступає як курсор, слід по потоку документа і зупиняється кожному вузлі цьому шляху.

## Огляд класів

```classsynopsis

     
    

    
     
      class XMLReader
     
     {

    /* Константы */

     
      const
      int
       NONE = 0;

     const
      int
       ELEMENT = 1;

     const
      int
       ATTRIBUTE = 2;

     const
      int
       TEXT = 3;

     const
      int
       CDATA = 4;

     const
      int
       ENTITY_REF = 5;

     const
      int
       ENTITY = 6;

     const
      int
       PI = 7;

     const
      int
       COMMENT = 8;

     const
      int
       DOC = 9;

     const
      int
       DOC_TYPE = 10;

     const
      int
       DOC_FRAGMENT = 11;

     const
      int
       NOTATION = 12;

     const
      int
       WHITESPACE = 13;

     const
      int
       SIGNIFICANT_WHITESPACE = 14;

     const
      int
       END_ELEMENT = 15;

     const
      int
       END_ENTITY = 16;

     const
      int
       XML_DECLARATION = 17;

     const
      int
       LOADDTD = 1;

     const
      int
       DEFAULTATTRS = 2;

     const
      int
       VALIDATE = 3;

     const
      int
       SUBST_ENTITIES = 4;



    /* Свойства */
    public
     int
      $attributeCount;

    public
     string
      $baseURI;

    public
     int
      $depth;

    public
     bool
      $hasAttributes;

    public
     bool
      $hasValue;

    public
     bool
      $isDefault;

    public
     bool
      $isEmptyElement;

    public
     string
      $localName;

    public
     string
      $name;

    public
     string
      $namespaceURI;

    public
     int
      $nodeType;

    public
     string
      $prefix;

    public
     string
      $value;

    public
     string
      $xmlLang;


    /* Методы */
    
   public close(): bool
public expand(?DOMNode $baseNode = null): DOMNode|false
public getAttribute(string $name): ?string
public getAttributeNo(int $index): ?string
public getAttributeNs(string $name, string $namespace): ?string
public getParserProperty(int $property): bool
public isValid(): bool
public lookupNamespace(string $prefix): ?string
public
   moveToAttribute(string $name): bool
public
   moveToAttributeNo(int $index): bool
public moveToAttributeNs(string $name, string $namespace): bool
public moveToElement(): bool
public moveToFirstAttribute(): bool
public moveToNextAttribute(): bool
public next(?string $name = null): bool
public static open(string $uri, ?string $encoding = null, int $flags = 0): bool|XMLReader
public read(): bool
public readInnerXml(): string
public readOuterXml(): string
public readString(): string
public
   setParserProperty(int $property, bool $value): bool
public setRelaxNGSchema(?string $filename): bool
public setRelaxNGSchemaSource(?string $source): bool
public setSchema(?string $filename): bool
public static XML(string $source, ?string $encoding = null, int $flags = 0): bool|XMLReader

   }
```

## Властивості

attributeCount

Кількість атрибутів у вузлі

baseURI

Базовий URI вузла

depth

Глибина вузла в дереві, починаючи з 0

haSattributes

Показує, чи є у вузла атрибути

hasValue

Показує, чи має вузол текстове значення

isDefault

Показує, чи є стандартним атрибутом з DTD

isEmptyElement

Показує, чи є вузол порожнім тегом

localName

Локальне ім'я вузла

name

Повністю певне ім'я вузла

namespaceURI

URI простору імен пов'язаний з вузлом

nodeType

Тип вузла

prefix

Префікс простору імен пов'язаний із вузлом

value

Текстове значення вузла

xmlLang

Контекст xml:lang, де знаходиться вузол

## Обумовлені константи

## Типи вузлів XMLReader

**`XMLReader::NONE`**

Немає типу вузла

**`XMLReader::ELEMENT`**

Початковий елемент

**`XMLReader::ATTRIBUTE`**

Вузол атрибуту

**`XMLReader::TEXT`**

Текстовий вузол

**`XMLReader::CDATA`**

Вузол CDATA

**`XMLReader::ENTITY_REF`**

Вузол посилання на сутність

**`XMLReader::ENTITY`**

Вузол оголошення об'єкту

**`XMLReader::PI`**

Вузол інструкцій обробки

**`XMLReader::COMMENT`**

Вузол коментаря

**`XMLReader::DOC`**

Вузол документа

**`XMLReader::DOC_TYPE`**

Вузол типу документа

**`XMLReader::DOC_FRAGMENT`**

Вузол фрагмента документа

**`XMLReader::NOTATION`**

Вузол нотації

**`XMLReader::WHITESPACE`**

Пробільний вузол

**`XMLReader::SIGNIFICANT_WHITESPACE`**

Істотний пробільний вузол

**`XMLReader::END_ELEMENT`**

Завершення елемента

**`XMLReader::END_ENTITY`**

Завершення об'єкту

**`XMLReader::XML_DECLARATION`**

Вузол XML оголошення

## Опції аналізатора XMLReader

**`XMLReader::LOADDTD`**

Завантажувати DTD, але не перевіряти

**`XMLReader::DEFAULTATTRS`**

Завантажувати DTD та атрибути за замовчуванням, але не перевіряти

**`XMLReader::VALIDATE`**

Завантажувати DTD і перевіряти під час аналізу

**`XMLReader::SUBST_ENTITIES`**

Замінювати об'єкти та розгортати посилання

## Зміст

-   [XMLReader::close](xmlreader.close.md) — Закрити введення XMLReader
-   [XMLReader::expand](xmlreader.expand.md) — Повернути копію поточного вузла як об'єкт DOM
-   [XMLReader::getAttribute](xmlreader.getattribute.md) — Отримати значення атрибуту з певним ім'ям
-   [XMLReader::getAttributeNo](xmlreader.getattributeno.md) — Отримати значення атрибуту за індексом
-   [XMLReader::getAttributeNs](xmlreader.getattributens.md) — Отримати значення атрибуту по localname та URI
-   [XMLReader::getParserProperty](xmlreader.getparserproperty.md) — Вказує, чи була певна властивість встановлена
-   [XMLReader::isValid](xmlreader.isvalid.md) — Показати, чи розбирається документ синтаксично правильним
-   [XMLReader::lookupNamespace](xmlreader.lookupnamespace.md) - Знайти простір імен для префікса
-   [XMLReader::moveToAttribute](xmlreader.movetoattribute.md) — Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::moveToAttributeNo](xmlreader.movetoattributeno.md) — Перемістити курсор на атрибут за індексом
-   [XMLReader::moveToAttributeNs](xmlreader.movetoattributens.md) — Перемістити курсор до іменованого атрибуту
-   [XMLReader::moveToElement](xmlreader.movetoelement.md) — Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToFirstAttribute](xmlreader.movetofirstattribute.md) — Перемістити позицію курсору на перший атрибут
-   [XMLReader::moveToNextAttribute](xmlreader.movetonextattribute.md) — Перемістити позицію курсору на наступний атрибут
-   [XMLReader::next](xmlreader.next.md) — Перемістити курсор на наступний вузол, пропускаючи всі дерева.
-   [XMLReader::open](xmlreader.open.md) — Встановити URI, що містить XML-документ для аналізу
-   [XMLReader::read](xmlreader.read.md) — Переміститися до наступного сайту в документі
-   [XMLReader::readInnerXml](xmlreader.readinnerxml.md) — Вийняти XML із поточного вузла
-   [XMLReader::readOuterXml](xmlreader.readouterxml.md) — Отримати XML із поточного вузла, включаючи сам вузол
-   [XMLReader::readString](xmlreader.readstring.md) — Прочитати вміст поточного вузла як рядок
-   [XMLReader::setParserProperty](xmlreader.setparserproperty.md) - Встановлює опцію парсера
-   [XMLReader::setRelaxNGSchema](xmlreader.setrelaxngschema.md) — Встановити ім'я файлу або URI для схеми RelaxNG
-   [XMLReader::setRelaxNGSchemaSource](xmlreader.setrelaxngschemasource.md) - Встановлює дані, що містять схему RelaxNG
-   [XMLReader::setSchema](xmlreader.setschema.md) — Перевірити документ за допомогою XSD
-   [XMLReader::XML](xmlreader.xml.md) — Встановити дані, що містять XML для аналізу
