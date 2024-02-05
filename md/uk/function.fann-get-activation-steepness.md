---
navigation:
  - function.fann-get-activation-function.md: « fann\_get\_activation\_function
  - function.fann-get-bias-array.md: fann\_get\_bias\_array »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_activation\_steepness
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_activation\_steepness

(PECL fann >= 1.0.0)

fann\_get\_activation\_steepness — Повертає крутість активації для нейрона, що поставляється, і номери шару.

### Опис

```methodsynopsis
fann_get_activation_steepness(resource $ann, int $layer, int $neuron): float
```

Отримує крутість активації для нейрона з номером `neuron` у шарі з номером `layer`, Вважаючи вхідний шар, як шар 0.

Неможливо отримати крутість активації для нейронів у вхідному шарі.

Крутизна функції активації говорить про те, як швидко функція активації переходить від мінімуму до максимуму. Високе значення функції активації також надасть більш агресивне навчання.

Під час навчання нейронних мереж, де вихідні значення мають бути на граничних значеннях (зазвичай 0 і 1, залежно від функції активації), можна використовувати крута функція активації (наприклад, 1,0).

Крутизна активації за замовчуванням – 0,5.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`layer`

Номер шару

`neuron`

Номер нейрона

### Значення, що повертаються

Крутизна активації для нейрона або -1, якщо нейрон не визначений у нейронній мережі, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
-   [fann\_set\_activation\_steepness\_layer()](function.fann-set-activation-steepness-layer.md) \- Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fann\_set\_activation\_steepness\_hidden()](function.fann-set-activation-steepness-hidden.md) \- Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fann\_set\_activation\_steepness\_output()](function.fann-set-activation-steepness-output.md) \- Встановлює крутість активації у вихідному шарі
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.md) \- Встановлює крутість активації для вказаного нейрона та номера шару
