---
navigation:
  - features.dtrace.introduction.md: « Введення в PHP та DTrace
  - features.dtrace.systemtap.md: Використання SystemTap із статичними зондами PHP DTrace »
  - index.md: PHP Manual
  - features.dtrace.md: Динамічна трасування DTrace
title: Використання PHP та DTrace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Використання PHP та DTrace

PHP може бути налаштований зі статичними зондами DTrace на платформах, що підтримують динамічне трасування DTrace.

### Конфігурування PHP із статичними зондами DTrace

Зверніться до документації вашої платформи, щоб увімкнути підтримку DTrace у вашій операційній системі. Наприклад, в Oracle Linux необхідно завантажити ядро ​​UEK3 і зробити таке:

```php
# modprobe fasttrap
# chmod 666 /dev/dtrace/helper
```

Замість `chmod`, Ви можете використовувати пакет правил ACL для обмеження доступу для конкретного користувача.

Складання PHP з ключем `--enable-dtrace` :

```php
# ./configure --enable-dtrace ...
# make
# make install
```

Це включає статичні зонди в ядрі PHP. Будь-який модуль PHP, що надає власні зонди, повинен бути зібраний окремо як модуль, що розділяється.

### Статичні зонди DTrace у ядрі PHP

**Наступні статичні зонди доступні в PHP**

| Имя зонда | Опис зонда | Аргументы зонда |
| --- | --- | --- |
| `request-startup` | Спрацьовує на початку запиту. | char \*file, char \*request\_uri, char \*request\_method |
| `request-shutdown` | Спрацьовує після закінчення запиту. | char \*file, char \*request\_uri, char \*request\_method |
| `compile-file-entry` | Спрацьовує, коли розпочинається компіляція скрипту. | char \*compile\_file, char \*compile\_file\_translated |
| `compile-file-return` | Спрацьовує, коли закінчується компіляція скрипту. | char \*compile\_file, char \*compile\_file\_translated |
| `execute-entry` | Спрацьовує, коли запускається масив байт-коду. Наприклад, коли викликаються функції, відновлюється робота генератора чи відбувається include. | char \*request\_file, int lineno |
| `execute-return` | Спрацьовує після відпрацювання масиву байт-коду. | char \*request\_file, int lineno |
| `function-entry` | Спрацьовує, коли PHP починає запуск функції або методу. | char \*function\_name, char \*request\_file, int lineno, char \*classname, char \*scope |
| `function-return` | Спрацьовує, коли PHP повертається з функції або методу. | char \*function\_name, char \*request\_file, int lineno, char \*classname, char \*scope |
| `exception-thrown` | Спрацьовує, коли викинуто виняток. | char \*classname |
| `exception-caught` | Спрацьовує, коли виняток спійманий. | char \*classname |
| `error` | Спрацьовує, якщо сталася помилка, незалежно від рівня [error\_reporting](errorfunc.configuration.md#ini.error-reporting) | char \*errormsg, char \*request\_file, int lineno |

Модулі PHP можуть мати додаткові зонди.

### Список статичних зондів DTrace у PHP

Щоб отримати список зондів, запустіть процес PHP і виконайте:

```
# dtrace -l
```

Висновок буде приблизно такий:

```
ID   PROVIDER            MODULE                          FUNCTION NAME
   [ . . . ]
    4   php15271               php               dtrace_compile_file compile-file-entry
    5   php15271               php               dtrace_compile_file compile-file-return
    6   php15271               php                        zend_error error
    7   php15271               php  ZEND_CATCH_SPEC_CONST_CV_HANDLER exception-caught
    8   php15271               php     zend_throw_exception_internal exception-thrown
    9   php15271               php                 dtrace_execute_ex execute-entry
   10   php15271               php           dtrace_execute_internal execute-entry
   11   php15271               php                 dtrace_execute_ex execute-return
   12   php15271               php           dtrace_execute_internal execute-return
   13   php15271               php                 dtrace_execute_ex function-entry
   14   php15271               php                 dtrace_execute_ex function-return
   15   php15271               php              php_request_shutdown request-shutdown
   16   php15271               php               php_request_startup request-startup
```

Колонка Provider містить напис `php` та pid поточного запущеного процесу PHP.

Якщо запущено веб-сервер Apache, ім'я модуля може бути, наприклад, libphp5.so, і може бути безліч блоків списку по одному на кожен процес Apache.

Колонка Function посилається на ім'я внутрішньої функції PHP, що реалізує відповідний зонд.

Якщо PHP не запущено, то пов'язаних з ним зондів у списку не буде.

### Приклади використання DTrace із PHP

Цей приклад показує основні можливості скриптової мови DTrace D.

**Приклад #1 all\_probes.d - трасування всіх статичних зондів PHP за допомогою DTrace**

```
#!/usr/sbin/dtrace -Zs

#pragma D option quiet

php*:::compile-file-entry
{
    printf("PHP compile-file-entry\n");
    printf("  compile_file              %s\n", copyinstr(arg0));
    printf("  compile_file_translated   %s\n", copyinstr(arg1));
}

php*:::compile-file-return
{
    printf("PHP compile-file-return\n");
    printf("  compile_file              %s\n", copyinstr(arg0));
    printf("  compile_file_translated   %s\n", copyinstr(arg1));
}

php*:::error
{
    printf("PHP error\n");
    printf("  errormsg                  %s\n", copyinstr(arg0));
    printf("  request_file              %s\n", copyinstr(arg1));
    printf("  lineno                    %d\n", (int)arg2);
}

php*:::exception-caught
{
    printf("PHP exception-caught\n");
    printf("  classname                 %s\n", copyinstr(arg0));
}

php*:::exception-thrown
{
    printf("PHP exception-thrown\n");
    printf("  classname                 %s\n", copyinstr(arg0));
}

php*:::execute-entry
{
    printf("PHP execute-entry\n");
    printf("  request_file              %s\n", copyinstr(arg0));
    printf("  lineno                    %d\n", (int)arg1);
}

php*:::execute-return
{
    printf("PHP execute-return\n");
    printf("  request_file              %s\n", copyinstr(arg0));
    printf("  lineno                    %d\n", (int)arg1);
}

php*:::function-entry
{
    printf("PHP function-entry\n");
    printf("  function_name             %s\n", copyinstr(arg0));
    printf("  request_file              %s\n", copyinstr(arg1));
    printf("  lineno                    %d\n", (int)arg2);
    printf("  classname                 %s\n", copyinstr(arg3));
    printf("  scope                     %s\n", copyinstr(arg4));
}

php*:::function-return
{
    printf("PHP function-return\n");
    printf("  function_name             %s\n", copyinstr(arg0));
    printf("  request_file              %s\n", copyinstr(arg1));
    printf("  lineno                    %d\n", (int)arg2);
    printf("  classname                 %s\n", copyinstr(arg3));
    printf("  scope                     %s\n", copyinstr(arg4));
}

php*:::request-shutdown
{
    printf("PHP request-shutdown\n");
    printf("  file                      %s\n", copyinstr(arg0));
    printf("  request_uri               %s\n", copyinstr(arg1));
    printf("  request_method            %s\n", copyinstr(arg2));
}

php*:::request-startup
{
    printf("PHP request-startup\n");
    printf("  file                      %s\n", copyinstr(arg0));
    printf("  request_uri               %s\n", copyinstr(arg1));
    printf("  request_method            %s\n", copyinstr(arg2));
}
```

Цей скрипт використовує опцію `-Z` для dtrace, дозволяючи йому працювати навіть якщо жодного процесу PHP не запущено. Якщо не використовувати цю опцію, то скрипт відразу завершить виконання, оскільки не побачить жодного зонда, який йому треба відстежувати.

Скрипт відстежує всі статичні зонди PHP протягом усього роботи PHP-скрипту. Запускаємо D-скрипт:

```
# ./all_probes.d
```

Запустіть скрипт або програму PHP. Відстежуючий D-скрипт виводитиме аргументи всіх зондів, що спрацювали.

Коли ви побачили все, що хотіли, можна перервати роботу скрипта комбінацією CTRL+C.

На багатопроцесорних машинах порядок зондів може бути не послідовним, залежно від того, на яких процесорах працюють зонди і як мігрують потоки між процесорами. Відображення тимчасових міток дозволить уникнути конфузів. Наприклад:

```
php*:::function-entry
{
      printf("%lld: PHP function-entry ", walltimestamp);
      [ . . .]
}
```

### Дивіться також

-   [OCI8 та динамічне трасування DTrace](oci8.dtrace.md)
