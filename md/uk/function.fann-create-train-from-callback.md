---
navigation:
  - function.fann-create-standard.md: « fanncreatestandard
  - function.fann-create-train.md: fanncreatetrain »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreatetrainfromcallback
---
# fanncreatetrainfromcallback

(PECL fann> = 1.0.0)

fanncreatetrainfromcallback — Створює структуру даних навчання із наданої користувачем функції

### Опис

```methodsynopsis
fann_create_train_from_callback(    int $num_data,    int $num_input,    int $num_output,    callable $user_function): resource
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
function create_train_callback($num_data, $num_input, $num_output) {
    return array(
        "input" => array_fill(0, $num_input, 1),
        "output" => array_fill(0, $num_output, 1),
    );
}

$num_data = 3;
$num_input = 2;
$num_output = 1;
$train_data = fann_create_train_from_callback($num_data, $num_input, $num_output, "create_train_callback");
if ($train_data) {
    // Сделай что-нибудь с $train_data
}
?>
```

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannreadtrainfromfile()](function.fann-read-train-from-file.md) - Читає файл, у якому зберігаються дані навчання
-   [fanntrainвінdata()](function.fann-train-on-data.md) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanndestroytrain()](function.fann-destroy-train.md) - Знищує тренувальні дані
-   [fannsavetrain()](function.fann-save-train.md) - Зберігає структуру навчання у файл
