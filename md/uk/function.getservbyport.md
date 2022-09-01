---
navigation:
  - function.getservbyname.html: « getservbyname
  - function.header-register-callback.html: headerregistercallback »
  - index.html: PHP Manual
  - ref.network.html: Мережеві функції
title: getservbyport
---
# getservbyport

(PHP 4, PHP 5, PHP 7, PHP 8)

getservbyport — Отримує інтернет-службу, що відповідає заданому порту та протоколу

### Опис

```methodsynopsis
getservbyport(int $port, string $protocol): string|false
```

Функція **getservbyport()** повертає Інтернет-службу, що відповідає заданому у параметрі `port` порту для певного протоколу `protocol` згідно з /etc/services.

### Список параметрів

`port`

Номер порту.

`protocol`

Параметр `protocol` може бути `"tcp"` ор `"udp"` (У нижньому регістрі).

### Значення, що повертаються

Повертає ім'я Інтернет-служби у вигляді рядка або **`false`** у разі виникнення помилки.

### Дивіться також

-   [getservbyname()](function.getservbyname.md) - Отримує номер порту, пов'язаного з інтернет-службою та протоколом
