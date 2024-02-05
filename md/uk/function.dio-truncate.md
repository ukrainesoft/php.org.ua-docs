---
navigation:
  - function.dio-tcsetattr.md: « dio\_tcsetattr
  - function.dio-write.md: dio\_write »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dio\_truncate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dio\_truncate

(PHP 4 >= 4.2.0, PHP 5 < 5.1.0)

dio\_truncate — Обрізає файл до заданої кількості байт

### Опис

```methodsynopsis
dio_truncate(resource $fd, int $offset): bool
```

**dio\_truncate()** обрізає файл до `offset`байт.

Якщо файл був більшим за вказане значення, то зайві дані загубляться. Якщо файл був коротшим, то він або залишиться незмінним, або збільшиться - ця поведінка не визначена. Якщо файл збільшиться, то байти будуть заповнені нулями.

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dio\_open()](function.dio-open.md)

`offset`

Зміщення у байтах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження**: Для Windows-платформ ця функція не реалізована.
