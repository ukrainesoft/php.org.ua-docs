Отримує загальну кількість нейронів у всій мережі

-   [« fanngettotalconnections](function.fann-get-total-connections.html)
    
-   [fanngettrainerrorfunction »](function.fann-get-train-error-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Отримує загальну кількість нейронів у всій мережі
    

# fanngettotalneurons

(PECL fann> = 1.0.0)

fanngettotalneurons — Отримує загальну кількість нейронів у всій мережі

### Опис

```methodsynopsis
fann_get_total_neurons(resource $ann): int
```

Отримує загальну кількість нейронів у всій мережі. Число також включає нейрони усунення, тому мережа 2-4-2 має 2+4+2 +2 (зміщення) = 10 нейронів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Загальна кількість нейронів у всій мережі або **`false`** у разі виникнення помилки.