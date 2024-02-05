---
navigation:
  - function.getservbyname.md: « getservbyname
  - function.header-register-callback.md: header\_register\_callback »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: getservbyport
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getservbyport

(PHP 4, PHP 5, PHP 7, PHP 8)

getservbyport — Отримує інтернет-службу, що відповідає заданому порту та протоколу

### Опис

```methodsynopsis
getservbyport(int $port, string $protocol): string|false
```

Функция**getservbyport()** повертає Інтернет-службу, що відповідає заданому у параметрі `port` порту для певного протоколу `protocol`согласно /etc/services.

### Список параметрів

`port`

Номер порту.

`protocol`

Параметр`protocol` може бути `"tcp"`or`"udp"` (У нижньому регістрі).

### Значення, що повертаються

Повертає ім'я Інтернет-служби у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [getservbyname()](function.getservbyname.md) \- Отримує номер порту, пов'язаного з інтернет-службою та протоколом
