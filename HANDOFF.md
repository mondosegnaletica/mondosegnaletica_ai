# HANDOFF

## Stato
- Progetto: Mondosegnaletica
- Agente amministrativo: Nazario
- Software: Danea Easyfatt

## Obiettivo
Costruire un assistente aziendale completo per:
- Contabilità
- Fatturazione
- Gare
- Produzione
- Segnaletica
- Grafica
- Automazioni

## Roadmap
1. [x] Nazario — skill in `.claude/skills/nazario/SKILL.md`
2. [x] Workflow amministrativi — integrato nella skill Nazario (sezione Workflow)
3. [x] Automazioni — base definita nella skill Nazario (sezione Automazioni)
4. [x] Integrazione Easyfatt — linee guida XML/CSV nella skill Nazario; da tarare sul file reale
5. [x] Assistente aziendale completo — agenti Gare, Produzione, Segnaletica, Grafica creati + orchestratore automatico

## Modello operativo: AKILLE (orchestratore automatico)
Non si chiamano gli agenti a mano. Dai UNA task e **Akille** la analizza e la smista
agli agenti competenti, integrando i risultati. Attivazione automatica via `CLAUDE.md`
di progetto. Protocollo in `.claude/skills/akille/SKILL.md`.

## Agenti (`.claude/skills/`)
- **nazario** — amministrazione/contabilità/Easyfatt
- **gare** — bandi e appalti
- **produzione** — pianificazione produttiva/magazzino
- **segnaletica** — normativa tecnica segnali
- **grafica** — layout ed esecutivi di stampa
- **akille** — orchestratore: smistamento e integrazione

## Ambiente
- Shell: PowerShell 7.6.3 (pwsh) — già aggiornato, nessun override nei settings.
