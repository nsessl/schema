# Změny provedené od 1.7.2023

## Změny datových typů

* u některých elementů bylo povolena delší maximální délka
* u většiny hodnot omezení zůstala, aby se minimalizovala nutnost
  úpravy stávajích aplikací, které v některých případech počítají s
  pevnou délkou
* 

## Změny API

Změny v API byly provedeny co nejmenší, ale i přesto je změněn jmenný
prostor používaný v XML dokumentech, aby neaktulizované systémy nové
XML odmítli zpracovat a nedocházelo k nečekaným chybám.

Místo jmenného prostoru `http://nsess.public.cz/erms/v_02_00` se nyní
používá jmenný prostor `http://www.mvcr.cz/nsesss/2023/api`.

### Přidány následující funkce do synchronního rozhraní

* SpisPostoupeniZadost
* ProfilTypovehoSpisuZadost
* ProfilOsobyZadost
* OsobaZalozeni
* OsobaUprava
* OsobySeznam
* CiselnikySeznam
* DokumentVraceniZadost
* SpisVraceniZadost
* TypovySpisZalozeni
* UzivateleSeznam

### Přidány následující události do asynchronního rozhraní

* SpisVlozeniDoTypovehoSpisu
* SpisVyjmutiZTypovehoSpisu
* DokumentZalozeni
* DokumentUzavreni
* DokumentVyrizeni
* SpisVraceni
* OdkazVytvoreni
* OdkazZruseni








