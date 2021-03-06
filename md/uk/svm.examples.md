- [« Типи ресурсів](svm.resources.md)
- [SVM »](class.svm.md)

- [PHP Manual](index.md)
- [SVM](book.svm.md)
- Приклади

# Приклади

Процес досить простий: задаємо параметри, надаємо навчальні
дані, на основі яких буде створено модель, а потім робимо прогнози,
засновані на цій моделі. Набір стандартних параметрів гарантує
отримання будь-якого результату практично для будь-яких вхідних
даних, так що на ньому зупинятись не будемо і відразу перейдемо до
навчальним даним.

Є три шляхи надання навчальних даних: файл, потік та масив.
Якщо дані надаються за допомогою файлу або потоку, то на кожній
рядку повинен міститися один навчальний приклад, відформатований
наступним чином: на початку має бути ціле число (зазвичай 1 або -1),
це число позначається терміном "клас", а слідом за ним перерахування
пар ознака: значення в порядку збільшення ознаки. Ознаки мають бути
цілими числами, які значення раціональними, зазвичай, на діапазоні 0-1.
Наприклад:

-1 1:0.43 3:0.12 9284:0.2

У проблемі класифікації документів, наприклад, під час перевірки листа на
спам, кожен рядок має представляти один документ. Для завдання
перевірки на спам нам знадобиться два класи, -1 для спаму та 1 для
нормального листа. Кожна ознака має означати якесь слово, яке
значення - важливість цього слова в документі (можливо, частота
появи щодо довжини елемента). Ознаки зі значенням 0 (тобто.
слово в документі не зустрічається) просто не включаємо до набору.

У разі використання масиву дані повинні бути представлені у вигляді
масиву масивів, в якому кожен вкладений масив повинен першим
елементом містити клас, а всі наступні елементи містити пари
"ознака" = "значення".

Ці дані передаються навчальною функцією класу SVM, яка в результаті
поверне модель (SVMModel).

Створена модель може використовуватися для побудови припущень про
класі нових об'єктів, описаних ознаками та його значеннями. Дані, на
основі яких робляться припущення, повинні бути передані функції
моделі в тому ж форматі, що описаний вище, але без вказівки їхнього класу
(тобто без першого елемента), яка поверне гаданий клас,
підходящий під ці дані.

Модель згодом можна зберігати та завантажувати за допомогою функцій,
приймають шлях до файлу як параметр.

**Приклад #1 Навчання з масиву**

`<?php$data = array(    array(-1, 1 => 0.43, 3 => 0.12, 9284 => 0.2),     array(1, 1 =>  ) );$svm = new SVM();$model = $svm->train($data);$data = array(1 => 0.43, 3 => 0.12, 9284 => 0.2);$$ >predict($data);var_dump($result);$model->save('model.svm');?> `

Результатом виконання цього прикладу буде щось подібне:

int(-1)

**Приклад #2 Навчання з файлу**

` <?php$svm = new SVM();$model = $svm->train("traindata.txt");?> `
