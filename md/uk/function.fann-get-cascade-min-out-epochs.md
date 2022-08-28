Повертає мінімальну кількість періодів

-   [« fann\_get\_cascade\_min\_cand\_epochs](function.fann-get-cascade-min-cand-epochs.html)
    
-   [fann\_get\_cascade\_num\_candidate\_groups »](function.fann-get-cascade-num-candidate-groups.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає мінімальну кількість періодів
    

# fanngetcascademinoutepochs

(PECL fann> = 1.0.0)

fanngetcascademinoutepochs — Повертає мінімальну кількість періодів

### Опис

```methodsynopsis
fann_get_cascade_min_out_epochs(resource $ann): int
```

Мінімальна кількість періодів визначає кількість періодів, у яких вихідні з'єднання мають бути навчені після додавання нового нейрона-кандидата.

Мінімальна кількість періодів за замовчуванням – 50.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Мінімальна кількість періодів або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_cascade\_min\_out\_epochs()](function.fann-set-cascade-min-out-epochs.html) - Встановлює мінімальні епохи вихідних даних