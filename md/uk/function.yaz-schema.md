---
navigation:
  - function.yaz-scan.html: « yazscan
  - function.yaz-search.html: yazsearch »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazschema
---
# yazschema

(PHP 4> = 4.2.0, PECL yaz> = 0.9.0)

yazschema — Встановлює схему для значень, що повертаються.

### Опис

```methodsynopsis
yaz_schema(resource $id, string $schema): void
```

**yazschema()** встановлює схему для значень, що повертаються.

Функція має бути викликана до [yazsearch()](function.yaz-search.html) або [yazpresent()](function.yaz-present.html)

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

`schema`

Схема має бути визначена як OID (Object Identifier) ​​у вихідному поданні з роздільниками у вигляді точок (наприклад `1.2.840.10003.13.4`) або як одна з відомих форм імені схеми: `GILS-schema` `Holdings` `Zthes`

### Значення, що повертаються

Функція не повертає значення після виконання.
