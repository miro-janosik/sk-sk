# sk-sk

Repository containing source resources for training Speech-to-text (ASR) models for low-resource language Slovak and Carpathian Romani dialect used in Slovakia.

Repozitár obsahujúci zdrojové dáta na trénovanie modelov pre prevod Reč-do-textu.

# Cieľ

Nazbierať nahrávky a prepisy nahrávok, ktorých bude dostatok a s voľnou licenciou na vytvorenie ASR modelu buď nekomerčného, alebo aj na komerčné účely.

Taktiež na zbieranie dát ktoré sú používané slovenskými dialektami, nárečiami, prípadne slovenská rómčina.

# Prechodné odkazy na možné dáta:

## Librivox

https://librivox.org/search?primary_key=57&search_category=language&search_page=1&search_form=get_results
    Slovak (in Universal Declaration of Human Rights, Volume 02)
    Complete | Collaborative | Multilingual, 326MB

    Slovak - Závet (in The Testament)
    Complete | Poetry_weekly | Multilingual, 17MB

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
