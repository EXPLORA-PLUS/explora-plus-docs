# Explora+ - Segunda entrega PCG do 8º semestre

Versão consolidada da primeira entrega, com análise documental de viabilidade da integração de eventos geolocalizados. Data da pesquisa: 29/10/2026.

## Documento

- main.pdf: documento completo para leitura.
- main.tex: fonte principal e capa.
- analise-viabilidade.tex: nova seção de método, resultados documentais e discussão.
- referencias.bib: base anterior e referências acrescentadas.
- figuras/: imagens utilizadas no documento.
- FONTES-E-EVIDENCIAS.md: registro de consulta e rastreabilidade da análise.

A versão de setembro permanece em paper-pcg-2. O commit bb92d2a preserva essa base antes das alterações da segunda entrega. Frontend, backend e banco não foram alterados.

## Alcance

O trabalho apresenta pesquisa documental e inspeção estática de código. Não houve execução de comparação entre rotas com e sem eventos, medição de desvio ou avaliação por usuários. A conclusão de viabilidade técnica é condicionada, e a diferença em relação à experimentação prevista na primeira entrega está explícita no documento.

## Compilação

Abrir main.tex no editor LaTeX do Codex e compilar. Para exportar pelo MiKTeX local, executar nesta pasta, verificando o sucesso de cada etapa:

~~~text
pdflatex -interaction=nonstopmode -halt-on-error main.tex
biber main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
~~~

Conferência visual: renderização do PDF e inspeção de capa, sumário, figuras, tabelas, conclusão e referências. Os arquivos auxiliares da compilação são ignorados pelo Git.