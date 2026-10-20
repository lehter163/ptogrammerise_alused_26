from math import * #pi, sqrt
from random import * #randint(a,b) juhuslik täisarv a ja b vahel

# Kirjuta enda esimene programm, mis väljastab käsureale teksti: “Tere, maailm!”. 
# Küsi kasutaja nimi ja muuda tekst, et ta näeks välja nii: “Tere, maailm! Tervitan sind Mati”, kui kasutaja nimi on Mati.

# Küsi kasutajalt sisend tema vanuse kohta ning väljasta see ekraanile:

# “Tere, maailm! Tervitan sind Mati! Sa oled N aastat vana.”
# Ülesanne1
print("Tere, maailm!")
nimi=input("Mis on sinu nimi? ")
print("Tere, maailm! Tervitan sind",nimi)
try:
    vanus=int(input("Kui vana sa oled? "))
    print("Tere, maailm! Tervitan sind",nimi,"! Sa oled",vanus,"aastat vana")
except ValueError:
    print("Palun sisesta oma vanus numbrina.")

# ülesanne 2
# Mis tüüpi on järgnevad muutujad:

# a) vanus = 18
# b) eesnimi = "Jaak"
# c) pikkus = 16.5
# d) kas_käib_koolis = True
# Mis võimalus veel peale True oleks viimast muutujat väärtustada? Kuidas võiks nende muutujate väärtusi koodis kontrollida?
# Kirjuta kood tüüpide kontrollimiseks.
vanus = 18
eesnimi = "Jaak"
pikkus = 16.5
kas_käib_koolis = True
print("vanus:",vanus,"tüüp:", type(vanus))
print("eesnimi:",eesnimi,"tüpp:", type(eesnimi))
print("pikkus:", pikkus, "tüpp:", type(pikkus))
print("kas_käib_koolis:", kas_käib_koolis,"tüpp:", type(kas_käib_koolis))

# Kirjuta enda koodis laual olevate kommide arv muutujasse(kommide arv on juhuslik). Seejärel kuva muutujas olev kommide arv ekraanile kasutades print() käsku.
# Küsi kasutajalt sisendit, mitu kommi ta soovib laualt ära võtta. Eemalda soovitud kommide arv laual olevate kommide arvust ja kuva ekraanile, kui palju komme laual nüüd on.


kommide_arv=randint(1,100) #1-100 vahel juhuslik täisarv
print("laual on",kommide_arv, "kommi.")
try:
    b=int(input("Mitu kommi soovid laualt ära võtta? "))
    kommide_arv -=b #kommidearv väheneb b võrra
    print("laual on nüüd", kommide_arv, "kommi.")
 except ValueError:
    print("palun sisesta kommid numbrina.")

# Puu läbimõõdu arvutamine
# Kirjuta programm, mis küsib kasutaja käest puu ümbermõõdu ning teatab selle peale puu läbimõõdu.

ümbermõõt=float(input("sisesta puu umbermõõt:"))

labimõõt=ümbermõõt/pi
print("puu labimõõt on:", labimõõt)

#ülesanne 5
# Arvutage Pythoni käsureal, kui pikk on ristkülikukujulise maatüki diagonaal, mille mõõtmed on Nm x Mm. N ja M küsi kasutajalt.
N = float(input("sisesta maatüki pikkus (N): "))
M = float(input("sisesta maatüki laius (M): "))
diagonaal = sqrt(N**2 + M**2) #** astendamine
print("ristkülikukujulise maatüki diagonaal on:", round(diagonaal,2))
#round() ümardab kahe kümnendkohani

#ülesanne 6
# Leidke järgnevast näiteprogrammist loogiline viga:
aeg = float(input("Mitu tundi kulus sõiduks? "))
teepikkus = float(input("Mitu kilomeetrit sõitsid? "))
kiirus = teepikkus / aeg

print ("sinu kiirus oli" + str(kiirus) + "km/h")

# ülesanne 7
# Koostada programm, mis arvutab aritmeetilise keskmise suvalisest etteantud 5 täis arvust.
# Leia nende arvude summa, jagatuna kasutaja poolt sisestatud arvuga, täisarvuline osa ja jääk
arv1=int(input("sisesta esimene täisarv: "))
arv2=int(input("sisesta teine täisarv: "))
arv3=int(input("sisesta kolmas täisarv: "))
arv4=int(input("sisesta neljas täisarv: "))
arv5=int(input("sisesta viies täisarv: "))
summa=arv1+arv2+arv3+arv4+arv5
jagaja=int(input("sisesta arv, millega jagada: "))
tulemus=summa/jagaja
print("tulemus:", tulemus) #tulemus=3.75
print("täisarvuline osa:", int(tulemus))
#
print("jääk:", summa % jagaja)

#ülesanne 8
print("  @..@")
print(" (----)")
print("( \__/ )")
print(" ^^ "" ^^ ")

#ülesanne 9 
A=float(input("sisesta A täisarv: "))
B=float(input("sisesta B täisarv: "))
C=float(input("sisesta C täisarv: "))
P=A+B+C

print("kolmnurga ümbermõõdu on: ", P)

#ülesanne 10
# Pitsa
# Võtsite sõpradega (näiteks P inimest) suure pitsa, mille hind on 12,90 €.
# Jätate teenindajale 10% jootraha.
# Koosta programm, mis arvutab, kui palju igaüks peab maksma.

p = int(input("inimeste arv: "))

hind = 12.90
jootraha = 0.10

kokku = hind + (hind * jootraha)

osa = kokku / p

print("iga inimene peab maksma:", round(osa, 2), "euro")
