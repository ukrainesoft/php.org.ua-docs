---
navigation:
  - function.xml-set-end-namespace-decl-handler.html: « xmlsetendnamespacedeclhandler
  - function.xml-set-notation-decl-handler.html: xmlsetnotationdeclhandler »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlsetexternalentityrefhandler
---
# xmlsetexternalentityrefhandler

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlsetexternalentityrefhandler - Встановлення обробника зовнішніх сутностей

### Опис

```methodsynopsis
xml_set_external_entity_ref_handler(XMLParser $parser, callable $handler): bool
```

Задає функцію обробник зовнішніх сутностей для XML-аналізатора `parser`

### Список параметрів

`parser`

Посилання на аналізатор XML.

`handler`

`handler` - рядок, що містить ім'я функції, яка повинна бути визначена на момент виклику функції [xmlparse()](function.xml-parse.html) з аналізатора `parser`

Функція з ім'ям `handler` має приймати п'ять аргументів та повертати цілий результат. Якщо обробник поверне **`false`** (як і нічого не поверне), XML аналізатор припинить роботу, а функція [xmlgeterrorcode()](function.xml-get-error-code.html) повертатиме константу **`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**

```methodsynopsis
handler(    XMLParser $parser,    string $open_entity_names,    string $base,    string $system_id,    string $public_id)
```

`parser`

Перший аргумент parser є посиланням на XML-аналізатор, що викликає обробник.

`open_entity_names`

Другий аргумент `open_entity_names` - список розділених пробілами імен сутностей, які можуть брати участь у аналізі поточної сутності (включаючи поточну сутність).

`base`

Це основа для дозволу системного ідентифікатора (`system_id`) Зовнішньої сутності. На даний момент як цей аргумент завжди передається порожній рядок.

`system_id`

Четвертий аргумент `system_id` - Системний ідентифікатор у тому вигляді, як він представлений в оголошенні сутності.

`public_id`

П'ятий аргумент `public_id` - загальнодоступний ідентифікатор у вигляді, як і представлений у оголошенні сутності, чи порожній рядок, якщо такого немає; пробіли в ідентифікаторі будуть нормалізовані відповідно до вимог специфікації XML.

Якщо як обробник передано порожній рядок або **`false`**, цей обробник вимикається.

> **Зауваження**: Як аргумент замість імені функції може бути переданий масив, що містить посилання на об'єкт та ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |
|  | Значення, що повертається `handler` більше не ігнорується, якщо модуль був зібраний із бібліотекою libxml. Раніше значення, що поверталося, ігнорувалося, а розбір ніколи не зупинявся. |
