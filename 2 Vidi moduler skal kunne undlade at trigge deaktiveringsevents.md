# RFC 2: Vidi moduler skal kunne undlade at trigge deaktiveringsevents

## 1. Motivation
Når der skiftes mellem moduler (lagtræ, baggrunds, tegning mv.) udløses en stop- og oprydningshandling som alle moduler lytter til. Det enkelte modul skal så sørge for at deaktivere og rydde op efter sig. Det betyder, at to eller flere moduler ikke kan være aktive på samme tid. Dette har gjort det mere enkelt at skrive moduler, da man ikke skal tage stilling til hvilke moduler, som ikke fungerer sammen og derfor skal deaktiveres. Men det har den store ulempe, at hvis man fx laver en konfliktsøgning og gerne vil have skiftet baggrundskort, bliver konfliktsøgningen deativeret og nulstillet.   

## 2. Foreslået løsning
En række moduler skal beskrives som "passive". Dvs. at de ikke ændrer klik-i-kortet-handlingen eller aktiverer tegneværktøjer. Af standardmodulerne er det: Lagtræ, baggrundskort, signatur og projekter. Af extensions kan nævnes Koordinater.

På en eller måde skal modulet undertrykke stop- og oprydningshandlin, der bliver udløst ved skift mellem moduler. Det er vigtigt, at denne undertrykkelse er placeret i modulet kode, således module-forfatteren selv kan implementere undertrykkelsen.

## 3. Problemer med bagudkompatibilitet

## 4. Sikkerhedsmæssige implikationer

## 5. Performance-implikationer

## 6. Dokumentationsbehov

## 7. Issue tracker
