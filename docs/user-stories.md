# Histórias de Usuário

As histórias abaixo foram derivadas dos requisitos funcionais do projeto. Os critérios de aceitação são verificáveis e podem ser usados para alimentar o backlog e as sprint reviews.

## US01 — Descobrir serviços disponíveis

**Como** usuário do sistema, **quero** visualizar os serviços disponíveis no Agregador de Métricas, **para** saber quais serviços estão sendo monitorados.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF01 — Descoberta de serviços |
| Prioridade | Alta |
| Story Points | 3 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O sistema consulta o endpoint de serviços.
- [ ] Os serviços retornados são exibidos no dashboard.
- [ ] Cada serviço apresenta seu identificador.
- [ ] Uma mensagem adequada é exibida quando a consulta falha.

## US02 — Atualizar a lista de serviços

**Como** usuário do sistema, **quero** que a lista de serviços seja atualizada automaticamente, **para** acompanhar inclusões, remoções e mudanças de disponibilidade.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF02 — Monitoramento dinâmico |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O sistema identifica novos serviços.
- [ ] O sistema identifica serviços removidos.
- [ ] O sistema identifica serviços indisponíveis e o retorno de serviços.
- [ ] A interface reflete as alterações sem recarregar a página.

## US03 — Coletar métricas por serviço

**Como** usuário do sistema, **quero** que as métricas sejam coletadas periodicamente, **para** acompanhar o estado atual de cada serviço.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF03 — Coleta de métricas por serviço |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O sistema consulta `/metrics/{id_servico}` para cada serviço disponível.
- [ ] A coleta ocorre em intervalos definidos pela aplicação.
- [ ] O horário da última coleta é registrado.
- [ ] Uma falha em um serviço não interrompe a coleta dos demais.

## US04 — Atualizar métricas variáveis

**Como** usuário do sistema, **quero** visualizar os valores mais recentes das métricas, **para** acompanhar sua variação ao longo do tempo.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF04 — Tratamento da variação das métricas |
| Prioridade | Alta |
| Story Points | 3 |
| Status | A fazer |

### Critérios de aceitação

- [ ] Cada nova resposta da API pode atualizar os valores exibidos.
- [ ] O sistema não assume que uma métrica permanece constante.
- [ ] A data e hora da atualização são exibidas ao usuário.

## US05 — Identificar serviços indisponíveis

**Como** usuário do sistema, **quero** ser avisado quando um serviço não responder, **para** diferenciar serviços ativos de serviços indisponíveis.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF05 — Detecção de indisponibilidade |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O sistema identifica timeout, erro de conexão ou resposta inválida.
- [ ] O serviço é marcado como indisponível.
- [ ] O dashboard apresenta a quantidade de serviços ativos e indisponíveis.
- [ ] O erro de um serviço não derruba a aplicação.

## US06 — Identificar ausência de métricas

**Como** usuário do sistema, **quero** saber quando um serviço ativo não envia métricas, **para** diferenciar ausência de dados de indisponibilidade do serviço.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF06 — Detecção de ausência de métricas |
| Prioridade | Alta |
| Story Points | 3 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O sistema compara os serviços listados em `/services` com os serviços que enviam métricas.
- [ ] O serviço ativo sem métricas recebe um estado específico.
- [ ] O dashboard informa que não há métricas disponíveis.

## US07 — Calcular impacto individual

**Como** usuário do sistema, **quero** visualizar o consumo e a emissão de cada serviço, **para** analisar seu impacto ambiental individual.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF07 — Cálculo individual |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O consumo energético estimado é calculado por serviço.
- [ ] A emissão estimada de CO₂e é calculada por serviço.
- [ ] As unidades de medida são exibidas.
- [ ] Os valores calculados correspondem ao período selecionado.

## US08 — Visualizar dashboard operacional

**Como** usuário do sistema, **quero** consultar um dashboard com as informações dos serviços, **para** acompanhar o ambiente monitorado em um único lugar.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF09 — Dashboard operacional |
| Prioridade | Alta |
| Story Points | 8 |
| Status | A fazer |

### Critérios de aceitação

- [ ] Cada serviço exibe seu estado de monitoramento.
- [ ] Cada serviço exibe suas métricas disponíveis.
- [ ] Cada serviço exibe consumo energético e emissão estimada.
- [ ] O dashboard apresenta indicadores consolidados.

## US09 — Consultar histórico de coletas

**Como** usuário do sistema, **quero** consultar o histórico das coletas, **para** analisar a evolução das métricas ao longo do tempo.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF10 — Histórico de coletas |
| Prioridade | Média |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] Cada coleta é armazenada com data e hora.
- [ ] O histórico pode ser consultado posteriormente.
- [ ] Os dados históricos podem ser filtrados por serviço e período.

## US10 — Atualizar o dashboard automaticamente

**Como** usuário do sistema, **quero** que o dashboard seja atualizado sem recarregar a página, **para** acompanhar os dados continuamente.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF11 — Atualização contínua; RNF02 — Atualização em tempo real |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] A aplicação atualiza os dados em intervalo definido.
- [ ] O intervalo de atualização é informado ao usuário.
- [ ] A data e hora da última atualização são exibidas.
- [ ] O usuário não precisa recarregar a página.

## US11 — Visualizar localização dos serviços

**Como** usuário do sistema, **quero** visualizar a localização dos serviços, **para** entender onde eles estão hospedados.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF12 — Localização dos serviços |
| Prioridade | Média |
| Story Points | 3 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O sistema exibe país e região quando disponíveis.
- [ ] O sistema exibe cidade quando disponível.
- [ ] A ausência de uma informação de localização não impede a exibição do serviço.

## US12 — Visualizar serviços em mapa

**Como** usuário do sistema, **quero** visualizar em um mapa os serviços que possuem coordenadas, **para** analisar sua distribuição geográfica.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF13 — Visualização geográfica |
| Prioridade | Baixa |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] Serviços com latitude e longitude são exibidos no mapa.
- [ ] A posição apresentada é identificada pelo serviço correspondente.
- [ ] Serviços sem coordenadas continuam visíveis nas demais áreas do sistema.

## US13 — Ordenar ranking de impacto

**Como** usuário do sistema, **quero** ordenar os serviços por consumo ou emissão, **para** identificar os serviços de maior impacto no período analisado.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF14 — Ranking de impacto |
| Prioridade | Média |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O ranking pode ser ordenado por consumo energético.
- [ ] O ranking pode ser ordenado por emissão de CO₂e.
- [ ] O período considerado é exibido.
- [ ] A ordenação é atualizada conforme os filtros selecionados.

## US14 — Comparar serviços

**Como** usuário do sistema, **quero** comparar dois ou mais serviços, **para** analisar suas métricas e indicadores ambientais no mesmo período.

| Campo | Informação |
|---|---|
| Requisito relacionado | RF15 — Comparação entre serviços |
| Prioridade | Média |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O usuário pode selecionar dois ou mais serviços.
- [ ] Os serviços são comparados no mesmo período.
- [ ] As métricas e indicadores ambientais são apresentados lado a lado.
- [ ] O período da comparação é exibido.

## US15 — Configurar o monitoramento com autenticação

**Como** administrador, **quero** acessar a área de configuração com autenticação segura, **para** controlar as configurações do monitoramento.

| Campo | Informação |
|---|---|
| Requisito relacionado | RP06 — Autenticação |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] O login é validado no backend.
- [ ] O backend utiliza JWT para autenticar as requisições protegidas.
- [ ] Usuários não autenticados não acessam a área de configuração.
- [ ] O frontend não é o único responsável pelo controle de acesso.

## US16 — Executar a aplicação em containers

**Como** integrante da equipe, **quero** executar a aplicação completa com Docker, **para** manter um ambiente padronizado de desenvolvimento e demonstração.

| Campo | Informação |
|---|---|
| Requisito relacionado | RP04 — Execução containerizada |
| Prioridade | Alta |
| Story Points | 5 |
| Status | A fazer |

### Critérios de aceitação

- [ ] Frontend, backend e banco de dados são iniciados por containers.
- [ ] As instruções de execução estão documentadas.
- [ ] A aplicação funciona sem depender de instalações locais adicionais não documentadas.

## US17 — Documentar a solução

**Como** integrante da equipe, **quero** manter a documentação técnica atualizada, **para** facilitar a execução, manutenção e avaliação do projeto.

| Campo | Informação |
|---|---|
| Requisito relacionado | RNF05 — Documentação técnica |
| Prioridade | Média |
| Story Points | 3 |
| Status | A fazer |

### Critérios de aceitação

- [ ] As instruções de execução estão documentadas.
- [ ] A arquitetura e o modelo de dados estão descritos.
- [ ] Os endpoints desenvolvidos pela equipe estão documentados.
- [ ] As configurações das APIs auxiliares estão documentadas.
