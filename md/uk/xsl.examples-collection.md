- [« Приклади](xsl.examples.md)
- [Обробка помилок за допомогою функцій обробки помилок libxml »](xsl.examples-errors.md)

- [PHP Manual](index.md)
- [Приклади](xsl.examples.md)
- Файли collection.xml та collection.xsl для прикладів

## Файли collection.xml та collection.xsl для прикладів

Багато прикладів у цьому розділі документації містять обидва файли: XML і
XSL. Ми будемо використовувати `collection.xml` та `collection.xsl` з
наступним змістом:

**Приклад #1 collection.xml**

`` xmlcode
<collection>
<cd>
<title>Fight for your mind</title>
<artist>Ben Harper</artist>
<year>1995</year>
</cd>
<cd>
<title>Electric Ladyland</title>
<artist>Jimi Hendrix</artist>
<year>1997</year>
</cd>
</collection>
````

**Приклад #2 collection.xsl**

`` xmlcode
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:param name="owner" select="'Nicolas Eliaszewicz'"/>
<xsl:output method="html" encoding="iso-8859-1" indent="no"/>
<xsl:template match="collection">
Hey! Welcome to <xsl:value-of select="$owner"/>'s sweet CD collection!
<xsl:apply-templates/>
</xsl:template>
<xsl:template match="cd">
<h1><xsl:value-of select="title"/></h1>
<h2>by <xsl:value-of select="artist"/> - <xsl:value-of select="year"/></h2>
<hr />
</xsl:template>
</xsl:stylesheet>
````
