---
navigation:
  - function.fann-create-train-from-callback.html: « fanncreatetrainfromcallback
  - function.fann-descale-input.html: fanndescaleinput »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreatetrain
---
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

-   [fannreadtrainfromfile()](function.fann-read-train-from-file.md) - Читає файл, у якому зберігаються дані навчання
-   [fanntrainвінdata()](function.fann-train-on-data.md) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanndestroytrain()](function.fann-destroy-train.md) - Знищує тренувальні дані
-   [fannsavetrain()](function.fann-save-train.md) - Зберігає структуру навчання у файл
