# Dossier de Pneumàtica (4t ESO)

Compilació: `main.tex` amb Tectonic / XeTeX (VSCodium) o qualsevol motor LaTeX.

## Estructura
- `main.tex` — portada, índex i ordre dels blocs. Interruptor del solucionari (`\solucionsfalse` / `\solucionstrue`).
- `preambul.tex` — paquets, colors, quadres (idea, exemple, guiada…), nivells d'exercici, macros de diagrames espai-fase.
- `pneumatica-tikz.sty` — **biblioteca reutilitzable** de símbols pneumàtics i elèctrics en TikZ (ISO 1219). Copia'l a qualsevol dossier i fes `\usepackage{pneumatica-tikz}`.
- `blocs/` — un fitxer per bloc (0 a 12) + `formulari.tex`.

## Compilar el solucionari
Canvia `\solucionsfalse` per `\solucionstrue` a `main.tex`, o compila amb `\def\solucionsactives{}` abans del `\documentclass`.

## Macros de la biblioteca (resum)
`\pnvalve{nom}{x}{y}{32nc|32no|22nc|42|52}{esq}{dre}` amb accionaments `man pol lever pedal roll spring pilot elec none`;
`\pncyl{nom}{x}{y}{s|d}`; `\pncompressor \pntank \pnfilter \pnregulator \pnlubricator \pnmaintenance \pnmanometer \pnpressureswitch`;
`\pncheck \pnflow \pnand \pnor \pnmotor \pnrotary \pnsource \pnexhaust`; elèctrics: `\pnrails \pnelcontact \pnelcoil`.
Les connexions es poden unir amb `\draw[pn] (nom-1)--(...)`.
