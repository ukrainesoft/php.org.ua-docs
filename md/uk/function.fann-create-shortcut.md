---
navigation:
  - function.fann-create-shortcut-array.md: « fann\_create\_shortcut\_array
  - function.fann-create-sparse-array.md: fann\_create\_sparse\_array »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_shortcut
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_shortcut

(PECL fann >= 1.0.0)

fann\_create\_shortcut — Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання.

### Опис

```methodsynopsis
fann_create_shortcut(    int $num_layers,    int $num_neurons1,    int $num_neurons2,    int ...$num_neuronsN): resource
```

Створює стандартну нейронну мережу зворотного розповсюдження, яка повністю підключена і має з'єднання швидкого доступу.

З'єднання швидкого доступу – це з'єднання, що пропускають шари. Повністю підключена мережа зі з'єднаннями швидкого доступу - це мережа, де всі нейрони пов'язані з усіма нейронами більш пізніх рівнях. Включаючи прямі з'єднання від вхідного шару до вихідного шару.

### Список параметрів

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`num_neurons1`

Кількість нейронів у першому шарі.

`num_neurons2`

Кількість нейронів у другому шарі.

`num_neuronsN`

Кількість нейронів у наступних шарах.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_create\_shortcut\_array()](function.fann-create-shortcut-array.md) \- Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
-   [fann\_create\_sparse()](function.fann-create-sparse.md) \- створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fann\_create\_standard()](function.fann-create-standard.md) \- Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
