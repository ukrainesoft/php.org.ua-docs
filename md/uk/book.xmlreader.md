---
navigation:
  - class.xmlparser.md: « XmlParser
  - intro.xmlreader.md: Вступ "
  - index.md: PHP Manual
  - refs.xml.md: Обробка XML
title: XMLReader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader

-   [Вступ](intro.xmlreader.md)
-   [Встановлення та налаштування](xmlreader.setup.md)
    -   [Вимоги](xmlreader.requirements.md)
    -   [Установка](xmlreader.installation.md)
    -   [Налаштування під час виконання](xmlreader.configuration.md)
    -   [Типи ресурсів](xmlreader.resources.md)
-   [XMLReader](class.xmlreader.md) \- Клас XMLReader
    -   [XMLReader::close](xmlreader.close.md)— Закрити введення XMLReader
    -   [XMLReader::expand](xmlreader.expand.md)— Повернути копію поточного вузла як об'єкт DOM
    -   [XMLReader::getAttribute](xmlreader.getattribute.md)— Отримати значення атрибута з певним ім'ям
    -   [XMLReader::getAttributeNo](xmlreader.getattributeno.md)— Отримати значення атрибуту за індексом
    -   [XMLReader::getAttributeNs](xmlreader.getattributens.md)— Отримати значення атрибуту по localname та URI
    -   [XMLReader::getParserProperty](xmlreader.getparserproperty.md)— Вказує, чи була певна властивість встановлена
    -   [XMLReader::isValid](xmlreader.isvalid.md)— Показати, чи розбирається документ синтаксично правильним
    -   [XMLReader::lookupNamespace](xmlreader.lookupnamespace.md) \- Знайти простір імен для префікса
    -   [XMLReader::moveToAttribute](xmlreader.movetoattribute.md)— Перемістити курсор до атрибуту із заданим ім'ям
    -   [XMLReader::moveToAttributeNo](xmlreader.movetoattributeno.md)— Перемістити курсор на атрибут за індексом
    -   [XMLReader::moveToAttributeNs](xmlreader.movetoattributens.md)— Перемістити курсор до іменованого атрибуту
    -   [XMLReader::moveToElement](xmlreader.movetoelement.md)— Позиціонувати курсор на батьківському елементі поточного атрибуту
    -   [XMLReader::moveToFirstAttribute](xmlreader.movetofirstattribute.md)— Перемістити позицію курсору на перший атрибут
    -   [XMLReader::moveToNextAttribute](xmlreader.movetonextattribute.md)— Перемістити позицію курсору на наступний атрибут
    -   [XMLReader::next](xmlreader.next.md)— Перемістити курсор на наступний вузол, пропускаючи всі дерева.
    -   [XMLReader::open](xmlreader.open.md)— Встановити URI, що містить XML-документ для аналізу
    -   [XMLReader::read](xmlreader.read.md)— Переміститися до наступного сайту в документі
    -   [XMLReader::readInnerXml](xmlreader.readinnerxml.md)— Вийняти XML із поточного вузла
    -   [XMLReader::readOuterXml](xmlreader.readouterxml.md)— Отримати XML із поточного вузла, включаючи сам вузол
    -   [XMLReader::readString](xmlreader.readstring.md)— Прочитати вміст поточного вузла як рядок
    -   [XMLReader::setParserProperty](xmlreader.setparserproperty.md) \- Встановлює опцію парсера
    -   [XMLReader::setRelaxNGSchema](xmlreader.setrelaxngschema.md)— Встановити ім'я файлу або URI для схеми RelaxNG
    -   [XMLReader::setRelaxNGSchemaSource](xmlreader.setrelaxngschemasource.md) \- Встановлює дані, що містять схему RelaxNG
    -   [XMLReader::setSchema](xmlreader.setschema.md)— Перевірити документ за допомогою XSD
    -   [XMLReader::XML](xmlreader.xml.md)— Встановити дані, що містять XML для аналізу
