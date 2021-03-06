- [« Вимоги](libxml.requirements.md)
- [Налаштування під час виконання »](libxml.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](libxml.setup.md)
- Встановлення

## Установка

Модуль libxml включений за замовчуванням, але може бути відключений за допомогою
директиви **-disable-libxml**.

Необов'язкова директива **-with-libxml-dir** використовується для завдання
розташування `libxml` у системах, на яких PHP скомпільовано, якщо не
директива не використовується, пошук буде проводитись тільки по
стандартних шляхів. Процес `configure` здійснює пошук libxml
(особливо, `xml2-config`) по шляхах у такому порядку:

1. Розташування ([DIR]), вказане за допомогою директиви
**--with-libxml-dir** ([DIR]=`/bin/xml2-config`)

2. `/usr/local/bin/xml2-config`

3. `/usr/bin/xml2-config`

Якщо `configure` не знайде `xml2-config` у директорії, заданій
директивою **--with-libxml-dir**, він продовжить пошук за стандартними
шляхів.
