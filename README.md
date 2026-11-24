# Calculadora RCV

Eina web de suport a la decisió clínica per a la valoració del **risc cardiovascular** i la **selecció del tractament hipolipemiant** en prevenció cardiovascular. És un únic fitxer HTML (`index.html`) que funciona al navegador, sense instal·lació i sense connexió.

> **Avís important.** Aquesta eina és un ajut per al professional sanitari. No substitueix el criteri clínic ni les fonts originals, i no s'ha avaluat ni certificat com a producte sanitari. Els resultats s'han de contrastar amb les guies i la fitxa tècnica de cada fàrmac abans d'aplicar-los a un pacient concret.

## Què fa

L'aplicació s'organitza en cinc pestanyes:

| Pestanya | Contingut |
|---|---|
| **Risc** | Càlcul del risc a 10 anys (SCORE2 / SCORE2-OP), modificadors (lipoproteïna(a), calci coronari, país de residència i origen) i categoria final de risc. |
| **Teràpia** | Objectius de LDL-c, no-HDL i apoB segons la categoria; tractament actual; pautes per assolir l'objectiu i percentatge de reducció esperat. |
| **Fàrmacs** | Eficàcia i situació de cada fàrmac o combinació, amb la distinció entre indicació estudiada, autoritzada i finançada. |
| **Genètica** | Puntuació de l'hipercolesterolèmia familiar (DLCN) i de la quilomicronèmia familiar (score de Moulin 2018). |
| **Analítica** | Càlcul del LDL-c a partir del perfil lipídic estàndard (colesterol total, HDL i triglicèrids) amb fórmules publicades. |

## Fonts

L'eina combina i mostra per separat el que diuen diverses guies; quan es contradiuen, ho assenyala en lloc de resoldre-ho en silenci:

- Guia ESC 2021 de prevenció cardiovascular (SCORE2 i SCORE2-OP).
- Guia clínica XULA 2022 sobre el maneig de les dislipèmies (Catalunya).
- Guia ESC/EAS 2019 de dislipèmies i actualització focalitzada ESC/EAS 2025.
- Guia ESC 2023 de diabetis, prediabetis i malaltia cardiovascular.
- Guia ESC 2026 de malaltia cardiovascular i malaltia renal crònica.
- Estàndards SEA 2026 (Societat Espanyola d'Arteriosclerosi).
- Escala regional de l'OMS 2019 (Kaptoge, *Lancet Glob Health* 2019) i model SCORE2-LAC, com a informació complementària.
- Finançament: BIFIMED i CatSalut, amb acords CFT-SISCAT (consulta del 24/10/2026 per al finançament dels hipolipemiants).

## Limitacions que cal tenir presents

- **Finançament i autorització canvien.** Les dades de finançament són de la data de consulta indicada a l'aplicació: confirma-les abans de prescriure.
- **Percentil de calci coronari (MESA).** És sempre una *estimació* a partir de les taules publicades, no el valor del calculador oficial de MESA; no està validat a Espanya.
- **Origen del pacient.** El SCORE2 es calcula sempre amb el país de residència; l'origen només s'ofereix com a informació («si visqués a…»), no validada en migrants a Espanya.
- **Escales d'eficàcia.** Les guies (XULA, SEA, ESC) fan servir escales diferents d'eficàcia i d'evidència; l'aplicació les mostra sense unificar-les.
- **Països.** No tots els països tenen una família de model pròpia; en aquests casos s'usa el país de residència o Espanya, amb avís.

## Privacitat

- No envia cap dada: la pàgina declara una política de seguretat que bloqueja qualsevol connexió de sortida.
- No desa dades de pacients. Només es conserven al dispositiu els ajustos de l'aplicació (clau `rcv.ajustos` de `localStorage`).
- No hi ha seguiment, anàlisi d'ús ni recursos externs.

## Com utilitzar-la

1. Descarrega `index.html` d'aquest repositori (botó **Raw** → *Desa com…*).
2. Obre'l amb qualsevol navegador modern (mòbil o ordinador). Un cop obert, no cal connexió.

## Estat i llicència

- Versió publicada: 24/11/2026.
- **© 2026 Aleix Serralonga Fustier. Tots els drets reservats** (vegeu el fitxer [LICENSE](LICENSE)). Es pot utilitzar l'eina per a ús personal i professional no comercial. Copiar-la, modificar-la, redistribuir-la, vendre-la o fer-ne qualsevol ús comercial requereix autorització escrita de l'autor.
- Les guies i taules de tercers que l'eina recull pertanyen als seus titulars.
- Aquest repositori conté només la versió compilada (`index.html`); el codi font es manté en privat.
- Per a errors o suggeriments, obre una *issue* en aquest repositori.
