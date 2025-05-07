# 🚀 Roteiro: Criar uma Máquina Virtual no Azure

Cassio Simões de Oliveira

Este guia fornece um passo a passo para criar uma máquina virtual (VM) na nuvem utilizando o Microsoft Azure.

## ✅ Pré-requisitos

- Conta ativa no [Azure Portal](https://portal.azure.com/)
- Assinatura com crédito ativo (Azure Free Tier ou assinatura paga)

---

## 1. Acessar o Portal do Azure

Acesse o [Azure Portal](https://portal.azure.com) e faça login com sua conta.

---

## 2. Iniciar a Criação da Máquina Virtual

1. No menu esquerdo ou na barra de busca, digite **"Máquinas Virtuais"**.
2. Clique em **“+ Criar”** > **“Máquina virtual do Azure”**.

---

## 3. Configurar as Informações Básicas

- **Assinatura:** selecione sua assinatura ativa.
- **Grupo de Recursos:** crie um novo ou selecione um existente.
- **Nome da VM:** defina um nome identificável.
- **Região:** escolha a localização do datacenter (ex: Brazil South).
- **Imagem (SO):** escolha o sistema operacional (ex: Ubuntu, Windows Server).
- **Tamanho:** selecione o tipo de VM (ex: B1s para uso leve).
- **Usuário e Autenticação:** defina nome de usuário e senha ou chave SSH.

---

## 4. Disco

- Escolha o tipo de disco:
  - SSD Premium
  - SSD Padrão
  - HDD
- Para equilíbrio entre desempenho e custo, recomenda-se **SSD padrão**.

---

## 5. Rede

- Azure cria uma **rede virtual** automaticamente, mas você pode personalizar.
- Habilite a porta adequada para acesso:
  - Porta **22** para **Linux (SSH)**
  - Porta **3389** para **Windows (RDP)**

---

## 6. Configurações Avançadas (Opcional)

- Ative **monitoramento** com Azure Monitor e Log Analytics.
- Configure scripts de inicialização se necessário.

---

## 7. Revisar e Criar

- Clique em **“Revisar + criar”**.
- Verifique todas as configurações.
- Clique em **“Criar”**.

---

## 8. Acessar a VM

Após a criação:

- Acesse a VM no portal.
- Copie o **IP público**.
- Conecte-se via:
  - **SSH (Linux):**
    ```bash
    ssh usuario@IP
    ```
  - **RDP (Windows):**
    Use o Cliente de Área de Trabalho Remota (mstsc)

---

## 9. Gerenciamento e Encerramento

- Para evitar cobranças indevidas:
  - **Pare** ou **exclua** a VM quando não estiver em uso.
  - Configure o **desligamento automático** nas configurações da VM.

---

## 📌 Observações

- Os recursos utilizados (CPU, disco, tráfego) impactam diretamente o custo.
- Consulte a [Calculadora de Preço do Azure](https://azure.microsoft.com/pt-br/pricing/calculator/) para estimativas.
