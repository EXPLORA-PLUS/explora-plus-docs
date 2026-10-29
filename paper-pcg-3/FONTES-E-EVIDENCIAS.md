# Registro de fontes e evidências

Consulta: 29/10/2026. Método: leitura de fontes oficiais e inspeção estática do código local.
Nenhuma consulta autenticada a APIs de eventos, execução de rotas ou avaliação de usuários integra esta pesquisa.

## Base e critérios

A primeira entrega, em paper-pcg-2, está preservada no commit bb92d2a.
O parecer foi transcrito da informação fornecida pelo grupo na conversa: Roseli Fernandes Rocha (5017), conceito Deferido, 12/10/2026 às 16:03; entrega registrada em 26/09/2026 às 07:54.
Os critérios mantidos são proximidade geográfica, compatibilidade de horário e relevância turística.

## Fontes externas verificadas

1. Ticketmaster Discovery API v2
   https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/
   Evidência: filtros de localização, data e classificação; chave de API e limites de requisições.
   Limite: a documentação não comprova cobertura suficiente em Santos. Não houve execução autenticada.

2. Sympla - contrato OpenAPI
   https://developers.sympla.com.br/api-docs
   Evidência: GET /v1.6.0/events lista eventos do produtor autenticado. Autenticação s_token; EventResponseDTO inclui datas, endereço, categoria, URL e cancelamento. end_date não consta entre os campos obrigatórios.
   Limite: não permite presumir catálogo irrestrito de todos os eventos de Santos.

3. Turismo Santos - agenda
   https://www.turismosantos.com.br/pt-br/eventos
   Evidência: publicação local de atrações com datas e categorias e, em vários registros, endereços.
   Limite: não foi identificado contrato de API na página consultada; não se afirma inexistência de outros canais.

4. Turismo Santos - Chororô
   https://www.turismosantos.com.br/pt-br/eventos/choror%C3%B4-festival-de-choro-de-santos
   Evidência: período de 29/10 a 31/10; Clube do Choro, Rua Quinze de Novembro, 68; horário remete à programação.
   Limite: não se aferiram coordenadas, distância a trajeto ou horário de chegada. Exemplo de completude documental, não cenário experimental.

5. PostGIS - ST_DWithin
   https://postgis.net/docs/ST_DWithin.html
   Evidência: consulta de proximidade com distâncias em metros para geography.
   Limite: possibilidade técnica, sem consulta implementada ou executada nesta etapa.

6. Django 5.2 - Time zones
   https://docs.djangoproject.com/en/5.2/topics/i18n/timezones/
   Evidência: datas com fuso e armazenamento em UTC com suporte habilitado.
   Limite: suporte do framework não implementa a lógica de seleção temporal.

## Código inspecionado

Backend local: revisão 0957f154531fc67bf696f627539679fc2a73735c.
Remote configurado: https://github.com/Portugol-Devoteers/explora-plus-backend
A análise refere-se ao checkout local. Não se verificou implantação em produção.

- places/models.py: localização geography SRID 4326, categoria, event_start_at, event_end_at, price_cents, currency e source_url; datas opcionais; is_event verifica apenas presença do início.
- places/serializers.py: PlaceSerializer não expõe as datas de evento; ausência de preço é apresentada como grátis na implementação atual, por isso o texto propõe distinguir preço desconhecido numa evolução futura.
- tour_routes/services/planner.py: candidatos por Overpass e preferências; não se identificou seleção de eventos por chegada. Passeio livre usa distância geométrica e velocidade constante de 1,35 m/s.
- tour_routes/services/geometry.py: projeção de ponto sobre rota, distância e progresso.
- tour_routes/serializers.py: pedido de rota recebe origem e destino, sem horário de saída ou janela de visita.
- tour_routes/search_preferences.py e serializers.py: preferências de categorias e raios de 150, 250 e 400 metros.
- tour_routes/persistence.py: chave considera origem, destino e preferências; não inclui dimensão temporal de eventos.
- explora_plus/settings/base.py: TIME_ZONE America/Sao_Paulo e USE_TZ True.
- places/management/commands/seed_demo.py: registros demonstrativos com datas relativas; não utilizados como dados reais da pesquisa.

## Interpretação

A correspondência entre requisitos e recursos documentados sustenta viabilidade técnica documental condicionada.
Não foram comprovados desempenho, qualidade da recomendação, satisfação de usuários, impacto comercial ou operação em produção.
A comparação prática prevista na primeira entrega permanece pendente; essa limitação está na metodologia, nos resultados, na discussão e na conclusão.

## Conteúdo anterior

A base técnica e as referências teóricas de paper-pcg-2 foram preservadas como contexto histórico.
As novas conclusões se apoiam nas fontes verificadas acima e no código, não em supostos resultados experimentais derivados do material anterior.