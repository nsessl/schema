# Změny provedené od verze z 4. července 2017

## Změny ve struktuře příloh

* Přílohy 2 a 3 bylo sloučeny do přílohy 2
* Nová příloha 3 obsahuje definici popisných metadat pro automatizované
  zpracování dokumentu
* Nová příloha 7 obsahuje schéma pro migraci dat mezi spisovými
  službami a spisovou rozluku

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

* DokumentSkartacniNavrh
* DokumentVytvoreni
* DokumentZalozeni
* OdkazVytvoreni
* OdkazZruseni
* SpisSkartacniNavrh
* SpisVlozeniDoTypovehoSpisu
* SpisVyjmutiZTypovehoSpisu

#### Odstraněny následující události

* DokumentUzavreni

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
* forma uchování komponenty může nyní být i "digitalizát",
  "kontejner" a "analogová"
  * u digitalizátu lze specifikovat uložení analogového originálu
  * analogová komponenta odpovídá části v terminologii nové vyhlášky
* do dílu lze vkládat i spisy
* evidenční číslo je nyní nepovinné
* vylepšena definice plně určeného spisového znaku
* způsob vyřízení je nepovinný
* element `TypDokumentu` byl nahrazen elementem `DruhDokumentu` a
  rozšířen o nepovinný skartační režim
* věcná skupina byla rozšířena o nové podelementy
  

## Změny v transakčním protokolu

Místo jmenného prostoru `http://nsess.public.cz/erms_trans/v_01_01` se nyní
používá jmenný prostor `http://www.mvcr.cz/nsesss/2023/log`.

Zároveň byla odstraněna nekonzistence, kdy elementy `HodnotaID` a
`ZdrojID` byly v jiném jméném prostoru než všechny ostatní elementy
transakčního protokolu.
