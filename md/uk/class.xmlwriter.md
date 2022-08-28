Клас XMLWriter

-   [« Работа с объектно-ориентированным API](example.xmlwriter-oop.html)
    
-   [XMLWriter::endAttribute »](xmlwriter.endattribute.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](book.xmlwriter.html)
    
-   Клас XMLWriter
    

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

-   [XMLWriter::endAttribute](xmlwriter.endattribute.html) - Завершити атрибут
-   [XMLWriter::endCdata](xmlwriter.endcdata.html) — Завершити поточну секцію CDATA
-   [XMLWriter::endComment](xmlwriter.endcomment.html) — Завершити коментар
-   [XMLWriter::endDocument](xmlwriter.enddocument.html) — Завершити поточний документ
-   [XMLWriter::endDtd](xmlwriter.enddtd.html) - Завершити поточний DTD
-   [XMLWriter::endDtdAttlist](xmlwriter.enddtdattlist.html) — Завершити поточний список атрибутів DTD
-   [XMLWriter::endDtdElement](xmlwriter.enddtdelement.html) — Завершити поточний елемент DTD
-   [XMLWriter::endDtdEntity](xmlwriter.enddtdentity.html) — Завершити поточний запис DTD
-   [XMLWriter::endElement](xmlwriter.endelement.html) — Завершити поточний елемент
-   [XMLWriter::endPi](xmlwriter.endpi.html) — Закінчити поточну інструкцію обробки (PI)
-   [XMLWriter::flush](xmlwriter.flush.html) - Скинути поточний буфер
-   [XMLWriter::fullEndElement](xmlwriter.fullendelement.html) — Завершити поточний елемент
-   [XMLWriter::openMemory](xmlwriter.openmemory.html) — Створити новий об'єкт XMLWriter, використовуючи пам'ять для рядкового виводу
-   [XMLWriter::openUri](xmlwriter.openuri.html) — Створити новий об'єкт XMLWriter, використовуючи вихідний URI для виводу
-   [XMLWriter::outputMemory](xmlwriter.outputmemory.html) - Повертає поточний буфер
-   [XMLWriter::setIndent](xmlwriter.setindent.html) — Увімкнути або вимкнути відступи
-   [XMLWriter::setIndentString](xmlwriter.setindentstring.html) — Встановити рядок, який використовується для відступів
-   [XMLWriter::startAttribute](xmlwriter.startattribute.html) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs](xmlwriter.startattributens.html) - Створити стартовий атрибут простору імен
-   [XMLWriter::startCdata](xmlwriter.startcdata.html) - Створити початковий тег CDATA
-   [XMLWriter::startComment](xmlwriter.startcomment.html) - Створює стартовий коментар
-   [XMLWriter::startDocument](xmlwriter.startdocument.html) - Створити тег документа
-   [XMLWriter::startDtd](xmlwriter.startdtd.html) - Створити стартовий DTD тег
-   [XMLWriter::startDtdAttlist](xmlwriter.startdtdattlist.html) - Створює стартовий список атрибутів DTD
-   [XMLWriter::startDtdElement](xmlwriter.startdtdelement.html) - Створити стартовий елемент DTD
-   [XMLWriter::startDtdEntity](xmlwriter.startdtdentity.html) — Створити стартовий запис DTD
-   [XMLWriter::startElement](xmlwriter.startelement.html) - Створити стартовий тег елемента
-   [XMLWriter::startElementNs](xmlwriter.startelementns.html) — Створити стартовий тег елемента простору імен
-   [XMLWriter::startPi](xmlwriter.startpi.html) - Створити стартовий тег PI
-   [XMLWriter::text](xmlwriter.text.html) - Записати текст
-   [XMLWriter::writeAttribute](xmlwriter.writeattribute.html) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs](xmlwriter.writeattributens.html) - Записати повний атрибут простору імен
-   [XMLWriter::writeCdata](xmlwriter.writecdata.html) — Записати повний тег CDATA
-   [XMLWriter::writeComment](xmlwriter.writecomment.html) — Записати повний тег коментаря
-   [XMLWriter::writeDtd](xmlwriter.writedtd.html) — Записати повний тег DTD
-   [XMLWriter::writeDtdAttlist](xmlwriter.writedtdattlist.html) — Записати повний тег DTD AttList
-   [XMLWriter::writeDtdElement](xmlwriter.writedtdelement.html) — Записати повний тег елемента DTD
-   [XMLWriter::writeDtdEntity](xmlwriter.writedtdentity.html) — Записати повний тег DTD запису
-   [XMLWriter::writeElement](xmlwriter.writeelement.html) — Записати повний тег елемента
-   [XMLWriter::writeElementNs](xmlwriter.writeelementns.html) — Записати повний простір імен тега елемента
-   [XMLWriter::writePi](xmlwriter.writepi.html) - Записати інструкцію обробки (PI)
-   [XMLWriter::writeRaw](xmlwriter.writeraw.html) — Записати необроблений XML-текст