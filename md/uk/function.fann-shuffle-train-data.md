Перемішує навчальні дані у випадковому порядку

-   [« fannsetweight](function.fann-set-weight.html)
    
-   [fannsubsettraindata »](function.fann-subset-train-data.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Перемішує навчальні дані у випадковому порядку
    

# fannshuffletraindata

(PECL fann> = 1.0.0)

fannshuffletraindata — Перемішує навчальні дані у випадковому порядку

### Опис

```methodsynopsis
fann_shuffle_train_data(resource $train_data): bool
```

Перемішує навчальні дані у випадковому порядку. Рекомендується використовувати при інкрементальному навчанні, але не впливає на пакетне навчання.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.