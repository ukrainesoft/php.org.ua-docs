---
navigation:
  - function.pcntl-unshare.md: pcntlunshare
  - function.pcntl-waitpid.md: pcntlwaitpid »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwait
---
# pcntlwait

(PHP 5, PHP 7, PHP 8)

pcntlwait — Очікує чи повертає статус породженого дочірнього процесу

### Опис

```methodsynopsis
pcntl_wait(int &$status, int $flags = 0, array &$resource_usage = []): int
```

Функція очікування призупиняє виконання поточного процесу до тих пір, поки дочірній процес не завершиться або поки не буде отримано сигнал, який завершує поточний процес або викликає функцію обробки сигналу. Якщо дочірній процес вже завершився на час виклику (так звані "зомбі" процеси), функція негайно поверне керування. Зверніться до вашого системного посібника (man) wait(2) для уточнення специфіки роботи wait у вашій системі.

> **Зауваження**
> 
> Ця функція еквівалентна виклику [pcntlwaitpid()](function.pcntl-waitpid.md) з аргументом `process_id` рівним `-1` і без аргументу `flags`

### Список параметрів

`status`

**pcntlwait()** розмістить інформацію про статус за посиланням у аргументі `status`, який може бути переданий у такі функції: [pcntlwifexited()](function.pcntl-wifexited.md) [pcntlwifstopped()](function.pcntl-wifstopped.md) [pcntlwifsignaled()](function.pcntl-wifsignaled.md) [pcntlwexitstatus()](function.pcntl-wexitstatus.md) [pcntlwtermsig()](function.pcntl-wtermsig.md) і [pcntlwstopsig()](function.pcntl-wstopsig.md)

`flags`

Якщо системний виклик wait3 (man 2 wait3) доступний у вашій системі (як правило, у BSD-подібних системах), ви можете задати необов'язковий аргумент `flags`. Якщо цей параметр не заданий, буде використано стандартний системний дзвінок wait. Якщо системний виклик wait3 не є доступним для вашої системи, передача значення аргументу `flags` не матиме значення. Значення аргументу `flags` - це бітова маска, яка може набувати значення нуль або більше шляхом логічного об'єднання наступних констант:

<table class="doctable table"><caption><strong>Можливі значення для <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">WNOHANG</code></td><td>Негайно повернути управління, якщо жоден з дочірніх процесів не завершено</td></tr><tr><td>&lt; code class="literal"&gt;WUNTRACED</td><td>Повернути управління для зупинених дочірніх процесів, про статус яких ще не повідомлено</td></tr></tbody></table>

### Значення, що повертаються

**pcntlwait()** повертає ID завершеного дочірнього процесу, -1 у разі виникнення помилки або нуль, якщо `WNOHANG` було передано в аргумент `options` (На системах з доступним системним викликом wait3) і не було доступних дочірніх процесів.

### Дивіться також

-   [pcntlfork()](function.pcntl-fork.md) - Розгалужити (fork) поточний запущений процес
-   [pcntlsignal()](function.pcntl-signal.md) - Встановлення оброблювача сигналу
-   [pcntlwifexited()](function.pcntl-wifexited.md) - Перевіряє, чи код завершення процесу відповідає нормальному завершенню
-   [pcntlwifstopped()](function.pcntl-wifstopped.md) - Перевірити, чи зупинено дочірній процес
-   [pcntlwifsignaled()](function.pcntl-wifsignaled.md) - Перевірити, чи код завершення процесу завершення по сигналу
-   [pcntlwexitstatus()](function.pcntl-wexitstatus.md) - Отримати код повернення завершеного дочірнього процесу
-   [pcntlwtermsig()](function.pcntl-wtermsig.md) - Отримати сигнал, через який було примусово завершено дочірній процес
-   [pcntlwstopsig()](function.pcntl-wstopsig.md) - Отримати сигнал, через який було зупинено дочірній процес
-   [pcntlwaitpid()](function.pcntl-waitpid.md) - Очікує чи повертає статус породженого дочірнього процесу
