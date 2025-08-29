# Electronic Invoice Corpus / XML Dateien

Dieses Verzeichnis enthält XML-Dateien, wie sie in ZUGFeRD Rechnungen eingebettet werden. Die Dateien folgen meistens der europäischen Norm
EN 16931 für Strukur und enhaltene Informationen. Derzeit keine UBL Demodateien. Format ist UN/CEFACT CII. XML-Dateien, wie diese hier, können
mit dem browserbasierten Validierungstool des ZUGFeRD-Portals geprüft werden.

## Dateien:

- `invalid-currencyCodeDiffers-en16931.xml` - Währungsangaben im Kopf und der Schlusskalkulation sind unterschiedlich
- `invalid-currencyCodeMissing-en16931.xml` - Währungsangaben fehlen
- `invalid-damagedXml-en16931.xml` - der XML-Code ist beschädigt
- `invalid-invalidProfileInvalidEnumeration.xml` - uses enumeration in a tokenized list, with a hash as separator in ram:ID
- `invalid-invalidProfileInvalidEnumeration-regulatoryNotesMissing.xml` - unzulässige Profile-Aneinanderreihung und REG Informationen fehlen
- `invalid-InvalidProfileInvalidSaxDoubleRamId.xml` - uses the ram:ID element twice
- `invalid-InvalidProfileInvalidSaxDoubleRamId-regulatoryNotesMissing.xml` - unzulässige Profile-Aufzählung und REG Informationen fehlen
- `invalid-noLineItems-en16931.xml` - die Rechnung enthält keine Rechnungspositionen (Posten bzw. Line Items)
- `invalid-noMonetarySummation-en16931.xml` - die Rechnung enthält keine Schlusskalkulation
- `invalid-onlyBasicXML.xml` - die Datei ist nur basales XML
- `invalid-wrongVatId-en16931.xml` - die Rechnung enthält eine ungültige Umsatzsteuer-ID (Prüfziffer ist falsch)
- `valid-en16931.xml` - eine valide Rechnung
- `valid-RegulatoryNotesMissing-en16931.xml` - eine valide Rechnung allerdings ohne vollständige Pflichtangaben
- `valid-withSchemaLocation-en16931.xml` - valide mit zusätzlichem optionalem "schema location" Attribut im XML root tag

# Notes:

It can be tempting for users to try making an XML invoice simultaneously valid as both a Factur-X and an EN 16931-compliant invoice. Theoretically,
there are two ways to achieve this in XML: either by concatenating both standard IDs into the ram:ID element of ram:GuidelineSpecifiedDocumentContextParameter,
or by including the ram:ID element twice. While both approaches are technically valid in XML syntax, they do not comply with the specifications for electronic invoices.
See the "invalid-invalidProfileInvalid..." example files.
