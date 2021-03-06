## TinyMCE anpassen

Diese Seite erklärt, wie man die Rich Text Editor-Konfiguration anpasst und
updatesicher speichert. Beachten Sie, dass Contao standardmäßig nicht alle
TinyMCE-Plugins enthält und fehlende Ressourcen gegebenenfalls von der
[TinyMCE-Projektwebseite][1] heruntergeladen und in den Ordner
`assets/tinyMCE/plugins` Ihrer Contao-Installation kopiert werden müssen.

![](images/rich-text-editor.jpg)

Das obige Bild zeigt die Standardkonfiguration des Editors, die in der Datei
`system/config/tinyMCE.php` hinterlegt ist. Um eine eigene Konfiguration zu
erstellen, duplizieren Sie die Datei, fügen Sie Ihre Änderungen ein und
speichern Sie die neue Datei als `tinyCustom.php`. Passen Sie dann noch die
[DCA-Konfiguration][2] in der Datei `system/config/dcaconfig.php` an, damit
Contao zukünftig die neue Konfigurationsdatei lädt.

```php
// Die eigene RTE-Konfiguration für Text-Elemente verwenden
$GLOBALS['TL_DCA']['tl_content']['fields']['text']['eval']['rte'] = 'tinyCustom';
```


[1]: http://tinymce.moxiecode.com
[2]: ../07-contao-anpassen/konfiguration-anpassen.md#die-dca-konfiguration-anpassen
