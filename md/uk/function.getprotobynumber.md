---
navigation:
  - function.getprotobyname.html: « getprotobyname
  - function.getservbyname.html: getservbyname »
  - index.html: PHP Manual
  - ref.network.html: Мережеві функції
title: getprotobynumber
---
# getprotobynumber

(PHP 4, PHP 5, PHP 7, PHP 8)

getprotobynumber — Отримує ім'я протоколу за номером

### Опис

```methodsynopsis
getprotobynumber(int $protocol): string|false
```

Функція **getprotobynumber()** повертає ім'я протоколу за номером, вказаним у параметрі `protocol` згідно з /etc/protocols.

### Список параметрів

`protocol`

Номер протоколу.

### Значення, що повертаються

Повертає ім'я протоколу у вигляді рядка або **`false`** у разі виникнення помилки.

### Дивіться також

-   [getprotobyname()](function.getprotobyname.html) - Отримує номер протоколу на ім'я
