---
navigation:
  - function.wddx-serialize-vars.html: « wddxserializevars
  - intro.xmldiff.md: Введение »
  - index.md: PHP Manual
  - refs.xml.md: Обработка XML
title: Порівняння та об'єднання XML
---
# Порівняння та об'єднання XML

-   [Введение](intro.xmldiff.md)
-   [Встановлення та налаштування](xmldiff.setup.md)
    -   [Вимоги](xmldiff.requirements.md)
    -   [Установка](xmldiff.installation.md)
-   [XMLDiffBase](class.xmldiff-base.md) - Клас XMLDiffBase
    -   [XMLDiffBase::construct](xmldiff-base.construct.md) - Конструктор
    -   [XMLDiffBase::diff](xmldiff-base.diff.md) — Здійснює порівняння двох документів XML
    -   [XMLDiffBase::merge](xmldiff-base.merge.md) — Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого
-   [XMLDiffDOM](class.xmldiff-dom.md) - Клас XMLDiffDOM
    -   [XMLDiffDOM::diff](xmldiff-dom.diff.md) — Пошук відмінностей у двох об'єктах DOMDocument
    -   [XMLDiffDOM::merge](xmldiff-dom.merge.md) — Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff
-   [XMLDiffMemory](class.xmldiff-memory.md) - Клас XMLDiffMemory
    -   [XMLDiffMemory::diff](xmldiff-memory.diff.md) — Порівняння двох документів XML
    -   [XMLDiffMemory::merge](xmldiff-memory.merge.md) — Застосувати зміни до документа XML
-   [XMLDiffFile](class.xmldiff-file.md) - Клас XMLDiffFile
    -   [XMLDiffFile::diff](xmldiff-file.diff.md) — Порівняння двох файлів XML
    -   [XMLDiffFile::merge](xmldiff-file.merge.md) — Застосувати зміни до документа XML
