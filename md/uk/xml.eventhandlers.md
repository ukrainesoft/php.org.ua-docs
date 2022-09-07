---
navigation:
  - xml.constants.md: « Обумовлені константи
  - xml.case-folding.md: Приведення до одного регістру »
  - index.md: PHP Manual
  - book.xml.md: Разбор XML
title: Обробники подій
---
# Обробники подій

Список обробників подій XML:

**Підтримувані XML обробники**

| Функции PHP для установки обработчика | Описание события |
| --- | --- |
| [xmlsetelementhandler()](function.xml-set-element-handler.md) | Події елементів видаються кожного разу, коли XML-парсер зустрічає початковий або кінцевий теги. Є різні обробники для початкових та кінцевих тегів. |
| [xmlsetcharacterdatahandler()](function.xml-set-character-data-handler.md) | Символьні дані – це приблизно весь нерозмічений вміст XML документів, включаючи недруковані символи між тегами. Зазначимо, що XML аналізатор не додає або видаляє жодних недрукованих символів, оскільки ця програма (тобто користувач) вирішує, де недруковані символи значні. |
| [xmlsetprocessinginstructionhandler()](function.xml-set-processing-instruction-handler.md) | PHP програмісти повинні бути вже знайомі з інструкціями обробки (PIs) . є обробною інструкцією, де php є "PI метою". Обробка цих інструкцій залежить від програми, за винятком того, що всі цілі PI починаються із зарезервованого слова "XML". |
| [xmlsetdefaulthandler()](function.xml-set-default-handler.md) | Якщо немає спеціального оброблювача, викликається оброблювач за замовчуванням. Ви отримаєте XML та оголошення типів документа за допомогою стандартного обробника. |
| [xmlsetunparsedentitydeclhandler()](function.xml-set-unparsed-entity-decl-handler.md) | Цей обробник буде викликатись для декларування непроаналізованих (NDATA) сутностей. |
| [xmlsetnotationdeclhandler()](function.xml-set-notation-decl-handler.md) | Цей оброблювач викликається при оголошенні нотації. |
| [xmlsetexternalentityrefhandler()](function.xml-set-external-entity-ref-handler.md) | Цей обробник викликається, коли аналізатор XML знаходить посилання на зовнішню сутність. Наприклад, це може бути посилання на файл або URL-адресу. Дивіться [приклад зовнішньої сутності](example.xml-external-entity.md) |
| [xmlsetstartnamespacedeclhandler()](function.xml-set-start-namespace-decl-handler.md) | Цей обробник викликається на початку оголошення простору імен. |
| [xmlsetendnamespacedeclhandler()](function.xml-set-end-namespace-decl-handler.md) | Цей обробник викликається наприкінці оголошення простору імен. Зазначимо, що ця подія *не* викликається LibXML. |
