Language Modeling with Neural Nets
This project explores the foundational stages of building a large language model. It begins with simple bigram and trigram frequency models and progresses toward neural network-based prediction.


***Bigram*** 

We begin in the bigram model where we generate a probability matrix based on every letter and the probability of the next letter. Upon calculating the normalized loss at: 2.5476.

This becomes important as this is the smallest loss that can be obtained using a bigram model on this set of words. It is trained on the complete set and the exact probabilities of each preceding letter. Upon running the training a couple times without a lot of optimization: 

Iteration 0: 2.5717759132385254

Iteration 10: 2.584181547164917

Iteration 20: 2.565087080001831

Iteration 30: 2.5721383094787598

Iteration 40: 2.584561347961426

Iteration 50: 2.57720685005188

Iteration 60: 2.572263240814209

Iteration 70: 2.5789268016815186

Iteration 80: 2.595059871673584

Iteration 90: 2.5762507915496826

 
This leads us to a difference of 0.02865079154 -- pretty good for not a totally optimized network.


Generating some words gave us: 

sscorerrmonrindringaspledoulionnishasumeablaly.

onun.

rinabblin.

sviopoes.

sere.

ideon.

tiog.

telabiasambleurac.

relly.

llyrararblis.

abecasstagramoron.

hgeerbmalotimackunfentadalesubicha.

gerbrrespriorinespeprivesacrdet.

celetc.

ocacookarrustethraterdiexpppoweg.

bumicyrestuly.

lictum.

meelathunereerafonged.

c.

ar.

g.

siniohy.

jasiatuldind.

cofumiziempaidese.

mpepochesizilie.

ve.

ylintus.

lagg.


None of which look super great. Let's see if a trigram can achieve slightly better results.


***Trigram***

Generating a similar probability matrix, this time looking at a series of 2 letters and the probability any individual letter comes next gives us a new matrix that is (729,27). Looking at the cost function of straight probability optimization we get: 2.2377. A noticable step up from the bigram. 

Following similar steps and training a net we are able to train to: 

Iteration 0: 2.5145952701568604

Iteration 10: 2.4939260482788086

Iteration 20: 2.475533962249756

Iteration 30: 2.4591174125671387

Iteration 40: 2.444380044937134

Iteration 50: 2.4310340881347656

Iteration 60: 2.418883800506592

Iteration 70: 2.407808303833008

Iteration 80: 2.397698163986206

Iteration 90: 2.3884317874908447


Which can easily be improved by more steps and marginal steps. Point is that the loss is lower, the trained net converges to lower and some words (although not much) seem to be a bit better.

oleaurdid.

blwizjwxeolalaqphavinimph.

kpaml.

lint.

uewassputeoe.

qyo.

aaoasiropoyggnstilllagerdfliyaftilifftudgutr.

azoposymftude.

olpe.

hark.

xidscarcelgaqffimirdo.

ke.

aj.

koterte.

qbbe.

biqw.

gpurtihyfze.

euiddo.

gge.





