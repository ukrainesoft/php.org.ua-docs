---
navigation:
  - ocilob.setbuffering.md: '« OCILob::setBuffering'
  - ocilob.tell.md: 'OCILob::tell »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::size'
---
# OCILob::size

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::size — Повертає розмір об'єкта LOB

### Опис

```methodsynopsis
public OCILob::size(): int|false
```

Повертає розмір об'єкта LOB

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає довжину об'єкта LOB або **`false`** у разі виникнення помилки. Для порожніх об'єктів довжина дорівнює нулю.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |
