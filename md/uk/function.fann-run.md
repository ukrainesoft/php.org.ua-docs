---
navigation:
  - function.fann-reset-mse.md: « fann\_reset\_MSE
  - function.fann-save-train.md: fann\_save\_train »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_run
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_run

(PECL fann >= 1.0.0)

fann\_run — Запускає нейронну мережу із заданими даними

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

Масив вихідних даних, або \*\*`false`\*\*в случае возникновения ошибки.
