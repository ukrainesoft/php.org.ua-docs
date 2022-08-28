Використання SystemTap зі статичними зондами PHP DTrace

-   [« Использование PHP и DTrace](features.dtrace.dtrace.html)
    
-   [Справочник функций »](funcref.html)
    
-   [PHP Manual](index.html)
    
-   [Динамическая трассировка DTrace](features.dtrace.html)
    
-   Використання SystemTap зі статичними зондами PHP DTrace
    

## Використання SystemTap зі статичними зондами PHP DTrace

У деяких дистрибутивах Linux можна використовувати утиліту трасування SystemTap для відстеження статичних зондів DTrace. Цей варіант доступний у PHP 5.4.20 та PHP 5.5.

### Установка PHP з SystemTap

Встановіть пакет SystemTap SDT:

yum install systemtap-sdt-devel

Встановіть PHP з DTrace:

./configure --enable-dtrace ...

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

**Приклад #1 allprobes.stp - трасування всіх статичних зондів PHP**

probe process("sapi/cli/php").provider("php").mark("compilefileentry") { printf("Probe compilefileentryn"); printf(" compilefile %sn", userstring($arg1)); printf(" compilefiletranslated %sn", userstring($arg2)); } probe process("sapi/cli/php").provider("php").mark("compilefilereturn") { printf("Probe compilefilereturnn"); printf(" compilefile %sn", userstring($arg1)); printf(" compilefiletranslated %sn", userstring($arg2)); } probe process("sapi/cli/php").provider("php").mark("error") { printf("Probe errorn"); printf(" errormsg %sn", userstring($arg1)); printf(" requestfile %sn", userstring($arg2)); printf(" lineno %dn", $ arg3); } probe process("sapi/cli/php").provider("php").mark("exceptioncaught") { printf("Probe exceptioncaughtn"); printf(" classname %sn", userstring($arg1)); } probe process("sapi/cli/php").provider("php").mark("exceptionthrown") { printf("Probe exceptionthrownn"); printf(" classname %sn", userstring($arg1)); } probe process("sapi/cli/php").provider("php").mark("executeentry") { printf("Probe executeentryn"); printf(" requestfile %sn", userstring($arg1)); printf(" lineno %dn", $ arg2); } probe process("sapi/cli/php").provider("php").mark("executereturn") { printf("Probe executereturnn"); printf(" requestfile %sn", userstring($arg1)); printf(" lineno %dn", $ arg2); } probe process("sapi/cli/php").provider("php").mark("functionentry") { printf("Probe functionentryn"); printf(" functionname %sn", userstring($arg1)); printf(" requestfile %sn", userstring($arg2)); printf(" lineno %dn", $ arg3); printf(" classname %sn", userstring($arg4)); printf(" scope %sn", userstring($arg5)); } probe process("sapi/cli/php").provider("php").mark("functionreturn") { printf("Probe functionreturn: %sn", userstring($arg1)); printf(" functionname %sn", userstring($arg1)); printf(" requestfile %sn", userstring($arg2)); printf(" lineno %dn", $ arg3); printf(" classname %sn", userstring($arg4)); printf(" scope %sn", userstring($arg5)); } probe process("sapi/cli/php").provider("php").mark("requestshutdown") { printf("Probe requestshutdownn"); printf(" file %sn", userstring($arg1)); printf(" requesturi %sn", userstring($arg2)); printf(" requestmethod %sn", userstring($arg3)); } probe process("sapi/cli/php").provider("php").mark("requeststartup") { printf("Probe requeststartupn"); printf(" file %sn", userstring($arg1)); printf(" requesturi %sn", userstring($arg2)); printf(" requestmethod %sn", userstring($arg3)); }

Наведений вище скрипт виводитиме дані статичних зондів PHP на всьому протязі роботи PHP-скрипту:

```
# stap -c 'sapi/cli/php test.php' all_probes.stp
```