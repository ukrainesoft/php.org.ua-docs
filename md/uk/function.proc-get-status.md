---
navigation:
  - function.proc-close.html: « procclose
  - function.proc-nice.html: procnice »
  - index.md: PHP Manual
  - ref.exec.md: Функции запуска программ
title: procgetstatus
---
# procgetstatus

(PHP 5, PHP 7, PHP 8)

procgetstatus — Отримати інформацію про процес, відкритий [procopen()](function.proc-open.md)

### Опис

```methodsynopsis
proc_get_status(resource $process): array
```

**procgetstatus()** отримує дані про процес, відкритий за допомогою функції [procopen()](function.proc-open.md)

### Список параметрів

`process`

Дескриптор типу resource, відкритий за допомогою [procopen()](function.proc-open.md), що буде досліджуватися.

### Значення, що повертаються

Масив (array) із отриманою інформацією. Отримуваний масив містить такі елементи:

| элемент | тип | описание |
| --- | --- | --- |
| command | string | Рядок з командою, яка була передана функції [procopen()](function.proc-open.md) |
| pid | int | ідентифікатор процесу |
| running | bool | **`true`**, якщо процес все ще запущено, \*\*`false`\*\*якщо він був завершений. |
| signaled | bool | \*\*`true`\*\*якщо дочірній процес був завершений неперехопленим сигналом. Завжди встановлюється в **`false`** у Windows. |
| stopped | bool | \*\*`true`\*\*якщо дочірній процес був зупинений сигналом. Завжди встановлюється в **`false`** у Windows. |
| exitcode | int | Код повернення, що передається процесом (має значення лише в тому випадку, якщо `running` одно **`false`**). Тільки перший дзвінок цієї функції поверне реальне значення, наступні дзвінки будуть повертати `-1` |
| termsig | int | Номер сигналу, який змусив дочірній процес припинити його виконання (має значення лише в тому випадку, якщо `signaled` одно **`true`** |
| stopsig | int | Номер сигналу, який змусив дочірній процес зупинити його виконання (має значення лише в тому випадку, якщо `stopped` одно **`true`** |

### Дивіться також

-   [procopen()](function.proc-open.md) - Виконати команду та відкрити покажчик на файл для введення/виводу
