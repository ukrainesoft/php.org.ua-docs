---
navigation:
  - function.fann-save-train.html: « fannsavetrain
  - function.fann-scale-input-train-data.html: fannscaleinputtraindata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsave
---
# fannsave

(PECL fann> = 1.0.0)

fannsave — Зберігає всю мережу у конфігураційному файлі

### Опис

```methodsynopsis
fann_save(resource $ann, string $configuration_file): bool
```

Зберігає всю мережу файл конфігурації.

Файл конфігурації містить всю інформацію про нейронну мережу і дозволяє функції [fanncreatefromfile()](function.fann-create-from-file.md) створювати точну копію нейронної мережі та всіх параметрів, пов'язаних з нейронною мережею.

Три параметри ([fannsetcallback()](function.fann-set-callback.html) [fannseterrorlog()](function.fann-set-error-log.html) **fannsetuserdata()**) НЕ зберігаються у файл, тому що їх не можна безпечно перенести в інше місце. Також не зберігаються часові параметри, згенеровані під час навчання, такі як [fanngetMSE()](function.fann-get-mse.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`configuration_file`

Шлях до конфігураційного файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanncreatefromfile()](function.fann-create-from-file.md) - Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу
