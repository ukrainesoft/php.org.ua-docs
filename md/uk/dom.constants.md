---
navigation:
  - dom.resources.md: « Типи ресурсів
  - dom.examples.md: Приклади »
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**XML константи**

| Константа | Значение | Опис |
| --- | --- | --- |
| **`XML_ELEMENT_NODE`**(int) |  | Вузол класу [DOMElement](class.domelement.md) |
| **`XML_ATTRIBUTE_NODE`**(int) |  | Вузол класу [DOMAttr](class.domattr.md) |
| **`XML_TEXT_NODE`**(int) | 3 | Вузол класу [DOMText](class.domtext.md) |
| **`XML_CDATA_SECTION_NODE`**(int) | 4 | Вузол класу [DOMCharacterData](class.domcharacterdata.md) |
| **`XML_ENTITY_REF_NODE`**(int) | 5 | Вузол класу [DOMEntityReference](class.domentityreference.md) |
| **`XML_ENTITY_NODE`**(int) | 6 | Вузол класу [DOMEntity](class.domentity.md) |
| **`XML_PI_NODE`**(int) | 7 | Вузол класу [DOMProcessingInstruction](class.domprocessinginstruction.md) |
| **`XML_COMMENT_NODE`**(int) | 8 | Вузол класу [DOMComment](class.domcomment.md) |
| **`XML_DOCUMENT_NODE`**(int) | 9 | Вузол класу [DOMDocument](class.domdocument.md) |
| **`XML_DOCUMENT_TYPE_NODE`**(int) | 10 | Вузол класу [DOMDocumentType](class.domdocumenttype.md) |
| **`XML_DOCUMENT_FRAG_NODE`**(int) | 11 | Вузол класу [DOMDocumentFragment](class.domdocumentfragment.md) |
| **`XML_NOTATION_NODE`**(int) | 12 | Вузол класу [DOMNotation](class.domnotation.md) |
| **`XML_HTML_DOCUMENT_NODE`**(int) | 13 |  |
| **`XML_DTD_NODE`**(int) | 14 |  |
| **`XML_ELEMENT_DECL_NODE`**(int) | 15 |  |
| **`XML_ATTRIBUTE_DECL_NODE`**(int) | 16 |  |
| **`XML_ENTITY_DECL_NODE`**(int) | 17 |  |
| **`XML_NAMESPACE_DECL_NODE`**(int) | 18 |  |
| **`XML_ATTRIBUTE_CDATA`**(int) |  |  |
| **`XML_ATTRIBUTE_ID`**(int) |  |  |
| **`XML_ATTRIBUTE_IDREF`**(int) | 3 |  |
| **`XML_ATTRIBUTE_IDREFS`**(int) | 4 |  |
| **`XML_ATTRIBUTE_ENTITY`**(int) | 5 |  |
| **`XML_ATTRIBUTE_NMTOKEN`**(int) | 7 |  |
| **`XML_ATTRIBUTE_NMTOKENS`**(int) | 8 |  |
| **`XML_ATTRIBUTE_ENUMERATION`**(int) | 9 |  |
| **`XML_ATTRIBUTE_NOTATION`**(int) | 10 |  |

**Константи DOMException**

| Константа | Значение | Опис |
| --- | --- | --- |
| **`DOM_PHP_ERR`**(int) |  | Цей код помилки не є частиною специфікації DOM. Призначена для помилок PHP. |
| **`DOM_INDEX_SIZE_ERR`**(int) |  | Якщо індекс або розмір є негативним або виходить за межі можливих значень. |
| **`DOMSTRING_SIZE_ERR`**(int) |  | Якщо вказаний фрагмент тексту не міститься в **DOMString** |
| **`DOM_HIERARCHY_REQUEST_ERR`**(int) | 3 | Якщо неможливо вставити вузол |
| **`DOM_WRONG_DOCUMENT_ERR`**(int) | 4 | Якщо вузол використовується в іншому документі, а не в тому, де його було створено. |
| **`DOM_INVALID_CHARACTER_ERR`**(int) | 5 | Якщо вказано неприпустимий символ, наприклад, у імені. |
| **`DOM_NO_DATA_ALLOWED_ERR`**(int) | 6 | Якщо дані, вказані для сайту, не підтримуються. |
| **`DOM_NO_MODIFICATION_ALLOWED_ERR`**(int) | 7 | Якщо спроба змінити об'єкт, який не підтримує зміни. |
| **`DOM_NOT_FOUND_ERR`**(int) | 8 | Якщо робиться спроба посилатися на вузол у контексті, якого не існує |
| **`DOM_NOT_SUPPORTED_ERR`**(int) | 9 | Якщо реалізація не підтримує вибраний тип об'єкта або операції. |
| **`DOM_INUSE_ATTRIBUTE_ERR`**(int) | 10 | Якщо додати атрибут, який використовується в іншому місці. |
| **`DOM_INVALID_STATE_ERR`**(int) | 11 | Якщо намагатись використовувати об'єкт, якого немає або неможливо використати. |
| **`DOM_SYNTAX_ERR`**(int) | 12 | Якщо використовується неправильний рядок. |
| **`DOM_INVALID_MODIFICATION_ERR`**(int) | 13 | Якщо ви намагаєтеся змінити тип базового об'єкта. |
| **`DOM_NAMESPACE_ERR`**(int) | 14 | Якщо ви намагаєтеся створити або змінити об'єкт з некоректним простором імен. |
| **`DOM_INVALID_ACCESS_ERR`**(int) | 15 | Якщо параметр або операція не підтримується базовим об'єктом. |
| **`DOM_VALIDATION_ERR`**(int) | 16 | Якщо виклик методу, такого як insertBefore або removeChild, зробить вузол недійсним, викине виняток і операція не буде виконана. |
