---
navigation:
  - xmldiff-file.merge.md: '« XMLDiff\\File::merge'
  - intro.xml.md: Вступ "
  - index.md: PHP Manual
  - refs.xml.md: Обробка XML
title: Розбір XML
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Розбір XML

-   [Вступ](intro.xml.md)
-   [Встановлення та налаштування](xml.setup.md)
    -   [Вимоги](xml.requirements.md)
    -   [Установка](xml.installation.md)
    -   [Налаштування під час виконання](xml.configuration.md)
    -   [Типи ресурсів](xml.resources.md)
-   [Обумовлені константи](xml.constants.md)
-   [Обробники подій](xml.eventhandlers.md)
-   [Приведення до одного регістру](xml.case-folding.md)
-   [Коди помилок](xml.error-codes.md)
-   [Кодування символів](xml.encoding.md)
-   [Приклади](xml.examples.md)
    -   [Приклад Структури Елементу XML](example.xml-structure.md)
    -   [Приклад відображення тегів XML](example.xml-map-tags.md)
    -   [Приклад використання зовнішніх сутностей XML](example.xml-external-entity.md)
-   [Функції парсера XML](ref.xml.md)
    -   [xml\_error\_string](function.xml-error-string.md)— Отримання рядка помилки XML-аналізатора
    -   [xml\_get\_current\_byte\_index](function.xml-get-current-byte-index.md)— Отримує поточний для XML-аналізатора байтовий індекс
    -   [xml\_get\_current\_column\_number](function.xml-get-current-column-number.md)— Отримує від XML-аналізатора номер поточного стовпця
    -   [xml\_get\_current\_line\_number](function.xml-get-current-line-number.md)— Отримує від XML-аналізатора номер поточного рядка
    -   [xml\_get\_error\_code](function.xml-get-error-code.md)— Отримує код помилки XML-аналізатора
    -   [xml\_parse\_into\_struct](function.xml-parse-into-struct.md) \- Розбір XML-даних та поміщення в масив
    -   [xml\_parse](function.xml-parse.md)— Запускає аналіз XML-документа
    -   [xml\_parser\_create\_ns](function.xml-parser-create-ns.md)— Створення XML-аналізатора з підтримкою просторів імен
    -   [xml\_parser\_create](function.xml-parser-create.md)— Створення XML-аналізатора
    -   [xml\_parser\_free](function.xml-parser-free.md)— Звільнення XML-аналізатора
    -   [xml\_parser\_get\_option](function.xml-parser-get-option.md)— Отримує значення налаштування XML-аналізатора
    -   [xml\_parser\_set\_option](function.xml-parser-set-option.md)— Встановити значення налаштування XML-аналізатора
    -   [xml\_set\_character\_data\_handler](function.xml-set-character-data-handler.md)— Встановлення обробника символьних даних
    -   [xml\_set\_default\_handler](function.xml-set-default-handler.md)— Установка оброблювача за замовчуванням
    -   [xml\_set\_element\_handler](function.xml-set-element-handler.md)— Встановлення обробника початкового та кінцевого елементів
    -   [xml\_set\_end\_namespace\_decl\_handler](function.xml-set-end-namespace-decl-handler.md) \- Встановлення обробника виходу за межі простору імен
    -   [xml\_set\_external\_entity\_ref\_handler](function.xml-set-external-entity-ref-handler.md)— Встановлення оброблювача зовнішніх сутностей
    -   [xml\_set\_notation\_decl\_handler](function.xml-set-notation-decl-handler.md)— Встановлення оброблювача оголошення умовних позначень
    -   [xml\_set\_object](function.xml-set-object.md)— Використання XML-аналізатора всередині об'єкта
    -   [xml\_set\_processing\_instruction\_handler](function.xml-set-processing-instruction-handler.md) \- Встановлення обробника інструкцій препроцесора (PI)
    -   [xml\_set\_start\_namespace\_decl\_handler](function.xml-set-start-namespace-decl-handler.md) \- Встановлює обробник входу в межі простору імен
    -   [xml\_set\_unparsed\_entity\_decl\_handler](function.xml-set-unparsed-entity-decl-handler.md) \- Встановлення обробника нерозібраних оголошень сутностей
-   [XmlParser](class.xmlparser.md) \- Клас XmlParser
