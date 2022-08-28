Встановлює вагу зв'язку

-   [« FANNConnection::getWeight](fannconnection.getweight.html)
    
-   [Igbinary »](book.igbinary.html)
    
-   [PHP Manual](index.html)
    
-   [FANNConnection](class.fannconnection.html)
    
-   Встановлює вагу зв'язку
    

# FANNConnection::setWeight

(PECL fann> = 1.0.0)

FANNConnection::setWeight — Встановлює вагу зв'язку

### Опис

```methodsynopsis
public FANNConnection::setWeight(float $weight): void
```

Встановлює вагу зв'язку.

Цей метод відрізняється від [fann\_set\_weight()](function.fann-set-weight.html). Він не оновлює значення ваги мережі. Значення в мережі оновиться лише після дзвінка [fann\_set\_weight\_array()](function.fann-set-weight-array.html)

### Список параметрів

`weight`

Вага зв'язку.

### Значення, що повертаються

Не повертає жодного значення.