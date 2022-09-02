---
navigation:
  - function.pcntl-wait.md: pcntlwait
  - function.pcntl-wexitstatus.md: pcntlwexitstatus »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwaitpid
---
# pcntlwaitpid

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwaitpid — Очікує чи повертає статус породженого дочірнього процесу

### Опис

```methodsynopsis
pcntl_waitpid(    int $process_id,    int &$status,    int $flags = 0,    array &$resource_usage = []): int
```

Функція очікування призупиняє виконання поточного процесу доти, доки дочірній процес, зазначений у аргументі `process_id`, не завершиться або доки не буде отримано сигнал, який завершує поточний процес або викликає функцію обробки сигналу.

Якщо дочірній процес, зазначений у аргументі `process_id`, вже завершився до часу виклику (так звані "зомбі" процеси), функція негайно поверне управління. Будь-які системні ресурси, що використовуються дочірнім процесом, будуть звільнені. Зверніться до вашого системного посібника waitpid(2) для уточнення специфіки роботи waitpid у вашій системі.

### Список параметрів

`process_id`

Аргумент `process_id` може приймати одне з наступних значень:

<table class="doctable table"><caption><strong>можливі значення аргументу <code class="parameter">process_id</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">&lt; -1</code></td><td>очікувати будь-який дочірній процес, у якого значення ідентифікатора групи процесів (group ID) дорівнює модулю значення аргументу |<code class=" parameter">process_id</code>|.</td></tr><tr><td><code class="literal">-1</code></td><td>очікувати будь-який дочірній процес; це така ж поведінка, що й у функції wait. ідентифікатор групи процесів (group ID) якого дорівнює ідентифікатору поточного процесу.</td><td>очікувати процес ID якого дорівнює <code class="parameter">process_id</code>.</td></tr></tbody></table>

> **Зауваження**
> 
> Вказівка `-1` в якості `process_id` - це аналог функції [pcntlwait()](function.pcntl-wait.md) (мінус `flags`

`status`

**pcntlwaitpid()** розмістить інформацію про статус за посиланням у аргументі `status`, який може бути переданий у такі функції: [pcntlwifexited()](function.pcntl-wifexited.md) [pcntlwifstopped()](function.pcntl-wifstopped.md) [pcntlwifsignaled()](function.pcntl-wifsignaled.md) [pcntlwexitstatus()](function.pcntl-wexitstatus.md) [pcntlwtermsig()](function.pcntl-wtermsig.md) і [pcntlwstopsig()](function.pcntl-wstopsig.md)

`flags`

Значення аргументу `flags` - це бітова маска, яка може набувати значення нуль або більше шляхом логічного об'єднання наступних констант:

<table class="doctable table"><caption><strong>Можливі значення для <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">WNOHANG</code></td><td>Негайно повернути управління, якщо жоден з дочірніх процесів не завершено</td></tr><tr><td>&lt; code class="literal"&gt;WUNTRACED</td><td>Повернути управління для зупинених дочірніх процесів, про статус яких ще не повідомлено</td></tr></tbody></table>

### Значення, що повертаються

[pcntlwait()](function.pcntl-wait.md) повертає ID завершеного дочірнього процесу, -1 у разі виникнення помилки або нуль, якщо **`WNOHANG`** було передано в аргумент `flags` і не було доступних дочірніх процесів.

### Дивіться також

-   [pcntlfork()](function.pcntl-fork.md) - Розгалужити (fork) поточний запущений процес
-   [pcntlsignal()](function.pcntl-signal.md) - Встановлення оброблювача сигналу
-   [pcntlwifexited()](function.pcntl-wifexited.md) - Перевіряє, чи код завершення процесу відповідає нормальному завершенню
-   [pcntlwifstopped()](function.pcntl-wifstopped.md) - Перевірити, чи зупинено дочірній процес
-   [pcntlwifsignaled()](function.pcntl-wifsignaled.md) - Перевірити, чи код завершення процесу завершення по сигналу
-   [pcntlwexitstatus()](function.pcntl-wexitstatus.md) - Отримати код повернення завершеного дочірнього процесу
-   [pcntlwtermsig()](function.pcntl-wtermsig.md) - Отримати сигнал, через який було примусово завершено дочірній процес
-   [pcntlwstopsig()](function.pcntl-wstopsig.md) - Отримати сигнал, через який було зупинено дочірній процес
