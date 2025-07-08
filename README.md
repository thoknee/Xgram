#  Language Modeling with Neural Nets

This project explores the foundational stages of building a large language model. It begins with simple **bigram** and **trigram** frequency models and progresses toward neural network-based prediction.

---

##  Bigram

We begin with the bigram model, where we generate a **probability matrix** based on each letter and the likelihood of the next letter. The lowest achievable normalized loss for a perfect bigram model on this dataset is approximately:

```
Loss = 2.5476
```

Training without much optimization gives the following results:

```
Iteration 0:  2.5718
Iteration 10: 2.5842
Iteration 20: 2.5651
Iteration 30: 2.5721
Iteration 40: 2.5846
Iteration 50: 2.5772
Iteration 60: 2.5723
Iteration 70: 2.5789
Iteration 80: 2.5951
Iteration 90: 2.5763
```

This results in a difference from optimal of only `0.0287` — not bad for a simple, unoptimized network!

###  Example Bigram-Generated Words
```
sscorerrmonrindringaspledoulionnishasumeablaly
onun
rinabblin
sviopoes
sere
ideon
tiog
telabiasambleurac
relly
llyrararblis
abecasstagramoron
hgeerbmalotimackunfentadalesubicha
gerbrrespriorinespeprivesacrdet
celetc
ocacookarrustethraterdiexpppoweg
bumicyrestuly
lictum
meelathunereerafonged
c
ar
g
siniohy
jasiatuldind
cofumiziempaidese
mpepochesizilie
ve
ylintus
lagg
```

While the results aren’t coherent, this forms the baseline for improvement.

---

##  Trigram

We now use a **trigram** model, where we calculate the probability of a letter given the two preceding letters. The resulting probability matrix has shape `(729, 27)`.

The theoretical minimum loss (based on probability optimization) improves to:

```
Loss = 2.2377
```

Training the trigram-based network yields:

```
Iteration 0:  2.5146
Iteration 10: 2.4939
Iteration 20: 2.4755
Iteration 30: 2.4591
Iteration 40: 2.4444
Iteration 50: 2.4310
Iteration 60: 2.4189
Iteration 70: 2.4078
Iteration 80: 2.3977
Iteration 90: 2.3884
```

This clearly shows improvement over the bigram network. With more training and tuning, the model could converge even closer to optimal.

###  Example Trigram-Generated Words
```
oleaurdid
blwizjwxeolalaqphavinimph
kpaml
lint
uewassputeoe
qyo
aaoasiropoyggnstilllagerdfliyaftilifftudgutr
azoposymftude
olpe
hark
xidscarcelgaqffimirdo
ke
aj
koterte
qbbe
biqw
gpurtihyfze
euiddo
gge
```

The outputs still contain nonsense, but some show slightly more structure and consistency compared to the bigram model.
