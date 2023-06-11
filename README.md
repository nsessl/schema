# XML schémata pro Národní standard pro elektronické systémy spisové služby

## [Přehled změn](CHANGES.md)

## Hlášení chyb

Pokud ve schématech najdete chybu, nahlašte ji jako nové issue na
adrese https://github.com/nsessl/schema/issues/new

Pro nahlášení problému je potřeba být přihlášen pomocí GitHub účtu (to
nám umožní vás kontaktovat v případě nejasností s nahlášeným
problémem). GitHub účet si můžete zdarma založit na adrese
https://github.com/signup

## Příloha 1 – Schéma pro výměnu dokumentů a jejich metadat (WS API)

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

* [dokumentace schématu](doc/1-api/ermsAPI.html)

## Příloha 2 – Schéma pro zaznamenání popisných metadat uvnitř datového balíčku SIP

Normativní části přílohy:

* [`nsesss.xsd`](src/nsesss.xsd) – schéma pro popisná metadata

Doplňující informace:

* [dokumentace schématu](doc/2-metadata/nsesss.html)

## Příloha 3 – Schéma pro vytvoření datového balíčku

Normativní části přílohy tvoří schémata ze standardu METS:

* [`mets.xsd`](src/mets.xsd) – schéma METS
* [`mets-xlink.xsd`](src/mets-xlink.xsd) – schéma XLink používané
  schématem METS

## Příloha 4 – Schéma pro zasílání údajů o rozhodnutí ve skartačním řízení a potvrzení přejímky

Normativní části přílohy:

* [`nsesss-DA.xsd`](src/nsesss-DA.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/4-da/nsesss-DA.html)

## Příloha 5 – Schéma pro export a import spisového a skartačního plánu

Normativní části přílohy:

* [`nsesss-plan.xsd`](src/nsesss-plan.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/5-plan/nsesss-plan.html)

## Příloha 6 – Schéma pro export a import transakčního protokolu

Normativní části přílohy:

* [`nsesss-TrP.xsd`](src/nsesss-TrP.xsd) – schéma transakčního protokolu

Doplňující informace:

* [dokumentace schématu](doc/6-trp/nsesss-trp.html)

## Příloha X – ...

...

## Příloha Y – ...

...

## Příloha C – Schéma pro spisovou rozluku

Normativní části přílohy:

* [Textová část přílohy](PrilohaC.md)
* [`ermsExportPrenos.xsd`](src/ermsExportPrenos.xsd) – schéma

Doplňující informace:

* [dokumentace schématu](doc/C-export/ermsExportPrenos.html)


