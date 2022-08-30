Повертає частку зміни виходу каскаду

-   [« fanngetcascadenumcandidates](function.fann-get-cascade-num-candidates.html)
    
-   [fanngetcascadeoutputstagnationepochs »](function.fann-get-cascade-output-stagnation-epochs.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Повертає частку зміни виходу каскаду
    

# fanngetcascadeoutputchangefraction

(PECL fann> = 1.0.0)

fanngetcascadeoutputchangefraction — Повертає частку зміни виходу каскаду

### Опис

```methodsynopsis
fann_get_cascade_output_change_fraction(resource $ann): float
```

Частка зміни виходу каскаду - це число від 0 до 1, що визначає, наскільки більша частина значення [fanngetMSE()](function.fann-get-mse.html) має змінитися в [fanngetcascadeoutputstagnationepochs()](function.fann-get-cascade-output-stagnation-epochs.html) під час навчання вихідних з'єднань, щоб навчання, щоб не застоювалося. Якщо навчання зупиниться, навчання вихідних з'єднань буде припинено та будуть підготовлені нові кандидати.

Це означає, що якщо MSE не змінюється на частку **fanngetcascadeoutputchangefraction()** протягом періоду [fanngetcascadeoutputstagnationepochs()](function.fann-get-cascade-output-stagnation-epochs.html), Навчання вихідних з'єднань припиниться, тому що навчання зупинилося.

Якщо частка зміни виходу каскаду мала, вихідні з'єднання навчатимуться більше, і якщо частка висока, вони навчатимуться менше.

Частка зміни виходу каскаду за замовчуванням становить 0.01, що еквівалентно зміни MSE на 1%.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Частка зміни виходу каскаду або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadeoutputchangefraction()](function.fann-set-cascade-output-change-fraction.html) - Встановлює частку зміни каскадних вихідних даних
-   [fanngetMSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fanngetcascadeoutputstagnationepochs()](function.fann-get-cascade-output-stagnation-epochs.html) - Повертає кількість каскадних періодів застою кандидатів