# Editionsagenten

Arbeitsrepository für Dokumentation, Auswertung und Präsentation des Vortrags
„Editionsagenten: Wie gestalten große Sprachmodelle digitale Editionen?“ bei
Editopia 2026.

Die gemeinsame Editionsgrundlage sowie die vollständigen Arbeitsstände der
einzelnen Coding-Agenten sind im
[Coding-Lab-Repository](https://github.com/Bpolitycki/agentic_ed_coding_lab)
dokumentiert.

## Aufbau

- `docs/runs/`: unveränderte Run-Artefakte und Screenshots
- `docs/analysis/`: Auswertungsinstrumente, deskriptive Befunde und Synthese
- `docs/expectations.md`, `docs/prompts.md`: Erwartungshorizont und Aufgabenfolge
- `slides/`: Quarto-/reveal.js-Foliensatz und dessen Assets

## Arbeitsprinzip

Beobachtung, Interpretation und Präsentationsform werden getrennt gehalten.
Die Auswertung fragt nicht nach dem „besten“ Interface, sondern nach den
epistemischen Ordnungen, die aus derselben Editionsdatenbasis entstehen.

## Präsentation bauen

```sh
quarto render slides/index.qmd
```