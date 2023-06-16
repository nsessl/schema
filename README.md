# XML schémata pro Národní standard pro elektronické systémy spisové služby

## Přehled změn

[Přehled změn](CHANGES.md)

## Hlášení chyb

Pokud ve schématech najdete chybu,
[nahlašte ji jako nové issue](https://github.com/nsessl/schema/issues/new). Předtím
se ještě
[podívejte, zda již tato chyba není nahlášena](https://github.com/nsessl/schema/issues).

Pro nahlášení problému je potřeba být přihlášen pomocí GitHub účtu (to
nám umožní vás kontaktovat v případě nejasností s nahlášeným
problémem). [Založení GitHub účtu](https://github.com/signup).

Pokud jste nenašli přímo chybu, ale máte nějaký dotaz či nejasnost,
[využijte diskuse pro položení dotazu](https://github.com/nsessl/schema/discussions).

## Příloha 1 – Schéma XML pro výměnu dokumentů a jejich metadat (WS API)

Normativní části přílohy:

* [`ermsAPI.wsdl`](src/ermsAPI.wsdl) – definice rozhraní ve formátu
  WSDL
* [`ermsIFSyn.xsd`](src/ermsIFSyn.xsd) – schéma popisující struktury
  používané v synchroním rozhraní
* [`ermsIFAsyn.xsd`](src/ermsIFASyn.xsd) – schéma popisující struktury
  používané v asynchroním rozhraní
* [`dmBaseTypes.xsd`](src/dmBaseTypes.xsd) – schéma definující datové
  typy používané v ISDS
* [`ermsTypes.xsd`](src/ermsTypes.xsd) – schéma definující datové typy
  používané v API
* [`ermsAsynU.xsd`](src/ermsAsynU.xsd) – schéma definující datové typy
  používané v API

Doplňující informace:

* [dokumentace synchronního rozhraní](doc/1-api-sync/ermsAPI.html)
* [dokumentace asynchronní komunikace](doc/1-api-async/ermsIFASyn.html)

## Příloha 2 – Schéma XML pro vytvoření datového balíčku SIP a pro zaznamenání popisných metadat uvnitř datového balíčku SIP

Normativní části přílohy:

* [Textová část přílohy](Priloha2.rtf)
* [`nsesss.xsd`](src/nsesss.xsd) – schéma pro popisná metadata
* [`nsesss-common.xsd`](src/nsesss-common.xsd) – schéma sdílených
  datových typů

Normativní části přílohy tvoří i schémata ze standardu METS:

* [`mets.xsd`](src/mets.xsd) – schéma METS
* [`mets-xlink.xsd`](src/mets-xlink.xsd) – schéma XLink používané
  schématem METS

Doplňující informace:

* [dokumentace schématu](doc/2-metadata/nsesss.html)

Příloha v sobě slučuju i předchozí přílohu 2.

## Příloha 3 – Struktura popisných metadat pro automatizované zpracování dokumentu nebo spisu

Normativní části přílohy:

* [Textová část přílohy](Priloha3.md)
* [`nsesss-document.xsd`](src/nsesss-document.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/3-doc/nsesss-document.html)

  
## Příloha 4 – Schéma XML pro zasílání údajů o rozhodnutí ve skartačním řízení a potvrzení přejímky s identifikátory digitálního archivu původci

Normativní části přílohy:

* [`nsesss-DA.xsd`](src/nsesss-DA.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/4-da/nsesss-DA.html)

## Příloha 5 – Schéma pro export a import spisového a skartačního plánu

Normativní části přílohy:

* [`nsesss-plan.xsd`](src/nsesss-plan.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/5-plan/nsesss-plan.html)

## Příloha 6 – Schéma XML pro ztvárnění transakčního protokolu

Normativní části přílohy:

* [`nsesss-TrP.xsd`](src/nsesss-TrP.xsd) – schéma transakčního protokolu

Doplňující informace:

* [dokumentace schématu](doc/6-trp/nsesss-trp.html)

## Příloha 7 – Schéma XML pro migraci dat mezi elektronickými systémy spisové služby

Normativní části přílohy:

* [Textová část přílohy](Priloha7.md)
* [`ermsExportPrenos.xsd`](src/ermsExportPrenos.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/C-export/ermsExportPrenos.html)


