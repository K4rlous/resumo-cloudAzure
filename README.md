# ☁️ Introdução à Computação em Nuvem – AZ-900

**AZ-900** é uma certificação **de entrada** para quem está começando no mundo da computação em nuvem, especialmente com foco na **Microsoft Azure**. Ela é ideal para quem quer entender os **conceitos básicos de cloud**, mesmo sem experiência técnica prévia.

> ⚠️ A Azure possui serviços gratuitos e pagos. Ao usar laboratórios e testes, **lembre-se de excluir os recursos após o uso** para evitar cobranças inesperadas.

---

## 🌐 O que é Computação em Nuvem?

É o fornecimento de **serviços de computação pela internet** (“a nuvem”), como:

- Servidores
- Armazenamento
- Bancos de dados
- Redes
- Softwares
- Análises e inteligência

A nuvem permite **inovações mais rápidas**, **escalabilidade sob demanda** e **redução de custos**, pois **elimina a necessidade de datacenters físicos** (as famosas “salas frias”).

A base da computação em nuvem é a **virtualização**, que permite que um único servidor físico simule várias **máquinas virtuais (VMs)**, otimizando o uso de recursos e facilitando o gerenciamento.

---

## ☁️ Modelos de Nuvem

### 🏢 1. Nuvem Privada (Private Cloud)
Infraestrutura **exclusiva para uma organização**, localizada no próprio datacenter ou em um ambiente controlado por terceiros.

📌 **Vantagens**: mais controle, segurança, personalização e conformidade.

---

### ☁️ 2. Nuvem Pública (Public Cloud)
Serviços fornecidos por terceiros (como **AWS, Azure, Google Cloud**), acessados via internet e **compartilhados entre vários clientes**.

📌 **Vantagens**: baixo custo inicial, escalabilidade, sem necessidade de gerenciar infraestrutura.

---

### 🔁 3. Nuvem Híbrida (Hybrid Cloud)
Combina nuvem pública e privada. Permite mover dados e aplicações entre ambientes.

📌 **Vantagens**: equilíbrio entre segurança e escalabilidade.

---

### 🌐 4. Nuvem Comunitária (Community Cloud)
Infraestrutura compartilhada por **organizações com interesses comuns**, como hospitais ou órgãos públicos.

📌 **Vantagens**: custo dividido, colaboração segura, foco em necessidades específicas.

---

### ☁️🔀 Multicloud

**Multicloud** é o uso de **múltiplos provedores de nuvem pública** simultaneamente (ex: AWS + Azure + Google Cloud).

🔸 **Multicloud ≠ Nuvem Híbrida**

- **Multicloud**: várias nuvens públicas diferentes.
- **Híbrida**: mistura de nuvem pública com privada.

📌 **Benefícios**:
- Evita dependência de um único fornecedor (vendor lock-in).
- Aproveita o melhor de cada serviço.
- Maior disponibilidade e redundância.
- Otimização de custos.

📌 **Exemplo prático**:
- Hospedar site na AWS,
- Usar banco de dados no Azure,
- Armazenar backups no Google Cloud.

---

## 📊 Comparação entre os Modelos de Nuvem

| Modelo          | Características                                                                 |
|-----------------|----------------------------------------------------------------------------------|
| **Pública**     | Sem CAPEX, escalável, provisionamento rápido, pagamento pelo uso real           |
| **Privada**     | Total controle sobre segurança e recursos, manutenção por conta da organização   |
| **Híbrida**     | Flexibilidade, controle sobre segurança e conformidade, escolha de execução      |

---

## 💸 CAPEX vs OPEX

### 💰 CAPEX (Capital Expenditure)
Despesas de capital com **infraestrutura de longo prazo**, como compra de servidores e construção de datacenters.

- Alto custo inicial
- Registrado como ativo
- Valor se deprecia com o tempo

> Com a nuvem, o CAPEX é reduzido ou eliminado, pois os recursos são alugados.

---

### 🔄 OPEX (Operational Expenditure)
Despesas operacionais com **serviços e manutenção diária**, como assinaturas e pagamento por uso.

- Baixo custo inicial
- Flexível e escalável
- Aumenta conforme a necessidade operacional

---

## ⚙️ Modelo Baseado em Consumo

Na nuvem, os serviços funcionam sob o modelo de **pagamento por uso real**:

- Previsão de custos facilitada
- Cobrança apenas pelo que for usado
- Preços definidos por serviço/recurso

---

## 🔐 JumpServer

**JumpServer** é uma solução **open-source** de **bastion host** usada para gerenciar o **acesso remoto seguro a servidores** e dispositivos de rede.

- Atua como um intermediário entre usuários e servidores de destino
- Registra e audita conexões (SSH, RDP, etc.)
- Aumenta a segurança e evita acessos diretos não autorizados

---

## 🧪 Lab na Azure – Dica Importante

> ⚠️ **Evite usar recursos em "versão prévia"** nos laboratórios, pois podem ser instáveis e causar problemas em ambientes de produção!

---
