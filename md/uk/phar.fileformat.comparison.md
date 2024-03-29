---
navigation:
  - phar.fileformat.stub.md: « Заглушка Phar-файлу
  - phar.fileformat.tar.md: 'Phar-архіви, засновані на tar »'
  - index.md: PHP Manual
  - phar.fileformat.md: Чим відрізняється phar від tar-або zip-архіву?
title: 'Порівняння Phar, Tar та Zip'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Порівняння Phar, Tar та Zip

Що хорошого та поганого у трьох підтримуваних форматах файлу в модулі phar? У цій таблиці зроблено спробу вирішити це питання.

**Матриця функціоналу: Phar проти Tar проти Zip**

| Функционал | Phar | Tar | Zip |
| --- | --- | --- | --- |
| Стандартний формат файлу | Ні | Так | Так |
| Можливе виконання без модуля Phar [\[1\]](phar.fileformat.comparison.md#phar.fileformat.phartip) | Так | Ні | Ні |
| Пофайловий стиск | Так | Ні | Так |
| Стиснення всього архіву | Так | Так | Ні |
| Перевірка підпису всього архіву | Так | Так | Так |
| Підтримка веб-застосунків | Так | Так | Так |
| Пофайлові метадані | Так | Так | Так |
| Метадані всього архіву | Так | Так | Так |
| Створення/зміна архіву [\[2\]](phar.fileformat.comparison.md#phar.fileformat.phartip2) | Так | Так | Так |
| Повна підтримка всіх функцій - обертання потоку | Так | Так | Так |
| Може бути створено/змінено, навіть якщо phar.readonly=1 [\[3\]](phar.fileformat.comparison.md#phar.fileformat.phartip3) | Ні | Так | Так |

**Підказка**

\[ \] Без модуля Phar PHP може отримати прямий доступ до вмісту Phar-архіву лише в тому випадку, якщо в ньому використовується `заглушка`, яка витягує вміст phar-архіву. Заглушка, створена за допомогою [Phar::createDefaultStub()](phar.createdefaultstub.md), розпаковує phar-архів і запускає його вміст із тимчасового каталогу в тому випадку, якщо не було знайдено модуль phar.

**Підказка**

\[ \] Для доступу до запису потрібно, щоб було вимкнено параметр `phar.readonly` у php.ini або безпосередньо в консолі.

**Підказка**

\[3\] Тільки архіви tar та zip без `.phar` в імені файлу і без заглушки, що виконується. `.phar/stub.php` можуть бути створені, якщо phar.readonly=1.
