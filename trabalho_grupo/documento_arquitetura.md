**Universidade Federal de Goiás \- UFG**  
**Instituto de Informática \- INF**  
**Disciplina**: Arquitetura de Software   **Semestre:** 2025.1  
**Curso**: Engenharia de Software  
**Professor**: Gilmar Arantes  
**Alunos**: Arthur Felipe Nascimento, Janderson Oliveira, Luis Felipe Ferreira, Phablo Tavares, Thiago Vicente **Grupo:** 3

**Documento de Arquitetura dos requisitos definidos**

**Objetivos da Arquitetura**

\- Permitir visualização detalhada do consumo de energia por cômodo e dispositivo.  
\- Prover integração com assistentes inteligentes e APIs de controle de dispositivos.  
\- Gerar projeções de consumo e recomendações baseadas em dados reais.  
\- Notificar usuários sobre eventos relevantes, como picos de tarifa.  
\- Garantir modularidade, escalabilidade e facilidade de manutenção.

 **Componentes Arquiteturais**

1\. Interface do Usuário (Frontend)  
\- Responsável por: Exibir dados, gráficos de consumo, alertas, simulações e projeções.  
\- Tecnologias sugeridas: ReactJS, Vue ou Flutter Web.  
\- Funcionalidades:  
  \- Visualização por cômodo/dispositivo  
  \- Projeção de consumo  
  \- Recebimento de alertas

2\. Backend (API REST/GraphQL)  
\- Responsável por: Orquestrar dados, executar lógica de negócio, gerar recomendações.  
\- Tecnologias sugeridas: Node.js, Django, FastAPI ou Spring Boot.  
\- Funcionalidades:  
  \- Processamento de dados recebidos dos sensores  
  \- Geração de alertas e projeções  
  \- Recomendação de economia

3\. Banco de Dados

\- Responsável por: Armazenar medições, perfis de consumo, configurações de usuário.  
\- Tecnologias sugeridas: PostgreSQL, MongoDB ou TimescaleDB.  
\- Tabelas principais:  
  \- usuários, cômodos, dispositivos, consumo, alertas, projeções, recomendações.

4\. Módulo de Coleta de Dados  
\- Responsável por: Capturar dados dos dispositivos/sensores inteligentes de energia.  
\- Tecnologias sugeridas: MQTT, HTTP, integração com ESP32 ou Raspberry Pi.  
\- Funcionalidades:  
  \- Coleta contínua ou periódica dos dados  
  \- Envio para o backend via API

 5\. Módulo de Notificações  
\- Responsável por: Enviar notificações sobre alertas de tarifa ou consumo excessivo.  
\- Tecnologias: Firebase, OneSignal, Web Push  
\- Eventos monitorados:  
  \- Pico de consumo  
  \- Alta tarifa  
  \- Equipamento acima da média

6\. Módulo de Inteligência e Projeção  
\- Responsável por: Analisar o consumo e prever tendências futuras.  
\- Tecnologias sugeridas: Python (Pandas, Scikit-learn), TensorFlow Lite  
\- Entradas: Dados históricos de consumo  
\- Saídas: Projeções mensais, alertas preditivos

7\. Integração com Assistentes (Alexa, Google Home)  
\- Responsável por: Permitir comandos e monitoramento via voz.  
\- Tecnologias: Alexa Skills Kit, Google Smart Home Actions  
\- Exemplo de comando: "Alexa, qual foi o consumo da cozinha ontem?"

 **Comunicação entre Componentes**

\- Frontend ↔ Backend: HTTP/HTTPS via REST/GraphQL.  
\- Sensores ↔ Backend: MQTT ou HTTP POST com dados de energia.  
\- Backend ↔ DB: ORM ou drivers nativos.  
\- Backend ↔ Notificações: SDKs de push notification.  
\- Backend ↔ Assistentes: Webhooks e APIs específicas.

Qualidade Arquitetural

| Qualidade       | Estratégia |  
|------------------|------------|  
| Escalabilidade  | Separação de microserviços; filas de eventos para dados dos sensores. |  
| Segurança       | Autenticação JWT, criptografia HTTPS, controle de acesso baseado em perfil. |  
| Manutenibilidade | Componentização e documentação de APIs. |  
| Desempenho  | Armazenamento em cache de projeções e dados agregados. |

Visão

\- Implementação dos módulos de coleta, visualização e projeção de dados.  
\- Alertas simples e notificações por email/push.  
\- Interface básica com painel de consumo por cômodo.

\- Adição de recomendações inteligentes.  
\- Integração com assistentes de voz.  
\- Simulação de cenários e ações automatizadas.  
\- Sensores de alta precisão aplicados a equipamentos críticos.

Tecnologias Recomendadas 

| Camada           | Tecnologia |  
|------------------|------------|  
| Frontend         | ReactJS ou Vue |  
| Backend/API      | Node.js com Express ou Python com FastAPI |  
| Banco de Dados   | PostgreSQL ou MongoDB |  
| Dispositivos     | ESP32, Raspberry Pi, MQTT |  
| IA/Projeções     | Python \+ Scikit-learn |  
| Integrações Voz  | Alexa Skills, Google Home SDK |  
| Notificações     | Firebase Cloud Messaging |

