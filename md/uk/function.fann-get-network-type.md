Отримує тип нейронної мережі

-   [« fanngetMSE](function.fann-get-mse.html)
    
-   [fanngetnuminput »](function.fann-get-num-input.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Отримує тип нейронної мережі
    

# fanngetnetworktype

(PECL fann> = 1.0.0)

fanngetnetworktype — Отримує тип нейронної мережі

### Опис

```methodsynopsis
fann_get_network_type(resource $ann): int
```

Отримує тип нейронної мережі, де вона була створена.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [типа сети](fann.constants.html#constants.fann-nettype) або **`false`** у разі виникнення помилки.