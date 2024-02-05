---
navigation:
  - pdostatement.setfetchmode.md: '« PDOStatement::setFetchMode'
  - class.pdoexception.md: PDOException »
  - index.md: PHP Manual
  - book.pdo.md: PDO
title: Клас PDORow
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PDORow

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 1.0.0)

## Вступ

Представляет строку из набора результатов, возвращаемого методом[PDOStatement::fetch()](pdostatement.fetch.md), викликаним у режимі вибірки **`PDO_FETCH_LAZY`**

Об'єкти цього класу не можна створювати чи серіалізувати.

Об'єкт **PDORow** дозволяє доступ до даних, що повертаються так, ніби включений і режим **`PDO::FETCH_OBJ`**, і режим **`PDO::FETCH_BOTH`**. Тобто до даних, що повертаються, вийде звернутися і як до властивостей об'єкта, і як до елементів масиву, проіндексованих як по імені стовпця, так і за номером зміщення стовпця.

**Застереження**

Доступ до невизначеної властивості поверне **`null`** без видачі застереження.

## Огляд класів

```classsynopsis

    
     final
     class PDORow
     {

    /* Свойства */
    
     public
     string
      $queryString;

   }
```

## Властивості

queryString

Рядок запиту для об'єкта класу [PDOStatement](class.pdostatement.md), яку повернув об'єкт **PDORow**

## Помилки

При спробі записати властивість або видалити властивість через мовну конструкцію [unset()](function.unset.md) викидає виняток [Error](class.error.md)
