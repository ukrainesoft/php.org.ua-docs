Створює копію структури fann

-   [« fann\_clear\_scaling\_params](function.fann-clear-scaling-params.html)
    
-   [fann\_create\_from\_file »](function.fann-create-from-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Створює копію структури fann
    

# fanncopy

(PECL fann> = 1.0.0)

fanncopy — Створює копію структури fann

### Опис

```methodsynopsis
fann_copy(resource $ann): resource
```

Створює копію структури fann.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

У разі успішного виконання повертає копію ресурсу нейронного ланцюга або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_test()](function.fann-test.html) - Тестування з набором вхідних даних та бажаним результатом