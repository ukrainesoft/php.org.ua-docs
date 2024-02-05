---
navigation:
  - function.flush.md: « flush
  - function.ob-end-clean.md: ob\_end\_clean »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_clean
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_clean

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ob\_clean - Очищає (стирає) вміст активного буфера виводу

### Опис

```methodsynopsis
ob_clean(): bool
```

Функція викликає обробник виведення (з прапором **`PHP_OUTPUT_HANDLER_CLEAN`**), видаляє повернене їм значення та очищає (стирає) вміст активного буфера виведення.

Функція не відключає активний буфер виводу, як це роблять функції [ob\_end\_clean()](function.ob-end-clean.md) і [ob\_get\_clean()](function.ob-get-clean.md)

Функция**ob\_clean()** завершиться невдало, якщо активний буфер виведення було запущено без прапора **`PHP_OUTPUT_HANDLER_CLEANABLE`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо функція завершується невдало, вона видає помилку рівня **`E_NOTICE`**

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [ob\_get\_contents()](function.ob-get-contents.md) \- Повертає вміст буфера виводу
-   [ob\_end\_clean()](function.ob-end-clean.md) \- Очищає (стирає) вміст активного буфера виведення та відключає його
-   [ob\_get\_clean()](function.ob-get-clean.md) \- Отримує вміст активного буфера виводу та вимикає його
-   [ob\_flush()](function.ob-flush.md) \- Скидає (відправляє) повернене активним обробником висновку значення
