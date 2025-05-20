# ☁️ Introdução à Computação em Nuvem – AZ-900

**AZ-900** é uma certificação **de entrada** para quem está começando no mundo da computação em nuvem, especialmente com foco na **Microsoft Azure**. Ela é ideal para quem quer entender os **conceitos básicos de cloud**, mesmo sem experiência técnica prévia.

> ⚠️ A Azure possui serviços gratuitos e pagos. Ao usar laboratórios e testes, **lembre-se de excluir os recursos após o uso** para evitar cobranças inesperadas.

---

## 📑 Índice

1. [O que é Computação em Nuvem?](#o-que-é-computação-em-nuvem)  
2. [Modelos de Nuvem](#modelos-de-nuvem)  
   2.1 [Nuvem Privada](#nuvem-privada)  
   2.2 [Nuvem Pública](#nuvem-pública)  
   2.3 [Nuvem Híbrida](#nuvem-híbrida)  
   2.4 [Nuvem Comunitária](#nuvem-comunitária)  
   2.5 [Multicloud](#multicloud)  
3. [Comparação entre os Modelos de Nuvem](#comparação-entre-os-modelos-de-nuvem)  
4. [CAPEX vs OPEX](#capex-vs-opex)  
5. [Modelo Baseado em Consumo](#modelo-baseado-em-consumo)  
6. [JumpServer](#jumpserver)  
7. [Lab na Azure – Dica Importante](#lab-na-azure–dica-importante)  
8. [Benefícios da Computação em Nuvem](#benefícios-da-computação-em-nuvem)  
   8.1 [Alta Disponibilidade](#alta-disponibilidade)  
   8.2 [Escalabilidade](#escalabilidade)  
   8.3 [Elasticidade](#elasticidade)  
   8.4 [Confiabilidade](#confiabilidade)  
   8.5 [Previsibilidade](#previsibilidade)  
   8.6 [Segurança](#segurança)  
9. [Azure Policy (Apólices)](#azure-policy-apólices)  
10. [Governança na Nuvem](#governança-na-nuvem)  
11. [Gerenciabilidade](#gerenciabilidade)  

---

## O que é Computação em Nuvem?

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

## Modelos de Nuvem

### Nuvem Privada (Private Cloud)

Infraestrutura **exclusiva para uma organização**, localizada no próprio datacenter ou em um ambiente controlado por terceiros.

📌 **Vantagens**: mais controle, segurança, personalização e conformidade.

---

### Nuvem Pública (Public Cloud)

Serviços fornecidos por terceiros (como **AWS, Azure, Google Cloud**), acessados via internet e **compartilhados entre vários clientes**.

📌 **Vantagens**: baixo custo inicial, escalabilidade, sem necessidade de gerenciar infraestrutura.

---

### Nuvem Híbrida (Hybrid Cloud)

Combina nuvem pública e privada. Permite mover dados e aplicações entre ambientes.

📌 **Vantagens**: equilíbrio entre segurança e escalabilidade.

---

### Nuvem Comunitária (Community Cloud)

Infraestrutura compartilhada por **organizações com interesses comuns**, como hospitais ou órgãos públicos.

📌 **Vantagens**: custo dividido, colaboração segura, foco em necessidades específicas.

---

### Multicloud

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

## Comparação entre os Modelos de Nuvem

| Modelo      | Características                                                                |
|-------------|--------------------------------------------------------------------------------|
| Pública     | Sem CAPEX, escalável, provisionamento rápido, pagamento pelo uso real          |
| Privada     | Total controle sobre segurança e recursos, manutenção por conta da organização |
| Híbrida     | Flexibilidade, controle sobre segurança e conformidade, escolha de execução    |

---

## CAPEX vs OPEX

### CAPEX (Capital Expenditure)

Despesas de capital com **infraestrutura de longo prazo**, como compra de servidores e construção de datacenters.

- Alto custo inicial  
- Registrado como ativo  
- Valor se deprecia com o tempo  

> Com a nuvem, o CAPEX é reduzido ou eliminado, pois os recursos são alugados.

---

### OPEX (Operational Expenditure)

Despesas operacionais com **serviços e manutenção diária**, como assinaturas e pagamento por uso.

- Baixo custo inicial  
- Flexível e escalável  
- Aumenta conforme a necessidade operacional  

---

## Modelo Baseado em Consumo

Na nuvem, os serviços funcionam sob o modelo de **pagamento por uso real**:

- Previsão de custos facilitada  
- Cobrança apenas pelo que for usado  
- Preços definidos por serviço/recurso  

---

## JumpServer

**JumpServer** é uma solução **open-source** de **bastion host** usada para gerenciar o **acesso remoto seguro a servidores** e dispositivos de rede.

- Atua como um intermediário entre usuários e servidores de destino  
- Registra e audita conexões (SSH, RDP, etc.)  
- Aumenta a segurança e evita acessos diretos não autorizados  

---

## Lab na Azure – Dica Importante

> ⚠️ **Evite usar recursos em "versão prévia"** nos laboratórios, pois podem ser instáveis e causar problemas em ambientes de produção!

---

## Benefícios da Computação em Nuvem

### Alta Disponibilidade

Alta disponibilidade se concentra em garantir que os serviços estejam sempre funcionando, mesmo diante de falhas ou interrupções. Recursos ficam acessíveis de múltiplos locais, e com redundância e boas práticas, é possível garantir que o sistema continue operando.

#### SLA da Azure – Resumo

| SLA     | Tempo máximo de indisponibilidade (mensal) |
|---------|---------------------------------------------|
| 99%     | 7h 12min                                    |
| 99,9%   | 43min                                       |
| 99,95%  | 21,6min                                     |
| 99,99%  | 4,32min                                     |

> Quanto maior o SLA, menor o tempo que o serviço pode ficar fora do ar no mês.

Para alcançar alta disponibilidade, é necessário usar:  
- Zonas de disponibilidade  
- Balanceamento de carga  
- Backups e replicação  

🔗 Status dos Serviços Azure  
Acompanhe o status em tempo real:  
👉 [https://status.azure.com](https://status.azure.com)

---

### Escalabilidade

Escalabilidade é a capacidade de **aumentar ou reduzir** recursos computacionais para atender à demanda.

📌 Características:  
- Escala horizontal (scale-out) ou vertical (scale-up)  
- Redução de custos por uso eficiente  
- Você paga apenas pelo que consome  

⚠️ Diferença:  
- **Escalabilidade**: Ajuste conforme necessário  
- **Elasticidade**: Ajuste automático conforme a carga  

---

### Elasticidade

Elasticidade é a **capacidade automática** da nuvem de expandir ou reduzir recursos conforme a carga.  
Exemplo: Em uma Black Friday, o sistema aumenta os recursos automaticamente e reduz após o evento.

📌 Benefícios:  
- Alta performance sob demanda  
- Economia de custos  
- Gerenciamento automático sem intervenção manual  

---

### Confiabilidade

Confiabilidade garante que os serviços continuem funcionando de forma consistente e resiliente, mesmo diante de falhas.

📌 Como a nuvem garante confiabilidade:  
- Replicação entre zonas/regiões  
- Balanceamento de carga  
- Backups automáticos  
- Monitoramento e failover  

---

### Previsibilidade

Previsibilidade permite estimar custos, desempenho e uso futuro com maior controle.

📌 Benefícios:  
- Controle financeiro com cobrança baseada em consumo  
- Planejamento estratégico da capacidade  
- Estabilidade operacional com uso de ferramentas como:  
  - Calculadoras de custo  
  - Azure Cost Management  
  - SLAs previsíveis  

---

### Segurança

Segurança na nuvem protege dados e aplicações contra acessos indevidos e ataques.

📌 Recursos:  
- Criptografia em trânsito e repouso  
- Autenticação multifator (MFA) e RBAC  
- Firewalls, redes privadas e monitoramento  
- Backups e recuperação de desastres  

### Modelo de responsabilidade compartilhada:  
- **Azure**: Segurança da nuvem (infraestrutura)  
- **Cliente**: Segurança na nuvem (dados e configurações)  

---

## Azure Policy (Apólices)

Azure Policy permite definir e aplicar regras que forçam padrões em seus recursos.

### Exemplos de uso:  
- Restringir regiões de criação  
- Exigir tags obrigatórias  
- Limitar tipos de máquinas virtuais  
- Garantir criptografia de discos  

### Como funciona:  
1. Criar ou escolher uma política pronta  
2. Atribuir a escopos (assinatura, grupo de recursos)  
3. Monitorar e aplicar automaticamente  

### Tipos de ação:  
- `Deny`: nega criação/modificação  
- `Audit`: apenas registra violação  
- `Append`: adiciona propriedades  
- `DeployIfNotExists`: implanta recurso se necessário  

---

## Governança na Nuvem

Governança é o conjunto de regras e ferramentas que garantem **uso seguro, controlado e eficiente da nuvem**.

### Objetivos:  
- Evitar desperdícios  
- Garantir conformidade (LGPD, ISO etc.)  
- Padronizar configurações e acessos  
- Proteger dados e monitorar uso  

### Ferramentas no Azure:

| Recurso              | Função                                                   |
|----------------------|----------------------------------------------------------|
| Azure Policy         | Regras automáticas de conformidade                       |
| Management Groups    | Organização hierárquica de assinaturas                   |
| Resource Locks       | Impede exclusão/modificação acidental de recursos        |
| Tags                 | Categorização e controle por metadados                   |
| Azure Blueprints     | Conjuntos de políticas, RBAC e templates padronizados    |
| RBAC                 | Controle de acesso baseado em funções                     |

---

## Gerenciabilidade

Gerenciabilidade é a capacidade de **monitorar, controlar e otimizar** recursos de nuvem de forma centralizada.

### Objetivos:  
- Monitoramento de desempenho e segurança  
- Automação de tarefas administrativas  
- Auditoria e rastreamento de usuários  
- Organização com tags e relatórios detalhados  

### Ferramentas de Gerenciabilidade:

| Recurso                 | Função                                                       |
|-------------------------|--------------------------------------------------------------|
| Azure Monitor           | Métricas e logs em tempo real                                 |
| Azure Log Analytics     | Análise e insights detalhados sobre logs                      |
| Azure Advisor           | Sugestões de melhorias em custo, segurança e performance     |
| Azure Cost Management   | Controle de orçamentos e monitoramento de gastos             |
| Azure Automation        | Execução automatizada de tarefas (como desligar VMs fora do expediente) |

### Benefícios:  
- Visibilidade total do ambiente  
- Redução de falhas  
- Eficiência operacional  
- Suporte à governança e conformidade  

---

