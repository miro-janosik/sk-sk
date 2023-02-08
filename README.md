# sk-sk

Repository containing source resources for training Speech-to-text (ASR) models for low-resource language Slovak and Carpathian Romani dialect used in Slovakia.

Repozitár obsahujúci zdrojové dáta na trénovanie modelov pre prevod Reč-do-textu.

# Status - stav

Collecting ideas, listing sources.

Zbieranie nápadov, tvorba zoznamov zdrojov dát

# Ciele

 * Nazbierať nahrávky a prepisy nahrávok, ktorých bude dostatok a s voľnou licenciou na vytvorenie ASR modelu buď nekomerčného, alebo aj na komerčné účely.
 * Zbieranie dát ktoré sú používané slovenskými dialektami, nárečiami, prípadne slovenská rómčina.
 * Investovať čas do kontroly nahrávok, prečistenia a doladenia formy aby boli použiteľné na trénovanie ASR modelu.
 * Zverejniť natrénovaný model, a modely podskupín (dialekty, príkazy, phonecall 8khz) a postupne ho zlepšovať

# Ďalšie kroky

 * Zbieranie zdrojov
 * Tvorba a úprava metodiky - formátov pre audio, prepisy, jazykový korpus - inšpirácie existujúcimi korpusmi. Pokiaľ možno aj vrátane anonymizovaného SpeakerId

# Neskôr

 * Kontrola licenčných podmienok dát
 * Vytvorenie modelu výslovnosti, foném - potrebné pre tvorbu modelu
 * Získanie veľkej databázy iba textu (10gb) na tvorbu jazykového modelu
 * Delenie dlhých nahrávok pomocou VoiceActivityDetector

# Možné dáta:

## Librivox

~~~
https://librivox.org/search?primary_key=57&search_category=language&search_page=1&search_form=get_results

    Slovak (in Universal Declaration of Human Rights, Volume 02)
    Complete | Collaborative | Multilingual, 326MB

    Slovak - Závet (in The Testament)
    Complete | Poetry_weekly | Multilingual, 17MB
~~~

## Mozzila Common Voice

short sentences
~~~
https://commonvoice.mozilla.org/en/datasets

Slovak
Common Voice Corpus 11.0	9/21/2022	377.74 MB	Validated hours: 19	CC-0	145
~~~

## Tatoeba
https://tatoeba.org/en/downloads

## OpenSLR

https://www.openslr.org/index.html
https://www.openslr.org/12 librispeech

## OSCAR

Check what is available. https://oscar-project.org/post/oscar-v22-01/

## Nezaradené

 - https://github.com/hromi/our-voices-model-competition/tree/main/submit/Variant_Accent_Dialect/SlovakoCzech-band-C
 - Slovak corpora database from Slovak Language institute: korpus.sav.sk => https://korpus.sk/
 - there were done a lot of recordings in the past where one interviewer was collecting all the small town dialects recordings
 - Parliament speech recordings and transcripts
 - Podcasts
   - newspapers podcasts published with source texts (require cleaning) - sme, dennikn
   - http://www.repository.voxforge1.org/downloads/SpeechCorpus/Trunk/
 - https://kinit.sk/research/natural-language-processing/
 - https://sciendo.com/article/10.2478/jazcas-2021-0053
 - RTVS

# Štruktúra

~~~
  +- folder1
  |    info.ini
  |    audio files (wav, mp3)
  |    transcripts (txt, ?)
  |
  |
  +- folder2
  |    ...
~~~

# info.ini

~~~ini
   Name=Name of the dataset part
   NumHoursAudio=10.2
   NumHoursVAD=9.8
   Tags=slovak,romani,radio,television,phonecall,streetrecording,8khz,(dialects...)
   Source=
   LicenseCC=CC BY-NC-ND 4.0 # from https://creativecommons.org/
   LicenseText= or url
~~~

# kde môže byť výsledný model zverejnený, využitý

 * https://alphacephei.com/vosk/ (publicly available ASR for PC and small computers)
 * https://github.com/rhasspy/rhasspy (small computer voice assistant)
 * v akomkoľvek projekte ktorý vyžaduje ASR, či už hlasový asistent, alebo prepis audia do textu, titulkovania, systému kedy sa nedá použiť online pripojenie (ktoré vyžaduje napríklad Google), toto môžu byť aj hobby-projekty ale aj komerčné projekty
 * titulkovanie videí pre nepočujúcich, napríklad záznamov z festivalov a prednášok
 * dostupnosť aj pre výskumníkov a komerčné subjekty (podľa licencie dát)
 * rozvoj jazyka a jazykových technológi
 
