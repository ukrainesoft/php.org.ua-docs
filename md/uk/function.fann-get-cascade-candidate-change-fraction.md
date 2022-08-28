Повертає частку зміни каскаду кандидата

-   [« fann\_get\_cascade\_activation\_steepnesses](function.fann-get-cascade-activation-steepnesses.html)
    
-   [fann\_get\_cascade\_candidate\_limit »](function.fann-get-cascade-candidate-limit.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає частку зміни каскаду кандидата
    

# fanngetcascadecandidatechangefraction

(PECL fann> = 1.0.0)

fanngetcascadecandidatechangefraction - Повертає частку зміни каскаду кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_change_fraction(resource $ann): float
```

Частка зміни каскаду кандидата - це число від 0 до 1, що визначає, наскільки велике значення [fann\_get\_MSE()](function.fann-get-mse.html), що має змінитися в межах [fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.html) під час навчання нейронів-кандидатів, щоби навчання не застоювалося. Якщо навчання застоюється, навчання нейронів-кандидатів припиняється і вибирається найкращий кандидат.

Це означає, що якщо MSE не змінюється на частку **fanngetcascadecandidatechangefraction()** протягом періоду [fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.html), навчання нейронів-кандидатів припиняється, тому що навчання зупинилося.

Якщо частка зміни каскаду кандидатів мала, нейрони-кандидати навчатимуться більше, і якщо частка висока, вони навчатимуться менше.

Частка зміни каскаду за замовчуванням кандидата становить 0.01, що еквівалентно зміні MSE на 1%.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Частка зміни каскаду кандидата або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_cascade\_candidate\_change\_fraction()](function.fann-set-cascade-candidate-change-fraction.html) - встановлює частку каскадної зміни кандидата
-   [fann\_get\_MSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.html) - Повертає кількість періодів застою каскаду кандидата