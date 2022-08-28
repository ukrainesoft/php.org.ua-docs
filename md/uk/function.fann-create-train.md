Створює порожню структуру даних для навчання

-   [« fann\_create\_train\_from\_callback](function.fann-create-train-from-callback.html)
    
-   [fann\_descale\_input »](function.fann-descale-input.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Створює порожню структуру даних для навчання
    

# fanncreatetrain

(PECL fann> = 1.0.0)

fanncreatetrain — Створює порожню структуру даних для навчання

### Опис

```methodsynopsis
fann_create_train(int $num_data, int $num_input, int $num_output): resource
```

Створює порожню структуру даних на навчання.

### Список параметрів

`num_data`

Кількість тренувальних даних

`num_input`

Кількість входів на тренувальних даних

`num_output`

Кількість виходів на тренувальних даних

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.html) - Читає файл, у якому зберігаються дані навчання
-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_destroy\_train()](function.fann-destroy-train.html) - Знищує тренувальні дані
-   [fann\_save\_train()](function.fann-save-train.html) - Зберігає структуру навчання у файл