Отримує найбільший період кандидата

-   [« fann\_get\_cascade\_candidate\_stagnation\_epochs](function.fann-get-cascade-candidate-stagnation-epochs.html)
    
-   [fann\_get\_cascade\_max\_out\_epochs »](function.fann-get-cascade-max-out-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Отримує найбільший період кандидата
    

# fanngetcascademaxcandepochs

(PECL fann> = 1.0.0)

fanngetcascademaxcandepochs - Отримує найбільший період кандидата

### Опис

```methodsynopsis
fann_get_cascade_max_cand_epochs(resource $ann): int
```

Максимальний період кандидата визначає максимальну кількість періодів, у яких вхідні з'єднання з кандидатами можуть бути навчені перед додаванням нового нейрона-кандидата.

Максимальний період кандидата за умовчанням – 150.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальний період кандидата чи **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_cascade\_max\_cand\_epochs()](function.fann-set-cascade-max-cand-epochs.html) - встановлює найбільший період кандидата