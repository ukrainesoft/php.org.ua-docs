---
navigation:
  - function.fann-set-cascade-weight-multiplier.html: « fannsetcascadeweightmultiplier
  - function.fann-set-input-scaling-params.html: fannsetinputscalingparams »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannseterrorlog
---
# fannseterrorlog

(PECL fann> = 1.0.0)

fannseterrorlog — Встановлює, де реєструються помилки

### Опис

```methodsynopsis
fann_set_error_log(resource $errdat, string $log_file): void
```

Встановлює, де реєструються помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

`log_file`

Шлях до файлу ліг.

### Значення, що повертаються

Не повертає жодного значення.
