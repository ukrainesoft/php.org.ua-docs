---
navigation:
  - function.xml-parser-get-option.md: « xml\_parser\_get\_option
  - function.xml-set-character-data-handler.md: xml\_set\_character\_data\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_parser\_set\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_parser\_set\_option

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_parser\_set\_option — Встановлення значення налаштування XML-аналізатора

### Опис

```methodsynopsis
xml_parser_set_option(XMLParser $parser, int $option, string|int|bool $value): bool
```

Встановлює налаштування XML-аналізатора.

### Список параметрів

`parser`

Посилання на аналізатор XML.

`option`

Яке налаштування потрібно встановити. Дивіться нижче.

Доступні такі параметри:

**Налаштування XML-аналізатора**

| Константа | Тип данных | Опис |
| --- | --- | --- |
| **`XML_OPTION_CASE_FOLDING`** | bool | Чи потрібно включити [case-folding](xml.case-folding.md) для цього аналізатора. Увімкнено за замовчуванням. |
| **`XML_OPTION_SKIP_TAGSTART`** | integer | Задає кількість символів з початку імені тега, які потрібно пропустити. |
| **`XML_OPTION_SKIP_WHITE`** | bool | Чи потрібно пропускати значення, що складаються з прогалин. |
| **`XML_OPTION_TARGET_ENCODING`** | string | Устанавливает[кодування](xml.encoding.md), яка буде використовуватися аналізатором XML. За замовчуванням використовується кодування, задане при виклику функції [xml\_parser\_create()](function.xml-parser-create.md). . Підтримуються кодування `ISO-8859-1` `US-ASCII`и`UTF-8` |

`value`

Нове значення налаштування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо параметр `option` передано неприпустиме значення, викидається виняток [ValueError](class.valueerror.md)

До PHP 8.0.0 функция возвращала значение false, когда отправка в параметр`option` неприпустимого значення призводила до помилки рівня **`E_WARNING`**, що змушувало функцію повертати логічне значення **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер параметр `value` також набуває логічних значень. Налаштування **`XML_OPTION_CASE_FOLDING`**и**`XML_OPTION_SKIP_WHITE`** тепер логічні. |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md), если значение параметра`option`недопустимо. |
