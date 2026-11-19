# Consolidação do encerramento do Explora+

Atualização de 19/11/2026. O termo Word foi preenchido a partir do PCE anterior, do último PCG e do código atualizado da organização EXPLORA-PLUS. Inclui anexo relacionando compromissos, resultados e alcance da entrega.

## Decisões confirmadas

- Roseli Fernandes Rocha é a Product Owner desde **01/10/2026**, em substituição a Felipe Pacheco Fernandes.
- O aceite é **exclusivamente acadêmico**. O termo não transfere à professora a propriedade da aplicação nem obrigações de publicação, hospedagem ou manutenção.
- Reuniões e aprovações anteriores permanecem atribuídas aos participantes da época.
- A equipe segue o último PCG e os nomes dos contatos enviados: Felipe Barbosa dos Santos, Arthur Almeida Lima, João Gabriel Henriques Cardoso, Lucas Carmona Neto e Lucas Cerqueira Galvão.
- Lucas Cerqueira Galvão é o contato principal do grupo no termo.

## E-mails e suas fontes

| Integrante | E-mail no termo | Fonte |
| --- | --- | --- |
| Felipe Barbosa dos Santos | felipebsantos@unisantos.br | Primeira entrega PCG, página 1. |
| Arthur Almeida Lima | arthurlima@unisantos.br | Informado pela equipe nesta revisão. |
| João Gabriel Henriques Cardoso | joaogabriel@unisantos.br | Primeira entrega PCG, página 1. |
| Lucas Carmona Neto | lucas.carmona@unisantos.br | Primeira entrega PCG, página 1. |
| Lucas Cerqueira Galvão | lucas.g@unisantos.br | Primeira entrega PCG, página 1. |
| Roseli Fernandes Rocha | roselifrocha@unisantos.br | Modelo institucional do termo. |

A primeira entrega está em `paper-pcg/entrega1-pcg.pdf`, com cópia em `paper-pcg-2/entrega1-pcg.pdf`. Foram priorizados os e-mails institucionais ali publicados. O perfil da organização identifica João Gabriel Catalão com outro e-mail; esse endereço não foi atribuído a João Gabriel Henriques Cardoso. O e-mail de Arthur foi incluído após fornecimento direto pela equipe.

## Contatos enviados pela equipe

| Identificação recebida | Telefone | Uso |
| --- | --- | --- |
| Lucas Galvão | +55 (13) 98878-1000 | Contato principal no termo. |
| Felipe Barbosa dos Santos | +55 (13) 99631-0735 | Complementar. |
| João Gabriel Unisantos | +55 (13) 99726-1133 | Complementar, conforme identificação recebida. |
| Lucas Carmona | +55 (13) 99625-1308 | Complementar. |
| Arthur | +55 (13) 97403-5979 | Complementar. |
| João | +55 (13) 98881-5733 | Identificação incompleta; não vinculado automaticamente a um integrante. |

## Relação com as entregas anteriores

O PCE em `paper-pce/main.tex` registra o MVP de junho: autenticação, planejamento de rotas, mapa, categorias, preferências, detalhe enriquecido, visitados, exclusão de paradas, biblioteca, perfil básico e cache. A revisão de escopo adiou APIs comerciais de eventos, mobilidade e transporte público, outros modais, compra real de ingressos, edição de perfil e busca por voz. O termo não apresenta essas integrações adiadas como concluídas.

O PCG do 8º semestre distingue anúncios no aplicativo como funcionalidade do PCE, usando a expressão Google Ads, e pesquisa da integração de eventos geolocalizados como inovação do PCG. O código demonstra anúncios no estilo AdMob; não há integração operacional com o SDK real.

O último PCG, `paper-pcg-3`, apresenta pesquisa documental de 29/10/2026, sobre o backend `0957f15`, e conclui viabilidade técnica condicionada. Foram discutidos dados espaciais e temporais, fontes de eventos, proximidade, fuso horário, exposição dos dados e cache. Não foram executadas comparação de rotas, medições ou avaliação por usuários. Essa limitação foi preservada.

O código de novembro é uma evolução posterior: eventos curados ativos ou com início nas próximas três horas, proximidade ao trajeto, destaques patrocinados, apresentação de datas e patrocínio na interface e atualização de rotas em função de mudanças nos destaques. Isso atende parte das condições técnicas levantadas; não comprova retroativamente experimentação em outubro. A janela temporal atual não estima chegada a cada evento.

## Evidências técnicas e sincronização

- Backend: revisão `c0bd52b05dfaa9ac12374d71a2026f4578e2cda4`. Consultados `places/models.py`, `seed_highlights.py`, `tour_routes/services/curated_pois.py`, `planner.py`, `serializers.py` e `views.py`.
- Frontend: revisão `35b23a908377e6806b70bf1ed89012de188390ff`. Consultados `src/ads/config.ts`, `AdSlot.tsx`, `ExploreScreen.tsx`, `PlacesScreen.tsx` e `TourPoiDetailModal.tsx`. `ADS_MODE` está em `mock`; o caminho não simulado retorna `null`.
- Documentos: `paper-pce/main.tex`, `paper-pce-meetings/main.tex`, `paper-pcg-2/main.tex`, `paper-pcg-3/main.tex`, `paper-pcg-3/analise-viabilidade.tex`, `paper-pcg-3/FONTES-E-EVIDENCIAS.md` e a primeira entrega PCG em PDF.
- Pulls com `--ff-only`: backend de `0957f15` para `c0bd52b`; frontend de `73f40c0` para `35b23a9`; documentação e perfil já atualizados. Arquivos locais preservados e sem conflitos.
- Na sincronização anterior ao preenchimento, a documentação estava em `8d16ad1`, dois commits à frente do remoto `explora-plus/main` em `bef1664`. Os pulls usaram o remoto da organização EXPLORA-PLUS; os remotos antigos não foram alterados.

A revisão foi documental e estática. Não foram executadas migrações, testes da aplicação ou implantação. Não foram comprovados receita, veiculação real de anúncios, contratação de patrocinadores, importação automática de eventos ou benefícios medidos com usuários. Os cadastros de `seed_highlights` são de demonstração.

## Modelo e campos para os signatários

O original está preservado em `modelos/Termo Encerramento PCE original.docx`, SHA-256 `fea597dc33ff4fdce0b6c89fc4b58868a550b2347bca99c81542cc89d4a4a757`. A versão preenchida reutiliza o cabeçalho institucional e a estrutura do modelo, com ajustes de tabelas e paginação e inclusão do Anexo I. As partes do pacote Word fora do corpo foram preservadas byte a byte.

A equipe informou **26/11/2026** como data de encerramento e selecionou **Produtos e serviços considerados conformes**. Esses campos foram preenchidos. As assinaturas permanecem em branco para assinatura pelo gov.br, em campos com 6,5 cm de largura e altura mínima de 2,4 cm. Os campos de PO e docente foram mantidos conforme o modelo, ambos identificando Roseli em suas respectivas funções.

## Conferência final

A versão anterior foi renderizada em quatro páginas. A revisão atual preenche data, conformidade e e-mail de Arthur e amplia os campos de assinatura; a conferência da nova paginação é registrada ao final. Tabelas, quebras de página e cabeçalho conferidos. O modelo original e as partes do pacote Word fora do corpo foram verificados por hash.

Conferência da revisão para assinatura: mantidas quatro páginas, todas renderizadas e inspecionadas. Campos de assinatura com 6,5 cm de largura e 2,4 cm de altura mínima, sem divisão entre páginas. Data 26/11/2026, opção de conformidade e e-mail de Arthur conferidos.
