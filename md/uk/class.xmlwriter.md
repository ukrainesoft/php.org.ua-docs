---
navigation:
  - example.xmlwriter-oop.html: « Робота з об'єктно-орієнтованим API
  - xmlwriter.endattribute.md: 'XMLWriter::endAttribute »'
  - index.md: PHP Manual
  - book.xmlwriter.md: XMLWriter
title: Клас XMLWriter
---
# Клас XMLWriter

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class XMLWriter
     
     {

    /* Методы */
    
   public endAttribute(): bool
public endCdata(): bool
public endComment(): bool
public endDocument(): bool
public endDtd(): bool
public endDtdAttlist(): bool
public endDtdElement(): bool
public endDtdEntity(): bool
public endElement(): bool
public endPi(): bool
public flush(bool $empty = true): string|int
public fullEndElement(): bool
public openMemory(): bool
public openUri(string $uri): bool
public outputMemory(bool $flush = true): string
public setIndent(bool $enable): bool
public setIndentString(string $indentation): bool
public startAttribute(string $name): bool
public startAttributeNs(?string $prefix, string $name, ?string $namespace): bool
public startCdata(): bool
public startComment(): bool
public startDocument(?string $version = "1.0", ?string $encoding = null, ?string $standalone = null): bool
public startDtd(string $qualifiedName, ?string $publicId = null, ?string $systemId = null): bool
public startDtdAttlist(string $name): bool
public startDtdElement(string $qualifiedName): bool
public startDtdEntity(string $name, bool $isParam): bool
public startElement(string $name): bool
public startElementNs(?string $prefix, string $name, ?string $namespace): bool
public startPi(string $target): bool
public text(string $content): bool
public writeAttribute(string $name, string $value): bool
public writeAttributeNs(    ?string $prefix,    string $name,    ?string $namespace,    string $value): bool
public writeCdata(string $content): bool
public writeComment(string $content): bool
public writeDtd(    string $name,    ?string $publicId = null,    ?string $systemId = null,    ?string $content = null): bool
public writeDtdAttlist(string $name, string $content): bool
public writeDtdElement(string $name, string $content): bool
public writeDtdEntity(    string $name,    string $content,    bool $isParam = false,    ?string $publicId = null,    ?string $systemId = null,    ?string $notationData = null): bool
public writeElement(string $name, ?string $content = null): bool
public writeElementNs(    ?string $prefix,    string $name,    ?string $namespace,    ?string $content = null): bool
public writePi(string $target, string $content): bool
public writeRaw(string $content): bool

   }
```

## Зміст

-   [XMLWriter::endAttribute](xmlwriter.endattribute.md) - Завершити атрибут
-   [XMLWriter::endCdata](xmlwriter.endcdata.md) — Завершити поточну секцію CDATA
-   [XMLWriter::endComment](xmlwriter.endcomment.md) — Завершити коментар
-   [XMLWriter::endDocument](xmlwriter.enddocument.md) — Завершити поточний документ
-   [XMLWriter::endDtd](xmlwriter.enddtd.md) - Завершити поточний DTD
-   [XMLWriter::endDtdAttlist](xmlwriter.enddtdattlist.md) — Завершити поточний список атрибутів DTD
-   [XMLWriter::endDtdElement](xmlwriter.enddtdelement.md) — Завершити поточний елемент DTD
-   [XMLWriter::endDtdEntity](xmlwriter.enddtdentity.md) — Завершити поточний запис DTD
-   [XMLWriter::endElement](xmlwriter.endelement.md) — Завершити поточний елемент
-   [XMLWriter::endPi](xmlwriter.endpi.md) — Закінчити поточну інструкцію обробки (PI)
-   [XMLWriter::flush](xmlwriter.flush.md) - Скинути поточний буфер
-   [XMLWriter::fullEndElement](xmlwriter.fullendelement.md) — Завершити поточний елемент
-   [XMLWriter::openMemory](xmlwriter.openmemory.md) — Створити новий об'єкт XMLWriter, використовуючи пам'ять для рядкового виводу
-   [XMLWriter::openUri](xmlwriter.openuri.md) — Створити новий об'єкт XMLWriter, використовуючи вихідний URI для виводу
-   [XMLWriter::outputMemory](xmlwriter.outputmemory.md) - Повертає поточний буфер
-   [XMLWriter::setIndent](xmlwriter.setindent.md) — Увімкнути або вимкнути відступи
-   [XMLWriter::setIndentString](xmlwriter.setindentstring.md) — Встановити рядок, який використовується для відступів
-   [XMLWriter::startAttribute](xmlwriter.startattribute.md) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs](xmlwriter.startattributens.md) - Створити стартовий атрибут простору імен
-   [XMLWriter::startCdata](xmlwriter.startcdata.md) - Створити початковий тег CDATA
-   [XMLWriter::startComment](xmlwriter.startcomment.md) - Створює стартовий коментар
-   [XMLWriter::startDocument](xmlwriter.startdocument.md) - Створити тег документа
-   [XMLWriter::startDtd](xmlwriter.startdtd.md) - Створити стартовий DTD тег
-   [XMLWriter::startDtdAttlist](xmlwriter.startdtdattlist.md) - Створює стартовий список атрибутів DTD
-   [XMLWriter::startDtdElement](xmlwriter.startdtdelement.md) - Створити стартовий елемент DTD
-   [XMLWriter::startDtdEntity](xmlwriter.startdtdentity.md) — Створити стартовий запис DTD
-   [XMLWriter::startElement](xmlwriter.startelement.md) - Створити стартовий тег елемента
-   [XMLWriter::startElementNs](xmlwriter.startelementns.md) — Створити стартовий тег елемента простору імен
-   [XMLWriter::startPi](xmlwriter.startpi.md) - Створити стартовий тег PI
-   [XMLWriter::text](xmlwriter.text.md) - Записати текст
-   [XMLWriter::writeAttribute](xmlwriter.writeattribute.md) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs](xmlwriter.writeattributens.md) - Записати повний атрибут простору імен
-   [XMLWriter::writeCdata](xmlwriter.writecdata.md) — Записати повний тег CDATA
-   [XMLWriter::writeComment](xmlwriter.writecomment.md) — Записати повний тег коментаря
-   [XMLWriter::writeDtd](xmlwriter.writedtd.md) — Записати повний тег DTD
-   [XMLWriter::writeDtdAttlist](xmlwriter.writedtdattlist.md) — Записати повний тег DTD AttList
-   [XMLWriter::writeDtdElement](xmlwriter.writedtdelement.md) — Записати повний тег елемента DTD
-   [XMLWriter::writeDtdEntity](xmlwriter.writedtdentity.md) — Записати повний тег DTD запису
-   [XMLWriter::writeElement](xmlwriter.writeelement.md) — Записати повний тег елемента
-   [XMLWriter::writeElementNs](xmlwriter.writeelementns.md) — Записати повний простір імен тега елемента
-   [XMLWriter::writePi](xmlwriter.writepi.md) - Записати інструкцію обробки (PI)
-   [XMLWriter::writeRaw](xmlwriter.writeraw.md) — Записати необроблений XML-текст
