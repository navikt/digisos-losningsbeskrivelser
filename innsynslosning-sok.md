| Scenario | Status på søknad nav.no | Hva skal vises til søker | Fagsystemet (FS) avgir opplysninger til nav.no |
|-----------|-----------|-----------|-----------|
| Søknad videresendes til et annet Nav-kontor innenfor samme kommune | Mottatt / Under behandling | Informasjon om at søknad og vedlegg er videresendt (ikke antall vedlegg) og hvor. Vises under «Status i søknaden din» (historikken). | Det trigges hendelsene **Tildelt Nav-kontor** og **Mottatt**. Innsynsfil (`digisos-soker.json`) opprettes/oppdateres og sendes til KS Fiks. |
| Nav-kontoret registrerer saken inn | Mottatt → Under behandling | Søker kan se at søknaden eventuelt er delt i flere saker. Tittel på sak vises. | Sak registreres. Saksreferanse og sakstittel sendes til nav.no. Endringer i sakstittel sendes. |
| Nav-kontoret ber om mer dokumentasjon fra søker | Under behandling | Oppgaver om etterspurt dokumentasjon. Brevoversikt. Standardtekster. Søker kan ettersende dokumentasjon. | Brevreferanse, liste over manglende dokumentasjon, dokumenttyper, frister og oppdateringer i dokumentasjonslisten sendes. |
| Nav-kontoret sender varsel om forlenget saksbehandlingstid | Under behandling | Standardtekst vises. Brevet vises sammen med andre brev fra Nav. | Referanse til brevet (ID og hentelokasjon) sendes. |
| Søker har lastet opp etterspurt dokumentasjon | Under behandling | Opplastingsbekreftelse. Samlet oversikt over innsendt dokumentasjon. | Dokumenttype, tilleggsinformasjon, filnavn, hendelsetype og hendelsereferanse mottas i FS. |
| Søker velger selv å laste opp annen dokumentasjon | Under behandling | Mulighet til å ettersende dokumentasjon så lenge søknaden er tilgjengelig i innsyn. | Dokument sendes med type «Annet» og tilleggsinformasjon «Annet». |
| Søknad om andre sosiale tjenester enn økonomisk sosialhjelp | «Vi kan ikke vise status» (teknisk: FERDIGBEHANDLET) | Informasjon om at søknaden er mottatt, men ikke omfattes av innsyn. | Sakstittel og referanse sendes med saksstatus `IKKE_INNSYN`. |
| Nav-kontoret realitetsbehandler ikke saken | «Vi kan ikke vise status» (teknisk: BEHANDLES_IKKE) | Informasjon om at Nav ikke kan vise status i saken. | Saksstatus `BEHANDLES_IKKE`. Ingen flere oppdateringer sendes. |
| Søknaden splittes i flere saker/vedtak | Under behandling | Søker ser saker, vedtak og utfall. | Sakstitler, referanser, vedtak og utfall sendes som hendelser. |
| Sak feilregistreres av Nav-kontoret | Mottatt / Under behandling → Ingen visning | Saken skal ikke vises på nav.no. | Tittel og referanse sendes med saksstatus `FEILREGISTRERT`. |
| Vedtak fattet | Under behandling → Ferdig behandlet | Vedtak og vedtaksbrev vises på riktig sak. | Hendelsen «Vedtak fattet», vedtaksfil, saksreferanse og utfall sendes. |
| Søknad splittes i flere saker etter Ferdigbehandlet | Ferdig behandlet → Under behandling → Ferdig behandlet | Ny sak og tilknyttede hendelser vises. | Ny saksreferanse, sakstittel og tilhørende hendelser sendes. |
| Endringsvedtak | Ferdigbehandlet | Alle vedtak knyttet til samme sak vises. | Ny «Vedtak fattet»-hendelse knyttet til eksisterende saksreferanse sendes. |
| Nav-kontoret fatter et internt vedtak | Ikke vist | Skal ikke vises på nav.no. | Ingen innsynshendelse sendes. |
| Utbetalinger | Ferdigbehandlet | Kommende, utførte og stoppede utbetalinger vises. | Utbetalingshendelser med status PLANLAGT_UTBETALING, UTBETALT, STOPPET eller ANNULLERT sendes. |
| Vilkår (§§ 20 og 20a) | Ferdigbehandlet | Vilkår med tittel og beskrivelse vises. | Vilkår sendes med saksreferanse og status RELEVANT eller ANNULLERT. |
| Dokumentasjonskrav | Ferdigbehandlet | Dokumentasjonskrav med opplastingsmulighet vises. | Dokumentasjonskrav sendes med status RELEVANT, ANNULLERT eller LEVERT_TIDLIGERE. |
