---
navigation:
  - features.dtrace.dtrace.md: « Використання PHP та DTrace
  - funcref.md: Довідник функцій »
  - index.md: PHP Manual
  - features.dtrace.md: Динамічна трасування DTrace
title: Використання SystemTap зі статичними зондами PHP DTrace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Використання SystemTap зі статичними зондами PHP DTrace

У деяких дистрибутивах Linux можна використовувати утиліту трасування SystemTap для відстеження статичних зондів DTrace. Даний варіант доступний у PHP 5.4.20 та PHP 5.5.

### Установка PHP з SystemTap

Встановіть пакет SystemTap SDT:

#yum install systemtap-sdt-devel

Встановіть PHP з DTrace:

#./configure --enable-dtrace ...

# make

### Отримання списку статичних зондів за допомогою SystemTap

Статичні зонди PHP можна подивитися за допомогою stap:

```
# stap -l 'process.provider("php").mark("*")' -c 'sapi/cli/php -i'
```

Зразковий висновок:

```
process("sapi/cli/php").provider("php").mark("compile__file__entry")
process("sapi/cli/php").provider("php").mark("compile__file__return")
process("sapi/cli/php").provider("php").mark("error")
process("sapi/cli/php").provider("php").mark("exception__caught")
process("sapi/cli/php").provider("php").mark("exception__thrown")
process("sapi/cli/php").provider("php").mark("execute__entry")
process("sapi/cli/php").provider("php").mark("execute__return")
process("sapi/cli/php").provider("php").mark("function__entry")
process("sapi/cli/php").provider("php").mark("function__return")
process("sapi/cli/php").provider("php").mark("request__shutdown")
process("sapi/cli/php").provider("php").mark("request__startup")
```

### Приклад використання SystemTap з PHP

**Приклад #1 all\_probes.stp - трасування всіх статичних зондів PHP**

probe process("sapi/cli/php").provider("php").mark("compile\_\_file\_\_entry") { printf("Probe compile\_\_file\_\_entry\\n"); printf(" compile\_file %s\\n", user\_string($arg1)); printf(" compile\_file\_translated %s\\n", user\_string($arg2)); } probe process("sapi/cli/php").provider("php").mark("compile\_\_file\_\_return") { printf("Probe compile\_\_file\_\_return\\n"); printf(" compile\_file %s\\n", user\_string($arg1)); printf(" compile\_file\_translated %s\\n", user\_string($arg2)); } probe process("sapi/cli/php").provider("php").mark("error") { printf("Probe error\\n"); printf(" errormsg %s\\n", user\_string($arg1)); printf(" request\_file %s\\n", user\_string($arg2)); printf(" lineno %d\\n", $arg3); } probe process("sapi/cli/php").provider("php").mark("exception\_\_caught") { printf("Probe exception\_\_caught\\n"); printf(" classname %s\\n", user\_string($arg1)); } probe process("sapi/cli/php").provider("php").mark("exception\_\_thrown") { printf("Probe exception\_\_thrown\\n"); printf(" classname %s\\n", user\_string($arg1)); } probe process("sapi/cli/php").provider("php").mark("execute\_\_entry") { printf("Probe execute\_\_entry\\n"); printf(" request\_file %s\\n", user\_string($arg1)); printf(" lineno %d\\n", $arg2); } probe process("sapi/cli/php").provider("php").mark("execute\_\_return") { printf("Probe execute\_\_return\\n"); printf(" request\_file %s\\n", user\_string($arg1)); printf(" lineno %d\\n", $arg2); } probe process("sapi/cli/php").provider("php").mark("function\_\_entry") { printf("Probe function\_\_entry\\n"); printf(" function\_name %s\\n", user\_string($arg1)); printf(" request\_file %s\\n", user\_string($arg2)); printf(" lineno %d\\n", $arg3); printf(" classname %s\\n", user\_string($arg4)); printf(" scope %s\\n", user\_string($arg5)); } probe process("sapi/cli/php").provider("php").mark("function\_\_return") { printf("Probe function\_\_return: %s\\n", user\_string($arg1)); printf(" function\_name %s\\n", user\_string($arg1)); printf(" request\_file %s\\n", user\_string($arg2)); printf(" lineno %d\\n", $arg3); printf(" classname %s\\n", user\_string($arg4)); printf(" scope %s\\n", user\_string($arg5)); } probe process("sapi/cli/php").provider("php").mark("request\_\_shutdown") { printf("Probe request\_\_shutdown\\n"); printf(" file %s\\n", user\_string($arg1)); printf(" request\_uri %s\\n", user\_string($arg2)); printf(" request\_method %s\\n", user\_string($arg3)); } probe process("sapi/cli/php").provider("php").mark("request\_\_startup") { printf("Probe request\_\_startup\\n"); printf(" file %s\\n", user\_string($arg1)); printf(" request\_uri %s\\n", user\_string($arg2)); printf(" request\_method %s\\n", user\_string($arg3)); }

Наведений вище скрипт виводитиме дані статичних зондів PHP на всьому протязі роботи PHP-скрипту:

```
# stap -c 'sapi/cli/php test.php' all_probes.stp
```
