# Observabilidade com Grafana

## 📘 Sobre o projeto

Este repositório faz parte de uma jornada de aprendizado focada em **observabilidade, monitoramento e confiabilidade de sistemas**, utilizando uma stack baseada em **Docker, Prometheus, Grafana e Alert Manager**.

Ao longo deste treinamento, configuramos uma infraestrutura completa de observabilidade com foco na **experiência do usuário**, métricas e alertas, aplicando conceitos amplamente utilizados em ambientes modernos de produção.

---

## 🧭 Conteúdo abordado

Nesta jornada, abordaremos os seguintes tópicos:

- Aplicabilidade do
- Requisitos necessários  
- Os quatro sinais de ouro (*Golden Signals*)  
- Metodologias RED e USE  
- Cenário prático  
- Benefícios de realizar este treinamento  

---

## 🎯 Aplicabilidade

 Destinado a:

- Pessoas desenvolvedoras  
- Pessoas de operação de infraestrutura  
- Profissionais de DevOps  
- Pessoas de engenharia de confiabilidade de sites (SRE – *Site Reliability Engineering*)

---

## 📋 Requisitos

- A instrumentação de uma API Spring  
- Exposição de métricas padrão da JVM  
- Criação de métricas personalizadas  
- Uso do Spring Actuator e Micrometer  
- Integração dessas métricas com o Prometheus  
- Introdução à linguagem PromQL  
- Compreensão dos tipos de métricas e sua composição  

### Outros pré-requisitos
- Docker instalado  
- Docker Compose instalado  

---

## ⭐ Golden Signals (Sinais de Ouro)

Durante o treinamento, trabalharemos com os **quatro Golden Signals**, definidos pelo Google:

- **Latência**  
- **Tráfego**  
- **Saturação**  
- **Erros**

Esses sinais representam os quatro principais aspectos que devem ser observados em uma aplicação:

- **Latência**: tempo de resposta da aplicação  
- **Tráfego**: volume de requisições recebidas  
- **Saturação**: uso excessivo dos recursos disponíveis  
- **Erros**: falhas durante a execução da aplicação ou na infraestrutura  

Esses conceitos são amplamente referenciados no livro **Site Reliability Engineering (SRE)**, do Google, e são fundamentais para o planejamento de uma camada eficiente de observabilidade e monitoramento.

---

## 🔍 Metodologias USE e RED

Para facilitar o monitoramento desses sinais, utilizamos metodologias consolidadas:

### Método USE
- Foca em **Utilização**, **Saturação** e **Erros**
- Muito voltado para infraestrutura
- Analisa recursos como disco, IO, rede e comunicação entre componentes  

Este método não é o foco principal do treinamento, pois seu escopo é bastante amplo e demandaria um curso específico.

### Método RED
O método RED é o foco e aborda:

- **Rate** (taxa de requisições)  
- **Errors** (erros gerados)  
- **Duration** (duração das requisições)  

Esse método é fortemente ligado a aplicações HTTP e tem como principal objetivo **mensurar a experiência do usuário final**, analisando a satisfação de quem consome a API.

Alguns conceitos do método USE também são abordados como complemento ao RED.

---

## 🧪 Cenário 

O cenário do é composto por:

- Um cliente sintético (container com script que consome a API de forma não previsível)  
- Um proxy reverso  
- Uma API  
- Um cache  
- Um banco de dados  

Cada componente roda em seu próprio container, todos orquestrados via **Docker Compose**.

Além disso:
- O Prometheus já está configurado  
- As métricas já estão sendo coletadas  

### O que será implementado 
- Configuração do **Grafana**
- Criação de dashboards completos
- Subida e configuração do **Alert Manager**
- Integração do Alert Manager com o **Slack**
- Envio de alertas para um canal específico do Slack
- Comunicação entre Prometheus, Alert Manager, Grafana e Slack

Todo incidente crítico gerará alertas automáticos, que serão visualizados pelo time de suporte e pelas pessoas desenvolvedoras.

---

## 🚀 Benefícios do treinamento

Ao concluir este treinamento, você será capaz de:

- Reduzir o **MTTD (Mean Time To Detect)**  
- Reduzir o **MTTR (Mean Time To Repair)**  
- Detectar degradações antes que se tornem incidentes  
- Trabalhar com métricas de forma estratégica  

Também serão abordados conceitos importantes como:

- **SLA (Service Level Agreement)**  
- **SLO (Service Level Objective)**  
- **SLI (Service Level Indicators)**  
- **Error Budget** (Orçamento de Erro)  
- Baseline comportamental baseada em séries temporais  
- Ações reativas (alertas e automações)  
- Ações proativas (escalabilidade preditiva)  

🎯 **Objetivo final:**  
Mensurar e melhorar a **experiência do usuário**, caminhando em direção a sistemas mais confiáveis e resilientes.

---

## 🛠️ Tecnologias utilizadas

- Docker  
- Docker Compose  
- Prometheus  
- Grafana  
- Alert Manager  
- Slack  

---
