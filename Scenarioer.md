# Scenarioer

| Scenario | Status på søknad | nav.no - hva skal vises til søker | Fagsystemet (FS) avgir opplysninger til nav.no |
|-----------|-----------|-----------|-----------|
| Søknad videresendes til et annet Nav-kontor innenfor samme kommune | Mottatt / Under behandling | Informasjon om at søknad og vedlegg er videresendt (ikke antall vedlegg) og hvor (under “Status i søknaden din” (historikken)) | Det skal trigges to hendelser: Tildelt Nav-kontor og Mottatt. Innsynsfilen (digisos-soker.json) skal opprettes/oppdateres og sendes til KS Fiks med informasjonselementer som beskriver de to hendelsene. |
| Nav-kontoret registrerer saken inn | Mottatt => Under behandling | Søker kan se at søknad eventuelt er delt i flere saker.<br>Tittel på sak vises for søker | Sak registreres inn. <br>Sak får evt. ny tittel.<br>Saksreferanse og -tittel sendes til nav.no. |
| Nav-kontoret ber om mer dokumentasjon fra søker (ubegrenset antall ganger) | Under behandling | informasjon om vedlegg søker kan sende basert på valgene i søknaden, byttes ut med det Nav-kontoret etterspør<br>Viser frem oppgaver om etterspurt dokumentasjon<br>Visning av standardtekster til søker med nødvendig info.<br>Søker ser alle brev som omhandler etterspurt dokumentasjon i en samlet oversikt.<br>Søker kan forstå hvilken søknad det er etterspurt dokumentasjon til.<br>Søker kan ettersende dok. via ettersendelsesfunksjonen så lenge søknaden er tilgjengelig i innsyn. | Referanse til brev, manglende dokumentasjon, dokumenttyper, tilleggsinformasjon, frister og oppdateringer sendes til nav.no. |

