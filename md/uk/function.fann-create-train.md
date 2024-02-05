---
navigation:
  - function.fann-create-train-from-callback.md: « fann\_create\_train\_from\_callback
  - function.fann-descale-input.md: fann\_descale\_input »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_train
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_train

(PECL fann >= 1.0.0)

fann\_create\_train — Створює порожню структуру даних для навчання

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

Повертає ресурс (resource) навчальних даних, або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.md) \- Читає файл, у якому зберігаються дані навчання
-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_destroy\_train()](function.fann-destroy-train.md) \- Знищує тренувальні дані
-   [fann\_save\_train()](function.fann-save-train.md) \- Зберігає структуру навчання у файл
