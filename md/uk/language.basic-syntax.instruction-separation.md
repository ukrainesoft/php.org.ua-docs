- [« Ізолювання від HTML](language.basic-syntax.phpmode.md)
- [Коментарі »](language.basic-syntax.comments.md)

- [PHP Manual](index.md)
- [Основи синтаксису](language.basic-syntax.md)
- Поділ інструкцій

## Поділ інструкцій

Як в C або Perl, PHP вимагає закінчення інструкцій точкою коми в
кінці кожної інструкції. Закриваючий тег блоку PHP-коду автоматично
застосовує крапку з комою; тобто. немає необхідності ставити крапку з
комою в кінці останнього рядка блоку з PHP-кодом. Закриває тег
блоку "поглине" негайно наступний за ним перехід на новий рядок,
якщо така буде виявлена.

**Приклад #1 Приклад, що показує тег, що закриває, що охоплює
завершальний новий рядок**

`<?php echo "Якийсь текст"; ?>Нет нового рядка<?= "А зараз, нова рядок" ?> `

Результат виконання цього прикладу:

Якийсь текстНемає нового рядка
А зараз, новий рядок

Приклади входу та виходу з парсера PHP:

<?php    echo 'Це тест';?><?php echo 'Це тест' ?><?php echo 'Ми опустили останній закриваючий тег'; `

> **Примітка**:
>
> Закриваючий тег PHP-блоку в кінці файлу не є обов'язковим, і в
> деяких випадках його опускання досить корисне, наприклад, при
> використання [include](function.include.md) або
> [require](function.require.md), так що небажані прогалини не
> залишаться в кінці файлу і ви все ще зможете додати http-заголовки
> після підключення до відповіді сервера. Це також зручно при використанні
> буферизації виведення, де також небажано мати прогалини в кінці
> частин відповіді, згенерованого файлами, що підключаються.
