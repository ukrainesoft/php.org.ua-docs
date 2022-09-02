---
navigation:
  - xmldiff-file.diff.md: '« XMLDiffFile::diff'
  - book.xml.md: Разбор XML »
  - index.md: PHP Manual
  - class.xmldiff-file.md: XMLDiffFile
title: 'XMLDiffFile::merge'
---
# XMLDiffFile::merge

(PECL xmldiff >= 0.8.0)

XMLDiffFile::merge — Застосувати зміни до документа XML

### Опис

```methodsynopsis
public XMLDiff\File::merge(string $src, string $diff): string
```

Створює новий документ XML на базі джерела та списку змін.

### Список параметрів

`src`

Шлях до XML-документа джерела.

`diff`

Шлях до XML-документа, що містить інформацію про зміни.

### Значення, що повертаються

Рядок з новим XML-документом або **`null`**
