# Příloha C -- Migrace dat mezi spisovými službami, spisová rozluka

Tato příloha definuje formát dat a pravidla používané při exportu dat nebo
při přenosu dat z jednoho systému do druhého (tzv. spisová rozluka).

## Archiv s dávkou

Data se přenášejí jako archiv ve formátu ZIP definovaném ve
specifikaci
[APPNOTE](https://pkware.cachefly.net/webdocs/APPNOTE/APPNOTE-6.3.10.TXT)
a musí navíc splnit následující požadavky:

* Soubory uložené v archivu musí být nekomprimované nebo musí používat
  kompresní metodu „deflate“ popsanou v RFC1951.

* Archiv nesmí používat šifrování.

* Archiv nesmí používat digitální podpisy.

* Archiv nesmí používat funkci „patch data“.

* Archiv nesmí být rozdělen do více souborů.

* Jména souborů musí být uložena v kódování UTF-8 a musí být nastaven
  příznak „Language encoding flag“ (bit 11).

* Archiv musí v kořenovém adresáři obsahovat soubor `manifest.xml`,
  který obsahuje kořenový element `Davka` validní vůči schématu
  `ermsExportPrenos.xsd`.

## Přenos entit

Všechny entity a jejich metadata se přenášejí uvnitř archivu ZIP a je
doporučeno je ukládat do vhodné adresářové struktury uvnitř archivu.

Dávka v souboru `manifest.xml` kromě nezbytných metadat obsahuje
seznam všech entit, které se přenášejí/exportují. Pro každou entitu je
zde odkaz na další dokument XML, který popisuje jednu entitu. Soubor s
popisem entity musí použít kořenový element `Export` validní vůči
schématu `ermsExportPrenos.xsd`.

## Potvrzení přenosu

Pokud se při spisové rozluce data přenášejí z jednoho systému do
druhého, první systém data smaže až poté, co obdrží potvrzení o
úspěšném a kompletním přenosu. Potvrzení má podobu dokumentu XML,
který má kořenový element `PrenosPotvrzeni` validní vůči schématu
`ermsExportPrenos.xsd`.
