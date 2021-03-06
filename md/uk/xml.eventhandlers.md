- [«Зумовлені константи](xml.constants.md)
- [Приведення до одного регістру»](xml.case-folding.md)

- [PHP Manual](index.md)
- [Розбір XML](book.xml.md)
- обробники подій

# Обробники подій

Список обробників подій XML:

| Функції PHP для встановлення обробника Опис                                                    |
| ---------------------------------------------------------------------------------------------- |
| [xml_set_element_handler()](function.xml-set-element-handler.md)                               | Події елементів видаються щоразу, коли XML-парсер зустрічає початковий або кінцевий теги. Є різні обробники для початкових та кінцевих тегів.
| [xml_set_character_data_handler()](function.xml-set-character-data-handler.md)                 | Символьні дані – це приблизно весь нерозмічений вміст XML документів, включаючи недруковані символи між тегами. Зазначимо, що XML аналізатор не додає або видаляє жодних недрукованих символів, так як ця програма (тобто користувач) вирішує, де недруковані символи значні.
| [xml_set_processing_instruction_handler()](function.xml-set-processing-instruction-handler.md) | PHP програмісти повинні бути вже ознайомлені з інструкціями обробки (PIs). \<?php ?\> є обробною інструкцією, де php є "PI метою". Обробка цих інструкцій залежить від програми, за винятком того, що всі цілі PI починаються із зарезервованого слова "XML".
| [xml_set_default_handler()](function.xml-set-default-handler.md)                               | Якщо немає спеціального обробника, викликається обробник за замовчуванням. Ви отримаєте XML та оголошення типів документа за допомогою стандартного обробника.
| [xml_set_unparsed_entity_decl_handler()](function.xml-set-unparsed-entity-decl-handler.md)     | Цей обробник буде викликатись для декларування непроаналізованих (NDATA) сутностей.
| [xml_set_notation_decl_handler()](function.xml-set-notation-decl-handler.md)                   | Цей обробник викликається при оголошенні нотації.
| [xml_set_external_entity_ref_handler()](function.xml-set-external-entity-ref-handler.md)       | Цей обробник викликається, коли аналізатор XML знаходить посилання на зовнішню сутність. Наприклад, це може бути посилання на файл або URL-адресу. Дивіться [Приклад зовнішньої сутності](example.xml-external-entity.md).
| [xml_set_start_namespace_decl_handler()](function.xml-set-start-namespace-decl-handler.md)     | Цей обробник викликається на початку оголошення простору імен.
| [xml_set_end_namespace_decl_handler()](function.xml-set-end-namespace-decl-handler.md)         | Цей обробник викликається наприкінці оголошення простору імен. Зазначимо, що ця подія не викликається LibXML.

**Підтримувані XML обробники**
