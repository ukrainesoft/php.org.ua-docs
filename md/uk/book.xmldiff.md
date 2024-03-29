---
navigation:
  - function.wddx-serialize-vars.md: « wddx\_serialize\_vars
  - intro.xmldiff.md: Вступ "
  - index.md: PHP Manual
  - refs.xml.md: Обробка XML
title: Порівняння та об'єднання XML
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Порівняння та об'єднання XML

-   [Вступ](intro.xmldiff.md)
-   [Встановлення та налаштування](xmldiff.setup.md)
    -   [Вимоги](xmldiff.requirements.md)
    -   [Установка](xmldiff.installation.md)
-   [XMLDiff\\Base](class.xmldiff-base.md) \- Клас XMLDiff\\Base
    -   [XMLDiff\\Base::\_\_construct](xmldiff-base.construct.md) \- Конструктор
    -   [XMLDiff\\Base::diff](xmldiff-base.diff.md)— Здійснює порівняння двох документів XML
    -   [XMLDiff\\Base::merge](xmldiff-base.merge.md)— Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого
-   [XMLDiff\\DOM](class.xmldiff-dom.md) \- Клас XMLDiff\\DOM
    -   [XMLDiff\\DOM::diff](xmldiff-dom.diff.md)— Пошук відмінностей у двох об'єктах DOMDocument
    -   [XMLDiff\\DOM::merge](xmldiff-dom.merge.md)— Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiff\\DOM::diff
-   [XMLDiff\\Memory](class.xmldiff-memory.md) \- Клас XMLDiff\\Memory
    -   [XMLDiff\\Memory::diff](xmldiff-memory.diff.md)— Порівняння двох документів XML
    -   [XMLDiff\\Memory::merge](xmldiff-memory.merge.md)— Застосувати зміни до документа XML
-   [XMLDiff\\File](class.xmldiff-file.md) \- Клас XMLDiff\\File
    -   [XMLDiff\\File::diff](xmldiff-file.diff.md)— Порівняння двох файлів XML
    -   [XMLDiff\\File::merge](xmldiff-file.merge.md)— Застосувати зміни до документа XML
