---
navigation:
  - xmldiff-memory.diff.md: '« XMLDiff\\Memory::diff'
  - class.xmldiff-file.md: XMLDiff\\File »
  - index.md: PHP Manual
  - class.xmldiff-memory.md: XMLDiff\\Memory
title: 'XMLDiff\\Memory::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\Memory::merge

(PECL xmldiff >= 0.8.0)

XMLDiff\\Memory::merge — Застосувати зміни до документа XML

### Опис

```methodsynopsis
public XMLDiff\Memory::merge(string $src, string $diff): string
```

Створює новий документ XML на базі документа джерела та списку змін.

### Список параметрів

`src`

XML-документ джерело.

`diff`

XML-документ, що містить інформацію про зміни.

### Значення, що повертаються

Рядок з новим XML-документом або **`null`**
