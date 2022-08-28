Встановлює найменший період кандидата

-   [« fann\_set\_cascade\_max\_out\_epochs](function.fann-set-cascade-max-out-epochs.html)
    
-   [fann\_set\_cascade\_min\_out\_epochs »](function.fann-set-cascade-min-out-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює найменший період кандидата
    

# fannsetcascademincandepochs

(PECL fann> = 1.0.0)

fannsetcascademincandepochs - Встановлює найменший період кандидата

### Опис

```methodsynopsis
fann_set_cascade_min_cand_epochs(resource $ann, int $cascade_min_cand_epochs): bool
```

Встановлює найменший період кандидата.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_min_cand_epochs`

Найменший період кандидата.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_cascade\_min\_cand\_epochs()](function.fann-get-cascade-min-cand-epochs.html) - отримує найменший період кандидата