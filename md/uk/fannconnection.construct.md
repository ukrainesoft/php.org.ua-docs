Конструктор зв'язку

-   [« FANNConnection](class.fannconnection.md)
    
-   [FANNConnection::getFromNeuron »](fannconnection.getfromneuron.md)
    
-   [PHP Manual](index.md)
    
-   [FANNConnection](class.fannconnection.md)
    
-   Конструктор зв'язку
    

# FANNConnection::construct

(PECL fann> = 1.0.0)

FANNConnection::construct — Конструктор зв'язку

### Опис

public **FANNConnection::construct**(int `$from_neuron`, int `$to_neuron`, float `$weight`

Створює новий зв'язок та ініціалізує його параметри. Після створення зв'язку можна буде змінити лише його вагу.

### Список параметрів

`from_neuron`

Позиція стартового нейрона.

`to_neuron`

Позиція кінцевого нейрону.

`weight`

Вага зв'язку.