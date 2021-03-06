- [« fann_get_bias_array](function.fann-get-bias-array.md)
- [fann_get_bit_fail »](function.fann-get-bit-fail.md)

- [PHP Manual](index.md)
- [Функції Fann](ref.fann.md)
- Повертає межу збою бітів, використану під час навчання

# fann_get_bit_fail_limit

(PECL fann = 1.0.0)

fann_get_bit_fail_limit — Повертає межу збою бітів, використану
під час навчання

### Опис

**fann_get_bit_fail_limit**(resource `$ann`): float

Повертає межу збою бітів, використану під час навчання.

Межа збою бітів використовується під час навчання, коли [функція зупинки](fann.constants.md#constants.fann-stopfunc) має значення
**`FANN_STOPFUNC_BIT`**.

Межа - це максимально допустима різниця між бажаним результатом та
фактичний результат під час тренування. Кожен вихід, який
розходиться більше цієї межі, вважається як біт зі збоєм. Ця різниця
ділиться на два під час роботи з симетричними функціями активації, так що
симетричні та не симетричні функції активації можуть використовувати один
і та сама межа.

Граничне значення стандартного збою становить 0,35.

### Список параметрів

`ann`
Ресурс нейронної мережі.

### Значення, що повертаються

Межа збою бітів або **`false`** у разі виникнення помилки.

### Дивіться також

- [fann_set_bit_fail_limit()](function.fann-set-bit-fail-limit.md) -
Встановлює межу помилок, що використовується під час навчання
