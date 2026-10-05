# Requisitos do Projeto

## Requisitos Funcionais

| ID | Requisito | Descrição |
|---|---|---|
| RF01 | Descoberta de serviços | O sistema deve consultar o Agregador de Métricas para identificar os serviços disponíveis. |
| RF02 | Monitoramento dinâmico | O sistema deve reconhecer a inclusão, remoção, indisponibilidade e retorno de serviços durante sua execução, atualizando as informações apresentadas ao usuário. |
| RF03 | Coleta de métricas por serviço | O sistema deve consultar periodicamente o endpoint `/metrics/{id_servico}` para cada serviço disponível. |
| RF04 | Tratamento da variação das métricas | O sistema deve considerar que os valores retornados pela API podem mudar a cada requisição. |
| RF05 | Detecção de indisponibilidade | O sistema deve calcular indicadores consolidados, como consumo total, emissão total, serviços ativos e serviços indisponíveis. O sistema deve identificar e sinalizar quando um serviço monitorado não responder à consulta ou estiver indisponível. |
| RF06 | Detecção de ausência de métricas | O sistema deve identificar quando um serviço estiver ativo, mas deixar de exportar métricas. Ou seja, está listado em `/services`, mas não está enviando métricas. |
| RF07 | Cálculo individual | O sistema deve calcular consumo energético e emissão de CO₂e para cada serviço monitorado. |
| RF09 | Dashboard operacional | O sistema deve apresentar, para cada serviço, seu estado de monitoramento, localização, métricas disponíveis, consumo energético estimado e emissão estimada de CO₂e. |
| RF10 | Histórico de coletas | O sistema deve armazenar o histórico das coletas realizadas para permitir análise temporal. |
| RF11 | Atualização contínua | O dashboard deve atualizar periodicamente suas informações, sem exigir que o usuário recarregue a página. |
| RF12 | Localização dos serviços | O sistema deve exibir país, região e, quando disponível, cidade onde o serviço está hospedado. |
| RF13 | Visualização geográfica | O sistema poderá apresentar em um mapa a posição aproximada dos serviços para os quais a API fornecer latitude e longitude. A ausência dessas coordenadas não deve impedir a visualização das demais informações do serviço. |
| RF14 | Ranking de impacto | O sistema deve permitir ordenar os serviços por consumo energético estimado ou por emissão estimada de CO₂e, indicando o período considerado na comparação. |
| RF15 | Comparação entre serviços | O sistema deve permitir comparar dois ou mais serviços por métricas e indicadores ambientais referentes ao mesmo período. |

## Requisitos Não Funcionais

| ID | Requisito | Descrição |
|---|---|---|
| RNF01 | Usabilidade e responsividade | A interface deve ser simples, clara e responsiva, adequada ao uso em navegadores e dispositivos móveis. |
| RNF02 | Atualização em tempo real | A coleta e a atualização da interface devem ocorrer em intervalos definidos pela aplicação. O projeto deve informar esses intervalos e a data e hora da última atualização exibida ao usuário. |
| RNF03 | Desempenho | O tempo de resposta da interface deve ser adequado para acompanhamento contínuo do ambiente monitorado. |
| RNF04 | Tolerância a falhas | A indisponibilidade de um serviço monitorado ou de uma das APIs auxiliares não deve interromper o funcionamento da aplicação, devendo ser apresentada ao usuário de forma adequada. |
| RNF05 | Documentação técnica | O projeto deve conter instruções de execução, descrição da arquitetura, modelo de dados, documentação dos endpoints desenvolvidos pela equipe e orientações para configurar o acesso às APIs auxiliares. |

## Restrições de Projeto

| ID | Restrição | Descrição |
|---|---|---|
| RP01 | Frontend Obrigatoriamente React com TypeScript |  |
| RP02 | Backend Obrigatoriamente Node.js com TypeScript | O backend deve expor endpoints HTTP para o frontend e organizar as funcionalidades em módulos, controllers e services. |
| RP03 | Banco de Dados Obrigatoriamente PostgreSQL | Deve haver uso explícito de DDL e DML. Não será permitido o uso de ORM (Object-Relational Mapping). |
| RP04 | Execução containerizada | A aplicação completa deve ser executada exclusivamente por meio de containers Docker. |
| RP05 | MVP | O escopo deve ser compatível com o tempo do semestre, priorizando um MVP funcional com navegação completa, respostas estruturadas e exibição de evidências documentais. |
| RP06 | Autenticação | A autenticação da área de configuração deve ser implementada no backend utilizando JWT. Não será aceito controle de acesso realizado apenas no frontend. |
| RP07 | Gestão ágil do projeto | A equipe deve manter um backlog priorizado, com histórias ou itens de trabalho e respectivos critérios de aceitação. Em cada sprint review, deve demonstrar as funcionalidades concluídas, registrar o retorno recebido e atualizar o planejamento das entregas seguintes. |
