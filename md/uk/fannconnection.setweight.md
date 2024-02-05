---
navigation:
  - fannconnection.getweight.md: '« FANNConnection::getWeight'
  - book.igbinary.md: Igbinary »
  - index.md: PHP Manual
  - class.fannconnection.md: FANNConnection
title: 'FANNConnection::setWeight'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FANNConnection::setWeight

(PECL fann >= 1.0.0)

FANNConnection::setWeight — Встановлює вагу зв'язку

### Опис

```methodsynopsis
public FANNConnection::setWeight(float $weight): void
```

Встановлює вагу зв'язку.

Цей метод відрізняється від [fann\_set\_weight()](function.fann-set-weight.md). Він не оновлює значення ваги мережі. Значення в мережі оновиться лише після дзвінка [fann\_set\_weight\_array()](function.fann-set-weight-array.md)

### Список параметрів

`weight`

Вага зв'язку.

### Значення, що повертаються

Не повертає жодного значення.
