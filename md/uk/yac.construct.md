---
navigation:
  - yac.add.md: '« Yac::add'
  - yac.delete.md: 'Yac::delete »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yac::\_\_construct

(PECL yac >= 1.0.0)

Yac::\_\_construct - Конструктор класу

### Опис

public **Yac::\_\_construct**(string`$prefix` = "")

Префікс використовується для додавання ключів, його можна використовувати для запобігання конфліктам між додатками.

### Список параметрів

`prefix`

Префікс (string)

### Помилки

Викидає [Exception](class.exception.md), якщо Yac не включено. Викидає [Exception](class.exception.md), якщо `prefix` перевищує максимальну довжину ключа 48 (**`YAC_MAX_KEY_LEN`**) байтів.
