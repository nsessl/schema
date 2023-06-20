# Příloha 7 -- Schéma XML pro migraci dat mezi elektronickými systémy spisové služby

Tato příloha definuje formát dat a pravidla používané při exportu dat nebo
při přenosu dat z jednoho systému do druhého (tzv. spisová rozluka).

## Kontejner s dávkou

Data se přenášejí jako kontejner ve formátu ZIP definovaném ve
specifikaci
[APPNOTE](https://pkware.cachefly.net/webdocs/APPNOTE/APPNOTE-6.3.10.TXT)
a musí navíc splnit následující požadavky:

* Soubory uložené v kontejneru musí být nekomprimované nebo musí
  používat kompresní metodu „deflate“ popsanou v RFC1951.

* Kontejner nesmí používat šifrování.

* Kontejner nesmí používat digitální podpisy.

* Kontejner nesmí používat funkci „patch data“.

* Kontejner nesmí být rozdělen do více souborů.

* Jména souborů musí být uložena v kódování UTF-8 a musí být nastaven
  příznak „Language encoding flag“ (bit 11).

* Kontejner musí v kořenovém adresáři obsahovat soubor `manifest.xml`,
  který obsahuje kořenový element `Davka` validní vůči schématu
  `ermsExportPrenos.xsd`.

## Přenos entit

Všechny entity a jejich metadata se přenášejí uvnitř kontejneru ZIP a
je doporučeno je ukládat do vhodné adresářové struktury uvnitř
kontejneru.

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
