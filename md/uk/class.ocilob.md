---
navigation:
  - ocicollection.trim.md: '« OCICollection::trim'
  - ocilob.append.md: 'OCILob::append »'
  - index.md: PHP Manual
  - book.oci8.md: OCI8
title: Клас OCILob
---
# Клас OCILob

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

## Вступ

Функціональність OCI8 LOB для великих бінарних (BLOB) та символьних (CLOB) об'єктів.

> **Зауваження**
> 
> Клас **OCI-Lob** був перейменований на **OCILob** у PHP 8 OCI8 3.0.0 відповідно до стандартів іменування PHP.

## Огляд класів

```classsynopsis

     
    

    
     
      class OCILob
     
     {

    /* Методы */
    
   public append(OCILob $from): bool
public close(): bool
public eof(): bool
public erase(?int $offset = null, ?int $length = null): int|false
public export(string $filename, ?int $offset = null, ?int $length = null): bool
public flush(int $flag = 0): bool
public free(): bool
public getBuffering(): bool
public import(string $filename): bool
public load(): string|false
public read(int $length): string|false
public rewind(): bool
public save(string $data, int $offset = 0): bool
public seek(int $offset, int $whence = OCI_SEEK_SET): bool
public setBuffering(bool $mode): bool
public size(): int|false
public tell(): int|false
public truncate(int $length = 0): bool
public write(string $data, ?int $length = null): int|false
public writeTemporary(string $data, int $type = OCI_TEMP_CLOB): bool

   }
```

## Зміст

-   [OCILob::append](ocilob.append.md) — Додає дані з об'єкта LOB до кінця іншого об'єкта
-   [OCILob::close](ocilob.close.md) - Закриває дескриптор об'єкта LOB
-   [OCILob::eof](ocilob.eof.md) — Перевіряє, чи вказівник LOB знаходиться на кінці об'єкта.
-   [OCILob::erase](ocilob.erase.md) — Очищає вказану частину об'єкта LOB
-   [OCILob::export](ocilob.export.md) — Зберігає вміст об'єкта LOB у файл
-   [OCILob::flush](ocilob.flush.md) — Очищає та записує буфер об'єкта LOB на сервер
-   [OCILob::free](ocilob.free.md) - Звільняє ресурси, пов'язані з дескриптором LOB
-   [OCILob::getBuffering](ocilob.getbuffering.md) — Повертає поточний стан буферизації великого об'єкта (LOB)
-   [OCILob::import](ocilob.import.md) — Записує вміст файлу на об'єкт LOB
-   [OCILob::load](ocilob.load.md) — Повертає вміст LOB
-   [OCILob::read](ocilob.read.md) — Повертає частину об'єкта LOB
-   [OCILob::rewind](ocilob.rewind.md) — Переводить вказівник об'єкта на початок великого об'єкта
-   [OCILob::save](ocilob.save.md) - Зберігає дані в LOB
-   [OCILob::saveFile](ocilob.savefile.md) - Псевдонім OCILob::import
-   [OCILob::seek](ocilob.seek.md) — Встановлює позицію внутрішнього покажчика LOB
-   [OCILob::setBuffering](ocilob.setbuffering.md) — Змінює поточний стан буферизації великого об'єкта (LOB)
-   [OCILob::size](ocilob.size.md) — Повертає розмір об'єкта LOB
-   [OCILob::tell](ocilob.tell.md) — Повертає поточну позицію внутрішнього покажчика об'єкта LOB
-   [OCILob::truncate](ocilob.truncate.md) - Обрізає великий об'єкт
-   [OCILob::write](ocilob.write.md) - Записує дані в об'єкт LOB
-   [OCILob::writeTemporary](ocilob.writetemporary.md) — Записує великий тимчасовий об'єкт (LOB)
-   [OCILob::writeToFile](ocilob.writetofile.md) - Псевдонім OCILob::export
