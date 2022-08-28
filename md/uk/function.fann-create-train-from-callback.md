Створює структуру даних навчання із наданої користувачем функції

-   [« fann\_create\_standard](function.fann-create-standard.html)
    
-   [fann\_create\_train »](function.fann-create-train.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Створює структуру даних навчання із наданої користувачем функції
    

# fanncreatetrainfromcallback

(PECL fann> = 1.0.0)

fanncreatetrainfromcallback — Створює структуру даних навчання із наданої користувачем функції

### Опис

```methodsynopsis
fann_create_train_from_callback(    int $num_data,    int $num_input,    int $num_output,    callable $user_function): resource
```

Створює структуру даних навчання із наданої користувачем функції. Оскільки навчальні дані є пронумерованими (дані 1, дані 2...), користувач повинен написати функцію, яка отримує номер набору навчальних даних (вхід, вихід) та повертає набір.

### Список параметрів

`num_data`

Кількість тренувальних даних

`num_input`

Кількість входів на тренувальних даних

`num_output`

Кількість виходів на тренувальних даних

`user_function`

Функція, надана користувачем із наступними параметрами:

-   `num` - Кількість навчальних даних
-   `num_input` - кількість входів на тренувальних даних
-   `num_output` - кількість виходів на тренувальних даних

Функція має повертати асоціативний масив із ключами `input` і `output` і двома значеннями масиву input та output.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **fanncreatetrainfromcallback()****

```php
<?php
function create_train_callback($num_data, $num_input, $num_output) {
    return array(
        "input" => array_fill(0, $num_input, 1),
        "output" => array_fill(0, $num_output, 1),
    );
}

$num_data = 3;
$num_input = 2;
$num_output = 1;
$train_data = fann_create_train_from_callback($num_data, $num_input, $num_output, "create_train_callback");
if ($train_data) {
    // Сделай что-нибудь с $train_data
}
?>
```

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.html) - Читає файл, у якому зберігаються дані навчання
-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_destroy\_train()](function.fann-destroy-train.html) - Знищує тренувальні дані
-   [fann\_save\_train()](function.fann-save-train.html) - Зберігає структуру навчання у файл