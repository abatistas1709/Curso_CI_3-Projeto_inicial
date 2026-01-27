# CI/CD com Go, Docker e AWS

## 📌 Visão Geral

Este repositório contém um projeto demonstrativo desenvolvido como parte da **Formação Integração Contínua e Entrega Contínua** da Alura.
O objetivo é demonstrar, de forma prática, a implementação de um **pipeline completo de CI/CD**, desde o build e testes de uma aplicação até o deploy automatizado em diferentes ambientes na **AWS**.

O projeto aborda práticas modernas de **DevOps**, **containerização**, **automação** e **cloud computing**, utilizando uma aplicação simples escrita em **Go** como base para os exemplos.

---

## 🎯 Objetivos do Projeto

* Implementar pipelines de **Integração Contínua e Entrega Contínua**
* Automatizar build, testes, empacotamento e deploy
* Comparar diferentes modelos de deploy:

  * VM tradicional (EC2)
  * Containers gerenciados (ECS)
  * Orquestração Kubernetes (EKS)
* Consolidar conceitos de DevOps aplicados à nuvem AWS

---

## 🏗️ Visão Geral da Arquitetura

A solução é composta pelos seguintes elementos:

* Aplicação backend simples desenvolvida em **Go**
* Pipelines de CI/CD implementados com **GitHub Actions**
* **Docker** para criação de imagens da aplicação
* Infraestrutura na **AWS**, contemplando:

  * **EC2** para deploy em máquina virtual
  * **ECS** para execução de containers gerenciados
  * **EKS** para deploy em cluster Kubernetes
* Execução de **testes automatizados** e **teste de carga** durante o pipeline

O pipeline automatiza todo o fluxo desde o commit do código até o deploy nos ambientes configurados.

---

## 🔄 Pipeline de CI/CD

O pipeline é executado automaticamente a partir de eventos de push e pull request no repositório e contém as seguintes etapas:

### 1️⃣ Build

* Compilação da aplicação Go
* Validação de dependências

### 2️⃣ Testes Automatizados

* Execução de testes unitários
* Falha do pipeline em caso de erro

### 3️⃣ Build da Imagem Docker

* Criação da imagem Docker da aplicação
* Versionamento da imagem

### 4️⃣ Deploy Automatizado

* **EC2**: deploy direto em máquina virtual via pipeline
* **ECS**: atualização de serviço com nova imagem
* **EKS**: aplicação de manifests Kubernetes para atualização do deployment

### 5️⃣ Teste de Carga

* Execução de teste básico de carga para validação funcional após o deploy

---

## ☁️ Estratégias de Deploy

### 🔹 Deploy em EC2

* Modelo tradicional baseado em máquina virtual
* Utilizado para demonstrar deploy direto sem orquestração de containers
* Facilita a comparação com abordagens mais modernas

### 🔹 Deploy em ECS

* Deploy da aplicação como container
* Uso de orquestração gerenciada pela AWS
* Maior simplicidade operacional e escalabilidade em relação ao EC2

### 🔹 Deploy em EKS

* Deploy utilizando Kubernetes
* Uso de manifests para Deployment
* Abordagem cloud-native com maior controle e flexibilidade

---

## 🛠️ Tecnologias Utilizadas

* Linguagem: **Go**
* CI/CD: **GitHub Actions**
* Containers: **Docker**
* Cloud Provider: **AWS**
* Serviços AWS:

  * EC2
  * ECS
  * EKS
* Orquestração de Containers: **Kubernetes**
* Testes de Carga: **Locust**
* Controle de Versão: **Git / GitHub**

---

## 🔐 Segurança e Boas Práticas

* Uso de **GitHub Secrets** para gerenciamento de credenciais
* Nenhuma credencial sensível armazenada no repositório
* Pipeline com etapas bem definidas e falha automática em caso de erro
* Princípios básicos de **segurança em CI/CD** aplicados

---

## 📚 Principais Aprendizados

* Diferenças práticas entre deploy em EC2, ECS e EKS
* Benefícios da automação no ciclo de vida da aplicação
* Importância de testes automatizados em pipelines de CI/CD
* Desafios e vantagens da orquestração de containers
* Integração entre pipelines e serviços de cloud

---

## ⚠️ Aviso Importante

Este projeto foi desenvolvido **exclusivamente para fins educacionais e demonstrativos**, como parte de estudos em DevOps e Cloud Computing.
Não deve ser utilizado diretamente em ambientes produtivos sem as devidas adaptações e validações.

---

## 👤 Autor

Alexandre Batista da Silva

Profissional com experiência em infraestrutura, cloud computing e práticas DevOps, em constante evolução na área de automação, CI/CD e plataformas em nuvem.
