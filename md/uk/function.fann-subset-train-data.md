Отримати копію підмножини з навчальних даних

-   [« fann\_shuffle\_train\_data](function.fann-shuffle-train-data.html)
    
-   [fann\_test\_data »](function.fann-test-data.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Отримати копію підмножини з навчальних даних
    

# fannsubsettraindata

(PECL fann> = 1.0.0)

fannsubsettraindata — Отримати копію підмножини з навчальних даних

### Опис

```methodsynopsis
fann_subset_train_data(resource $data, int $pos, int $length): resource
```

Повертає копію підмножини з навчальних даних resource, що починаються з `pos` та довжиною `length` елементів.

`fann_subset_train_data(train_data, 0, fann_length_train_data(train_data))` робить те саме, що і [fann\_duplicate\_train\_data()](function.fann-duplicate-train-data.html)

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`pos`

Початкова позиція.

`length`

Кількість елементів, що копіюються.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_duplicate\_train\_data()](function.fann-duplicate-train-data.html) - Повертає точну копію тренувальних даних