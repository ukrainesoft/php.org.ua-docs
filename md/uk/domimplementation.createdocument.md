---
navigation:
  - domimplementation.construct.md: '« DOMImplementation::construct'
  - domimplementation.createdocumenttype.md: 'DOMImplementation::createDocumentType »'
  - index.md: PHP Manual
  - class.domimplementation.md: DOMImplementation
title: 'DOMImplementation::createDocument'
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

Новий об'єкт класу [DOMDocument](class.domdocument.md). Якщо аргументи `namespace` `qualifiedName`, і `doctype` мають значення null, об'єкт, що повертається [DOMDocument](class.domdocument.md) буде порожнім та без елемента document.

### Помилки

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо аргумент `doctype` вже використовувався з іншим документом або було створено в іншій реалізації.

**`DOM_NAMESPACE_ERR`**

Виникає, якщо виявлена ​​помилка у рядках `namespace` і `qualifiedName`

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `namespace` тепер допускає значення null. |
|  | `doctype` тепер допускає значення null. |

### Дивіться також

-   [DOMDocument::construct()](domdocument.construct.md) - Створює новий об'єкт DOMDocument
-   [DOMImplementation::createDocumentType()](domimplementation.createdocumenttype.md) - Створює порожній об'єкт класу DOMDocumentType
