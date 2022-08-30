Повертає кількість каскадних періодів застою кандидатів

-   [« fanngetcascadeoutputchangefraction](function.fann-get-cascade-output-change-fraction.html)
    
-   [fanngetcascadeweightmultiplier »](function.fann-get-cascade-weight-multiplier.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає кількість каскадних періодів застою кандидатів
    

# fanngetcascadeoutputstagnationepochs

(PECL fann> = 1.0.0)

fanngetcascadeoutputstagnationepochs - Повертає кількість каскадних періодів застою кандидатів

### Опис

```methodsynopsis
fann_get_cascade_output_stagnation_epochs(resource $ann): int
```

Кількість каскадних періодів застою кандидатів визначає кількість періодів навчання, яка буде продовжена без зміни оцінки MSE за допомогою [fanngetcascadeoutputchangefraction()](function.fann-get-cascade-output-change-fraction.html)

Дивіться додаткову інформацію про цей параметр у [fanngetcascadeoutputchangefraction()](function.fann-get-cascade-output-change-fraction.html)

За замовчуванням кількість періодів застою каскадного виводу дорівнює 12.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість каскадних періодів застою кандидатів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadeoutputstagnationepochs()](function.fann-set-cascade-output-stagnation-epochs.html) - встановлює кількість періодів стагнації каскадного виводу
-   [fanngetcascadeoutputchangefraction()](function.fann-get-cascade-output-change-fraction.html) - Повертає частку зміни виходу каскаду