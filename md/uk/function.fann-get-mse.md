---
navigation:
  - function.fann-get-learning-rate.html: « fanngetlearningrate
  - function.fann-get-network-type.html: fanngetnetworktype »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetMSE
---
# fanngetMSE

(PECL fann> = 1.0.0)

fanngetMSE — Зчитує середньоквадратичну помилку мережі

### Опис

```methodsynopsis
fann_get_MSE(resource $ann): float
```

Зчитує середньоквадратичну помилку мережі.

Зчитує середньоквадратичну помилку мережі. Це значення обчислюється під час навчання або тестування і тому іноді може трохи відрізнятися, якщо вага була змінена з моменту останнього обчислення значення.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Середньоквадратична помилка або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanntestdata()](function.fann-test-data.md) - Тестування набору навчальних даних та обчислення MSE для нього
