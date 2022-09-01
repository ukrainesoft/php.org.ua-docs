---
navigation:
  - pcntl.resources.md: « Типи ресурсів
  - pcntl.examples.md: Приклади »
  - index.md: PHP Manual
  - book.pcntl.md: PCNTL
title: Обумовлені константи
---
# Обумовлені константи

Функції управління процесами підтримують наступний список сигналів. Для детального ознайомлення зі стандартною поведінкою цих сигналів зверніться до системного посібника signal(7).

**Константи управління процесом**

**`WNOHANG`** (int)

**`WUNTRACED`** (int)

**Константи SIG**

**`SIG_IGN`** (int)

**`SIG_DFL`** (int)

**`SIG_ERR`** (int)

**`SIGHUP`** (int)

**`SIGINT`** (int)

**`SIGQUIT`** (int)

**`SIGILL`** (int)

**`SIGTRAP`** (int)

**`SIGABRT`** (int)

**`SIGIOT`** (int)

**`SIGBUS`** (int)

**`SIGFPE`** (int)

**`SIGKILL`** (int)

**`SIGUSR1`** (int)

**`SIGSEGV`** (int)

**`SIGUSR2`** (int)

**`SIGPIPE`** (int)

**`SIGALRM`** (int)

**`SIGTERM`** (int)

**`SIGSTKFLT`** (int)

**`SIGCLD`** (int)

**`SIGCHLD`** (int)

**`SIGCONT`** (int)

**`SIGSTOP`** (int)

**`SIGTSTP`** (int)

**`SIGTTIN`** (int)

**`SIGTTOU`** (int)

**`SIGURG`** (int)

**`SIGXCPU`** (int)

**`SIGXFSZ`** (int)

**`SIGVTALRM`** (int)

**`SIGPROF`** (int)

**`SIGWINCH`** (int)

**`SIGPOLL`** (int)

**`SIGIO`** (int)

**`SIGPWR`** (int)

**`SIGSYS`** (int)

**`SIGBABY`** (int)

**`SIG_BLOCK`** (int)

**`SIG_UNBLOCK`** (int)

**`SIG_SETMASK`** (int)

**`SI_USER`** (int)

**`SI_NOINFO`** (int)

**`SI_KERNEL`** (int)

**`SI_QUEUE`** (int)

**`SI_TIMER`** (int)

**`SI_MSGGQ`** (int)

**`SI_ASYNCIO`** (int)

**`SI_SIGIO`** (int)

**`SI_TKILL`** (int)

**Константи CLD**

**`CLD_EXITED`** (int)

**`CLD_KILLED`** (int)

**`CLD_DUMPED`** (int)

**`CLD_TRAPPED`** (int)

**`CLD_STOPPED`** (int)

**`CLD_CONTINUED`** (int)

**Константи TRAP**

**`TRAP_BRKPT`** (int)

**`TRAP_TRACE`** (int)

**`POLL_IN`** (int)

**`POLL_OUT`** (int)

**`POLL_MSG`** (int)

**`POLL_ERR`** (int)

**`POLL_PRI`** (int)

**`POLL_HUP`** (int)

**Константи ILL**

**`ILL_ILLOPC`** (int)

**`ILL_ILLOPN`** (int)

**`ILL_ILLADR`** (int)

**`ILL_ILLTRP`** (int)

**`ILL_PRVOPC`** (int)

**`ILL_PRVREG`** (int)

**`ILL_COPROC`** (int)

**`ILL_BADSTK`** (int)

**Константи FPE**

**`FPE_INTDIV`** (int)

**`FPE_INTOVF`** (int)

**`FPE_FLTDIV`** (int)

**`FPE_FLTOVF`** (int)

**`FPE_FLTUND`** (int)

**`FPE_FLTRES`** (int)

**`FPE_FLTINV`** (int)

**`FPE_FLTSUB`** (int)

**Константи SEGV**

**`SEGV_MAPERR`** (int)

**`SEGV_ACCERR`** (int)

**Константи BUS**

**`BUS_ADRALN`** (int)

**`BUS_ADRERR`** (int)

**`BUS_OBJERR`** (int)

**Константи CLONE**

**`CLONE_NEWNS`** (int)

Доступно, починаючи з PHP 7.4.0

**`CLONE_NEWIPC`** (int)

Доступно, починаючи з PHP 7.4.0

**`CLONE_NEWUTS`** (int)

Доступно, починаючи з PHP 7.4.0

**`CLONE_NEWNET`** (int)

Доступно, починаючи з PHP 7.4.0

**`CLONE_NEWPID`** (int)

Доступно, починаючи з PHP 7.4.0

**`CLONE_NEWUSER`** (int)

Доступно, починаючи з PHP 7.4.0

**`CLONE_NEWCGROUP`** (int)

Доступно, починаючи з PHP 7.4.0

**Константи PRIO**

**`PRIO_PGRP`** (int)

**`PRIO_USER`** (int)

**`PRIO_PROCESS`** (int)

**`PRIO_DARWIN_BG`** (int)

Доступно з PHP 8.1.0.

**`PRIO_DARWIN_THREAD`** (int)

Доступно з PHP 8.1.0.
