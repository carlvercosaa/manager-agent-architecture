## 🧠 Manager Agent Architecture
Este repositório contém a implementação de uma arquitetura Manager Agent, responsável por coordenar um sistema multi-agente baseado em especialização, controle centralizado e execução eficiente de tarefas. O fluxo de execução segue uma abordagem estruturada que simula a interação entre agentes como Manager, Researcher e Writer, otimizando o processamento de consultas complexas.

## 📌 Visão Geral
A arquitetura Manager Agent organiza agentes subordinados em torno de um agente gerente central (Manager), que atua como:

Orquestrador das tarefas;

Tomador de decisão sobre qual agente será acionado;

Consolidador dos resultados para entrega ao usuário final.

Cada agente subordinado possui especialização específica, permitindo que as tarefas sejam atribuídas à entidade mais adequada para a execução.

## 📷 Diagrama de Fluxo

## 🔁 Fluxo de Execução
O processo completo é dividido nas seguintes etapas:

1. Recebendo pergunta
O processo se inicia quando o usuário submete uma consulta.
O Manager analisa a consulta e define uma estratégia para tratá-la, decidindo se envolverá o Researcher, o Writer ou ambos.

2. Acionando o Researcher
Se a consulta requer pesquisa, coleta de dados ou checagem de fatos, o Manager delega a tarefa ao Researcher.
O Researcher pode usar Tool-Calling (APIs, mecanismos de busca, ferramentas externas) para coletar os dados necessários.

3. Retornando a resposta do Researcher
O Researcher envia os dados processados de volta ao Manager, podendo ser uma resposta bruta ou parcial.

4. Acionando o Writer
Com base na análise inicial ou na resposta do Researcher, o Manager pode acionar o Writer.
O Writer é responsável por refinar, reestruturar ou reescrever o conteúdo, garantindo clareza e coerência.

5. Atualizando e Monitorando
O Manager supervisiona o conteúdo gerado e assegura que ele esteja alinhado com a solicitação original.
Caso necessário, o Manager reativa o Researcher ou o Writer para ajustes adicionais.

6. Consolidação da resposta final
Uma vez que todas as etapas são concluídas, o Manager consolida o conteúdo final e o entrega ao usuário.

## 🚀 Como Executar
- Clone o repositório.
- Abra o notebook.
- Defina uma key para a llm.
- Execute célula por célula para acompanhar a execução do fluxo entre os agentes.


