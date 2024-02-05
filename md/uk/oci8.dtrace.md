---
navigation:
  - oci8.taf.md: >-
      « Підтримка прозорого для програм відновлення після відмови (Transparent
      Application Failover або TAF) для OCI8
  - oci8.datatypes.md: 'Типи даних, що підтримуються »'
  - index.md: PHP Manual
  - book.oci8.md: OCI8
title: OCI8 та динамічне трасування DTrace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCI8 та динамічне трасування DTrace

OCI8 2.0 містить статичні зонди DTrace, які можна використовувати в операційних системах, які підтримують DTrace. Докладніше взаємини PHP та DTrace описані в розділі [Динамічна трасування DTrace](features.dtrace.md)

## Установка OCI8 з підтримкою DTrace

Для включення підтримки DTrace в PHP OCI8, зберіть OCI8 як модуль, що розділяється після установки змінної оточення `PHP_DTRACE`

```
$ export PHP_DTRACE=yes
$ pecl install oci8
```

Отредактируйте php.ini, задав[extension\_dir](ini.core.md#ini.extension-dir) рівним директорії, в якій створився oci8.so, а також увімкніть модуль таким чином:

```
extension=oci8.so
```

Якщо ви встановили PHP OCI8 з PECL з використанням phpize і configure (замість pecl), вам все ще потрібно буде встановити `PHP_DTRACE=yes`. Це тому, що опція `--enable-dtrace` буде проігноровано обмеженим скриптом configure модуля PECL.

Более подробно об установке PECL модулей читайте в разделе[Встановлення модулів PECL](install.pecl.md)

## Статичні зонди DTrace у PHP OCI8

**Наступні статичні зонди доступні в PHP OCI8**

| Имя зонда | Опис зонда | Аргументы зонда |
| --- | --- | --- |
| `oci8-connect-entry` | Ініціюється oci\_connect(), oci\_pconnect() та oci\_new\_connect(). Спрацьовує доти, як з'єднання було встановлено. | char \*username, char \*dbname, char \*charset, long session\_mode, int persistent, int exclusive |
| `oci8-connect-return` | Спрацьовує після встановлення з'єднання. | void \*connection |
| `oci8-check-connection` | Спрацьовує, якщо помилка Oracle може призвести до псування з'єднання. | void \*connection, char \*client\_id, int is\_open, long errcode, unsigned long server\_status |
| `oci8-sqltext` | Спрацьовує при запуску oci\_parse(). | void \*connection, char \*client\_id, void \*statement, char \*sql |
| `oci8-connection-close` | Спрацьовує, коли з'єднання остаточно знищено. | void \*connection |
| `oci8-error` | Спрацьовує, якщо виникла помилка Oracle. | int status, long errcode |
| `oci8-execute-mode` | Спрацьовує за [oci\_execute()](function.oci-execute.md) виявлення режиму запуску. | void \*connection, char \*client\_id, void \*statement, unsigned int mode |

Ці зонди корисні для налагодження скриптів OCI8.

Параметри connection та statement є вказівниками на внутрішні структури, які використовуються для відстеження з'єднань та запущених запитів.

Параметр client\_id встановлюється функцією [oci\_set\_client\_identifier()](function.oci-set-client-identifier.md)

Ядро PHP містить статичні зонди. Дивіться розділ [Статичні зонди DTrace у ядрі PHP](features.dtrace.dtrace.md#features.dtrace.static-probes)

**Внутрішні налагоджувальні зонди DTrace в OCI8**

| Имя зонда |
| --- |
| `oci8-connect-expiry` |
| `oci8-connect-lookup` |
| `oci8-connect-p-dtor-close` |
| `oci8-connect-p-dtor-release` |
| `oci8-connect-type` |
| `oci8-sesspool-create` |
| `oci8-sesspool-stats` |
| `oci8-sesspool-type` |

Ці зонди є корисними для розробників модуля OCI8. Для детальнішої інформації вивчайте вихідні коди OCI8.

## Отримання списку статичних зондів DTrace у PHP OCI8

Щоб отримати список доступних зондів, запустіть процес PHP і потім запустіть:

```
# dtrace -l
```

Висновок буде приблизно наступним:

```
ID   PROVIDER            MODULE                          FUNCTION NAME
   [ . . . ]
   17 phpoci22116           oci8.so   php_oci_dtrace_check_connection oci8-check-connection
   18 phpoci22116           oci8.so                php_oci_do_connect oci8-connect-entry
   19 phpoci22116           oci8.so         php_oci_persistent_helper oci8-connect-expiry
   20 phpoci22116           oci8.so             php_oci_do_connect_ex oci8-connect-lookup
   21 phpoci22116           oci8.so  php_oci_pconnection_list_np_dtor oci8-connect-p-dtor-close
   22 phpoci22116           oci8.so  php_oci_pconnection_list_np_dtor oci8-connect-p-dtor-release
   23 phpoci22116           oci8.so                php_oci_do_connect oci8-connect-return
   24 phpoci22116           oci8.so             php_oci_do_connect_ex oci8-connect-type
   25 phpoci22116           oci8.so          php_oci_connection_close oci8-connection-close
   26 phpoci22116           oci8.so                     php_oci_error oci8-error
   27 phpoci22116           oci8.so         php_oci_statement_execute oci8-execute-mode
   28 phpoci22116           oci8.so              php_oci_create_spool oci8-sesspool-create
   29 phpoci22116           oci8.so            php_oci_create_session oci8-sesspool-stats
   30 phpoci22116           oci8.so            php_oci_create_session oci8-sesspool-type
   31 phpoci22116           oci8.so          php_oci_statement_create oci8-sqltext
```

Стовпець "Provider" складається з `phpoci` та ідентифікатора запущеного процесу PHP.

Стовпець "Function" містить імена внутрішніх, написаних на C, функцій PHP, які містять відповідні провайдери (Provider).

Якщо процес PHP не запущено, то ніяких зондів PHP не буде показано.

## Приклад використання DTrace із PHP OCI8

У цьому прикладі показано основи скриптової мови DTrace D.

**Приклад #1\_oci8\_probes.d для трасування всіх статичних зондів PHP OCI8 за допомогою DTrace на рівні користувача**

```
#!/usr/sbin/dtrace -Zs

#pragma D option quiet

php*:::oci8-connect-entry
{
    printf("%lld: PHP connect-entry\n", walltimestamp);
    printf("  credentials=\"%s@%s\"\n", arg0 ? copyinstr(arg0) : "", arg1 ? copyinstr(arg1) : "");
    printf("  charset=\"%s\"\n", arg2 ? copyinstr(arg2) : "");
    printf("  session_mode=%ld\n", (long)arg3);
    printf("  persistent=%d\n", (int)arg4);
    printf("  exclusive=%d\n", (int)arg5);
}

php*:::oci8-connect-return
{
    printf("%lld: PHP oci8-connect-return\n", walltimestamp);
    printf("  connection=0x%p\n", (void *)arg0);
}

php*:::oci8-connection-close
{
    printf("%lld: PHP oci8-connect-close\n", walltimestamp);
    printf("  connection=0x%p\n", (void *)arg0);
}

php*:::oci8-error
{
    printf("%lld: PHP oci8-error\n", walltimestamp);
    printf("  status=%d\n", (int)arg0);
    printf("  errcode=%ld\n", (long)arg1);
}

php*:::oci8-check-connection
{
    printf("%lld: PHP oci8-check-connection\n", walltimestamp);
    printf("  connection=0x%p\n", (void *)arg0);
    printf("  client_id=\"%s\"\n", arg1 ? copyinstr(arg1) : "");
    printf("  is_open=%d\n", arg2);
    printf("  errcode=%ld\n", (long)arg3);
    printf("  server_status=%lu\n", (unsigned long)arg4);
}

php*:::oci8-sqltext
{
    printf("%lld: PHP oci8-sqltext\n", walltimestamp);
    printf("  connection=0x%p\n", (void *)arg0);
    printf("  client_id=\"%s\"\n", arg1 ? copyinstr(arg1) : "");
    printf("  statement=0x%p\n", (void *)arg2);
    printf("  sql=\"%s\"\n", arg3 ? copyinstr(arg3) : "");
}

php*:::oci8-execute-mode
{
    printf("%lld: PHP oci8-execute-mode\n", walltimestamp);
    printf("  connection=0x%p\n", (void *)arg0);
    printf("  client_id=\"%s\"\n", arg1 ? copyinstr(arg1) : "");
    printf("  statement=0x%p\n", (void *)arg2);
    printf("  mode=0x%x\n", arg3);
}
```

У цьому скрипті з dtrace використовується опція `-Z`, що дозволяє йому запускатись навіть якщо ніяких процесів PHP не запущено. Якщо не задати цю опцію, то скрипт відразу припинить свою роботу, тому що відсутні зонди для відстеження.

На багатопроцесорних машинах порядок зондів може бути послідовним. Це залежить від того, на яких ядрах працюють зонди і як потоки мігрують між ядрами. У такій ситуації є сенс орієнтуватися на тимчасові мітки зондів.

Скрипт відстежує всі повідомлення статичних зондів PHP OCI8 рівня користувача протягом роботи PHP. Запускаємо скрипт D:

```
# ./user_oci8_probes.d
```

Запускаємо скрипт PHP або свою програму. D-скрипт виводитиме всі аргументи зондів при їх спрацьовуванні. Наприклад, простий скрипт PHP, що виконує запит до бази даних може створювати такі повідомлення:

```
1381794982092854582: PHP connect-entry
  credentials="hr@localhost/pdborcl"
  charset=""
  session_mode=0
  persistent=0
  exclusive=0
1381794982183158766: PHP oci8-connect-return
  connection=0x7f4a7907bfb8
1381794982183594576: PHP oci8-sqltext
  connection=0x7f4a7907bfb8
  client_id="Chris"
  statement=0x7f4a7907c2a0
  sql="select * from employees"
1381794982183783706: PHP oci8-execute-mode
  connection=0x7f4a7907bfb8
  client_id="Chris"
  statement=0x7f4a7907c2a0
  mode=0x20
1381794982444344390: PHP oci8-connect-close
  connection=0x7f4a7907bfb8
```

Після завершення діагностики D-скрипт можна перервати за допомогою CTRL+C.

## Дивіться також

-   [Динамічна трасування DTrace](features.dtrace.md)
