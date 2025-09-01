# Electronic Invoice Corpus / ZUGFeRD Dateien

Dieses Verzeichnis enthält ZUGFeRD Rechnungen und Testfiles. ZUGFeRD ist ein hybrides Rechnungsformat, das den sichtbaren Teil einer PDF-Rechnung mit einem
angehängten maschinenlesbaren XML-File verbindet.

Die Dateien können z.B. auf dem [ZUGFeRD Portal](https://zugferd.goeszen.com/) getestet werden.

## Dateien:

- `invalid-incompleteXmp-validPdfA3b-validXml.pdf` - valide PDF/A-3b Datei und valides XML, aber die XMP-Daten definieren kein ConformanceLevel
- `invalid-isEncrypted.pdf` - die PDF-Datei ist verschlüsselt und damit nicht valide
- `invalid-multipageTest-noXmp-noAttachments-compressedIndividualObjectStreams.pdf`- keine Anhänge, PDF mit mehreren Seiten, Struktur: einzeln komprimierte Objekt-Streams
- `invalid-multipageTest-noXmp-noAttachments-oneCompressedObjectStream.pdf`- keine Anhänge, PDF mit mehreren Seiten, Struktur: ein komprimierter Objekt-Stream als top-level
- `invalid-multipageTest-noXmp-noAttachments-uncompressedStreams.pdf`- keine Anhänge, PDF mit mehreren Seiten, Struktur: einzelne unkomprimierte Objekt-Streams
- `invalid-notPdf.pdf` - die Datei ist gar keine PDF Datei (eigentlich ein PNG Bild)
- `invalid-noAttachments.pdf` - die Datei enthält gar keine Anhänge
- `invalid-noXmlAttachment-validPdfA3b.pdf` - valide PDF/A-3b Datei, aber ohne XML-Anhang, Struktur: einzelne Object-Streams
- `invalid-noXmlAttachment-validPdfA3b-compressedObjectStreams.pdf` - valide PDF/A-3b Datei, aber ohne XML-Anhang, Struktur: ein komprimierter Objekt-Stream als top-level
- `invalid-noXmp.pdf` - der für eine gültige PDF/A-3b Datei nötige XMP Metadaten-Stream fehlt, zudem ist AFRelationship für den XML-Anhang nicht gesetzt
- `invalid-twoAttachments.pdf` - die Datei enthält zwei Anhänge (Bilder), keiner davon ist eine XML-Rechnung
- `invalid-oneAttachmentWrongMimeType.pdf` - die Datei enthält einen Anhang, aber mit falschem MIME-Type und falschem Datei-Suffix
- `valid-zugferd-validPdfA3b.pdf` - valide ZUGFeRD-Rechnung, erstellt mit der Micropolis ZUGFeRD-Portal Web-App
- `valid-zugferd-validPdfA3b_withOptionalBuyerRef-withOptionalBic.pdf` - valide Rechnung, zusätzlich mit optionaler Kundenreferenz und optionaler BIC-Angabe
