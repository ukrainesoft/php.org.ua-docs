- [« fann_set_sarprop_temperature](function.fann-set-sarprop-temperature.md)
- [fann_set_scaling_params »](function.fann-set-scaling-params.md)

- [PHP Manual](index.md)
- [Функції Fann](ref.fann.md)
- Встановлює зміщення загасання sarprop

# fann_set_sarprop_weight_decay_shift

(PECL fann = 1.0.0)

fann_set_sarprop_weight_decay_shift — Встановлює зсув загасання
sarprop

### Опис

**fann_set_sarprop_weight_decay_shift**(resource `$ann`, float
`$sarprop_weight_decay_shift`): bool

Встановлює усунення загасання sarprop.

### Список параметрів

`ann`
Ресурс нейронної мережі.

`sarprop_weight_decay_shift`
Зміщення загасання sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** у
інакше.

### Примітки

> **Примітка**:
>
> Функція доступна лише в тому випадку, якщо модуль fann був зібраний для
> libfann = 2.2.

### Дивіться також

- [fann_get_sarprop_weight_decay_shift()](function.fann-get-sarprop-weight-decay-shift.md) -
Повертає зсув зменшення ваги sarprop
