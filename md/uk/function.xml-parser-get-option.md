---
navigation:
  - function.xml-parser-free.md: « xml\_parser\_free
  - function.xml-parser-set-option.md: xml\_parser\_set\_option »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_parser\_get\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_parser\_get\_option

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_parser\_get\_option — Отримує значення налаштування XML-аналізатора

### Опис

```methodsynopsis
xml_parser_get_option(XMLParser $parser, int $option): string|int|bool
```

Отримує значення налаштування XML-аналізатора.

### Список параметрів

`parser`

Посилання на XML-аналізатор, налаштування якого потрібно отримати.

`option`

Яке налаштування отримати. Доступні параметри: **`XML_OPTION_CASE_FOLDING`** **`XML_OPTION_SKIP_TAGSTART`** **`XML_OPTION_SKIP_WHITE`** і **`XML_OPTION_TARGET_ENCODING`**. Вони описані у документації до функції [xml\_parser\_set\_option()](function.xml-parser-set-option.md)

### Значення, що повертаються

Повертає значення налаштування.

### Помилки

Якщо параметр `option` передано неприпустиме значення, буде викинуто виняток [ValueError](class.valueerror.md)

До PHP 8.0.0 передача недопустимого значение в параметр`option`генерировало ошибку уровня\*\*`E_WARNING`\*\*, що змушувало функцію повертати логічне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер функція повертає логічне значення логічних налаштувань. |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
| 8.0.0 | Если значение параметра`option` неприпустимо, тепер викидається виняток [ValueError](class.valueerror.md) |
| 7.1.24, 7.2.12, 7.3.0 | Тепер параметр `options` підтримує значення **`XML_OPTION_SKIP_TAGSTART`** і **`XML_OPTION_SKIP_WHITE`** |
