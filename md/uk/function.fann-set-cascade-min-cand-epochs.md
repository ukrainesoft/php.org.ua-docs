Встановлює найменший період кандидата

-   [« fannsetcascademaxoutepochs](function.fann-set-cascade-max-out-epochs.html)
    
-   [fannsetcascademinoutepochs »](function.fann-set-cascade-min-out-epochs.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
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

-   [fanngetcascademincandepochs()](function.fann-get-cascade-min-cand-epochs.html) - отримує найменший період кандидата