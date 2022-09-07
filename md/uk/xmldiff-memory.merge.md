---
navigation:
  - xmldiff-memory.diff.md: '« XMLDiffMemory::diff'
  - class.xmldiff-file.md: XMLDiffFile »
  - index.md: PHP Manual
  - class.xmldiff-memory.md: XMLDiffMemory
title: 'XMLDiffMemory::merge'
---
# XMLDiffMemory::merge

(PECL xmldiff >= 0.8.0)

XMLDiffMemory::merge — Застосувати зміни до документа XML

### Опис

```methodsynopsis
public XMLDiff\Memory::merge(string $src, string $diff): string
```

Створює новий документ XML на базі джерела та списку змін.

### Список параметрів

`src`

XML-документ джерело.

`diff`

XML-документ, що містить інформацію про зміни.

### Значення, що повертаються

Рядок з новим XML-документом або **`null`**
