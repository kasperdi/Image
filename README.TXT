OPGAVE 1

I Pixel klassens metode setValue er der en if-statement der tester,
om v�rdien af en pixel kommer over 255 eller under 0. Hvis dette sker,
s�tter den pixlens v�rdi til hhv. 255 og 0.

Dette betyder ogs�, at vi mister kvalitet, da nogle pixels vil blive lysere end andre.
Hvis vi derfor benytter brigthen efterfulgt af darken, vil vi ikke f� samme billede.


OPGAVE 2

Problemet med disse metoder er, at vi ikke kan gemme en pixels v�rdi i samme image, 
uden at overskrive en anden pixel. I princippet beh�ver vi dog kun at gemme halvdelen
af et image, og derefter kan vi overskrive i den gemte del.

Alternativt kunne man lave en swap metode, som tog to pixler som input, og byttede dem rundt:

public void swap(Pixel pixel1, Pixel pixel2) 
    {
        Pixel temp = pixel1;
        pixel1 = pixel2;
        pixel2 = temp;
    }

Dette er dog identitisk med at kopiere halvdelen af billedet, da "temp" koiperer halvdelen af
alle pixels.
