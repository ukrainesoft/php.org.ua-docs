---
navigation:
  - function.fann-reset-mse.html: « fannresetMSE
  - function.fann-save-train.html: fannsavetrain »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannrun
---
# fannrun

(PECL fann> = 1.0.0)

fannrun — Запускає нейронну мережу із заданими даними

### Опис

```methodsynopsis
fann_run(resource $ann, array $input): array
```

Запускає нейронну мережу із заданими даними, повертаючи масив виходів, номери яких відповідає номерам нейронів у вихідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних

### Значення, що повертаються

Масив вихідних даних, або **`false`** у разі виникнення помилки.
