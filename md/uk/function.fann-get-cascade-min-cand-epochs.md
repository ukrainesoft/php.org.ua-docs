Отримує найменший період кандидата

-   [« fann\_get\_cascade\_max\_out\_epochs](function.fann-get-cascade-max-out-epochs.html)
    
-   [fann\_get\_cascade\_min\_out\_epochs »](function.fann-get-cascade-min-out-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Отримує найменший період кандидата
    

# fanngetcascademincandepochs

(PECL fann> = 1.0.0)

fanngetcascademincandepochs - Отримує найменший період кандидата

### Опис

```methodsynopsis
fann_get_cascade_min_cand_epochs(resource $ann): int
```

Мінімальний період кандидата визначає мінімальну кількість періодів, у яких вхідні з'єднання з кандидатами можуть бути навчені перед додаванням нового нейрона-кандидата.

Мінімальний період кандидата за замовчуванням – 50.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Мінімальний період кандидата або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_cascade\_min\_cand\_epochs()](function.fann-set-cascade-min-cand-epochs.html) - встановлює найменший період кандидата