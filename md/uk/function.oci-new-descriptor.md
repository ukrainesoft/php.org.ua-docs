---
navigation:
  - function.oci-new-cursor.md: « oci\_new\_cursor
  - function.oci-num-fields.md: oci\_num\_fields »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_new\_descriptor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_new\_descriptor

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_new\_descriptor — Ініціалізує новий дескриптор об'єкта LOB чи FILE

### Опис

```methodsynopsis
oci_new_descriptor(resource $connection, int $type = OCI_DTYPE_LOB): ?OCILob
```

Резервує ресурси, необхідні зберігання дескриптора об'єкта чи LOB-локатора.

### Список параметрів

`connection`

Ідентифікатор з'єднання з сервером Oracle, який повертається функцією [oci\_connect()](function.oci-connect.md) або [oci\_pconnect()](function.oci-pconnect.md)

`type`

Допустимі значення параметра `type` **`OCI_DTYPE_FILE`** **`OCI_DTYPE_LOB`** і **`OCI_DTYPE_ROWID`**

### Значення, що повертаються

Повертає новий LOB або дескриптор FILE у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** oci\_new\_descriptor()\*\*\*\*

```php
<?php
/* Приведённый скрипт разработан для использования с HTML формами.
 * Это подразумевает, что $user, $password, $table, $where, и $commitsize
 * получены из формы. Скрипт удаляет записи с использованием
 * ROWID и закрывает транзакцию после каждого
 * $commitsize записей. (Используйте осторожно, откат изменений невозможен)
 */
$conn = oci_connect($user, $password);
$stmt = oci_parse($conn, "select rowid from $table $where");
$rowid = oci_new_descriptor($conn, OCI_D_ROWID);
oci_define_by_name($stmt, "ROWID", $rowid);
oci_execute($stmt);
while (oci_fetch($stmt)) {
    $nrows = oci_num_rows($stmt);
    $delete = oci_parse($conn, "delete from $table where ROWID = :rid");
    oci_bind_by_name($delete, ":rid", $rowid, -1, OCI_B_ROWID);
    oci_execute($delete);
    echo "$nrows\n";
    if (($nrows % $commitsize) == 0) {
        oci_commit($conn);
    }
}
$nrows = oci_num_rows($stmt);
echo "$nrows deleted...\n";
oci_free_statement($stmt);
oci_close($conn);
?>
```

```php
<?php
    /* Данный скрипт реализует загрузку файлов в LOB-столбцы
     * HTML-форма для скрипта выглядит Прикладно так:
     * <form action="upload.php" method="post" enctype="multipart/form-data">
     * <input type="file" name="lob_upload" />
     * ...
     */
  if (!isset($lob_upload) || $lob_upload == 'none'){
?>
<form action="upload.php" method="post" enctype="multipart/form-data">
Загрузить файл: <input type="file" name="lob_upload" /><br />
<input type="submit" value="Загрузить" /> - <input type="reset" value="Сбросить" />
</form>
<?php
  } else {

     // $lob_upload содержит временное имя загруженного файла

     // смотрите также раздел особенностей загрузки файлов,
     // если необходимо реализовать безопасную загрузку

     $conn = oci_connect($user, $password);
     $lob = oci_new_descriptor($conn, OCI_D_LOB);
     $stmt = oci_parse($conn, "insert into $table (id, the_blob)
               values(my_seq.NEXTVAL, EMPTY_BLOB()) returning the_blob into :the_blob");
     oci_bind_by_name($stmt, ':the_blob', $lob, -1, OCI_B_BLOB);
     oci_execute($stmt, OCI_DEFAULT);
     if ($lob->savefile($lob_upload)){
        oci_commit($conn);
        echo "Blob успешно загружен\n";
     }else{
        echo "Не удалось загрузить Blob\n";
     }
     $lob->free();
     oci_free_statement($stmt);
     oci_close($conn);
  }
?>
```

**Приклад #2 Приклад використання** oci\_new\_descriptor()\*\*\*\*

```php
<?php
/* Вызов хранимой процедуры PL/SQL, параметрами которой являются объекты CLOB
 * Приклад PL/SQL процедуры:
 *
 * PROCEDURE save_data
 *   Имя аргумента                    Тип                     In/Out По умолчанию?
 *   ------------------------------ ----------------------- ------ ------------
 *   KEY                            NUMBER(38)              IN
 *   DATA                           CLOB                    IN
 *
 */

$conn = oci_connect($user, $password);
$stmt = oci_parse($conn, "begin save_data(:key, :data); end;");
$clob = oci_new_descriptor($conn, OCI_D_LOB);
oci_bind_by_name($stmt, ':key', $key);
oci_bind_by_name($stmt, ':data', $clob, -1, OCI_B_CLOB);
$clob->write($data);
oci_execute($stmt, OCI_DEFAULT);
oci_commit($conn);
$clob->free();
oci_free_statement($stmt);
?>
```

### Дивіться також

-   [oci\_bind\_by\_name()](function.oci-bind-by-name.md) \- Прикріплює змінну PHP до відповідної мітки у SQL-вираженні
