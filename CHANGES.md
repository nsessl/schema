# Změny provedené od 1.7.2023

## Změny datových typů

* u některých elementů bylo povolena delší maximální délka
* u většiny hodnot omezení zůstala, aby se minimalizovala nutnost
  úpravy stávajích aplikací, které v některých případech počítají s
  pevnou délkou
* schémata již nepoužívají `nillable="true"` -- místo toho je daný
  element nepovinný

## Změny API

Změny v API byly provedeny co nejmenší, ale i přesto je změněn jmenný
prostor používaný v XML dokumentech, aby neaktulizované systémy nové
XML odmítly zpracovat a nedocházelo k nečekaným chybám.

Místo jmenného prostoru `http://nsess.public.cz/erms/v_02_00` se nyní
používá jmenný prostor `http://www.mvcr.cz/nsesss/2023/api`.

### Synchronní rozhraní

#### Přidány následující služby

* CiselnikySeznam
* DokumentVraceniZadost
* OsobaUprava
* OsobaZalozeni
* OsobySeznam
* ProfilOsobyZadost
* ProfilTypovehoSpisuZadost
* SpisPostoupeniZadost
* SpisVraceniZadost
* TypovySpisZalozeni
* UzivateleSeznam

#### Další důležité změny

* Služba DokumentZalozeni v požadavku nepřenáší kompletní profil
  dokumentu, ale jen údaje, které dávají smysl při založení popsané
  typem tProfilDokumentuZalozeni
* Služba SpisZalozeni v požadavku nepřenáší kompletní profil
  spisu, ale jen údaje, které dávají smysl při založení popsané
  typem tProfilSpisuZalozeni
* Služba CiselnikZadost používá pro určení číselníku element
  IdCiselniku a ne Kod.
* Položky číselníku mohou přenášet větší množství nepovinných položek
  podle potřeby

### Asynchronní rozhraní

#### Přidány následující události

* DokumentOdebran
* DokumentSkartacniNavrh
* DokumentUzavreni
* DokumentVyrizeni
* DokumentZalozeni
* OdkazVytvoreni
* OdkazZruseni
* SpisOdebran
* SpisSkartacniNavrh
* SpisVlozeniDoTypovehoSpisu
* SpisVraceni
* SpisVyjmutiZTypovehoSpisu

#### Další důležité změny

## Změny ve schématech pro popisná metadata, o rozhodnutí ve skartačním řízení, pro spisový a skartační plán

Níže popsané změny se týkají schémat `nsesss.xsd`, `nsesss-DA.xsd` a
`nsesss-plan.xsd`.

Změny ve schématech byly provedeny co nejmenší, ale i přesto je změněn
jmenný prostor používaný v XML dokumentech, aby neaktulizované systémy
nové XML odmítly zpracovat a nedocházelo k nečekaným chybám.

Místo jmenného prostoru `http://www.mvcr.cz/nsesss/v3` se nyní
používá jmenný prostor `http://www.mvcr.cz/nsesss/v4`.

* Sdílené definice jsou součástí schématu `nsesss-common.xsd`
* Metadata skartačního režimu rozšížena o rok vyřazení a lhůtu pro
  kontrolu
* element `Držitel` přejmenován na `Drzitel`
* forma uchování komponenty může nyní být i "digitalizát" a
  "kontejner"
* u digitalizátu lze specifikovat uložení analogového originálu
* do dílu lze vkládat i spisy
* evidenční číslo je nyní nepovinné
  

## Změny v transakčním protokolu

Místo jmenného prostoru `http://nsess.public.cz/erms_trans/v_01_01` se nyní
používá jmenný prostor `http://www.mvcr.cz/nsesss/2023/log`.

Zároveň byla odstraněna nekonzistence, kdy elementy `HodnotaID` a
`ZdrojID` byly v jiném jméném prostoru než všechny ostatní elementy
transakčního protokolu.
