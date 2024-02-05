---
navigation:
  - function.pcntl-unshare.md: « pcntl\_unshare
  - function.pcntl-waitpid.md: pcntl\_waitpid »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wait
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wait

(PHP 5, PHP 7, PHP 8)

pcntl\_wait — Очікує чи повертає статус породженого дочірнього процесу

### Опис

```methodsynopsis
pcntl_wait(int &$status, int $flags = 0, array &$resource_usage = []): int
```

Функція очікування призупиняє виконання поточного процесу до тих пір, поки дочірній процес не завершиться або поки не буде отримано сигнал, який завершує поточний процес або викликає функцію обробки сигналу. Якщо дочірній процес вже завершився на час виклику (так звані "зомбі" процеси), функція негайно поверне керування. Зверніться до вашого системного посібника (man) wait(2) для уточнення специфіки роботи wait у вашій системі.

> **Зауваження** :
> 
> Ця функція еквівалентна виклику [pcntl\_waitpid()](function.pcntl-waitpid.md) з аргументом `process_id` рівним `-1`и без аргумента`flags`

### Список параметрів

`status`

**pcntl\_wait()** розмістити інформацію про статус за посиланням у аргументі `status`, який може бути переданий у такі функції: [pcntl\_wifexited()](function.pcntl-wifexited.md) [pcntl\_wifstopped()](function.pcntl-wifstopped.md) [pcntl\_wifsignaled()](function.pcntl-wifsignaled.md) [pcntl\_wexitstatus()](function.pcntl-wexitstatus.md) [pcntl\_wtermsig()](function.pcntl-wtermsig.md) і [pcntl\_wstopsig()](function.pcntl-wstopsig.md)

`flags`

Якщо системний виклик wait3 (man 2 wait3) доступний у вашій системі (як правило, у BSD-подібних системах), ви можете задати необов'язковий аргумент `flags`. Якщо цей параметр не заданий, буде використано стандартний системний дзвінок wait. Якщо системний дзвінок wait3 недоступний для вашої системи, передача значення аргументу `flags`не будет иметь значения. Значение аргумента`flags` - це бітова маска, яка може набувати значення нуль або більше шляхом логічного об'єднання наступних констант:

<table class="doctable table"><caption><strong>Можливі значення для <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">WNOHANG</code></td><td>Негайно повернути керування, якщо жоден з дочірніх процесів не завершено</td></tr><tr><td>&lt; code class="literal"&gt;WUNTRACED</td><td>Повернути управління для зупинених дочірніх процесів, про статус яких ще не повідомлено</td></tr></tbody></table>

### Значення, що повертаються

**pcntl\_wait()** повертає ID завершеного дочірнього процесу, -1 у разі виникнення помилки або нуль, якщо `WNOHANG` було передано в аргумент `options` (На системах з доступним системним викликом wait3) і не було доступних дочірніх процесів.

### Дивіться також

-   [pcntl\_fork()](function.pcntl-fork.md) \- Розгалужити (fork) поточний запущений процес
-   [pcntl\_signal()](function.pcntl-signal.md) \- Встановлення оброблювача сигналу
-   [pcntl\_wifexited()](function.pcntl-wifexited.md) \- Перевіряє, чи код завершення процесу відповідає нормальному завершенню
-   [pcntl\_wifstopped()](function.pcntl-wifstopped.md) \- Перевірити, чи зупинено дочірній процес
-   [pcntl\_wifsignaled()](function.pcntl-wifsignaled.md) \- Перевірити, чи код завершення процесу завершення по сигналу
-   [pcntl\_wexitstatus()](function.pcntl-wexitstatus.md) \- Отримати код повернення завершеного дочірнього процесу
-   [pcntl\_wtermsig()](function.pcntl-wtermsig.md) \- Отримати сигнал, через який було примусово завершено дочірній процес
-   [pcntl\_wstopsig()](function.pcntl-wstopsig.md) \- Отримати сигнал, через який було зупинено дочірній процес
-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
