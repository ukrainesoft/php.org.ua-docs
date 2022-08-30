Повертає довжину BLOB-об'єкта та іншу корисну інформацію

-   [« ibaseblobimport](function.ibase-blob-import.html)
    
-   [ibaseblobopen »](function.ibase-blob-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Повертає довжину BLOB-об'єкта та іншу корисну інформацію
    

# ibaseblobinfo

(PHP 5, PHP 7 < 7.4.0)

ibaseblobinfo — Повертає довжину BLOB-об'єкта та іншу корисну інформацію

### Опис

```methodsynopsis
ibase_blob_info(resource $link_identifier, string $blob_id): array
```

```methodsynopsis
ibase_blob_info(string $blob_id): array
```

Повертає довжину BLOB-об'єкта та іншу корисну інформацію.

### Список параметрів

`link_identifier`

Ідентифікатор посилання на InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`blob_id`

Ідентифікатор об'єкта BLOB.

### Значення, що повертаються

Повертає масив, що містить інформацію про BLOB-об'єкт. Повертана інформація складається з довжини BLOB-об'єкта, кількості сегментів, що містяться в ньому, розміру найбільшого сегмента і того, чи є він BLOB-потоком або сегментованим BLOB-об'єктом.