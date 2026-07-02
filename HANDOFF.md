# HANDOFF — Stato del progetto Mondosegnaletica

> Documento **vivo**: rappresenta sempre lo stato aggiornato del progetto.
> Va aggiornato ad ogni modifica significativa (vedi regola in `CLAUDE.md`).

**Ultimo aggiornamento:** 2026-07-02

## Cos'è
Assistente aziendale completo per Mondosegnaletica (segnaletica stradale), costruito come
insieme di agenti Claude Code coordinati da un orchestratore (**Akille**).
Software gestionale di riferimento: **Danea Easyfatt**.

## Modello operativo: AKILLE (orchestratore automatico)
Non si chiamano gli agenti a mano. Dai UNA task ad Akille: lui la analizza, decide quali
agenti usare, li coordina (in parallelo o in sequenza) e integra i risultati in un unico
output. Attivazione automatica in questa cartella via `CLAUDE.md`.
Protocollo completo: `.claude/skills/akille/SKILL.md`.

## Agenti (`.claude/skills/`)
| Agente | Ruolo |
|---|---|
| **akille** | Orchestratore: riceve la task, smista agli agenti, integra l'output |
| **nazario** | Amministrazione/contabilità: IVA, fatture, DDT, preventivi, scadenze, report, Easyfatt |
| **gare** | Appalti: bandi, capitolati, offerte, requisiti, MEPA, CIG/CUP |
| **produzione** | Pianificazione produttiva: ordini di lavoro, materiali, magazzino, commesse |
| **segnaletica** | Tecnico-normativo: Codice della Strada, rifrangenza, dimensioni, conformità |
| **grafica** | Progettazione/prestampa: layout, file di stampa, pittogrammi, colori, esecutivi |

## Roadmap
1. [x] Nazario — agente amministrativo
2. [x] Workflow amministrativi — integrato in Nazario + `WORKFLOW.md`
3. [x] Automazioni — base in Nazario (scadenzario, riepilogo IVA, solleciti, report)
4. [x] Integrazione Easyfatt — linee guida XML/CSV; **da tarare sul file reale**
5. [x] Assistente completo — agenti Gare, Produzione, Segnaletica, Grafica + Akille

## Ambiente
- Repo GitHub: https://github.com/mondosegnaletica/mondosegnaletica_ai (branch `main`)
- Shell: PowerShell 7.6.3 (pwsh) — aggiornato, nessun override nei settings
- `.claude/settings.local.json` è escluso dal repo (permessi locali della macchina)

## Prossimi passi / da fare
- [ ] Collaudare Akille su una task reale (es. una gara o una fattura vera)
- [ ] Tarare l'integrazione Easyfatt su un export XML/CSV reale (colonne/tracciati effettivi)
- [ ] Definire eventuali automazioni ricorrenti (skill `schedule`) se richieste

## Registro modifiche
- **2026-07-02** — Progetto messo su GitHub (repo `mondosegnaletica_ai`, branch main).
- **2026-07-02** — Orchestratore rinominato in **Akille**.
- **2026-07-02** — Creati agenti Gare, Produzione, Segnaletica, Grafica + orchestratore;
  attivazione automatica via `CLAUDE.md`.
- **2026-07-02** — Creato agente **Nazario** (fasi 1-4 roadmap).
