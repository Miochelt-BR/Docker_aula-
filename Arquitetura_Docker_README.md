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
```

✅ O cliente envia esses comandos para o **Docker Host** (daemon), que realiza as operações solicitadas.

---

## 🔹 2. Docker Host

Responsável por executar os containers, inclui:

- **Docker Daemon:** Serviço que escuta comandos do Client e gerencia containers e imagens.
- **Images:** Modelos usados para criar containers (exemplo: imagem do Nginx).
- **Containers:** Instâncias isoladas e em execução das imagens.

💡 Quando você executa um `docker run`, o daemon:

- Verifica se a imagem está localmente.
- Se não estiver, baixa a imagem do Registry.
- Cria e executa o container com base na imagem.

---

## 🔹 3. Registry (Repositório de Imagens)

Local onde as imagens Docker ficam armazenadas.

🛠️ Exemplos de imagens:

- nginx
- centos
- redis

O mais popular é o **Docker Hub**, mas há registries privados como GitHub Container Registry e AWS ECR.

---

## 🎯 Fluxo Completo (Simplificado)

```text
[ Client ] ── docker pull/run ──► [ Docker Daemon (Host) ] ──► [ Registry ]
                                       │
                              [ Images + Containers ]
```

---

## ✅ Conclusão

| Componente   | Função                                     |
|--------------|--------------------------------------------|
| **Client**   | Onde o dev digita os comandos Docker       |
| **Docker Host** | Onde as imagens e containers são executados  |
| **Registry** | Onde as imagens ficam armazenadas          |

---


