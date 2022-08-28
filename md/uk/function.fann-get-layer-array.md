Отримує кількість нейронів у кожному шарі мережі

-   [« fann\_get\_errstr](function.fann-get-errstr.html)
    
-   [fann\_get\_learning\_momentum »](function.fann-get-learning-momentum.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Отримує кількість нейронів у кожному шарі мережі
    

# fanngetlayerarray

(PECL fann> = 1.0.0)

fanngetlayerarray — Отримує кількість нейронів у кожному шарі мережі

### Опис

```methodsynopsis
fann_get_layer_array(resource $ann): array
```

Отримує кількість нейронів у кожному шарі мережі.

Зміщення не включене, тому шари відповідають функцій fanncreate.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Масив чисел нейтронів у кожному шарі.