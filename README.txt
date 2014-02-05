Ovaj projekt je izra�en u sklopu kolegija Bioinformatika na Fakultetu elektrotehnike i ra�unarstva Sveu�ili�ta u Zagrebu 2014. godine.
Cijeli zadatak je uklju�ivao i implementacije u Javi i Pythonu.

Implementacija se pokre�e naredbom:
./biobloom ["-f"] "textfile.txt" ["queryFile.txt"]
Dakle, prilikom pokretanja je nu�no navesti barem jedan argument ("textfile.
txt"). Taj argument mora biti put do tekstualne datoteke koja u svakoj zasebnoj
liniji sadr�i klju� koji �e biti dodan u bloom filter. Pritom je u prvoj liniji mogu�e
navesti i �eljeni postotak pogre�ke u rasponu [1-99]%. Redak u tom slu�aju mora
zapo�injati s �?�.
Npr:
?1
wlhhxvd0
...
Datoteka mora biti formatirana za uporabu u unix okru�enju (lf umjesto crlf).
Ukoliko se implementacija pokrene u ovom modu rada, tada se nakon u�itavanja
svih klju�eva korisniku omogu�i postavljanje upita putem konzole. Iz tog
modula rada se izlazi postavljanjem upit ":Q".
Drugi na�in rada je da se osim ulazne datoteke s klju�evima definira i datoteka
u kojoj je zapisan neki upit ("queryfile.txt"). U tom se slu�aju nakon u�itavanja
svih klju�eva otvara i ta datoteka, te se vr�i provjera nalazi se klju� koji je tamo
zapisan u bloom filteru, te se rezultat ispisuje na ekran.
Prilikom pokretanja je mogu�e i postaviti zastavicu "-f". Ukoliko se postavi,
implementacija �e pretpostavljati da su svi zapisi u datotekama u FASTA formatu.

Uz prilo�enu testnu datoteku, implementacija se pokre�e naredbom:
./biobloom keyList.txt
Nakon toga je mogu�e upisati elemente koji postoje (npr. wlhhxvd0, e74...),
ili neke koji ne postoje u bloom filteru (npr. fer, fakultet, otorinolaringologija...).
Rezultat se ispisuje na ekran.