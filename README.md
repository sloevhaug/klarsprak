# Klarspråk

En skill for [Claude Code](https://claude.com/claude-code) som skriver om tekst til klar, presis og naturlig norsk.

Skillen bygger på [ASD-STE100](https://asd-ste100.org/) (Simplified Technical English), tilpasset norsk. Målet er tekst som leseren forstår på første forsøk, og som fortsatt lyder som et menneske har skrevet den.

## Hva skillen gjør

Du gir Claude en tekst som er tung, knotete eller uklar. Claude skriver teksten om, og du får bare den nye teksten tilbake.

Skillen passer for:

- Jira-kommentarer
- Slack-meldinger
- spørsmål til fagpersoner
- beskrivelser av merge requests
- dokumentasjon

## Eksempel

Før:

> Grunnet at det ved kjøring av nattjobben ble avdekket at enkelte bestillinger ikke ble plukket opp (trolig pga. manglende indeksering – dette undersøkes), er det i utgangspunktet besluttet å utsette lanseringen til over helgen, noe som egentlig ikke bør ha konsekvenser for kundene.

Etter:

> Vi utsetter lanseringen til over helgen, fordi nattjobben ikke plukket opp alle bestillingene. Årsaken er trolig at en indeks mangler, men vi undersøker fortsatt. Utsettelsen bør ikke få konsekvenser for kundene.

Hovedsaken står først, og setningene sier hvem som handler. Fyllordene er borte, men forbeholdene «trolig» og «bør» står igjen fordi de sier noe reelt.

## Installasjon

Du trenger Claude Code og git.

Klon repoet til mappen for personlige skills:

```bash
git clone https://github.com/sloevhaug/klarsprak.git ~/.claude/skills/klarsprak
```

Skillen er da tilgjengelig i alle prosjektene dine. Hvis du bare vil ha skillen i ett prosjekt, kloner du til `.claude/skills/klarsprak` i prosjektmappen.

Start en ny Claude Code-økt etter installasjonen.

### Oppdatering

```bash
git -C ~/.claude/skills/klarsprak pull
```

## Bruk

Kall skillen direkte og lim inn teksten:

```
/klarsprak <teksten din>
```

Claude bruker også skillen automatisk når du ber om det med vanlige ord, for eksempel:

- «Skriv om denne kommentaren, den er knotete.»
- «Gjør denne meldingen lettere å forstå.»
- «Kan du skrive dette i klarspråk?»

## Prinsipper

Reglene i skillen er hjelpemidler, ikke lover. Når to hensyn kolliderer, gjelder denne rekkefølgen:

1. **Behold meningen.** Innhold, alternativer og reell usikkerhet skal være med. Skillen legger ikke til fakta.
2. **Gjør teksten lett å forstå.** Leseren skal ikke måtte lese en setning to ganger.
3. **Skriv naturlig norsk.** Hvis en regel gir en stiv eller oppstykket setning, bryter skillen regelen.
4. **Følg retningslinjene** når de ikke kommer i veien for punkt 1 til 3.

De viktigste retningslinjene:

- korte setninger, med én hovedpåstand eller ett spørsmål i hver
- aktiv form når det er kjent hvem som handler
- korte og vanlige ord, og samme ord for samme ting hele veien
- bindeord som «fordi», «men» og «derfor» blir stående, slik at teksten henger sammen
- ingen fyllord, tankestreker, semikolon eller parenteser midt i setninger
- spørsmål får bakgrunn først og tydelige svaralternativer

Alle retningslinjene står i [SKILL.md](SKILL.md).

## Forholdet til ASD-STE100

ASD-STE100 er laget for engelske vedlikeholdsmanualer i luftfarten. Skillen bruker prinsippene, men følger ikke standarden slavisk.

| Fra STE | Tilpasset norsk |
|---|---|
| Maks 20 ord i instruksjoner og 25 ord i beskrivelser | Veiledende grense. Setninger over 25 ord deles. |
| Bruk aktiv form | Passiv er greit i beskrivelser når aktøren er ukjent eller uviktig. |
| Bare enkle verbtider | Perfektum er tillatt, fordi det er vanlig norsk. Kjeder av hjelpeverb unngås. |
| Maks tre ord i sammensatte substantiv | Lange sammensetninger løses opp med preposisjon. Etablerte fagord beholdes. |
| Ordliste med godkjente ord | Ingen ordliste. Skillen bruker ordene teamet bruker, også engelske. |

Disse retningslinjene finnes ikke i STE, og er lagt til for norsk:

- fast betydning for «skal», «må», «bør» og «kan»
- substantivet gjentas når «dette», «det» eller «den» kan peke på flere ting
- høflig spørreform når du ber et menneske om noe
- egne retningslinjer for spørsmål

## Innhold i repoet

| Fil | Innhold |
|---|---|
| `SKILL.md` | Selve skillen: prioritering, arbeidsflyt, retningslinjer, eksempler og sjekkliste |
| `README.md` | Denne filen |
| `LICENSE` | Lisensen |

## Bidra

Forslag og rettelser er velkomne. Opprett en issue eller en pull request.

Legg gjerne ved en tekst før og etter når du foreslår en ny retningslinje. Da er det lett å se hva retningslinjen gjør.

## Lisens

Skillen er lisensiert under [MIT-lisensen](LICENSE). Du kan fritt bruke, endre og dele den.
