---
navigation:
  - xmldiff-file.diff.md: '« XMLDiff\\File::diff'
  - book.xml.md: Розбір XML »
  - index.md: PHP Manual
  - class.xmldiff-file.md: XMLDiff\\File
title: 'XMLDiff\\File::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\File::merge

(PECL xmldiff >= 0.8.0)

XMLDiff\\File::merge — Застосувати зміни до документа XML

### Опис

```methodsynopsis
public XMLDiff\File::merge(string $src, string $diff): string
```

Створює новий документ XML на базі документа джерела та списку змін.

### Список параметрів

`src`

Шлях до XML-документа джерела.

`diff`

Шлях до XML-документа, що містить інформацію про зміни.

### Значення, що повертаються

Рядок з новим XML-документом або **`null`**
