---
navigation:
  - domimplementation.construct.md: '« DOMImplementation::\_\_construct'
  - domimplementation.createdocumenttype.md: 'DOMImplementation::createDocumentType »'
  - index.md: PHP Manual
  - class.domimplementation.md: DOMImplementation
title: 'DOMImplementation::createDocument'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMImplementation::createDocument

(PHP 5, PHP 7, PHP 8)

DOMImplementation::createDocument — Створює об'єкт класу DOMDocument заданого типу з його елементом.

### Опис

```methodsynopsis
public DOMImplementation::createDocument(?string $namespace = null, string $qualifiedName = "", ?DOMDocumentType $doctype = null): DOMDocument|false
```

Створює об'єкт класу [DOMDocument](class.domdocument.md) заданого типу із його елементом document.

### Список параметрів

`namespace`

URI простору імен створюваного елемента document.

`qualifiedName`

Кваліфіковане ім'я елемента document, що створюється.

`doctype`

Тип створюваного елемента document або **`null`**

### Значення, що повертаються

Новий об'єкт класу [DOMDocument](class.domdocument.md)или\*\*`false`\*\* у разі виникнення помилки. Якщо аргументи `namespace` `qualifiedName`, и`doctype` мають значення null, об'єкт, що повертається [DOMDocument](class.domdocument.md) буде порожнім та без елемента document.

### Помилки

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо аргумент `doctype` вже використовувався з іншим документом або було створено в іншій реалізації.

**`DOM_NAMESPACE_ERR`**

Виникає, якщо виявлена ​​помилка у рядках `namespace`и`qualifiedName`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.3 | `namespace` тепер допускає значення null. |
| 8.0.0 | `doctype` тепер допускає значення null. |
| 8.0.0 | При статичному виклику функції тепер викидається помилка [Error](class.error.md). . Раніше видавалася помилка рівня **`E_DEPRECATED`** |

### Дивіться також

-   [DOMDocument::\_\_construct()](domdocument.construct.md) \- Створює новий об'єкт DOMDocument
-   [DOMImplementation::createDocumentType()](domimplementation.createdocumenttype.md) \- Створює порожній об'єкт класу DOMDocumentType
