---
navigation:
  - function.fann-create-sparse.md: « fann\_create\_sparse
  - function.fann-create-standard.md: fann\_create\_standard »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_standard\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_standard\_array

(PECL fann >= 1.0.0)

fann\_create\_standard\_array - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження, використовуючи масив розмірів шарів

### Опис

```methodsynopsis
fann_create_standard_array(int $num_layers, array $layers): resource
```

Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження.

У кожному шарі буде зміщений нейрон (крім вихідного шару), і цей нейрон зміщення буде пов'язаний з усіма нейронами в наступному шарі. Працюючи в мережі вузли зміщення завжди випромінюють 1.

Щоб знищити нейронну мережу, скористайтеся функцією [fann\_destroy()](function.fann-destroy.md)

### Список параметрів

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`layers`

Масив розмірів шарів.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_create\_standard()](function.fann-create-standard.md) \- Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
-   [fann\_create\_sparse()](function.fann-create-sparse.md) \- створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fann\_create\_shortcut()](function.fann-create-shortcut.md) \- Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
