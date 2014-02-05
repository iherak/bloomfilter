Ovaj projekt je izraðen u sklopu kolegija Bioinformatika na Fakultetu elektrotehnike i raèunarstva Sveuèilišta u Zagrebu 2014. godine.
Cijeli zadatak je ukljuèivao i implementacije u Javi i Pythonu.

Implementacija se pokreæe naredbom:
./biobloom ["-f"] "textfile.txt" ["queryFile.txt"]
Dakle, prilikom pokretanja je nužno navesti barem jedan argument ("textfile.
txt"). Taj argument mora biti put do tekstualne datoteke koja u svakoj zasebnoj
liniji sadrži kljuè koji æe biti dodan u bloom filter. Pritom je u prvoj liniji moguæe
navesti i željeni postotak pogreške u rasponu [1-99]%. Redak u tom sluèaju mora
zapoèinjati s ’?’.
Npr:
?1
wlhhxvd0
...
Datoteka mora biti formatirana za uporabu u unix okruženju (lf umjesto crlf).
Ukoliko se implementacija pokrene u ovom modu rada, tada se nakon uèitavanja
svih kljuèeva korisniku omoguèi postavljanje upita putem konzole. Iz tog
modula rada se izlazi postavljanjem upit ":Q".
Drugi naèin rada je da se osim ulazne datoteke s kljuèevima definira i datoteka
u kojoj je zapisan neki upit ("queryfile.txt"). U tom se sluèaju nakon uèitavanja
svih kljuèeva otvara i ta datoteka, te se vrši provjera nalazi se kljuè koji je tamo
zapisan u bloom filteru, te se rezultat ispisuje na ekran.
Prilikom pokretanja je moguæe i postaviti zastavicu "-f". Ukoliko se postavi,
implementacija æe pretpostavljati da su svi zapisi u datotekama u FASTA formatu.

Uz priloženu testnu datoteku, implementacija se pokreæe naredbom:
./biobloom keyList.txt
Nakon toga je moguæe upisati elemente koji postoje (npr. wlhhxvd0, e74...),
ili neke koji ne postoje u bloom filteru (npr. fer, fakultet, otorinolaringologija...).
Rezultat se ispisuje na ekran.