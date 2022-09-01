---
navigation:
  - function.fann-get-activation-function.html: « fanngetactivationfunction
  - function.fann-get-bias-array.html: fanngetbiasarray »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetactivationsteepness
---
# fanngetactivationsteepness

(PECL fann> = 1.0.0)

fanngetactivationsteepness — Повертає крутість активації для нейрона, що поставляється, і номери шару.

### Опис

```methodsynopsis
fann_get_activation_steepness(resource $ann, int $layer, int $neuron): float
```

Отримує крутість активації для нейрона з номером `neuron` у шарі з номером `layer`, Вважаючи вхідний шар, як шар 0.

Неможливо отримати крутість активації для нейронів у вхідному шарі.

Крутизна функція активації говорить про те, як швидко функція активації переходить від мінімуму до максимуму. Високе значення функції активації також надасть більш агресивне навчання.

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

Крутизна активації для нейрона або -1, якщо нейрон не визначений у нейронній мережі, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetactivationfunction()](function.fann-set-activation-function.md) - Встановлює функцію активації для зазначеного нейрона та шару
-   [fannsetactivationsteepnesslayer()](function.fann-set-activation-steepness-layer.md) - Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fannsetactivationsteepnesshidden()](function.fann-set-activation-steepness-hidden.md) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fannsetactivationsteepnessoutput()](function.fann-set-activation-steepness-output.md) - Встановлює крутість активації у вихідному шарі
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.md) - Встановлює крутість активації для вказаного нейрона та номера шару
