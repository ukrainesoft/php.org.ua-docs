Клас FANNConnection

-   [« fanntrain](function.fann-train.html)
    
-   [FANNConnection::construct »](fannconnection.construct.html)
    
-   [PHP Manual](index.html)
    
-   [FANN](book.fann.html)
    
-   Клас FANNConnection
    

# Клас FANNConnection

(No version information available, might only be in Git)

## Вступ

**FANNConnection** використовується для зв'язку нейронної мережі. Об'єкти цього класу використовуються у функціях [fanngetconnectionarray()](function.fann-get-connection-array.html) і [fannsetweightarray()](function.fann-set-weight-array.html)

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

fromneuron

Перший нейрон (початковий)

тоneuron

Другий нейрон (кінцевий)

weight

Вага зв'язку

## Зміст

-   [FANNConnection::construct](fannconnection.construct.html) - Конструктор зв'язку
-   [FANNConnection::getFromNeuron](fannconnection.getfromneuron.html) — Повертає позицію стартового нейрона
-   [FANNConnection::getToNeuron](fannconnection.gettoneuron.html) — Повертає позицію кінцевого нейрона
-   [FANNConnection::getWeight](fannconnection.getweight.html) — Повертає вагу зв'язку
-   [FANNConnection::setWeight](fannconnection.setweight.html) - Встановлює вагу зв'язку