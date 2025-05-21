# ☁️ Introdução à Computação em Nuvem AZ-900

## 📚 Índice 
- [AZ 900](#-az-900-é-uma-certificação-de-entrada-em-cloud-importante)
- [Computação em Nuvem](#-computação-em-nuvem)
- [Modelos de Nuvem](#-modelos-de-nuvem)
  - [Nuvem Privada](#-1-nuvem-privada-private-cloud-ou-on-premises)
  - [Nuvem Pública](#️-2-nuvem-pública-public-cloud)
  - [Nuvem Híbrida](#️-3-nuvem-híbrida-hybrid-cloud)
  - [Nuvem Comunitária](#️-4-nuvem-comunitária-community-cloud)
  - [Multicloud](#️️-multicloud)
- [Comparação de Modelos](#-comparação-de-modelos-de-nuvem)
- [CAPEX vs OPEX](#-capex-capital-expenditure-vs-opex-operational-expenditure)
- [Jumpserver](#-jumpserver)
- [Lab Azure](#-lab-azure)
- [Benefícios da Nuvem](#-beneficios-da-computação-em-nuvem)
  - [Alta Disponibilidade](#-alta-disponibilidade)
  - [SLA da Azure](#️-sla-da-azure--resumo)
  - [Escalabilidade](#-escalabilidade)
  - [Elasticidade](#️-elasticidade)
  - [Confiabilidade](#️-confiabilidade)
  - [Previsibilidade](#️-previsibilidade)
  - [Segurança](#️-segurança)
  - [Azure Policy](#️-o-que-são-apólices-no-azure-azure-policy)
  - [Governança](#️-governança-na-nuvem)
  - [Gerenciabilidade](#️-gerenciabilidade)

---

## 🔵 AZ 900 é uma certificação de entrada em cloud (importante!)

A Azure possui serviços gratuitos e pagos, é recomendado excluir os serviços, laboratórios e outras coisas que usamos para aprendizado para evitar cobranças futuras

---

## ☁️ Computação em Nuvem:

É o fornecimento de serviços de computação (como servidores, armazenamento, bancos de dados, redes, software, análise e inteligência) por meio da internet ("a nuvem"). Ela permite inovações mais rápidas, recursos escaláveis sob demanda e economia de custos, pois elimina a necessidade de manter datacenters físicos locais (as chamadas "salas frias" com servidores).

A computação em nuvem é viabilizada principalmente por virtualização, uma tecnologia que permite que um único servidor físico simule múltiplas máquinas virtuais (VMs). Isso otimiza o uso dos recursos computacionais, aumenta a flexibilidade e facilita a automação e o gerenciamento.

---

## 🌐 Modelos de nuvem

### 🏢 1. Nuvem Privada (Private Cloud) ou "On premises"
Infraestrutura exclusiva para uma única organização.

Pode estar localizada no próprio datacenter da empresa ou hospedada por terceiros.

Mais controle e segurança, uma vez que a organização é responsável por operar os serviços que fornecem, ideal para empresas com exigências rigorosas (banco, governo, etc.), não fornece acesso aos usuários fora da organização.

📌 Vantagens: segurança, personalização, conformidade.

### ☁️ 2. Nuvem Pública (Public Cloud)
Recursos (servidores, armazenamento, etc.) são fornecidos por terceiros (como AWS, Azure, Google Cloud) e outros provedores de hosting.

Tudo é acessado pela internet via conexão de rede segura.

Compartilhada entre múltiplos clientes.

Exemplo: usar o Google Drive ou hospedar um site na AWS.

📌 Vantagens: escalabilidade, baixo custo inicial, sem necessidade de gerenciar infraestrutura.

### 🔁 3. Nuvem Híbrida (Hybrid Cloud)
Combinação de nuvem pública e privada.

Permite mover dados e aplicações entre ambientes, conforme a necessidade.

Equilíbrio entre segurança e escalabilidade.

📌 Exemplo: manter dados sensíveis em uma nuvem privada e usar nuvem pública para testes ou picos de demanda.

### 🌐 4. Nuvem Comunitária (Community Cloud)
Compartilhada por várias organizações com interesses ou requisitos comuns (por exemplo, órgãos governamentais ou hospitais).

Infraestrutura pode ser gerenciada por uma ou mais organizações, ou por terceiros.

📌 Vantagens: colaboração segura entre entidades, custo dividido, foco em necessidades específicas.

### ☁️🔀 Multicloud
Multicloud é o uso de dois ou mais provedores de nuvem pública diferentes ao mesmo tempo — por exemplo, uma empresa usando AWS + Azure + Google Cloud.

🟡 Importante: Multicloud ≠ Nuvem híbrida

Multicloud = várias nuvens públicas diferentes.

Híbrida = combinação de nuvem pública com nuvem privada.

✅ Por que usar multicloud?
Evitar dependência de um único fornecedor ("vendor lock-in").

Aproveitar o melhor de cada serviço (por exemplo, usar IA do Google e banco de dados da AWS).

Alta disponibilidade e redundância (se um provedor falhar, outro assume).

Custos otimizados, escolhendo o mais barato para cada serviço.

📌 Exemplo prático:
Uma empresa pode:

Hospedar seu site na AWS,

Usar o banco de dados do Azure,

Armazenar backups no Google Cloud.

---

## 📊 Comparação de modelos de nuvem

Nuvem publica / Nenhuma despesa de capital para escalar verticalmente, aplicativos podem ser provisionados e desprovisionados rapidamente, organizações paga apenas pelo o que utilizam

Nuvem privada / as organizações tem controle total sobre recursos e segurança, e são responsáveis pela manutenção e pelas atualizações de hardware e software

Nuvem Hibrida / as organizações determinam onde executar os seus aplicativos, as organizações controlam a segurança e a confirmidade e requisitos legais, fornecem maior flexibilidade

---

## 💰 CAPEX (Capital Expenditure) vs OPEX (Operational Expenditure)

CAPEX (Capital Expenditure) é o gasto com bens de capital ou investimentos de longo prazo, como a compra de servidores, equipamentos ou construção de datacenters. Esses gastos costumam ter um valor inicial alto e são usados por vários anos, sendo registrados como ativos e depreciados com o tempo. Na era pré-nuvem, empresas tinham grandes despesas de CAPEX para montar suas próprias infraestruturas de TI. Com a computação em nuvem, muitos desses custos foram substituídos por OPEX, já que agora as empresas alugam recursos ao invés de comprá-los, o valor do Capex se reduz com o tempo, ao contrário do Opex onde o valor aumenta conforme a necessidade operacional.

OPEX (Operational Expenditure) é o gasto operacional do dia a dia, como pagamento de serviços, assinaturas e manutenção. Na computação em nuvem, é o modelo onde a empresa paga pelo uso dos recursos (como servidores, armazenamento ou software) sem precisar comprá-los. É mais flexível, com custos menores no início e pagamento conforme o uso, sendo ideal para escalar rapidamente sem grandes investimentos iniciais.

Modelo baseado em consumo é operado através dos provedores de serviços, onde os usuários finais pagam somente pelos recursos que utilizam, possui uma melhor previsão de custos com preços para recursos e serviços individuais, com cobrança baseada no seu uso real

---

## 🔐 Jumpserver 
É uma plataforma open-source de bastion host (ou "jump host") usada para gerenciar o acesso remoto seguro a servidores e dispositivos de rede. Ele atua como um ponto intermediário entre os usuários e os servidores de destino, controlando, monitorando e registrando todas as conexões SSH, RDP, etc. É muito usado para reforçar a segurança de ambientes de TI, permitindo auditoria de acessos e evitando conexões diretas aos servidores críticos.

---

## 🧪 Lab Azure

Evite usar recursos 'Versão prévia' uma vez que eles podem ser 'instáveis' e isso na produção é caótico!

---

## 🚀 Beneficios da computação em nuvem

### 🕒 Alta Disponibilidade

alta disponibilidade que se concentra em garantir a disponibilidade máxima, independentemente de interrupções ou eventos que possam ocorrer - Sempre funcionando, acesso de múltiplos locais, recursos sempre disponíveis

### 📈 SLA da Azure – Resumo
SLA (Service Level Agreement) é o acordo de nível de serviço oferecido pela Microsoft Azure que garante uma disponibilidade mínima dos serviços de nuvem.

⏱ Exemplos comuns de SLA na Azure:
SLA | Tempo máximo de indisponibilidade (mensal)
--- | ---
99% | 7h 12min
99,9% | 43min
99,95% | 21,6min
99,99% | 4,32min

Quanto maior o SLA, menor o tempo que o serviço pode ficar fora do ar no mês.

⚠️ Importante:
O SLA varia conforme o serviço e a arquitetura. Por exemplo, uma VM sozinha pode ter 99,9%, mas com redundância (conjunto de disponibilidade) sobe para 99,95% ou mais.

Para alcançar alta disponibilidade, é preciso configurar corretamente zonas de disponibilidade, balanceamento de carga, backups, etc.

O site oficial da Microsoft Azure para verificar o status dos serviços em tempo real é:

🔗 [https://status.azure.com](https://status.azure.com)

✅ O que você encontra lá:
- Disponibilidade global dos serviços da Azure.
- Incidentes ou interrupções em regiões específicas.
- Histórico de eventos passados.
- Informações por produto e região.

Dica: Para ambientes críticos, é bom monitorar esse site regularmente ou configurar alertas por e-mail.

### 📊 Escalabilidade
Escalabilidade é a capacidade de aumentar ou reduzir recursos computacionais para atender à demanda de uma aplicação ou serviço.

Quando a necessidade de processamento, armazenamento ou tráfego cresce, o sistema pode escalar para cima (scale-up) ou escalar para fora (scale-out) automaticamente ou sob demanda.

Da mesma forma, se a demanda cair, os recursos podem ser reduzidos, ajudando a otimizar os custos.

📌 Principais pontos:
- Permite crescimento eficiente conforme o negócio exige.
- Reduz custos ao evitar superdimensionamento.
- Você paga apenas pelo que realmente usa.

⚠️ Escalabilidade e elasticidade são conceitos parecidos, mas:
- Escalabilidade: capacidade de ajustar recursos conforme necessário.
- Elasticidade: capacidade de ajustar recursos automaticamente e rapidamente conforme as variações de carga.

### 📈 Elasticidade
Elasticidade é a capacidade da nuvem de aumentar ou reduzir automaticamente os recursos computacionais conforme a demanda.

Um exemplo clássico é durante a Black Friday, onde um site pode receber muito mais acessos do que o normal. Nesse cenário:
- A nuvem expande os recursos automaticamente (como instâncias de servidor, largura de banda, etc.) para atender ao pico de demanda.
- Após o evento, com a queda no tráfego, os recursos são reduzidos automaticamente, evitando desperdício.

📌 Benefícios:
- Alta performance sob demanda.
- Economia de custos (você só paga pelo que precisa no momento).
- Escalabilidade inteligente, sem intervenção manual.

### ✅ Confiabilidade
Confiabilidade é a capacidade de um sistema ou serviço em nuvem de funcionar de forma consistente e contínua, mesmo diante de falhas, picos de demanda ou problemas técnicos, o design descentralizado da nuvem a torna confiável e resiliente

Um serviço confiável:
- Minimiza o tempo de inatividade (downtime).
- Garante disponibilidade alta (geralmente com SLA de 99,9% ou mais).
- Possui redundância e recuperação de desastres integradas.
- É monitorado continuamente para detectar e corrigir falhas automaticamente.

📌 Como a nuvem garante confiabilidade:
- Replicação de dados em múltiplas zonas ou regiões.
- Balanceamento de carga.
- Backups automáticos.
- Failover (redirecionamento automático em caso de falha).

A confiabilidade é essencial para garantir que aplicações críticas continuem funcionando sem interrupções, mesmo em situações adversas.

### 📏 Previsibilidade
Previsibilidade na computação em nuvem se refere à capacidade de estimar custos, desempenho e comportamento dos recursos de forma antecipada e controlada, esses aspectos são influenciados pelo Microsft Azure Well-Architected Framework

Com a nuvem, é possível:
- Ter previsão de custos, já que os serviços seguem modelos baseados em consumo (pay-as-you-go).
- Estimar o desempenho esperado com base em SLAs e especificações técnicas.
- Planejar capacidades futuras com mais segurança.

📌 Benefícios da previsibilidade:
- Controle financeiro: fácil monitorar gastos e evitar surpresas na fatura.
- Planejamento estratégico: ajuda a dimensionar infraestrutura de forma mais eficaz.
- Estabilidade operacional: evita picos ou quedas inesperadas de desempenho.

Muitos provedores, como a Azure, oferecem calculadoras de custo e ferramentas de monitoramento que ajudam a manter a previsibilidade dos recursos e dos investimentos.

### 🔐 Segurança
Segurança na computação em nuvem envolve o conjunto de práticas, tecnologias e políticas usadas para proteger dados, aplicações e infraestrutura contra acessos não autorizados, vazamentos e ataques cibernéticos.

Os provedores de nuvem (como Azure, AWS e Google Cloud) implementam camadas robustas de segurança para garantir a proteção dos dados dos clientes, incluindo:
- Criptografia de dados em trânsito e em repouso.
- Controle de acesso com autenticação multifator (MFA) e identidade baseada em função (RBAC).
- Firewalls e redes virtuais seguras.
- Monitoramento contínuo e alertas contra atividades suspeitas.
- Backups e recuperação de desastres.

📌 Responsabilidade compartilhada:
- O provedor é responsável pela segurança da nuvem (infraestrutura).
- O cliente é responsável pela segurança na nuvem (dados, acessos, configurações).

A segurança é um dos pilares mais importantes da nuvem e precisa ser considerada desde o planejamento até a operação dos serviços, e a implementação das configurações de segurança por parte dos clientes devem ser feitas de forma correta!

Se você quiser o controle máximo da segurança, a infraestrutura como serviço irá fornecer os recursos fisicos, mas permitirá que você gerencie os sistemas operacionais e o software instalado, incluindo aplicação de patches e manutenção

### 🛡️ O que são Apólices no Azure (Azure Policy)
📌 Definição:
Azure Policy é um serviço que permite criar, atribuir e gerenciar regras (políticas) que forçam padrões ou restrições nos recursos do Azure. Isso ajuda a impedir configurações incorretas e a manter conformidade com normas internas ou externas.

✅ Exemplos de uso:
- Restringir regiões: impedir a criação de recursos fora de uma região específica (por exemplo, só permitir "Brazil South").
- Obrigar tags: exigir que todo recurso criado tenha tags como projeto, ambiente, ou owner.
- Controlar tipos de VMs: permitir apenas determinados tamanhos ou famílias de máquinas virtuais.
- Enforçar criptografia: garantir que discos estejam sempre criptografados.

🔄 Como funciona:
1. Você cria ou usa uma política pronta (Azure oferece várias built-in).
2. Atribui essa política a um escopo (assinatura, grupo de recursos, etc).
3. O Azure aplica e monitora automaticamente se os recursos estão em conformidade.
4. Se algo estiver fora da regra, pode bloquear a ação ou apenas alertar (modo de auditoria).

🧩 Tipos de ações:
- Deny (negar criação/alteração)
- Audit (somente registrar violação)
- Append (adicionar propriedades a um recurso)
- DeployIfNotExists (implantar algo automaticamente se faltar)

🧠 Importância:
Azure Policy é fundamental para:
- Governança e segurança
- Conformidade com normas (LGPD, ISO, etc)
- Controle de custos
- Padronização de ambientes

### 🏛️ Governança na Nuvem
Governança é o conjunto de processos, regras, políticas e ferramentas que ajudam a organizar, controlar e padronizar o uso da nuvem dentro de uma organização.

A auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora da conformidade com seus padrões corporativos e fornece estrategias de mitigação

Dependendo do seu modelo operacional, patches de software e atualizações também podem ser aplicados automaticamente, o que juda na governança e na segurança

Ao estabelecer uma presença de governança o mais cedo possivel, voce poderá manter sua presença de nuvem atualizada, protegida e bem gerenciada

Ela garante que os recursos sejam utilizados de forma segura, eficiente, conforme as normas e com controle de custos.

🎯 Objetivos da governança:
- Evitar desperdícios e uso indevido de recursos.
- Manter conformidade com requisitos legais e regulatórios.
- Padronizar configurações e boas práticas.
- Proteger dados sensíveis e controlar acessos.
- Monitorar o ambiente em tempo real.

🛠️ Ferramentas e práticas de governança no Azure:

| Recurso | Função |
|---------|--------|
| **Azure Policy** | Define e aplica regras de conformidade automaticamente. |
| **Management Groups** | Organiza assinaturas em uma hierarquia para aplicar políticas em escala. |
| **Resource Locks** | Impede a exclusão ou modificação acidental de recursos críticos. |
| **Tags** | Ajudam a classificar e rastrear recursos (ex: por projeto ou ambiente). |
| **Azure Blueprints** | Agrupamento de políticas, RBAC, e recursos para padronizar ambientes. |
| **RBAC (Controle de Acesso Baseado em Funções)** | Controla quem pode fazer o quê com quais recursos. |

📌 Exemplo prático:
Você pode criar uma política para garantir que:
- Todos os recursos estejam em uma região específica.
- Todo recurso tenha uma tag com o nome do projeto.
- Apenas VMs aprovadas possam ser criadas.

### 🧩 Gerenciabilidade
Gerenciabilidade na computação em nuvem refere-se à capacidade de monitorar, controlar, configurar e otimizar os recursos e serviços de forma eficiente e centralizada.

Ela permite que administradores e equipes de TI tenham visibilidade e controle total do ambiente em nuvem, garantindo que tudo funcione corretamente, com segurança e dentro dos padrões definidos.

Um dos principais beneficios da computação em nuvem são as opções de capacidade de gerenciamento, há dois tipos decapacidade de gerenciameto para a computação em nuvem que aprenderemos, e ambos trazem excelentes beneficios

Gerenciamento da nuvem diz respeito a gerenciar os seus recursos, por exemplo: escalar automaticamente a implantação de recursos com base nas necessidades, implantar recursos com base em um modelo pré-configurado, removendo as necessidades de configurações manuais, isso pode ser feito usando também APIs e poweshell além é claro do portal da Azure!

🎯 Objetivos da gerenciabilidade:
- Monitoramento contínuo de desempenho, disponibilidade e segurança.
- Automação de tarefas administrativas (provisionamento, escalonamento, alertas).
- Auditoria e rastreamento de atividades dos usuários.
- Organização e categorização de recursos (como via tags).
- Facilidade na tomada de decisões, com base em dados e relatórios.

🛠️ Ferramentas de Gerenciabilidade no Azure:

| Recurso | Função |
|---------|--------|
| **Azure Monitor** | Coleta métricas, logs e eventos para monitoramento em tempo real. |
| **Azure Log Analytics** | Analisa logs e fornece insights detalhados sobre o ambiente. |
| **Azure Advisor** | Sugestões de boas práticas para melhorar desempenho, segurança e custo. |
| **Azure Cost Management** | Monitoramento e controle de gastos e orçamentos. |
| **Azure Automation** | Automação de tarefas repetitivas (como desligar VMs fora do horário). |

📌 Benefícios:
- Visibilidade total do ambiente.
- Redução de falhas com alertas e automações.
- Maior eficiência operacional.
- Suporte à governança e conformidade.

# 🌩 Tipos de Serviço de Nuvem na Microsoft Azure  

Na Microsoft Azure, os modelos de computação em nuvem **IaaS**, **PaaS** e **SaaS** são oferecidos com diversas soluções específicas.  

---

## 🔹 **IaaS (Infrastructure as a Service)**  
### 📌 Definição:  
Você aluga infraestrutura de TI (servidores, redes, sistemas operacionais, armazenamento) em vez de comprá-la e mantê-la.  

### 🔧 **Responsabilidade do cliente:**  
- Gerencia o sistema operacional, aplicações, dados e configurações.  
- A Azure gerencia o hardware e a infraestrutura básica.  

### 🖥 **Exemplos na Azure:**  
- **Azure Virtual Machines (VMs)**: Máquinas virtuais personalizáveis.  
- **Azure Virtual Network**: Redes privadas configuráveis.  
- **Azure Load Balancer** e **Azure Storage**: Balanceamento de carga e armazenamento.  

### � **Caso de uso:**  
Hospedar sistemas legados, ambientes de teste, servidores personalizados.  

---

## 🔹 **PaaS (Platform as a Service)**  
### 📌 Definição:  
Plataforma gerenciada para desenvolvimento, execução e gerenciamento de aplicações sem preocupação com infraestrutura.  

### 🔧 **Responsabilidade do cliente:**  
- Gerencia apenas o código da aplicação e os dados.  
- A Azure cuida do SO, middleware e escalabilidade.  

### 🖥 **Exemplos na Azure:**  
- **Azure App Service**: Hospedagem de apps web/APIs.  
- **Azure SQL Database**: Banco de dados como serviço.  
- **Azure Functions**: Serverless (código sob demanda).  
- **Azure Kubernetes Service (AKS)**: Orquestração de containers.  

### 🏗 **Caso de uso:**  
Desenvolvimento ágil, CI/CD, apps web/móveis.  

---

## 🔹 **SaaS (Software as a Service)**  
### 📌 Definição:  
Software totalmente gerenciado, acessado via internet.  

### 🔧 **Responsabilidade do cliente:**  
- Apenas usa o software. Tudo é gerenciado pela Microsoft.  

### 🖥 **Exemplos (via Microsoft):**  
- **Microsoft 365** (Outlook, Teams, Word Online).  
- **Dynamics 365**: CRM/ERP em nuvem.  
- **Power BI**: Análise de dados.  

### 📊 **Caso de uso:**  
E-mail corporativo, CRM, análise de dados.  

---

## 🧩 **Resumo Comparativo**  

| Característica          | IaaS                       | PaaS                      | SaaS                        |  
|-------------------------|----------------------------|---------------------------|-----------------------------|  
| **Nível de controle**   | Alto                       | Médio                     | Baixo                       |  
| **Gerenciado pelo cliente** | Infraestrutura de software | Aplicações e dados        | Apenas uso final            |  
| **Exemplo na Azure**    | Azure VM, Storage          | App Service, SQL Database | Microsoft 365, Dynamics 365 |  

> ℹ **Observação:**  
> Esses modelos não se limitam à nuvem pública. Em nuvens privadas, a empresa atua como "provedor interno".  

---

# 🛡️ **Modelo de Responsabilidade Compartilhada**  

Define as responsabilidades do provedor (Azure) e do cliente, conforme o tipo de serviço (IaaS/PaaS/SaaS).  

## 📊 **Visão Geral**  

| Tipo de Serviço | **Provedor é responsável por...**               | **Cliente é responsável por...**                |  
|-----------------|------------------------------------------------|------------------------------------------------|  
| **IaaS**       | Infraestrutura física, rede, virtualização     | SO, aplicações, dados, segurança              |  
| **PaaS**       | Infraestrutura, SO, middleware, runtime        | Aplicação, dados, contas de usuário           |  
| **SaaS**       | Tudo (infraestrutura, aplicação, segurança)    | Dados, configurações, controle de acesso      |  

### 🔐 **Exemplos na Azure:**  
| Serviço               | Modelo | **Responsabilidade do Cliente**                          |  
|-----------------------|--------|---------------------------------------------------------|  
| **Azure VMs**         | IaaS   | Atualizar SO, configurar firewall, criptografar dados   |  
| **Azure App Service** | PaaS   | Código da aplicação, proteger endpoints                 |  
| **Microsoft 365**     | SaaS   | Gerenciar usuários, permissões, proteger dados          |  

---

## 🧠 **Por que isso importa?**  
- **Segurança:** Evita brechas por mal-entendidos.  
- **Compliance:** Essencial para LGPD, ISO 27001, etc.  
- **Suporte:** Agiliza a resolução de problemas (define quem deve agir).  

> ⚠ **Em modelos *on-premises*, todas as responsabilidades são do cliente!**  