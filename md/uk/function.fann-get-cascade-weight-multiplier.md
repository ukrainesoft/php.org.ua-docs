Повертає множник ваги

-   [« fanngetcascadeoutputstagnationepochs](function.fann-get-cascade-output-stagnation-epochs.html)
    
-   [fanngetconnectionarray »](function.fann-get-connection-array.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає множник ваги
    

# fanngetcascadeweightmultiplier

(PECL fann> = 1.0.0)

fanngetcascadeweightmultiplier — Повертає множник ваги

### Опис

```methodsynopsis
fann_get_cascade_weight_multiplier(resource $ann): float
```

Множник ваги - це параметр, який використовується для множення ваги нейрона-кандидата перед додаванням нейрона до нейронної мережі. Цей параметр зазвичай знаходиться в діапазоні від 0 до 1 і використовується, щоб зробити тренування менш агресивним.

Множник ваги за промовчанням дорівнює 0.4.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Множник ваги або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadeweightmultiplier()](function.fann-set-cascade-weight-multiplier.html) - Встановлює множник ваги