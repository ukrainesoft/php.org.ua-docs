---
navigation:
  - function.dio-tcsetattr.html: « diotcsetattr
  - function.dio-write.html: diowrite »
  - index.html: PHP Manual
  - ref.dio.html: Функції прямого введення/виводу
title: diotruncate
---
# diotruncate

(PHP 4> = 4.2.0, PHP 5 <5.1.0)

diotruncate — Обрізає файл до заданої кількості байт

### Опис

```methodsynopsis
dio_truncate(resource $fd, int $offset): bool
```

**diotruncate()** обрізає файл до `offset` байт.

Якщо файл був більшим за вказане значення, то зайві дані загубляться. Якщо файл був коротшим, то він або залишиться незмінним, або збільшиться - ця поведінка не визначена. Якщо файл збільшиться, то байти будуть заповнені нулями.

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dioopen()](function.dio-open.html)

`offset`

Зміщення у байтах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**: Для Windows-платформ ця функція не реалізована.
