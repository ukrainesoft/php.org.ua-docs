---
navigation:
  - class.fannconnection.md: « FANNConnection
  - fannconnection.getfromneuron.md: 'FANNConnection::getFromNeuron »'
  - index.md: PHP Manual
  - class.fannconnection.md: FANNConnection
title: 'FANNConnection::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FANNConnection::\_\_construct

(PECL fann >= 1.0.0)

FANNConnection::\_\_construct — Конструктор зв'язку

### Опис

public**FANNConnection::\_\_construct**(int`$from_neuron`, int`$to_neuron`, float`$weight`) .

Створює новий зв'язок та ініціалізує його параметри. Після створення зв'язку можна буде змінити лише його вагу.

### Список параметрів

`from_neuron`

Позиція стартового нейрону.

`to_neuron`

Позиція кінцевого нейрону.

`weight`

Вага зв'язку.
