Обумовлені константи

-   [« Типи ресурсів](dom.resources.md)
    
-   [Приклади »](dom.examples.md)
    
-   [PHP Manual](index.md)
    
-   [DOM](book.dom.md)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**XML константи**

| Константа                             | Значение | Описание                                                                  |
|---------------------------------------|----------|---------------------------------------------------------------------------|
| **`XML_ELEMENT_NODE`** (int)          |          | Вузол класу [DOMElement](class.domelement.md)                             |
| **`XML_ATTRIBUTE_NODE`** (int)        |          | Вузол класу [DOMAttr](class.domattr.md)                                   |
| **`XML_TEXT_NODE`** (int)             |          | Вузол класу [DOMText](class.domtext.md)                                   |
| **`XML_CDATA_SECTION_NODE`** (int)    |          | Вузол класу [DOMCharacterData](class.domcharacterdata.md)                 |
| **`XML_ENTITY_REF_NODE`** (int)       |          | Вузол класу [DOMEntityReference](class.domentityreference.md)             |
| **`XML_ENTITY_NODE`** (int)           |          | Вузол класу [DOMEntity](class.domentity.md)                               |
| **`XML_PI_NODE`** (int)               |          | Вузол класу [DOMProcessingInstruction](class.domprocessinginstruction.md) |
| **`XML_COMMENT_NODE`** (int)          |          | Вузол класу [DOMComment](class.domcomment.md)                             |
| **`XML_DOCUMENT_NODE`** (int)         |          | Вузол класу [DOMDocument](class.domdocument.md)                           |
| **`XML_DOCUMENT_TYPE_NODE`** (int)    |          | Вузол класу [DOMDocumentType](class.domdocumenttype.md)                   |
| **`XML_DOCUMENT_FRAG_NODE`** (int)    |          | Вузол класу [DOMDocumentFragment](class.domdocumentfragment.md)           |
| **`XML_NOTATION_NODE`** (int)         |          | Вузол класу [DOMNotation](class.domnotation.md)                           |
| **`XML_HTML_DOCUMENT_NODE`** (int)    |          |                                                                           |
| **`XML_DTD_NODE`** (int)              |          |                                                                           |
| **`XML_ELEMENT_DECL_NODE`** (int)     |          |                                                                           |
| **`XML_ATTRIBUTE_DECL_NODE`** (int)   |          |                                                                           |
| **`XML_ENTITY_DECL_NODE`** (int)      |          |                                                                           |
| **`XML_NAMESPACE_DECL_NODE`** (int)   |          |                                                                           |
| **`XML_ATTRIBUTE_CDATA`** (int)       |          |                                                                           |
| **`XML_ATTRIBUTE_ID`** (int)          |          |                                                                           |
| **`XML_ATTRIBUTE_IDREF`** (int)       |          |                                                                           |
| **`XML_ATTRIBUTE_IDREFS`** (int)      |          |                                                                           |
| **`XML_ATTRIBUTE_ENTITY`** (int)      |          |                                                                           |
| **`XML_ATTRIBUTE_NMTOKEN`** (int)     |          |                                                                           |
| **`XML_ATTRIBUTE_NMTOKENS`** (int)    |          |                                                                           |
| **`XML_ATTRIBUTE_ENUMERATION`** (int) |          |                                                                           |
| **`XML_ATTRIBUTE_NOTATION`** (int)    |          |                                                                           |

**Константи DOMException**

| Константа                                   | Значение | Описание                                                                                                                         |
|---------------------------------------------|----------|----------------------------------------------------------------------------------------------------------------------------------|
| **`DOM_PHP_ERR`** (int)                     |          | Цей код помилки не є частиною специфікації DOM. Призначена для помилок PHP.                                                      |
| **`DOM_INDEX_SIZE_ERR`** (int)              |          | Якщо індекс або розмір є негативним або виходить за межі можливих значень.                                                       |
| **`DOMSTRING_SIZE_ERR`** (int)              |          | Якщо вказаний фрагмент тексту не міститься в **DOMString**                                                                       |
| **`DOM_HIERARCHY_REQUEST_ERR`** (int)       |          | Якщо неможливо вставити вузол                                                                                                    |
| **`DOM_WRONG_DOCUMENT_ERR`** (int)          |          | Якщо вузол використовується в іншому документі, а не в тому, де його було створено.                                              |
| **`DOM_INVALID_CHARACTER_ERR`** (int)       |          | Якщо вказано неприпустимий символ, наприклад, у імені.                                                                           |
| **`DOM_NO_DATA_ALLOWED_ERR`** (int)         |          | Якщо дані, вказані для сайту, не підтримуються.                                                                                  |
| **`DOM_NO_MODIFICATION_ALLOWED_ERR`** (int) |          | Якщо спроба змінити об'єкт, який не підтримує зміни.                                                                             |
| **`DOM_NOT_FOUND_ERR`** (int)               |          | Якщо робиться спроба посилатися на вузол у контексті, якого не існує                                                             |
| **`DOM_NOT_SUPPORTED_ERR`** (int)           |          | Якщо реалізація не підтримує вибраний тип об'єкта або операції.                                                                  |
| **`DOM_INUSE_ATTRIBUTE_ERR`** (int)         |          | Якщо додати атрибут, який використовується в іншому місці.                                                                       |
| **`DOM_INVALID_STATE_ERR`** (int)           |          | Якщо ви намагаєтеся використовувати об'єкт, якого немає або неможливо використовувати.                                           |
| **`DOM_SYNTAX_ERR`** (int)                  |          | Якщо використовується неправильний рядок.                                                                                        |
| **`DOM_INVALID_MODIFICATION_ERR`** (int)    |          | Якщо ви намагаєтеся змінити тип базового об'єкта.                                                                                |
| **`DOM_NAMESPACE_ERR`** (int)               |          | Якщо ви намагаєтеся створити або змінити об'єкт з некоректним простором імен.                                                    |
| **`DOM_INVALID_ACCESS_ERR`** (int)          |          | Якщо параметр або операція не підтримується базовим об'єктом.                                                                    |
| **`DOM_VALIDATION_ERR`** (int)              |          | Якщо виклик методу, такого як insertBefore або removeChild, зробить вузол недійсним, викине виняток і операція не буде виконана. |