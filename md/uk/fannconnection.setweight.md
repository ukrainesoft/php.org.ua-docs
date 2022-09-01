---
navigation:
  - fannconnection.getweight.html: '« FANNConnection::getWeight'
  - book.igbinary.html: Igbinary »
  - index.html: PHP Manual
  - class.fannconnection.html: FANNConnection
title: 'FANNConnection::setWeight'
---
# FANNConnection::setWeight

(PECL fann> = 1.0.0)

FANNConnection::setWeight — Встановлює вагу зв'язку

### Опис

```methodsynopsis
public FANNConnection::setWeight(float $weight): void
```

Встановлює вагу зв'язку.

Цей метод відрізняється від [fannsetweight()](function.fann-set-weight.html). Він не оновлює значення ваги мережі. Значення в мережі оновиться лише після дзвінка [fannsetweightarray()](function.fann-set-weight-array.html)

### Список параметрів

`weight`

Вага зв'язку.

### Значення, що повертаються

Не повертає жодного значення.
