Повертає крутість активації для нейрона, що поставляється, і номери шару.

-   [« fann\_get\_activation\_function](function.fann-get-activation-function.html)
    
-   [fann\_get\_bias\_array »](function.fann-get-bias-array.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає крутість активації для нейрона, що поставляється, і номери шару.
    

# fanngetactivationsteepness

(PECL fann> = 1.0.0)

fanngetactivationsteepness — Повертає крутість активації для нейрона, що поставляється, і номери шару.

### Опис

```methodsynopsis
fann_get_activation_steepness(resource $ann, int $layer, int $neuron): float
```

Отримує крутість активації для нейрона з номером `neuron` у шарі з номером `layer`, Вважаючи вхідний шар, як шар 0.

Неможливо отримати крутість активації для нейронів у вхідному шарі.

Крутизна функція активації говорить про те, як швидко функція активації переходить від мінімуму до максимуму. Високе значення функції активації також надасть більш агресивне навчання.

Під час навчання нейронних мереж, де вихідні значення мають бути на граничних значеннях (зазвичай 0 і 1, залежно від функції активації), можна використовувати крута функція активації (наприклад, 1,0).

Крутизна активації за замовчуванням – 0,5.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`layer`

Номер шару

`neuron`

Номер нейрона

### Значення, що повертаються

Крутизна активації для нейрона або -1, якщо нейрон не визначений у нейронній мережі, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_activation\_function()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару
-   [fann\_set\_activation\_steepness\_layer()](function.fann-set-activation-steepness-layer.html) - Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fann\_set\_activation\_steepness\_hidden()](function.fann-set-activation-steepness-hidden.html) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fann\_set\_activation\_steepness\_output()](function.fann-set-activation-steepness-output.html) - Встановлює крутість активації у вихідному шарі
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару