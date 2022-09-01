---
navigation:
  - function.xml-parser-get-option.html: « xmlparsergetoption
  - function.xml-set-character-data-handler.html: xmlsetcharacterdatahandler »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlparsersetoption
---
# xmlparsersetoption

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparsersetoption — Встановлення значення налаштування XML-аналізатора

### Опис

```methodsynopsis
xml_parser_set_option(XMLParser $parser, int $option, string|int $value): bool
```

Встановлює налаштування XML-аналізатора.

### Список параметрів

`parser`

Посилання на аналізатор XML.

`option`

Яке налаштування потрібно встановити. Дивіться нижче.

Доступні такі параметри:

**Налаштування XML-аналізатора**

| Константа | Тип данных | Описание |
| --- | --- | --- |
| **`XML_OPTION_CASE_FOLDING`** | integer | Чи потрібно включити [case-folding](xml.case-folding.html) для цього аналізатора. Увімкнено за замовчуванням. |
| **`XML_OPTION_SKIP_TAGSTART`** | integer | Задає кількість символів з початку імені тега, які потрібно пропустити. |
| **`XML_OPTION_SKIP_WHITE`** | integer | Чи потрібно пропускати значення, що складаються з пропусків. |
| **`XML_OPTION_TARGET_ENCODING`** | string | Встановлює [кодування](xml.encoding.md), яка буде використовуватися аналізатором XML. За промовчанням використовується кодування, задане під час виклику функції [xmlparsercreate()](function.xml-parser-create.html). Підтримуються кодування `ISO-8859-1` `US-ASCII` і `UTF-8` |

`value`

Нове значення налаштування.

### Значення, що повертаються

Функція повертає **`false`**, якщо `parser` посилається на неприпустимий аналізатор або якщо налаштування не може бути встановлене. Інакше встановлюється нове значення налаштування та повертається значення **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |
