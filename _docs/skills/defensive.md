---
title: "Defensive"
permalink: /docs/skills/defensive/
excerpt: "Skill difensive"
toc: true
last_modified_at: 2018-03-20T15:19:22-04:00
---

## Detecting Hidden

Permette di rivelare gli hiddati entro 10 tiles dal punto bersagliato.

Il successo o il fallimento del rivelamento dipendono da diversi fattori:

CASO 1: tu hai detective hidden (senza tracking) e l’avversario hiding (senza stealth)

Successo rivelamento = tua detective hidden ≥ hiding  avversario

fallimento rivelamento = hiding avversario > tua detective hidden

CASO 2: tu hai 100 detective hidden + qualsiasi valore in tracking e l’avversario ha 100 hiding + qualsiasi valore in stealth

Successo rivelamento = tua tracking ≥ stealth avversario

fallimento rivelamento = stealth avversario > tua tracking

NOTA BENE: il caso 2 si “attiva” se e solo se avete esattamente 100 detective hidden / hiding altrimenti vale sempre la regola esposta nel caso 1!

## Healing

Abilità necessaria per curarsi con Bende e Magie

– All’attivazione, ti permette di curare i tuoi hp consumando 1 benda (bendata).

Il tempo base di bendata è di 9 secondi con 0 anatomy e di 4 secondi con 100 di anatomy (-1 secondo ogni 20 di anatomy)

La cura base per bendata è di 4 hp con 0 healing e di 44 hp con 100 healing (+0,4 hp ogni 1 di healing)

Il tempo di bendata viene aumentato di 0.5 secondi con 100 Evaluating Intelligence e di 1.5 secondi con 100 Inscription.

– Per quanto riguarda curare i tuoi hp con la magia, aprendo lo spellbook troverai le magie Heal, Greater Heal. La Cura dei tuoi hp è stabilita dal valore della skill Healing. Inoltre con la skill Ritualism darai un Bonus ulteriore alla Magia.

## Hiding

Permette di scomparire dalla vista degli altri (hiddarsi).

Riuscirai ad hiddarti con successo se non ci sono altri pg entro un certo range dalla tua posizione.

Il range di base è di 16 tiles. Può essere aumentato o diminuito da diversi fattori:

– skill: all’aumentare della skill, diminuirà il range ( -1 tile ogni 10 punti skill)
– dismounted: se sei nello status di “dismount”, diminuirà il range (-5 tiles)
– Physical Resistance: all’aumentare della physical resistance, aumenterà il range

In ogni caso, il range non può scendere al di sotto di 2 tiles

La durata dell’hiding dipende dalla skill (ad esempio: 1 di skill = 1,5 sec / 10 di skill = 15 sec / 100 di skill = 150 sec)

Formule:
range = base_range – skil_decrease_tile – not_mountedBonus + armor_malus;
base_range = 16
skill_decrease_tile = hiding_skill /10
armor_malus = Math.Pow(m.PhysicalResistance,2) * (10/Math.Pow(44, 2))
not_mountedBonus = 5
durata dell’hiddata = 1.5 * Hiding_skill

## Parrying

Parrying permette di parare colpi fisici e magici indossando uno scudo, Inoltre ti permette di usare un “Taunt”, ovvero attirare mostri verso se stesso in modo da nn far prendere danno ai suoi compagni di squadra, il personaggio ha una barra di caricamento, quando viene colpito accumula dei punti che puo utilizzare  usando la skill sul npc che si desidera attirare.

I colpi vengono parati solo se il pg che para si rivolge verso l’aggressore.

Gli attacchi subiti da altre direzioni non saranno ridotti.

Le percentuali di riduzione del danno con 100 parrying sono le seguenti:

30% riduzione danno delle armi da macer
40% riduzione danno delle armi da sword
50% riduzione danno delle armi da fencer
60% riduzione danno delle armi da archer

La riduzione del danno aumenta ulteriormente se sei dismounted (+30%) o indossi uno scudo di secondo livello, di maggiore qualità rispetto ad uno scudo basilare di primo livello. (+10%)

La riduzione del danno magico è del 10% a cavallo e del 20% a piedi (calcolato sul danno assoluto della magia con 100 di skill)

## Resisting Spells

Riduce passivamente tutto il danno magico subito dell’ 1% ogni 5 di skill (20% riduzione del danno magico a 100)

Riduce l’effetto delle magie Curse, Weaken, Clumsy, Feeblemind dell’ 1% ogni 5 di skill
Riduce il danno subito dal veleno dell’ 1% ogni 5 di skill
Riduce la durata di Paralyze dell’ 1% ogni 5 di skill

## Ritualism

Skill che potenzia gli effetti benefici di Buff,Magie e Pozioni:

Con 100 di Ritualism:

Le magie Heal, Greater Heal raddoppiano la cura (queste magie hanno efficacia se correlate a Magery e Healing).

Le magia con Buff benefici (Esempio Bless) raddoppiano il valore di Buff (se correlata con Magery)

Aumenta l’effetto di pozioni Benefiche (Heal potion,Strenght potion,Mana potion)

## Stealth

Ti permette di camminare e correre mentre sei hiddato ma consumerai molta stamina e sarai rivelato automaticamente se non ne hai più (è possibile utilizzare Full Refresh durante l’hiding).

Va in combo con Hiding contro Detective Hidden.

## Wrestling

Riduce il danno fisico subito. Tale bonus si “attiva” indossando una staffa:

Con 100 di wrestling:

la light staff riduce il danno fisico del 10% da dismounted e del 5% da mounted

la heavy staff riduce il danno fisico del 20% da dismounted e del 10% da mounted