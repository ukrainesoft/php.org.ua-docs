---
navigation:
  - function.fann-save-train.md: « fann\_save\_train
  - function.fann-scale-input-train-data.md: fann\_scale\_input\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_save
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_save

(PECL fann >= 1.0.0)

fann\_save — Зберігає всю мережу у конфігураційному файлі

### Опис

```methodsynopsis
fann_save(resource $ann, string $configuration_file): bool
```

Зберігає всю мережу файл конфігурації.

Файл конфігурації містить всю інформацію про нейронну мережу і дозволяє функції [fann\_create\_from\_file()](function.fann-create-from-file.md) створювати точну копію нейронної мережі та всіх параметрів, пов'язаних з нейронною мережею.

Три параметри ([fann\_set\_callback()](function.fann-set-callback.md) [fann\_set\_error\_log()](function.fann-set-error-log.md) **fann\_set\_user\_data()**) НЕ зберігаються у файл, тому що їх не можна безпечно перенести в інше місце. Також не зберігаються часові параметри, згенеровані під час навчання, такі як [fann\_get\_MSE()](function.fann-get-mse.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`configuration_file`

Шлях до конфігураційного файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_create\_from\_file()](function.fann-create-from-file.md) \- Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу
