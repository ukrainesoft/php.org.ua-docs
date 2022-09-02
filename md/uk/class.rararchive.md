---
navigation:
  - function.rar-wrapper-cache-stats.md: « rarwrappercachestats
  - rararchive.close.md: 'RarArchive::close »'
  - index.md: PHP Manual
  - book.rar.md: Rar
title: Клас RarArchive
---
# Клас RarArchive

(PECL rar >= 2.0.0)

## Вступ

Цей клас описує архів RAR, який може складатися з декількох томів (частин) і містити деяку кількість RAR записів (файли, директорії та інші спеціальні об'єкти, такі як символічні посилання).

Об'єкти цього класу можуть бути заповнені перебором, виходячи з записів, що зберігаються у відповідному архіві RAR. Ці записи можуть бути отримані за допомогою методів [RarArchive::getEntry()](rararchive.getentry.md) і [RarArchive::getEntries()](rararchive.getentries.md)

## Огляд класів

```classsynopsis



    
     
      final
      class RarArchive
     

     implements 
       Traversable {


    /* Методы */
    
   public close(): bool
public getComment(): string
public getEntries(): array|false
public getEntry(string $entryname): RarEntry|false
public isBroken(): bool
public isSolid(): bool
public static open(string $filename, string $password = NULL, callable $volume_callback = NULL): RarArchive|false
public setAllowBroken(bool $allow_broken): bool
public __toString(): string

   }
```

## Зміст

-   [RarArchive::close](rararchive.close.md) — Закриває RAR архів та звільняє всі ресурси
-   [RarArchive::getComment](rararchive.getcomment.md) — Отримати текст коментаря з архіву RAR
-   [RarArchive::getEntries](rararchive.getentries.md) — Повертає повний список елементів із RAR архіву
-   [RarArchive::getEntry](rararchive.getentry.md) — Повертає об'єкт елемента з архіву RAR
-   [RarArchive::isBroken](rararchive.isbroken.md) — Перевіряє, чи не зламано архів (не завершено)
-   [RarArchive::isSolid](rararchive.issolid.md) — Перевірити, чи є архів суцільним
-   [RarArchive::open](rararchive.open.md) — Відкриває архів RAR
-   [RarArchive::setAllowBroken](rararchive.setallowbroken.md) — Чи відкривати пошкоджені архіви
-   [RarArchive::toString](rararchive.tostring.md) — Отримати текстову виставу
