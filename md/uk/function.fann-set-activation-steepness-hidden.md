Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах

-   [« fannsetactivationfunction](function.fann-set-activation-function.html)
    
-   [fannsetactivationsteepnesslayer »](function.fann-set-activation-steepness-layer.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
    

# fannsetactivationsteepnesshidden

(PECL fann> = 1.0.0)

fannsetactivationsteepnesshidden - Встановлює крутизну крутизни активації для всіх нейронів у всіх прихованих шарах

### Опис

```methodsynopsis
fann_set_activation_steepness_hidden(resource $ann, float $activation_steepness): bool
```

Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_steepness`

Крутизна активації.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fannsetactivationsteepnesslayer()](function.fann-set-activation-steepness-layer.html) - Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fannsetactivationsteepnessoutput()](function.fann-set-activation-steepness-output.html) - Встановлює крутість активації у вихідному шарі
-   [fanngetactivationsteepness()](function.fann-get-activation-steepness.html) - Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару