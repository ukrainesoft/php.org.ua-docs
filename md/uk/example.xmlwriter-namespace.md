- [« Створення простого XML-документа](example.xmlwriter-simple.md)
- [Робота з об'єктно-орієнтованим API »](example.xmlwriter-oop.md)

- [PHP Manual](index.md)
- [Приклади](xmlwriter.examples.md)
- Робота з просторами імен XML

## Робота з просторами імен XML

У цьому вся прикладі демонструється створення елементів у просторі імен.

**Приклад #1 Робота з просторами імен XML**

` <?php$xw = xmlwriter_open_memory();xmlwriter_set_indent($xw, 1);$res = xmlwriter_set_indent_string($xw, ' ');xmlwriter_start_document($xw,' елемент );xmlwriter_end_attribute($xw);xmlwriter_text($xw, 'book1');xmlwriter_end_element($xw);xmlwriter_end_document($xw);echo xmlwriter_output_memory($xw); `

Результат виконання цього прикладу:

<?xml version="1.0" encoding="UTF-8"?>
<prefix:books isbn="" prefix:isbn="" xmlns:prefix="uri">book1</prefix:books>
