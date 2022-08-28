Перемішує навчальні дані у випадковому порядку

-   [« fann\_set\_weight](function.fann-set-weight.html)
    
-   [fann\_subset\_train\_data »](function.fann-subset-train-data.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
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