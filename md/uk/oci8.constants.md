---
navigation:
  - oci8.configuration.md: « Налаштування під час виконання
  - oci8.examples.md: Приклади »
  - index.md: PHP Manual
  - book.oci8.md: OCI8
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**Функції та методи OCI8**

| Константа | Описание |
| --- | --- |
| **`OCI_ASSOC`** | Використовується функціями [ocifetchall()](function.oci-fetch-all.html) і [ocifetcharray()](function.oci-fetch-array.html) для отримання результатів як асоціативного масиву. |
| **`OCI_BOTH`** | Використовується функціями [ocifetchall()](function.oci-fetch-all.html) і [ocifetcharray()](function.oci-fetch-array.html) для отримання результатів у вигляді масиву з асоціативними та числовими індексами. |
| **`OCI_COMMIT_ON_SUCCESS`** | Режим виконання виразів для [ociexecute()](function.oci-execute.html). Автоматично завершує транзакцію оператором COMMIT у разі успішного виконання виразу. |
| **`OCI_CRED_EXT`** | Використовується функцією [ociconnect()](function.oci-connect.html) для зовнішньої чи системної аутентифікації. Додано Introduced в PHP 5.3 та PECL OCI8 1.3.4. |
| **`OCI_DEFAULT`** | Дивіться **`OCI_NO_AUTO_COMMIT`** |
| **`OCI_DESCRIBE_ONLY`** | Режим виконання виразів для [ociexecute()](function.oci-execute.html). Використовуйте цей режим, якщо ви хочете отримати дані про виконання запиту, а не виконати запит. |
| **`OCI_EXACT_FETCH`** | Застаріло. Режим отримання результатів запиту. Використовується в тому випадку, якщо програмі відомо заздалегідь скільки рядків буде отримано в результаті. Oracle 8 і пізніші версії не використовують вибірку результатів із випередженням у цьому режимі, а курсори знищуються автоматично після вибірки очікуваної кількості рядків, що може зменшити вимоги сервера до ресурсів. |
| **`OCI_FETCHSTATEMENT_BY_COLUMN`** | Режим [ocifetchall()](function.oci-fetch-all.html) за замовчуванням. |
| **`OCI_FETCHSTATEMENT_BY_ROW`** | Альтернативний режим [ocifetchall()](function.oci-fetch-all.html) |
| **`OCI_LOB_BUFFER_FREE`** | Використовується функцією [OCILob::flush](ocilob.flush.md) для звільнення буферів, що використовуються. |
| **`OCI_NO_AUTO_COMMIT`** | Режим виконання виразів для [ociexecute()](function.oci-execute.html). У цьому режимі транзакція автоматично не завершується оператором COMMIT. Для підвищення читання використовуйте в новому коді цю константу замість старої рівносильної константи **`OCI_DEFAULT`**. Додана до PHP 5.3.2 (PECL OCI8 1.4). |
| **`OCI_NUM`** | Використовується з [ocifetchall()](function.oci-fetch-all.html) і [ocifetcharray()](function.oci-fetch-array.html) для одержання масиву з числовими індексами. |
| **`OCI_RETURN_LOBS`** | Використовується [ocifetcharray()](function.oci-fetch-array.html) для отримання об'єкта LOB замість дескриптора. |
| **`OCI_RETURN_NULLS`** | Використовується з [ocifetcharray()](function.oci-fetch-array.html) для отримання порожніх елементів масиву, якщо відповідне поле в результаті дорівнює **`null`** |
| **`OCI_SEEK_CUR`** | Використовується [OCILob::seek](ocilob.seek.md) для завдання позиції усунення. |
| **`OCI_SEEK_END`** | Використовується [OCILob::seek](ocilob.seek.md) для завдання позиції усунення. |
| **`OCI_SEEK_SET`** | Використовується [OCILob::seek](ocilob.seek.md) для завдання позиції усунення. |
| **`OCI_SYSDATE`** | Більше не використовується. |
| **`OCI_SYSDBA`** | Використовується функцією [ociconnect()](function.oci-connect.html) для з'єднання з привілеями SYSOPER. Опція php.ini [oci8.privilegedconnect](oci8.configuration.html#ini.oci8.privileged-connect) має бути включена. |
| **`OCI_SYSOPER`** | Використовується функцією [ociconnect()](function.oci-connect.html) для з'єднання з привілеями SYSOPER. Опція php.ini [oci8.privilegedconnect](oci8.configuration.html#ini.oci8.privileged-connect) має бути включена. |
| **`OCI_TEMP_BLOB`** | Використовується функцією [OCILob::writeTemporary](ocilob.writetemporary.md) для створення тимчасового BLOB. |
| **`OCI_TEMP_CLOB`** | Використовується функцією [OCILob::writeTemporary](ocilob.writetemporary.md) для створення тимчасового CLOB. |

**OCI8 прив'язка змінних та визначення типів**

| Константа | Описание |
| --- | --- |
| **`OCI_B_BFILE`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу BFILE. |
| **`OCI_B_BIN`** | Використовується разом із функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язування необроблених (RAW) даних. |
| **`OCI_B_BLOB`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу BLOB. |
| **`OCI_B_BOL`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу PL/SQL BOOLEAN. |
| **`OCI_B_CFILEE`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу CFILE. |
| **`OCI_B_CLOB`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу CLOB. |
| **`OCI_B_CURSOR`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки курсорів, раніше отриманих з [ocinewdescriptor()](function.oci-new-descriptor.html) |
| **`OCI_B_INT`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів елементів типу INTEGER |
| **`OCI_B_NTY`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки названих типів даних. Зверніть увагу: у PHP < 5.0 константа називалася **`OCI_B_SQLT_NTY`** |
| **`OCI_B_NUM`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів елементів NUMBER. |
| **`OCI_B_ROWID`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу ROWID. |
| **`SQLT_AFC`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язки масивів із елементами типу CHAR. |
| **`SQLT_AVC`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів з елементами VARCHAR2. |
| **`SQLT_BDOUBLE`** | Не підтримується. |
| **`SQLT_BFILEE`** | Те саме, що і **`OCI_B_BFILE`** |
| **`SQLT_BFLOAT`** | Не підтримується. |
| **`SQLT_BIN`** | Те саме, що і **`OCI_B_BIN`** |
| **`SQLT_BLOB`** | Те саме, що і **`OCI_B_BLOB`** |
| **`SQLT_BOL`** | Те саме, що і **`OCI_B_BOL`** |
| **`SQLT_CFILEE`** | Те саме, що і **`OCI_B_CFILEE`** |
| **`SQLT_CHR`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів з елементами VARCHAR2. Також використовується функцією [ocibindбname()](function.oci-bind-by-name.html) |
| **`SQLT_CLOB`** | Те саме, що і **`OCI_B_CLOB`** |
| **`SQLT_FLT`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів з елементами FLOAT. |
| **`SQLT_INT`** | Те саме, що і **`OCI_B_INT`** |
| **`SQLT_LBI`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу LONG RAW. |
| **`SQLT_LNG`** | Використовується функцією [ocibindбname()](function.oci-bind-by-name.html) для прив'язки змінних типу LONG. |
| **`SQLT_LVC`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів із елементами типу LONG VARCHAR. |
| **`SQLT_NTY`** | Те саме, що і **`OCI_B_NTY`** |
| **`SQLT_NUM`** | Те саме, що і **`OCI_B_NUM`** |
| **`SQLT_ODT`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів із елементами типу LONG. |
| **`SQLT_RDD`** | Те саме, що і **`OCI_B_ROWID`** |
| **`SQLT_RSET`** | Те саме, що і **`OCI_B_CURSOR`** |
| **`SQLT_STR`** | Використовується функцією [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язки масивів із елементами типу STRING. |
| **`SQLT_UIN`** | Не підтримується. |
| **`SQLT_VCS`** | Використовується спільно з [ocibindarrayбname()](function.oci-bind-array-by-name.html) для прив'язування масивів VARCHAR. |

**Типи дескрипторів OCI8**

| Константа | Описание |
| --- | --- |
| **`OCI_DTYPE_FILE`** | Прапор використовується [ocinewdescriptor()](function.oci-new-descriptor.html) для ініціалізації дескриптора типу FILE |
| **`OCI_DTYPE_LOB`** | Прапор використовується [ocinewdescriptor()](function.oci-new-descriptor.html) для ініціалізації дескриптора типу LOB |
| **`OCI_DTYPE_ROWID`** | Прапор використовується [ocinewdescriptor()](function.oci-new-descriptor.html) для ініціалізації дескриптора типу ROWID |
| **`OCI_D_FILE`** | Те саме, що і **`OCI_DTYPE_FILE`** |
| **`OCI_D_LOB`** | Те саме, що і **`OCI_DTYPE_LOB`** |
| **`OCI_D_ROWID`** | Те саме, що і **`OCI_DTYPE_ROWID`** |
