## Näytä lämpötila

Voit yhdistää lämpötilalukemasi kuvaan näyttääksesi lämpötilan myös graafisella tavalla. Esimerkiksi saatat näyttää lumimyrskyn kylmille lämpötiloille ja aurinkoisen päivän kuumille lämpötiloille:

![Kuuma ja kylmä](images/hot-and-cold.png)

--- task ---

Lisää ohjelman loppuun uusia värimuuttujia kaikille väreille, joita haluat käyttää kuvissasi. Olet ehkä jo määritellyt joitakin niistä edellisessä vaiheessa. Esimerkeissämme käytämme valkoista (`w`), keltaista (`y`), vihreää (`g`) ja mustaa/tyhjää (`b`).

```python
w = (255, 255, 255)
y = (255, 255, 0)
g = (0, 255, 0)
b = (0, 0, 0)
```

--- /task ---

--- task ---

Aivan kuten aiemminkin, piirrä kuvat luomalla ensin listan jokaista varten, ja sitten täyttämällä listan kohdat väreillä, joilla haluat pikselisi esitettävän.

```python
hot = [
  b, b, b, b, b, y, y, b,
  b, b, b, b, y, y, y, y,
  b, b, b, b, b, y, y, b,
  b, b, b, b, b, b, b, b,
  b, b, b, b, b, b, b, b,
  b, b, b, b, b, b, b, b,
  g, g, g, g, g, g, g, g,
  g, g, g, g, g, g, g, g
]


cold = [
  b, b, w, b, b, b, w, b,
  b, b, b, b, b, w, b, b,
  b, w, b, b, b, b, b, w,
  b, b, b, b, w, b, b, b,
  w, b, b, w, b, b, w, b,
  b, b, b, b, b, b, b, b,
  w, w, w, w, w, w, w, w,
  w, w, w, w, w, w, w, w
]
```

--- /task ---

--- task ---

Lisää koodi lämpötilan saamiseksi:

```python
temp = sense.temperature
```

--- /task ---

--- task ---

Päätä nyt, minkä kuvan haluat esitettäväksi. Tässä esimerkissä näytämme kuvan `hot`, jos lämpötilan lukema on 20 astetta tai sen yli, ja kuvan `cold`, jos lämpötilan lukema on alle 20 astetta.

```python
temp = sense.temperature
if temp >= 20:
    sense.set_pixels(hot)
else:
    sense.set_pixels(cold)
```

--- /task ---

--- task ---

Käytä lämpötilan liukusäädintä asettaaksesi lämpötilan emulaattorissa. Suorita ohjelma ja tarkista, että kyseiselle lämpötilalle valittu kuva näytetään oikein.

--- /task ---

--- task ---

Muuta koodiasi niin, että ohjelma näyttää lämpötilan astronauteille omalla valitsemallasi tavalla.

--- /task ---