---
navigation:
  - function.fann-create-standard.md: « fann\_create\_standard
  - function.fann-create-train.md: fann\_create\_train »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_train\_from\_callback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_train\_from\_callback

(PECL fann >= 1.0.0)

fann\_create\_train\_from\_callback — Створює структуру даних навчання із наданої користувачем функції

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

-   `num`\- Кількість навчальних даних
-   `num_input`\- кількість входів на тренувальних даних
-   `num_output`\- кількість виходів на тренувальних даних

Функція має повертати асоціативний масив із ключами `input`и`output` і двома значеннями масиву input та output.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**fann\_create\_train\_from\_callback()\*\*\*\*

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

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.md) \- Читає файл, у якому зберігаються дані навчання
-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_destroy\_train()](function.fann-destroy-train.md) \- Знищує тренувальні дані
-   [fann\_save\_train()](function.fann-save-train.md) \- Зберігає структуру навчання у файл
