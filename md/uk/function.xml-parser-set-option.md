- [« xml_parser_get_option](function.xml-parser-get-option.md)
- [xml_set_character_data_handler »](function.xml-set-character-data-handler.md)

- [PHP Manual](index.md)
- [Функції парсера XML](ref.xml.md)
- Встановлення значення налаштування XML-аналізатора

#xml_parser_set_option

(PHP 4, PHP 5, PHP 7, PHP 8)

xml_parser_set_option — Встановлення значення налаштування XML-аналізатора

### Опис

**xml_parser_set_option**([XMLParser](class.xmlparser.md) `$parser`,
int `$option`, string\|int `$value`): bool

Встановлює налаштування XML-аналізатора.

### Список параметрів

`parser`
Посилання на аналізатор XML.

`option`
Яку установку потрібно встановити. Дивіться нижче.

Доступні такі установки:

| Константа Тип даних Опис       |
| ------------------------------ |
| **XML_OPTION_CASE_FOLDING**    | integer | Чи потрібно увімкнути [case-folding](xml.case-folding.md) для цього аналізатора. Увімкнено за замовчуванням. 
| **XML_OPTION_SKIP_TAGSTART**   | integer | Задає кількість символів з початку імені тега, який слід пропустити.
| **XML_OPTION_SKIP_WHITE**      | integer | Чи потрібно пропускати значення, що складаються з прогалин.
| **XML_OPTION_TARGET_ENCODING** | string | Встановлює [кодування](xml.encoding.md), яке використовуватиметься XML аналізатором. За замовчуванням використовується кодування, задане при виклику функції [xml_parser_create()](function.xml-parser-create.md). Підтримуються кодування ISO-8859-1, US-ASCII та UTF-8.

**Налаштування XML-аналізатора**

`value`
Нове значення налаштування.

### Значення, що повертаються

Функція повертає **`false`**, якщо `parser` посилається на неприпустимий
аналізатор або якщо настроювання не може бути встановлене. В протилежному
у разі встановлюється нове значення налаштування та повертається значення
**`true`**.

### Список змін

| Версія | Опис                                                                                                    |
| ------ | ------------------------------------------------------------------------------------------------------- |
| 8.0.0  | Параметр parser чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікували ресурс (resource). |
