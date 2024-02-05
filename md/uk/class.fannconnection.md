---
navigation:
  - function.fann-train.md: « fann\_train
  - fannconnection.construct.md: 'FANNConnection::\_\_construct »'
  - index.md: PHP Manual
  - book.fann.md: FANN
title: Клас FANNConnection
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас FANNConnection

(No version information available, might only be in Git)

## Вступ

**FANNConnection** використовується для зв'язку нейронної мережі. Об'єкти цього класу використовуються у функціях [fann\_get\_connection\_array()](function.fann-get-connection-array.md) і [fann\_set\_weight\_array()](function.fann-set-weight-array.md)

## Огляд класів

```classsynopsis


    
    
     
      class FANNConnection
     
     {
    
    /* Свойства */
    
     public
      $from_neuron;

    public
      $to_neuron;

    public
      $weight;



    /* Методы */
    
   public __construct(int $from_neuron, int $to_neuron, float $weight)

    public getFromNeuron(): int
public getToNeuron(): int
public getWeight(): void
public setWeight(float $weight): void

   }
```

## Властивості

from\_neuron

Перший нейрон (початковий)

to\_neuron

Другий нейрон (кінцевий)

weight

Вага зв'язку

## Зміст

-   [FANNConnection::\_\_construct](fannconnection.construct.md) \- Конструктор зв'язку
-   [FANNConnection::getFromNeuron](fannconnection.getfromneuron.md)— Повертає позицію стартового нейрона
-   [FANNConnection::getToNeuron](fannconnection.gettoneuron.md)— Повертає позицію кінцевого нейрона
-   [FANNConnection::getWeight](fannconnection.getweight.md)— Повертає вагу зв'язку
-   [FANNConnection::setWeight](fannconnection.setweight.md) \- Встановлює вагу зв'язку
