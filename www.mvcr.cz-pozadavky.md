# Požadavky na publikování příloh Národního standardu pro elektronické systémy spisové služby na webu MVČR

## Stránka s distribucí schémat

Na vhodném místě webu vytvořit stránku, kde bude odkaz na stažení
distribuce schémat a dokumentace, tj. na soubor
`nsessl-schema-YYYYMMDD.zip` v jeho aktuální verzi.

Pokud budou v budoucnu vydávány další verze distribuce, bylo by vhodné
mít zde archiv předchozích verzí.

Na stránce umístit i odkaz na https://github.com/nsessl/schema
kde probíhá další vývoj schémat, sběr připomínek atd.

## Schémata přímo přístupná přes HTTP

Na adresu http://www.mvcr.cz/nsesss/v4 je potřeba umístit všechny
soubory, které se nacházejí v podadresáři `src` distribuce schémat.

Soubory musí být vraceny se správnými typem média `text/xml`.
(hlavička `Content-Type`).

## Stránky jmenných prostorů

Na adresy

* http://www.mvcr.cz/nsesss/v4
* http://www.mvcr.cz/nsesss/2023/api
* http://www.mvcr.cz/nsesss/2023/log

je potřeba umístit stránku s následujícím obsahem:

> Toto je jmenný prostor používaný v dokumentech XML definovaných v
> Národním standardu pro elektronické systémy spisové služby.
>
> Další informace:
>
> * _Odkaz na standard a jeho přílohy_
> * _Odkaz na stránku s distribucí schémat_

