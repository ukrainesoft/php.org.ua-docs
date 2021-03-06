- [« fann_create_sparse_array](function.fann-create-sparse-array.md)
- [fann_create_standard_array »](function.fann-create-standard-array.md)

- [PHP Manual](index.md)
- [Функції Fann](ref.fann.md)
- Створює стандартну нейронну мережу зворотного розповсюдження,
яка не повністю підключена

# fann_create_sparse

(PECL fann = 1.0.0)

fann_create_sparse — Створює стандартну нейронну мережу зворотного
поширення, яка не повністю підключена

### Опис

**fann_create_sparse**(
float `$connection_rate`,
int `$num_layers`,
int `$num_neurons1`,
int `$num_neurons2`,
int `...$num_neuronsN`
): resource

Створює стандартну нейронну мережу зворотного розповсюдження, яка не
повністю підключено.

### Список параметрів

`connection_rate`
Швидкість з'єднання визначає, скільки з'єднань буде у мережі. Якщо
швидкість з'єднання встановлена на 1, мережа буде повністю підключена,
але якщо вона встановлена на 0,5, буде встановлена лише половина
з'єднань. Швидкість з'єднання 1 дасть той самий результат, що і
[fann_create_standard()](function.fann-create-standard.md).

`num_layers`
Загальна кількість шарів, включаючи вхідний та вихідний шар.

`num_neurons1`
Кількість нейронів у першому шарі.

`num_neurons2`
Кількість нейронів у другому шарі.

`num_neuronsN`
Кількість нейронів у інших шарах.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або
**`false`** у разі виникнення помилки.

### Дивіться також

- [fann_create_sparse_array()](function.fann-create-sparse-array.md) -
Створює стандартну нейронну мережу зворотного розповсюдження,
яка не повністю підключена, використовуючи масив розмірів шарів
- [fann_create_standard()](function.fann-create-standard.md) -
Створює стандартну повністю підключену нейронну мережу зворотного
поширення
- [fann_create_shortcut()](function.fann-create-shortcut.md) -
Створює стандартну нейронну мережу зворотного розповсюдження,
яка не повністю підключена та має швидкі з'єднання
