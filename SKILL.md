---
name: klarsprak
description: >-
  Skriv om tekst til klar, presis og naturlig norsk. Bygger på ASD-STE100
  (Simplified Technical English), tilpasset norsk. Bruk når brukeren ber om å
  «skrive om», «forenkle», «gjøre lettere å forstå», «klarspråk», «STE», «enkel norsk», eller
  sier at en tekst er knotete, tung eller uklar. Gjelder Jira-kommentarer,
  Slack-meldinger, spørsmål til fagpersoner, MR-beskrivelser og dokumentasjon.
---

# Klarspråk (bygger på ASD-STE100)

Målet er tekst som leseren forstår på første forsøk. Teksten skal samtidig lyde som et menneske har skrevet den.

## Prioritering

Reglene under er hjelpemidler. Når to hensyn kolliderer, gjelder denne rekkefølgen:

1. **Behold meningen.** Ikke fjern innhold, alternativer eller reell usikkerhet. Ikke legg til fakta.
2. **Gjør teksten lett å forstå.** Leseren skal ikke måtte lese en setning to ganger.
3. **Skriv naturlig norsk.** Hvis en regel gir en stiv eller oppstykket setning, bryt regelen.
4. **Følg retningslinjene** når de ikke kommer i veien for punkt 1 til 3.

ASD-STE100 er laget for engelske vedlikeholdsmanualer. Vi bruker prinsippene, men ikke ordlisten og ikke reglene som bare passer for engelsk.

## Arbeidsflyt

1. Les teksten og finn hva leseren skal vite eller gjøre.
2. Del teksten i påstander og spørsmål.
3. Skriv hver setning på nytt etter retningslinjene under.
4. Les resultatet høyt for deg selv. Rett det som lyder som en robot eller et telegram.
5. Sammenlign med originalen. Sjekk at alt innholdet er med.
6. Gi bare den omskrevne teksten. Ikke forklar endringene med mindre brukeren spør.

Den omskrevne teksten skal alltid være fullstendig, vanlig norsk. Dette gjelder også når resten av samtalen har en kortere eller mer komprimert stil.

## Retningslinjer

### Setninger
- Sikt mot korte setninger. Del en setning som har mer enn 25 ord. Instruksjoner bør ha under 20 ord.
- Skriv én hovedpåstand eller ett spørsmål per setning. En kort begrunnelse eller betingelse kan stå i samme setning.
- Behold bindeord som «fordi», «derfor», «men» og «så». Bindeordene viser sammenhengen, og uten dem blir teksten hakkete.
- Ikke utelat småord for å spare plass. Behold «at», «som» og subjektet.
- Varier setningslengden. Mange like korte setninger på rad er tunge å lese.
- Sett hovedsaken tidlig i setningen. En kort betingelse kan stå først: «Hvis testen feiler, start jobben på nytt.»
- Skriv ett tema per avsnitt, og hold avsnittene korte.

### Aktiv og passiv
- Bruk aktiv form når du vet hvem som handler: «administratoren velger», ikke «det velges».
- Bruk aktiv form i instruksjoner.
- Passiv er greit i beskrivelser når aktøren er ukjent eller uviktig: «Meldingen ble sendt 3. mai», «Feltet vises ikke».
- Ikke finn på en aktør bare for å unngå passiv.
- Unngå «man» når du vet hvem det gjelder.

### Verb
- Bruk presens når det er mulig, også om framtid: «Vi leverer endringen på torsdag.»
- Perfektum er vanlig norsk og er greit: «Vi har lagret valget.»
- Unngå kjeder av hjelpeverb: «systemet kan lagre», ikke «systemet vil kunne komme til å lagre».
- Bruk modalverbene med fast betydning:
  - «skal» betyr krav eller noe som er bestemt
  - «må» betyr at noe er nødvendig
  - «bør» betyr anbefaling
  - «kan» betyr at noe er mulig eller tillatt
- Skriv steg i dokumentasjon i imperativ: «Oppdater beskrivelsen.»
- Når du ber et menneske om noe, spør høflig: «Kan du oppdatere beskrivelsen?»

### Ord
- Bruk korte, vanlige ord. Velg «bruke» framfor «benytte», og «før» framfor «forut for».
- Bruk samme ord for samme ting hele veien. Ikke bytt mellom «regel», «varslingsregel» og «e-postvarslingsregel» i samme tekst.
- Bruk navnet på feltet eller knappen nøyaktig slik det står i løsningen, i anførselstegn: «Hvem kan redigere?».
- Behold etablerte fagord og domeneord. Forklar dem bare hvis leseren ikke kjenner dem.
- Bruk ordene teamet bruker, også engelske: «merge request», «deploy». Ikke oversett et ord teamet ikke oversetter.
- Unngå lange sammensetninger som ikke er etablerte ord. Løs dem opp med preposisjon: «regel for varsling på e-post». Del aldri et sammensatt ord med mellomrom.
- Unngå substantivering: «når en bruker velger», ikke «ved valg av».
- Gjenta substantivet når «dette», «det» eller «den» kan peke på flere ting.
- Stryk fyllord: «egentlig», «i utgangspunktet», «på en måte».
- Behold forbehold som sier noe reelt. «Feilen skyldes trolig cachen» er ikke det samme som «Feilen skyldes cachen».
- Følg formvalgene i originalteksten, for eksempel «fram» eller «frem». Vær konsekvent i hele teksten.

### Tegnsetting
- Unngå tankestrek, semikolon og parentes midt i setninger. Lag heller to setninger.

### Spørsmål
Denne delen kommer ikke fra STE.

- Still ett spørsmål per punkt.
- Gi leseren nok bakgrunn til å svare. Fortell først hvordan det er i dag, og spør så. Felles bakgrunn kan stå i én linje over spørsmålene.
- Ikke finn på bakgrunn som ikke står i originalen. Spør brukeren hvis bakgrunnen mangler.
- Lag ja/nei-spørsmål eller spørsmål med tydelige svaralternativer når det går.
- Hvis to ting kan avklares hver for seg, lag to spørsmål.
- Behold alle alternativene fra originalen.

### Struktur
- Start med hva du vil og hvorfor, i én eller to setninger.
- Bruk nummererte lister for spørsmål og steg, og punktlister for fakta.
- Ikke lag liste av noe som er en sammenhengende forklaring. Skriv forklaringen som avsnitt.
- Legg merknader og tilleggsinformasjon etter hovedinnholdet, i egne avsnitt.
- Ikke skriv kode, filstier eller linjenumre til lesere som ikke er utviklere.

## Eksempler

### Spørsmål til fagperson

Før:
> Når «Del med andre» er satt til **Ja**: gjelder «Hvem kan redigere?» og unntakene for gjestebrukere fortsatt, eller er dette en egen mappetype uten disse feltene?

Etter:
> Spørsmålene gjelder mapper der «Del med andre» er satt til «Ja».
>
> 1. Skal feltet «Hvem kan redigere?» fortsatt gjelde for disse mappene?
> 2. Skal unntakene for gjestebrukere fortsatt gjelde for disse mappene?
> 3. Er en mappe med «Ja» en egen mappetype, uten feltet «Hvem kan redigere?» og uten unntakene for gjestebrukere?

### Sammenhengende tekst

Før:
> Grunnet at det ved kjøring av nattjobben ble avdekket at enkelte bestillinger ikke ble plukket opp (trolig pga. manglende indeksering – dette undersøkes), er det i utgangspunktet besluttet å utsette lanseringen til over helgen, noe som egentlig ikke bør ha konsekvenser for kundene.

Etter:
> Vi utsetter lanseringen til over helgen, fordi nattjobben ikke plukket opp alle bestillingene. Årsaken er trolig at en indeks mangler, men vi undersøker fortsatt. Utsettelsen bør ikke få konsekvenser for kundene.

Teksten er fortsatt et avsnitt, ikke en liste. Bindeordene «fordi» og «men» er beholdt, og forbeholdene «trolig» og «bør» står fordi de sier noe reelt.

## Sjekkliste

- [ ] Er alt innholdet fra originalen med, også alternativer og reelle forbehold?
- [ ] Forstår leseren hver setning på første forsøk?
- [ ] Lyder teksten naturlig når du leser den høyt?
- [ ] Er setninger over 25 ord delt?
- [ ] Sier setningene hvem som handler, der det er kjent?
- [ ] Bruker teksten samme ord for samme ting hele veien?
- [ ] Står feltnavn nøyaktig slik de står i løsningen?
- [ ] Er fyllord, tankestreker og semikolon borte?
- [ ] Peker «dette», «det» og «den» tydelig på én ting?
- [ ] Kan leseren svare på hvert spørsmål med bare bakgrunnslinjen og spørsmålet?
