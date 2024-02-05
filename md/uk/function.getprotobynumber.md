---
navigation:
  - function.getprotobyname.md: « getprotobyname
  - function.getservbyname.md: getservbyname »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: getprotobynumber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getprotobynumber

(PHP 4, PHP 5, PHP 7, PHP 8)

getprotobynumber — Отримує ім'я протоколу за номером

### Опис

```methodsynopsis
getprotobynumber(int $protocol): string|false
```

Функция**getprotobynumber()** повертає ім'я протоколу за номером, вказаним у параметрі `protocol`согласно /etc/protocols.

### Список параметрів

`protocol`

Номер протоколу.

### Значення, що повертаються

Повертає ім'я протоколу у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [getprotobyname()](function.getprotobyname.md) \- Отримує номер протоколу на ім'я
