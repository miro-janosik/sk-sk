# sk-sk

Repository containing source resources for training Speech-to-text (ASR) models for low-resource language Slovak and Carpathian Romani dialect used in Slovakia.

Repozitár obsahujúci zdrojové dáta na trénovanie modelov pre prevod Reč-do-textu.

# Status

Initial ideas, listing sources

# Cieľ

 * Nazbierať nahrávky a prepisy nahrávok, ktorých bude dostatok a s voľnou licenciou na vytvorenie ASR modelu buď nekomerčného, alebo aj na komerčné účely.
 * Zbieranie dát ktoré sú používané slovenskými dialektami, nárečiami, prípadne slovenská rómčina.
 * Investovať čas do kontroly nahrávok, prečistenia a doladenia formy aby boli použiteľné na trénovanie ASR modelu.
 * Zverejniť natrénovaný model, a modely podskupín (dialekty, príkazy, phonecall 8khz) a postupne ho zlepšovať

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

## Nezaradené

 * https://sciendo.com/article/10.2478/jazcas-2021-0053
 * RTVS

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
