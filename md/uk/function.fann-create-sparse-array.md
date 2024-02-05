---
navigation:
  - function.fann-create-shortcut.md: « fann\_create\_shortcut
  - function.fann-create-sparse.md: fann\_create\_sparse »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_sparse\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_sparse\_array

(PECL fann >= 1.0.0)

fann\_create\_sparse\_array - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена, використовуючи масив розмірів шарів

### Опис

```methodsynopsis
fann_create_sparse_array(float $connection_rate, int $num_layers, array $layers): resource
```

Створює стандартну нейронну мережу зворотного поширення, яка повністю підключена, використовуючи масив розмірів шарів.

### Список параметрів

`connection_rate`

Швидкість з'єднання визначає, скільки з'єднань буде в мережі. Якщо швидкість підключення встановлена ​​на 1, мережа буде повністю підключена, але якщо вона встановлена ​​на 0,5, буде встановлена ​​лише половина з'єднань. Швидкість з'єднання 1 дасть той же результат, що і [fann\_create\_standard()](function.fann-create-standard.md)

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`layers`

Масив розмірів шарів.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_create\_sparse()](function.fann-create-sparse.md) \- створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fann\_create\_standard()](function.fann-create-standard.md) \- Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
-   [fann\_create\_shortcut()](function.fann-create-shortcut.md) \- Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
