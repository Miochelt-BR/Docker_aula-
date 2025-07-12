
# Container vs Máquina Virtual (VM)

Este documento explica de forma simples e visual as principais diferenças entre **Containers** e **Máquinas Virtuais (VMs)**, além das vantagens de utilizar containers em ambientes modernos de desenvolvimento e produção.

---

## 🔍 Visão Geral

### 🧱 Máquina Virtual (Virtual Machine)

A estrutura de uma VM geralmente é composta por:

- **App** – Aplicação
- **Sistema Operacional (OS)** – Cada VM possui seu próprio sistema operacional completo.
- **Hypervisor** – Responsável por virtualizar o hardware.
- **Hardware** – Infraestrutura física do servidor.

📌 Cada VM carrega seu próprio sistema operacional, o que resulta em maior uso de recursos e tempo de inicialização.

---

### 📦 Container

A estrutura de containers é composta por:

- **Apps isoladas**, mas compartilhando o mesmo sistema operacional.
- **Container Engine** (ex: Docker) – Gerencia os containers.
- **Sistema Operacional (OS)** – Compartilhado entre os containers.
- **Hardware** – Infraestrutura física do servidor.

📌 Os containers são mais leves porque compartilham o mesmo kernel do sistema operacional e não carregam um sistema completo para cada aplicação.

---

## ✅ Vantagens dos Containers

- **🚀 Otimização de Recursos**  
  Containers utilizam menos recursos que VMs, pois compartilham o mesmo OS.

- **📦 Empacotamento**  
  Toda a aplicação, incluindo dependências e configurações, é empacotada em uma única imagem.

- **🔐 Imutabilidade**  
  Uma vez criada, a imagem do container não muda, garantindo consistência entre ambientes.

- **⚙️ Deploy Facilitado**  
  O processo de implantação é mais rápido e previsível com containers, ideal para integração contínua e DevOps.

---

## 🧠 Conclusão

Enquanto as **VMs** são úteis para isolar ambientes inteiros com seus próprios sistemas operacionais, os **containers** oferecem uma alternativa mais leve, eficiente e moderna para o desenvolvimento e a execução de aplicações, principalmente em ambientes em nuvem e microsserviços.



# Distribuição e Deploy com Docker

## 🚀 Visão Geral

Uma das grandes vantagens dos containers é que **podemos distribuir e deployar em qualquer lugar!**

Ao criar uma **imagem Docker** da sua aplicação, ela pode ser executada em diferentes ambientes que suportam **Container Engine** (como Docker ou outros orquestradores).

---

## 📦 Estrutura

- **Imagem Docker**
  - Contém o aplicativo empacotado com todas as suas dependências.

---

## 🌍 Destinos para Deploy

Você pode distribuir e executar a imagem Docker em diversos ambientes, como:

- **EC2 com Docker** (AWS)
- **ECS** (Elastic Container Service - AWS)
- **EKS** (Elastic Kubernetes Service - AWS)
- **On-premises** (servidores locais)
- **Azure ou GCP** (nuvem da Microsoft e Google)

---

## ✅ Benefícios

- Portabilidade: o mesmo container roda em qualquer ambiente com suporte a containers.
- Consistência: mesma imagem para todos os ambientes (desenvolvimento, testes e produção).
- Flexibilidade: escolha o ambiente que melhor atende ao seu projeto.

---


# Open Container Initiative (OCI)

A **Open Container Initiative (OCI)** é um projeto criado para padronizar os formatos de containers. Ela define **especificações abertas** e compatíveis para garantir portabilidade e interoperabilidade entre diferentes ferramentas do ecossistema de containers.

---

## 🔧 Especificações da OCI

A OCI é dividida em duas principais especificações:

### 1. Runtime Specification

Define como os containers devem ser **executados**.

Ferramentas que seguem essa especificação:
- Docker
- cri-o
- containerd

**documentação**
https://opencontainers.org/

# Como uma empresa usa Docker?

## 🧑‍💻 Ambiente de Desenvolvimento com Docker

No cenário de desenvolvimento, empresas utilizam o **Docker** para isolar e integrar diferentes serviços de forma prática e padronizada.

---

## 🔧 Ferramenta Utilizada

### `docker-compose`

Permite orquestrar múltiplos containers com apenas um comando:

```bash
$ docker-compose up



# Integração Contínua com Docker (CI)

## 🔁 O que é CI?

**Continuous Integration (CI)** é uma prática de desenvolvimento onde alterações no código são integradas com frequência e validadas automaticamente.

---

## 🔗 Fluxo da Integração Contínua com Docker

1. 🧑‍💻 **Dev** envia alterações para o **Git**
2. 🔁 O pipeline de **CI** é acionado
3. 🧪 **Testes automatizados** são executados
4. 📦 É feito o **build da imagem Docker**:
   ```bash
   docker build .


   # Deploy de Containers com Orquestradores

## 🔁 Visão Geral

Ao fazer o deploy de aplicações com Docker em produção, usamos orquestradores como:

- Kubernetes (K8s)
- Docker Swarm
- ECS (Elastic Container Service - AWS)

---

## 🚀 Fluxo do Deploy

1. **Build da Imagem**
   ```bash
   docker build -t minha-imagem .

# 🧱 Arquitetura do Docker (Resumo Visual e Conceitual)

Este documento explica de forma simples e visual a arquitetura do Docker, detalhando seus principais componentes e como eles interagem.

---

## 🔹 1. Client (Cliente Docker)

Interface usada para interagir com o Docker via terminal.

### Comandos comuns:

```bash
docker ps       # Lista containers em execução
docker pull     # Baixa uma imagem do Registry
docker run      # Cria e executa um container

