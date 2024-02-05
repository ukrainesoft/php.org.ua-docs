---
navigation:
  - function.yaz-scan.md: « yaz\_scan
  - function.yaz-search.md: yaz\_search »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_schema
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_schema

(PHP 4 >= 4.2.0, PECL yaz >= 0.9.0)

yaz\_schema — Встановлює схему для значень, що повертаються.

### Опис

```methodsynopsis
yaz_schema(resource $id, string $schema): void
```

**yaz\_schema()** встановлює схему для значень, що повертаються.

Функція має бути викликана до [yaz\_search()](function.yaz-search.md) або [yaz\_present()](function.yaz-present.md)

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`schema`

Схема має бути визначена як OID (Object Identifier) ​​у вихідному поданні з роздільниками у вигляді точок (наприклад `1.2.840.10003.13.4`) або як одна з відомих форм імені схеми: `GILS-schema` `Holdings` `Zthes`, ...

### Значення, що повертаються

Функція не повертає значення після виконання.
