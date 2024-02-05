---
navigation:
  - xml.constants.md: « Зумовлені константи
  - xml.case-folding.md: Приведення до одного регістру »
  - index.md: PHP Manual
  - book.xml.md: Розбір XML
title: Обробники подій
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обробники подій

Список обробників подій XML:

**Підтримувані XML обробники**

| Функции PHP для установки обработчика | Опис события |
| --- | --- |
| [xml\_set\_element\_handler()](function.xml-set-element-handler.md) | Події елементів видаються щоразу, коли XML парсер зустрічає початковий чи кінцевий теги. Є різні обробники для початкових та кінцевих тегів. |
| [xml\_set\_character\_data\_handler()](function.xml-set-character-data-handler.md) | Символьні дані – це приблизно весь нерозмічений вміст XML документів, включаючи недруковані символи між тегами. Зазначимо, що XML аналізатор не додає або видаляє жодних недрукованих символів, так як ця програма (тобто користувач) вирішує, де недруковані символи значні. |
| [xml\_set\_processing\_instruction\_handler()](function.xml-set-processing-instruction-handler.md) | PHP програмісти повинні бути вже ознайомлені з інструкціями обробки (PIs). . є обробною інструкцією, де php є "PI метою". Обробка цих інструкцій залежить від програми, за винятком того, що всі цілі PI починаються із зарезервованого слова "XML". |
| [xml\_set\_default\_handler()](function.xml-set-default-handler.md) | Якщо немає спеціального оброблювача, викликається оброблювач за замовчуванням. Ви отримаєте XML та оголошення типів документа за допомогою стандартного обробника. |
| [xml\_set\_unparsed\_entity\_decl\_handler()](function.xml-set-unparsed-entity-decl-handler.md) | Цей обробник буде викликатись для декларування непроаналізованих (NDATA) сутностей. |
| [xml\_set\_notation\_decl\_handler()](function.xml-set-notation-decl-handler.md) | Цей оброблювач викликається при оголошенні нотації. |
| [xml\_set\_external\_entity\_ref\_handler()](function.xml-set-external-entity-ref-handler.md) | Цей обробник викликається, коли аналізатор XML знаходить посилання на зовнішню сутність. Наприклад, це може бути посилання на файл або URL-адресу. Дивіться [приклад зовнішньої сутності](example.xml-external-entity.md) |
| [xml\_set\_start\_namespace\_decl\_handler()](function.xml-set-start-namespace-decl-handler.md) | Цей обробник викликається на початку оголошення простору імен. |
| [xml\_set\_end\_namespace\_decl\_handler()](function.xml-set-end-namespace-decl-handler.md) | Цей обробник викликається наприкінці оголошення простору імен. Зазначимо, що ця подія *не* викликається LibXML. |
