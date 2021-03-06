## Stylesheets

Barrierefreie Webseiten sollten immer mit CSS formatiert werden, daher enthält
Contao ein "Stylesheets"-Modul, mit dem Sie Formatdefinitionen bequem im Backend
verwalten können. Um die verschiedenen Contao-Elemente und -Module in einem
Stylesheet zu referenzieren, müssen Sie deren Klassennamen kennen.
[Inhaltselement-Klassen][1] beginnen mit "ce\_" (z.B. "ce\_text")
und [Modul-Klassen][2] mit "mod\_" (z.B. "mod\_search"). Falls
Sie sich nicht sicher sind, sehen Sie einfach im Quelltext der Webseite nach.

![](images/stylesheet.jpg)

Jedes Stylesheet kann auf einen oder mehrere Medientypen und/oder eine bestimmte
Version des Internet Explorers beschränkt werden, falls Sie einen der vielen
darin enthaltenen Fehler gesondert beheben müssen. Achten Sie dabei auf die
Reihenfolge der Formatdefinitionen, da frühere Anweisungen von späteren
überschrieben werden können.

```css
/* Zuerst den generellen Abstand setzen */
.mod_search {
    margin:24px;
}

/* Danach die spezielle IE7-Anweisung */
*:first-child+html .mod_search {
    margin:18px;
}
```

Wäre die Reihenfolge umgekehrt, würde der allgemeine Abstand den
IE-spezifischen Wert überschreiben.


[1]: ../04-inhalte-verwalten/artikel.md#artikel
[2]: ../03-seiten-verwalten/module.md#module
