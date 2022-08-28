Повертає частку зміни виходу каскаду

-   [« fann\_get\_cascade\_num\_candidates](function.fann-get-cascade-num-candidates.html)
    
-   [fann\_get\_cascade\_output\_stagnation\_epochs »](function.fann-get-cascade-output-stagnation-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає частку зміни виходу каскаду
    

# fanngetcascadeoutputchangefraction

(PECL fann> = 1.0.0)

fanngetcascadeoutputchangefraction — Повертає частку зміни виходу каскаду

### Опис

```methodsynopsis
fann_get_cascade_output_change_fraction(resource $ann): float
```

Частка зміни виходу каскаду - це число від 0 до 1, що визначає, наскільки більша частина значення [fann\_get\_MSE()](function.fann-get-mse.html) має змінитися в [fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.html) під час навчання вихідних з'єднань, щоб навчання, щоб не застоювалося. Якщо навчання зупиниться, навчання вихідних з'єднань буде припинено та будуть підготовлені нові кандидати.

Це означає, що якщо MSE не змінюється на частку **fanngetcascadeoutputchangefraction()** протягом періоду [fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.html), Навчання вихідних з'єднань припиниться, тому що навчання зупинилося.

Якщо частка зміни виходу каскаду мала, вихідні з'єднання навчатимуться більше, і якщо частка висока, вони навчатимуться менше.

Частка зміни виходу каскаду за замовчуванням становить 0.01, що еквівалентно зміни MSE на 1%.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Частка зміни виходу каскаду або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_cascade\_output\_change\_fraction()](function.fann-set-cascade-output-change-fraction.html) - Встановлює частку зміни каскадних вихідних даних
-   [fann\_get\_MSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.html) - Повертає кількість каскадних періодів застою кандидатів