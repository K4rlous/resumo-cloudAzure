# ☁️ Introdução à Computação em Nuvem AZ-900 & Conceitos Básicos de IA do Azure AI-900


## 📚 Índice

-   [AZ 900](#-az-900-é-uma-certificação-de-entrada-em-cloud-importante)
-   [Computação em Nuvem](#-computação-em-nuvem)
-   [Modelos de Nuvem](#-modelos-de-nuvem)
    -   [Nuvem Privada](#-1-nuvem-privada-private-cloud-ou-on-premises)
    -   [Nuvem Pública](#️-2-nuvem-pública-public-cloud)
    -   [Nuvem Híbrida](#️-3-nuvem-híbrida-hybrid-cloud)
    -   [Nuvem Comunitária](#️-4-nuvem-comunitária-community-cloud)
    -   [Multicloud](#️️-multicloud)
-   [Comparação de Modelos](#-comparação-de-modelos-de-nuvem)
-   [CAPEX vs OPEX](#-capex-capital-expenditure-vs-opex-operational-expenditure)
-   [Jumpserver](#-jumpserver)
-   [Lab Azure](#-lab-azure)
-   [Benefícios da Nuvem](#-beneficios-da-computação-em-nuvem)
    -   [Alta Disponibilidade](#-alta-disponibilidade)
    -   [SLA da Azure](#️-sla-da-azure--resumo)
    -   [Escalabilidade](#-escalabilidade)
    -   [Elasticidade](#️-elasticidade)
    -   [Confiabilidade](#️-confiabilidade)
    -   [Previsibilidade](#️-previsibilidade)
    -   [Segurança](#️-segurança)
    -   [Azure Policy](#️-o-que-são-apólices-no-azure-azure-policy)
    -   [Governança](#️-governança-na-nuvem)
    -   [Gerenciabilidade](#️-gerenciabilidade)

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

-   Disponibilidade global dos serviços da Azure.
-   Incidentes ou interrupções em regiões específicas.
-   Histórico de eventos passados.
-   Informações por produto e região.

Dica: Para ambientes críticos, é bom monitorar esse site regularmente ou configurar alertas por e-mail.

### 📊 Escalabilidade

Escalabilidade é a capacidade de aumentar ou reduzir recursos computacionais para atender à demanda de uma aplicação ou serviço.

Quando a necessidade de processamento, armazenamento ou tráfego cresce, o sistema pode escalar para cima (scale-up) ou escalar para fora (scale-out) automaticamente ou sob demanda.

Da mesma forma, se a demanda cair, os recursos podem ser reduzidos, ajudando a otimizar os custos.

📌 Principais pontos:

-   Permite crescimento eficiente conforme o negócio exige.
-   Reduz custos ao evitar superdimensionamento.
-   Você paga apenas pelo que realmente usa.

⚠️ Escalabilidade e elasticidade são conceitos parecidos, mas:

-   Escalabilidade: capacidade de ajustar recursos conforme necessário.
-   Elasticidade: capacidade de ajustar recursos automaticamente e rapidamente conforme as variações de carga.

### 📈 Elasticidade

Elasticidade é a capacidade da nuvem de aumentar ou reduzir automaticamente os recursos computacionais conforme a demanda.

Um exemplo clássico é durante a Black Friday, onde um site pode receber muito mais acessos do que o normal. Nesse cenário:

-   A nuvem expande os recursos automaticamente (como instâncias de servidor, largura de banda, etc.) para atender ao pico de demanda.
-   Após o evento, com a queda no tráfego, os recursos são reduzidos automaticamente, evitando desperdício.

📌 Benefícios:

-   Alta performance sob demanda.
-   Economia de custos (você só paga pelo que precisa no momento).
-   Escalabilidade inteligente, sem intervenção manual.

### ✅ Confiabilidade

Confiabilidade é a capacidade de um sistema ou serviço em nuvem de funcionar de forma consistente e contínua, mesmo diante de falhas, picos de demanda ou problemas técnicos, o design descentralizado da nuvem a torna confiável e resiliente

Um serviço confiável:

-   Minimiza o tempo de inatividade (downtime).
-   Garante disponibilidade alta (geralmente com SLA de 99,9% ou mais).
-   Possui redundância e recuperação de desastres integradas.
-   É monitorado continuamente para detectar e corrigir falhas automaticamente.

📌 Como a nuvem garante confiabilidade:

-   Replicação de dados em múltiplas zonas ou regiões.
-   Balanceamento de carga.
-   Backups automáticos.
-   Failover (redirecionamento automático em caso de falha).

A confiabilidade é essencial para garantir que aplicações críticas continuem funcionando sem interrupções, mesmo em situações adversas.

### 📏 Previsibilidade

Previsibilidade na computação em nuvem se refere à capacidade de estimar custos, desempenho e comportamento dos recursos de forma antecipada e controlada, esses aspectos são influenciados pelo Microsft Azure Well-Architected Framework

Com a nuvem, é possível:

-   Ter previsão de custos, já que os serviços seguem modelos baseados em consumo (pay-as-you-go).
-   Estimar o desempenho esperado com base em SLAs e especificações técnicas.
-   Planejar capacidades futuras com mais segurança.

📌 Benefícios da previsibilidade:

-   Controle financeiro: fácil monitorar gastos e evitar surpresas na fatura.
-   Planejamento estratégico: ajuda a dimensionar infraestrutura de forma mais eficaz.
-   Estabilidade operacional: evita picos ou quedas inesperadas de desempenho.

Muitos provedores, como a Azure, oferecem calculadoras de custo e ferramentas de monitoramento que ajudam a manter a previsibilidade dos recursos e dos investimentos.

### 🔐 Segurança

Segurança na computação em nuvem envolve o conjunto de práticas, tecnologias e políticas usadas para proteger dados, aplicações e infraestrutura contra acessos não autorizados, vazamentos e ataques cibernéticos.

Os provedores de nuvem (como Azure, AWS e Google Cloud) implementam camadas robustas de segurança para garantir a proteção dos dados dos clientes, incluindo:

-   Criptografia de dados em trânsito e em repouso.
-   Controle de acesso com autenticação multifator (MFA) e identidade baseada em função (RBAC).
-   Firewalls e redes virtuais seguras.
-   Monitoramento contínuo e alertas contra atividades suspeitas.
-   Backups e recuperação de desastres.

📌 Responsabilidade compartilhada:

-   O provedor é responsável pela segurança da nuvem (infraestrutura).
-   O cliente é responsável pela segurança na nuvem (dados, acessos, configurações).

A segurança é um dos pilares mais importantes da nuvem e precisa ser considerada desde o planejamento até a operação dos serviços, e a implementação das configurações de segurança por parte dos clientes devem ser feitas de forma correta!

Se você quiser o controle máximo da segurança, a infraestrutura como serviço irá fornecer os recursos fisicos, mas permitirá que você gerencie os sistemas operacionais e o software instalado, incluindo aplicação de patches e manutenção

### 🛡️ O que são Apólices no Azure (Azure Policy)

📌 Definição:
Azure Policy é um serviço que permite criar, atribuir e gerenciar regras (políticas) que forçam padrões ou restrições nos recursos do Azure. Isso ajuda a impedir configurações incorretas e a manter conformidade com normas internas ou externas.

✅ Exemplos de uso:

-   Restringir regiões: impedir a criação de recursos fora de uma região específica (por exemplo, só permitir "Brazil South").
-   Obrigar tags: exigir que todo recurso criado tenha tags como projeto, ambiente, ou owner.
-   Controlar tipos de VMs: permitir apenas determinados tamanhos ou famílias de máquinas virtuais.
-   Enforçar criptografia: garantir que discos estejam sempre criptografados.

🔄 Como funciona:

1. Você cria ou usa uma política pronta (Azure oferece várias built-in).
2. Atribui essa política a um escopo (assinatura, grupo de recursos, etc).
3. O Azure aplica e monitora automaticamente se os recursos estão em conformidade.
4. Se algo estiver fora da regra, pode bloquear a ação ou apenas alertar (modo de auditoria).

🧩 Tipos de ações:

-   Deny (negar criação/alteração)
-   Audit (somente registrar violação)
-   Append (adicionar propriedades a um recurso)
-   DeployIfNotExists (implantar algo automaticamente se faltar)

🧠 Importância:
Azure Policy é fundamental para:

-   Governança e segurança
-   Conformidade com normas (LGPD, ISO, etc)
-   Controle de custos
-   Padronização de ambientes

### 🏛️ Governança na Nuvem

Governança é o conjunto de processos, regras, políticas e ferramentas que ajudam a organizar, controlar e padronizar o uso da nuvem dentro de uma organização.

A auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora da conformidade com seus padrões corporativos e fornece estrategias de mitigação

Dependendo do seu modelo operacional, patches de software e atualizações também podem ser aplicados automaticamente, o que juda na governança e na segurança

Ao estabelecer uma presença de governança o mais cedo possivel, voce poderá manter sua presença de nuvem atualizada, protegida e bem gerenciada

Ela garante que os recursos sejam utilizados de forma segura, eficiente, conforme as normas e com controle de custos.

🎯 Objetivos da governança:

-   Evitar desperdícios e uso indevido de recursos.
-   Manter conformidade com requisitos legais e regulatórios.
-   Padronizar configurações e boas práticas.
-   Proteger dados sensíveis e controlar acessos.
-   Monitorar o ambiente em tempo real.

🛠️ Ferramentas e práticas de governança no Azure:

| Recurso                                          | Função                                                                   |
| ------------------------------------------------ | ------------------------------------------------------------------------ |
| **Azure Policy**                                 | Define e aplica regras de conformidade automaticamente.                  |
| **Management Groups**                            | Organiza assinaturas em uma hierarquia para aplicar políticas em escala. |
| **Resource Locks**                               | Impede a exclusão ou modificação acidental de recursos críticos.         |
| **Tags**                                         | Ajudam a classificar e rastrear recursos (ex: por projeto ou ambiente).  |
| **Azure Blueprints**                             | Agrupamento de políticas, RBAC, e recursos para padronizar ambientes.    |
| **RBAC (Controle de Acesso Baseado em Funções)** | Controla quem pode fazer o quê com quais recursos.                       |

📌 Exemplo prático:
Você pode criar uma política para garantir que:

-   Todos os recursos estejam em uma região específica.
-   Todo recurso tenha uma tag com o nome do projeto.
-   Apenas VMs aprovadas possam ser criadas.

### 🧩 Gerenciabilidade

Gerenciabilidade na computação em nuvem refere-se à capacidade de monitorar, controlar, configurar e otimizar os recursos e serviços de forma eficiente e centralizada.

Ela permite que administradores e equipes de TI tenham visibilidade e controle total do ambiente em nuvem, garantindo que tudo funcione corretamente, com segurança e dentro dos padrões definidos.

Um dos principais beneficios da computação em nuvem são as opções de capacidade de gerenciamento, há dois tipos decapacidade de gerenciameto para a computação em nuvem que aprenderemos, e ambos trazem excelentes beneficios

Gerenciamento da nuvem diz respeito a gerenciar os seus recursos, por exemplo: escalar automaticamente a implantação de recursos com base nas necessidades, implantar recursos com base em um modelo pré-configurado, removendo as necessidades de configurações manuais, isso pode ser feito usando também APIs e poweshell além é claro do portal da Azure!

🎯 Objetivos da gerenciabilidade:

-   Monitoramento contínuo de desempenho, disponibilidade e segurança.
-   Automação de tarefas administrativas (provisionamento, escalonamento, alertas).
-   Auditoria e rastreamento de atividades dos usuários.
-   Organização e categorização de recursos (como via tags).
-   Facilidade na tomada de decisões, com base em dados e relatórios.

🛠️ Ferramentas de Gerenciabilidade no Azure:

| Recurso                   | Função                                                                  |
| ------------------------- | ----------------------------------------------------------------------- |
| **Azure Monitor**         | Coleta métricas, logs e eventos para monitoramento em tempo real.       |
| **Azure Log Analytics**   | Analisa logs e fornece insights detalhados sobre o ambiente.            |
| **Azure Advisor**         | Sugestões de boas práticas para melhorar desempenho, segurança e custo. |
| **Azure Cost Management** | Monitoramento e controle de gastos e orçamentos.                        |
| **Azure Automation**      | Automação de tarefas repetitivas (como desligar VMs fora do horário).   |

📌 Benefícios:

-   Visibilidade total do ambiente.
-   Redução de falhas com alertas e automações.
-   Maior eficiência operacional.
-   Suporte à governança e conformidade.

# 🌩 Tipos de Serviço de Nuvem na Microsoft Azure

Na Microsoft Azure, os modelos de computação em nuvem **IaaS**, **PaaS** e **SaaS** são oferecidos com diversas soluções específicas.

---

## 🔹 **IaaS (Infrastructure as a Service)**

### 📌 Definição:

Você aluga infraestrutura de TI (servidores, redes, sistemas operacionais, armazenamento) em vez de comprá-la e mantê-la.

### 🔧 **Responsabilidade do cliente:**

-   Gerencia o sistema operacional, aplicações, dados e configurações.
-   A Azure gerencia o hardware e a infraestrutura básica.

### 🖥 **Exemplos na Azure:**

-   **Azure Virtual Machines (VMs)**: Máquinas virtuais personalizáveis.
-   **Azure Virtual Network**: Redes privadas configuráveis.
-   **Azure Load Balancer** e **Azure Storage**: Balanceamento de carga e armazenamento.

### � **Caso de uso:**

Hospedar sistemas legados, ambientes de teste, servidores personalizados.

---

## 🔹 **PaaS (Platform as a Service)**

### 📌 Definição:

Plataforma gerenciada para desenvolvimento, execução e gerenciamento de aplicações sem preocupação com infraestrutura.

### 🔧 **Responsabilidade do cliente:**

-   Gerencia apenas o código da aplicação e os dados.
-   A Azure cuida do SO, middleware e escalabilidade.

### 🖥 **Exemplos na Azure:**

-   **Azure App Service**: Hospedagem de apps web/APIs.
-   **Azure SQL Database**: Banco de dados como serviço.
-   **Azure Functions**: Serverless (código sob demanda).
-   **Azure Kubernetes Service (AKS)**: Orquestração de containers.

### 🏗 **Caso de uso:**

Desenvolvimento ágil, CI/CD, apps web/móveis.

---

## 🔹 **SaaS (Software as a Service)**

### 📌 Definição:

Software totalmente gerenciado, acessado via internet.

### 🔧 **Responsabilidade do cliente:**

-   Apenas usa o software. Tudo é gerenciado pela Microsoft.

### 🖥 **Exemplos (via Microsoft):**

-   **Microsoft 365** (Outlook, Teams, Word Online).
-   **Dynamics 365**: CRM/ERP em nuvem.
-   **Power BI**: Análise de dados.

### 📊 **Caso de uso:**

E-mail corporativo, CRM, análise de dados.

---

## 🧩 **Resumo Comparativo**

| Característica              | IaaS                       | PaaS                      | SaaS                        |
| --------------------------- | -------------------------- | ------------------------- | --------------------------- |
| **Nível de controle**       | Alto                       | Médio                     | Baixo                       |
| **Gerenciado pelo cliente** | Infraestrutura de software | Aplicações e dados        | Apenas uso final            |
| **Exemplo na Azure**        | Azure VM, Storage          | App Service, SQL Database | Microsoft 365, Dynamics 365 |

> ℹ **Observação:**  
> Esses modelos não se limitam à nuvem pública. Em nuvens privadas, a empresa atua como "provedor interno".

---

# 🛡️ **Modelo de Responsabilidade Compartilhada**

Define as responsabilidades do provedor (Azure) e do cliente, conforme o tipo de serviço (IaaS/PaaS/SaaS).

## 📊 **Visão Geral**

| Tipo de Serviço | **Provedor é responsável por...**           | **Cliente é responsável por...**         |
| --------------- | ------------------------------------------- | ---------------------------------------- |
| **IaaS**        | Infraestrutura física, rede, virtualização  | SO, aplicações, dados, segurança         |
| **PaaS**        | Infraestrutura, SO, middleware, runtime     | Aplicação, dados, contas de usuário      |
| **SaaS**        | Tudo (infraestrutura, aplicação, segurança) | Dados, configurações, controle de acesso |

### 🔐 **Exemplos na Azure:**

| Serviço               | Modelo | **Responsabilidade do Cliente**                       |
| --------------------- | ------ | ----------------------------------------------------- |
| **Azure VMs**         | IaaS   | Atualizar SO, configurar firewall, criptografar dados |
| **Azure App Service** | PaaS   | Código da aplicação, proteger endpoints               |
| **Microsoft 365**     | SaaS   | Gerenciar usuários, permissões, proteger dados        |

---

## 🧠 **Por que isso importa?**

-   **Segurança:** Evita brechas por mal-entendidos.
-   **Compliance:** Essencial para LGPD, ISO 27001, etc.
-   **Suporte:** Agiliza a resolução de problemas (define quem deve agir).

> ⚠ **Em modelos _on-premises_, todas as responsabilidades são do cliente!**

# 🌍 Componentes de Arquitetura do Azure

## 📌 Regiões

### 🌍 O que são Regiões no Azure?
No Microsoft Azure, uma região representa uma área geográfica específica que contém um ou mais datacenters altamente conectados entre si e gerenciados como uma única entidade lógica. Essas regiões são fundamentais para garantir alta disponibilidade, redução de latência e residência dos dados, além de facilitar o atendimento a exigências legais e regulatórias em diferentes países.

### 📌 Características das Regiões do Azure
1. **Maior cobertura global**  
   A Azure possui mais de 60 regiões distribuídas globalmente, mais do que qualquer outro provedor de nuvem (como AWS ou Google Cloud).  

   Essas regiões atendem a mais de 140 países, possibilitando que empresas escolham onde hospedar seus dados e aplicações de acordo com sua localização ou requisitos legais.

2. **Datacenters interconectados**  
   Cada região pode ter múltiplos datacenters (trabalhamos com a ideia de 3), chamados de availability zones (zonas de disponibilidade), que são isolados fisicamente e oferecem alta tolerância a falhas.  

   Isso garante resiliência: se um datacenter falhar, os serviços podem continuar operando a partir de outro.

3. **Baixa latência e desempenho**  
   Hospedar serviços em uma região próxima aos seus usuários finais permite respostas mais rápidas e melhor desempenho, já que os dados não precisam percorrer grandes distâncias.

4. **Residência e conformidade dos dados**  
   As regiões permitem que você mantenha os dados dentro das fronteiras legais de um país ou continente, importante para leis como:  

   - LGPD (Brasil)  
   - GDPR (Europa)  

   Isso facilita o cumprimento de normas de conformidade e segurança, exigidas por setores como saúde, finanças e governo.

5. **Redundância e recuperação de desastres**  
   Você pode replicar dados entre regiões (geo-replicação), o que permite planos de recuperação de desastres (DR) robustos, mantendo os sistemas disponíveis mesmo em eventos extremos.

---

## 🔁 Pares de Regiões

### 🔁 O que são Pares de Regiões no Azure?
Um par de regiões no Azure é uma relação geográfica e lógica entre duas regiões dentro da mesma área geopolítica (no mínimmo 300 milhas de separação entre pares de regiões), como o mesmo país ou continente. Esses pares são definidos pela própria Microsoft e têm como objetivo oferecer resiliência e continuidade dos serviços em cenários de falhas ou desastres.  

**Por exemplo:**  
- Brazil South é emparelhada com South Central US  
- East US é emparelhada com West US  

### ✅ Vantagens dos Pares de Regiões
1. **Recuperação de Desastres (Disaster Recovery)**  
   Se uma região sofrer uma falha grave (como um desastre natural ou problema de energia em larga escala), a outra região do par está pronta para assumir o funcionamento dos serviços, pois ela está fisicamente separada, mas ainda próxima o suficiente para permitir replicação automática eficiente (para alguns serviços).

2. **Atualizações planejadas com segurança**  
   Durante as atualizações de software ou manutenção da infraestrutura, o Azure nunca atualiza ambas as regiões de um par ao mesmo tempo. Isso reduz o risco de falhas simultâneas e ajuda a manter seus serviços disponíveis, ou seja atualizações distribuidas sequencialmente para minimizar o tempo de inatividade.

3. **Prioridade na recuperação**  
   Se ocorrer uma falha em escala global (muito rara), o Azure dá prioridade à restauração de serviços nas regiões que fazem parte de um par oficial, garantindo que os dados críticos tenham maior chance de recuperação rápida.

4. **Sincronização de dados**  
   Alguns serviços do Azure, como o Azure Storage com geo-redundância (GRS), usam automaticamente os pares de regiões para replicar os dados entre datacenters, garantindo redundância geográfica transparente.

### 🌐 Exemplo Prático
Suponha que você está hospedando um sistema crítico na região **East US**:  
- O Azure irá usar a região **West US** (o par oficial) como backup.  
- Os dados podem ser replicados automaticamente para essa região.  
- Se a região **East US** cair, você pode ativar os serviços manualmente ou automaticamente em **West US**.  
- Durante atualizações, uma região é atualizada por vez para evitar interrupções simultâneas.  

### 📌 Considerações
- Nem todos os serviços estão disponíveis em todas as regiões.  
- Você pode consultar os pares oficiais de regiões nesta documentação da Microsoft:  
  👉 [https://learn.microsoft.com/azure/best-practices-availability-paired-regions](https://learn.microsoft.com/azure/best-practices-availability-paired-regions)

---

## 🛡️ Regiões Soberanas do Azure

### 🛡️ O que são Regiões Soberanas do Azure?
As regiões soberanas do Azure são instâncias separadas da nuvem Azure pública, projetadas para atender a requisitos específicos de conformidade, segurança e soberania de dados. Elas são isoladas da infraestrutura global padrão do Azure e possuem controles mais rigorosos, muitas vezes exigidos por leis nacionais ou por organizações governamentais.

### 🔐 Principais Características
- **Isolamento Total**  
  As regiões soberanas são fisicamente e logicamente separadas da nuvem pública do Azure.  
  Nenhuma comunicação direta entre a nuvem pública e as nuvens soberanas.  

- **Soberania dos Dados**  
  Os dados permanecem dentro da jurisdição legal exigida (como o território nacional).  
  Ideal para governos e órgãos que não podem permitir que seus dados saiam do país.  

- **Operadas por Parceiros Locais ou pelo Governo**  
  Algumas dessas regiões são geridas por entidades governamentais ou empresas locais, em parceria com a Microsoft.  

- **Conformidade Rigorosa**  
  Atendem a padrões de segurança como:  
  - FedRAMP (EUA)  
  - DoD IL (níveis de segurança do Departamento de Defesa dos EUA)  
  - ITAR (controle internacional de exportação de armamentos)  
  - CJIS (para justiça criminal)  

### 🌐 Exemplos de Regiões Soberanas do Azure
1. **Azure Government (EUA)**  
   - Projetado para agências do governo dos Estados Unidos.  
   - Isolado da nuvem pública.  
   - Atende a altos níveis de conformidade: FedRAMP High, DoD Impact Level 5.  
   - Localizado exclusivamente nos EUA e operado por funcionários com autorização do governo.  

2. **Azure China**  
   - Operado pela 21Vianet, uma empresa local chinesa.  
   - Totalmente separado da Azure global.  
   - Atende às exigências de soberania de dados impostas pelo governo da China.  

3. **Azure Germany (descontinuado como soberano exclusivo)**  
   - Era operado de forma independente por um parceiro alemão (T-Systems).  
   - Oferecia uma nuvem isolada para atender às rigorosas leis de proteção de dados da Alemanha.  
   - Foi integrado posteriormente à nova estrutura de Azure Regiões da União Europeia, mantendo foco em conformidade.  

### ✅ Por que usar uma Região Soberana?
Essas regiões são ideais quando você precisa de:  
- Conformidade legal e regulatória rígida  
- Soberania de dados  
- Segurança nacional  
- Ambientes altamente sensíveis (defesa, justiça, inteligência)  

Essas regiões são relacionadas com o **Azure Governamental**, uma instância separada do Azure, fisicamente isolada de implantações que não sejam do governo dos EUA, acessível apenas para pessoal verificado e autorizado.  

Há outra instância do Azure separada chamada **Azure China**, a Microsoft atua como o primeiro provedor estrangeiro de serviços de nuvem publica para a China, em conformidade com as regulamentações governamentais.

---

## 📦 Grupos de Recursos no Azure

### 📦 O que são Grupos de Recursos no Azure?
Um **Grupo de Recursos** é um container lógico que agrupa vários recursos do Azure (como VMs, bancos de dados, redes, contas de armazenamento etc.) que compartilham um mesmo ciclo de vida, como implantação, atualização e exclusão.

### 🎯 Objetivos dos Grupos de Recursos
- **Gerenciamento unificado**: Permite aplicar políticas, monitoramento, controle de acesso (RBAC), e tags a um conjunto inteiro de recursos de uma só vez.  
- **Organização lógica**: Facilita a organização por projeto, ambiente (produção, teste), cliente ou departamento.  
- **Automação e infraestrutura como código**: Pode ser usado em conjunto com templates ARM ou Bicep para implantar ambientes completos com um clique.  

### 🔗 1. Agrupamento Unificado 
Todos os recursos de uma solução (ex.: aplicação web, banco de dados, máquina virtual e armazenamento) são colocados em um único grupo de recursos.  

**Vantagens:**  
- Mais fácil de gerenciar e excluir em conjunto  
- Simples para ambientes pequenos ou aplicações autônomas  

### 🔄 2. Agrupamento Separado por Função
Recursos são distribuídos entre diferentes grupos de recursos, como:  
- Um grupo para web e banco de dados  
- Um grupo para máquina virtual  
- Um grupo para armazenamento  

**Vantagens:**  
- Mais controle e flexibilidade em ambientes complexos  
- Permite aplicar permissões específicas para diferentes times  
- Ideal quando os recursos têm ciclos de vida distintos  

### 🔐 Considerações sobre uso
- Todos os recursos em um grupo devem estar em uma única região (exceto os que são globais).  
- O recurso pode ser movido entre grupos (com algumas limitações).  
- Importante para RBAC (controle de acesso baseado em função): você pode definir quem pode acessar e o que pode fazer dentro de um grupo.  

**OS GRUPOS DE RECURSOS NÃO PODEM SER RENOMEADOS!**  
**TODOS OS RECURSOS DO AZURE TEM QUE ESTAR VINCULADOS A UM GRUPO DE RECURSOS**  

### ✅ Por que isso é obrigatório?
O Grupo de Recursos é a unidade básica de organização e gerenciamento no Azure. Ele fornece:  
- 🌐 Localização lógica para os recursos  
- 🔐 Controle de acesso (RBAC) por grupo  
- 📊 Monitoramento e métricas agregadas  
- ⚙️ Gerenciamento de ciclo de vida (você pode deletar todos os recursos de uma vez ao excluir o grupo)  
- 🧾 Aplicação de políticas e tags  

---

## 🔧 Recursos do Azure

### 🖥️ Máquinas Virtuais (Virtual Machines)
As VMs do Azure permitem criar e executar sistemas operacionais completos na nuvem. São ideais para:  
- Hospedar aplicações legadas  
- Ambientes de desenvolvimento/teste  
- Migração de servidores físicos (lift and shift)  
É possível escolher diferentes tamanhos, regiões e sistemas operacionais, além de configurar escalabilidade sob demanda.  

### 🗃️ Contas de Armazenamento (Storage Accounts)
Serviço usado para armazenar blobs (arquivos), filas, tabelas e discos. Suporta:  
- Armazenamento de backup e dados não estruturados  
- Alta durabilidade (99.999999999%)  
- Opções de replicação geográfica (GRS, LRS)  
É fundamental para aplicações que exigem persistência de dados na nuvem.  

### 🌐 Redes Virtuais (Virtual Networks)
São como “redes privadas” na nuvem. Permitem:  
- Conectar recursos do Azure de forma segura  
- Estabelecer VPNs com redes locais (on-premises)  
- Controlar tráfego com Network Security Groups (NSG)  
Elas formam a base da comunicação entre serviços, sendo essenciais para arquiteturas seguras e escaláveis.  

### 🌍 Serviços de Aplicativos (App Services)
Serviço PaaS (Platform as a Service) que facilita a hospedagem de aplicações web, APIs REST e backends móveis sem se preocupar com infraestrutura. Oferece:  
- Escalabilidade automática  
- Suporte a várias linguagens (.NET, Node.js, Java, Python)  
- Integração contínua com GitHub, Azure DevOps  

### 🛢️ Bancos de Dados SQL (Azure SQL Database)
Banco de dados relacional gerenciado baseado no SQL Server. Fornece:  
- Alta disponibilidade integrada  
- Backup automático  
- Escalabilidade e performance sob demanda  
Ideal para aplicações empresariais que necessitam de dados estruturados e transações ACID.  

### ⚡ Funções (Azure Functions)
Serviço serverless para executar pequenos trechos de código em resposta a eventos. Vantagens:  
- Você paga apenas pelo tempo de execução  
- Integração com eventos de armazenamento, filas, HTTP, etc.  
- Redução significativa da complexidade e custo para tarefas automatizadas  

---

## 📌 Assinaturas do Azure

- Uma conta pode ter diversas assinaturas (grupos de gerenciamento), mas uma assinatura pode haver apenas uma conta, uma estratégia de refinamento de custos no Azure é criar uma assinatura diferente para cada grupo de trabalho.  

- Uma assinatura do Azure fornece acesso autenticado e autorizado às contas do Azure (note que autenticação não é a mesma coisa que autorização).  

- O limite de cobrança permite que você gere relatórios de cobrança e faturas separadas para cada assinatura, o limite de controle de acesso permite gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas especificas  

### 🔹 Hierarquia de Gerenciamento no Azure
1. **Conta do Azure**: É a identidade principal (usuário ou empresa) usada para acessar e gerenciar os serviços do Azure. Está associada a um e-mail e a um método de pagamento.  

2. **Assinaturas**: São divisões dentro da conta do Azure que separam ambientes ou projetos. Exemplos:  
   - Assinatura de Desenvolvimento  
   - Assinatura de Teste  
   - Assinatura de Produção  
   Cada assinatura possui recursos próprios, políticas e controle de acesso isolado.  

3. **Conta de Cobrança**: Agrupa os custos de uma ou mais assinaturas para fins de faturamento.  

4. **Perfil de Cobrança**: Subdivisão da conta de cobrança que gera faturas específicas para diferentes áreas ou departamentos.  

5. **Seção de Fatura**: Subdivisão do perfil de cobrança que organiza o faturamento de assinaturas específicas dentro da mesma fatura.  

---

## 🏢 Grupos de Gerenciamento

### 🏢 1. Grupos de Gerenciamento
- Estão no topo da hierarquia.  
- Usados para aplicar políticas e controle de acesso de forma centralizada.  
- Podem agrupar várias assinaturas.  
- As assinaturas herdam as condições aplicadas ao grupo de gerenciamento.  
- Ideal para grandes organizações com múltiplas áreas, departamentos ou projetos.  

### 📄 2. Assinaturas (Subscriptions)
- Ficam dentro dos grupos de gerenciamento.  
- Controlam limites de uso, cobrança e acesso a recursos do Azure.  
- Cada assinatura pode ter vários grupos de recursos.  

### 🗂️ 3. Grupos de Recursos (Resource Groups)
- Contêm os recursos do Azure (como VMs, bancos de dados, etc.).  
- Servem para organizar recursos relacionados que compartilham o mesmo ciclo de vida.  
- Permitem gerenciamento conjunto (por exemplo, exclusão ou aplicação de tags).  

### ⚙️ 4. Recursos (Resources)
- São os componentes reais usados na nuvem, como:  
  - Máquinas virtuais (VMs)  
  - Bancos de dados SQL  
  - Armazenamento  
  - Serviços de rede  
- Esses recursos são criados dentro dos grupos de recursos.  

### 📌 Conclusão:
A hierarquia é:  
**Grupos de Gerenciamento → Assinaturas → Grupos de Recursos → Recursos**  

Essa estrutura permite controle eficiente, governança, segurança e organização escalável em ambientes corporativos no Azure.  

---

## 🛠️ Criação de Grupo de Recursos
*A pasta 'images' contém capturas de tela que visam auxiliar no processo de criação de recursos no Azure!*

**01** - O grupo de recursos pode ser encontrado na aba "Geral" no painel de serviços do Azure  

**02** - Escolhemos a assinatura que iremos utilizar (empresas costumam ter várias assinaturas), definimos o nome do grupo de recursos e sua região  

**03** - Se necessário definimos as marcações do grupo de recursos, isso auxiliará a compreender a fatura, uma vez que a formatação dela possa ser confusa na ausência de informações, as marcações também tem um propósito organizacional  

**04** - Por fim podemos validar e finalmente criar nosso grupo de recursos  

**05** - Nosso grupo de recursos será criado, e já poderemos criar outros recursos como VMs e etc em seu interior  

**06** - No interior do grupo de recursos temos acesso a várias abas com incontáveis funcionalidades, vamos resumir brevemente as operações que se encontram no painel esquerdo do portal  

### 📌 Visão geral:
Exibe informações gerais sobre o grupo de recursos, como localização, assinaturas associadas, e os recursos contidos nele.  

### 📜 Log de atividade:
Mostra um histórico das ações realizadas no grupo de recursos, útil para auditoria e rastreamento de mudanças.  

### 🔐 IAM (Controle de acesso):
Gerencia permissões de usuários e grupos no grupo de recursos. Aqui você define quem pode acessar e o que pode fazer (RBAC – Controle de Acesso Baseado em Funções), é ideal sempre dar o menor nível de acesso para os usuários.  

### 🏷️ Marcações:
Permite adicionar pares chave-valor aos recursos, facilitando a organização, categorização e a gestão de custos.  

### 🌐 Visualizador de recursos:
Apresenta uma visualização hierárquica dos recursos no grupo, mostrando dependências e relações entre eles.  

### ⚠️ Eventos:
Exibe eventos de diagnóstico e alertas configurados para os recursos do grupo, auxiliando no monitoramento e resposta a incidentes.  

---

### 🔧 ABA DE CONFIGURAÇÕES:

#### 🚀 Implantações:
Lista e detalha todas as implantações feitas no grupo de recursos, como templates ARM. Útil para rastrear o histórico e reverter configurações.  

#### 🔒 Segurança:
Exibe recomendações de segurança e o status atual baseado no Microsoft Defender for Cloud. Ajuda a identificar vulnerabilidades nos recursos.  

#### 🏗️ Pilhas de implantação:
Gerencia configurações de infraestrutura como código (IaC) com controle total de ciclo de vida dos recursos criados por uma pilha.  

#### 📜 Políticas:
Mostra as políticas do Azure atreladas ao grupo de recursos, como restrições de tipos de recursos ou exigência de marcações.  

#### 📋 Propriedades:
Exibe metadados do grupo, como ID, assinatura, região e data de criação.  

#### 🔒 Bloqueios:
Permite adicionar bloqueios de leitura ou exclusão para proteger os recursos contra modificações ou remoções acidentais.  

---

### 💰 ABA DE GERENCIAMENTO DE CUSTOS 

#### 📊 Análise de custo:
Permite visualizar detalhadamente os custos dos recursos utilizados no grupo. Você pode filtrar por período, serviço, região, etc., para entender onde estão sendo gerados os maiores gastos.  

#### 🔔 Alertas de custo (versão prévia):
Cria alertas automáticos com base em valores de gasto pré-definidos. Ajuda a detectar picos de custo antes que ultrapassem o orçamento.  

#### 💸 Orçamentos:
Define limites de gastos e períodos (mensal, trimestral, etc.). Quando o gasto se aproxima ou ultrapassa o valor definido, você recebe notificações.  

#### 💡 Recomendações do supervisor:
Exibe sugestões automatizadas de economia, como redução de tamanho de máquinas virtuais subutilizadas, desligamento de recursos ociosos, entre outras.  

---

### 📊 ABA DE MONITORAMENTO

#### 🔍 Insights (versão prévia):
Visualização centralizada e inteligente do desempenho e integridade dos recursos. Fornece recomendações e gráficos baseados em dados de monitoramento.  

#### ⚠️ Alertas:
Permite configurar alertas com base em métricas, logs ou eventos. Por exemplo, enviar um e-mail se o uso de CPU ultrapassar um limite.  

#### 📈 Métrica:
Visualiza dados de desempenho em tempo real, como uso de CPU, memória, disco e rede dos recursos. Essencial para análise técnica.  

#### ⚙️ Configurações de diagnóstico:
Define quais logs e métricas devem ser coletados e enviados para destinos como Log Analytics, Event Hub ou Armazenamento.  

#### 📜 Logs:
Acesso ao Azure Monitor Logs, onde você pode usar a linguagem Kusto Query Language (KQL) para consultar eventos e diagnósticos.  

#### 💡 Recomendações do supervisor:
Sugestões para melhorar desempenho, segurança e reduzir custos com base na análise dos recursos.  

#### 📊 Pastas de trabalho:
Dashboards interativos que permitem combinar métricas, logs e visualizações personalizadas para monitoramento avançado.  

---

### ⚙️ ABA DE AUTOMAÇÃO 

O botão **Exportar modelo** permite gerar um modelo ARM (Azure Resource Manager) em formato JSON com a definição de todos os recursos presentes no grupo de recursos atual.  

**Para que serve:**  
- Infraestrutura como código (IaC): você pode reutilizar esse modelo para criar grupos de recursos idênticos em outros ambientes.  
- Automatização de deploys: integra com pipelines DevOps ou scripts.  
- Backup de configuração: serve como registro da estrutura dos recursos e suas configurações.  

--- 

## 🌐 Criação de Redes Virtuais (VNets)  

Uma vez que VMs precisam receber um IP, criaremos uma rede virtual para abranger os recursos que criaremos futuramente!  

**01** - As redes virtuais podem ser encontradas na aba 'Base da Rede' no portal da Azure  

**02** - Escolhemos a assinatura e o grupo de recursos (vamos utilizar o que criamos previamente), definimos o nome da rede virtual e sua região  

**03** - Vamos resumir o processo, mas caso seja necessário há como configurar detalhes de segurança, endereçamento IP e rótulos (que vimos nos grupos de recursos)  

**04** - Vamos revisar e criar a VNet  

**05** - Após a implementação, a VNet já estará presente em nosso grupo de recursos!  

---

# 🖥️ Computação e Rede no Azure  

A computação do Azure é um serviço sob demanda que fornece recursos de computação como discos, processadores, memória, rede e sistemas operacionais.  

Entre os principais serviços estão:  

## 🖥️ Máquinas Virtuais (Virtual Machines)  
- Permitem a criação de instâncias de computação configuráveis, facilitando a execução de aplicativos e cargas de trabalho específicas.  
- É possível fazer o balanceamento de carga para dimensionar os recursos das máquinas virtuais através de **conjuntos de dimensionamento**.  

### 🔄 Conjuntos de Dimensionamento de Máquinas Virtuais (VM Scale Sets)  
- Permitem criar e gerenciar um grupo de VMs com balanceamento de carga.  
- Ajustam automaticamente o número de instâncias conforme a demanda.  
- Oferecem **alta disponibilidade** e **resiliência** ao distribuir VMs entre **zonas de disponibilidade** ou **domínios de falha**.  

### 🛡️ Conjuntos de Disponibilidade (Availability Sets)  
- Garantem que as VMs sejam distribuídas entre múltiplos **domínios de falha** dentro de um datacenter.  
- Reduzem o impacto de falhas de hardware.  
- Melhoram a **confiabilidade do sistema**.  

### ⚠️ Domínios de Falha (Fault Domains)  
- Grupos de VMs distribuídas entre diferentes racks de hardware dentro de um datacenter.  
- Se um rack falhar, as VMs em outros racks continuam operando normalmente.  

### 🔄 Domínios de Atualização (Update Domains)  
- Garantem que as VMs sejam atualizadas em momentos diferentes.  
- Evitam reinicializações simultâneas durante manutenção.  

---  

## 🌐 Serviços de Aplicativos (App Services)  
- Plataforma para hospedar e gerenciar aplicações web, APIs e aplicativos móveis **sem se preocupar com infraestrutura subjacente**.  

---  

## 🐳 Instâncias de Contêiner (Container Instances)  
- Solução prática para executar contêineres no Azure **sem gerenciar servidores ou clusters**.  
- **Containers são leves, efêmeros e descartáveis** — uma das grandes vantagens deles.  

### ❓ Por que containers são leves e descartáveis?  
✔ **Compartilham o kernel do sistema operacional**: diferente de VMs, que precisam de um sistema completo.  
✔ **Isolamento leve**: isolam a aplicação e suas dependências sem a sobrecarga de um SO completo.  
✔ **Rápida inicialização e parada**: criados, iniciados, parados e deletados em segundos.  
✔ **Descarte seguro**: apagar um container não afeta o SO nem outros containers.  

### ❓ O que acontece ao apagar um container?  
🗑️ O container é removido, junto com o estado e dados não persistidos.  
💾 **Dados importantes devem usar volumes externos (armazenamento persistente)**.  
📦 A **imagem do container** (template) permanece intacta, a menos que apagada separadamente.  

---  

## 🐳 **Principais Serviços de Containers no Azure**  

| Serviço                          | Descrição                                                                 | Ideal para                                                                 |
|----------------------------------|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| **⚙️ Azure Kubernetes Service (AKS)** | Serviço gerenciado de Kubernetes.                                        | Aplicações complexas, microserviços, produção em escala.                  |
| **🧪 Azure Container Instances (ACI)** | Execução rápida de containers individuais **sem orquestrador**.          | Tarefas pontuais, jobs batch, APIs simples, testes, automações.           |
| **🚢 App Service com Docker Support** | Implantação de containers personalizados diretamente em um App Service.  | Web apps em container com menor complexidade que o AKS.                   |
| **🧱 Azure Container Registry (ACR)** | Registro privado para armazenar imagens Docker.                          | Armazenar e gerenciar imagens em ambientes corporativos.                  |
| **🧰 Azure Red Hat OpenShift (ARO)**  | Plataforma de containers baseada em OpenShift (Red Hat).                 | Empresas que já adotam o ecossistema Red Hat.                             |

---  

## 🖥️ Área de Trabalho Virtual do Azure (Azure Virtual Desktop)  
- Serviço para **virtualização de desktops e aplicativos**.  
- Útil para ambientes corporativos que demandam **acesso remoto**.  
- **Reduz riscos** (ex: evitar perda de notebooks com colaboradores desligados).  

### 🔄 **Múltiplas Sessões**  
- Várias pessoas podem usar a mesma máquina virtual simultaneamente.  
- **Reduz custos** e otimiza recursos.  
- **Microsoft Intune** suporta gestão de ambientes de várias sessões.  

---  

## 🔥 **Azure Functions**  
- Serviço **serverless** para executar pequenos trechos de código (“funções”) em resposta a eventos.  

### 🚀 Principais características:  
✔ **Serverless**: sem gerenciar servidores, SO ou clusters.  
✔ **Event-driven**: acionado por HTTP requests, mensagens em filas, mudanças em bancos, timers.  
✔ **Escalabilidade automática**: ajusta instâncias conforme demanda.  
✔ **Suporta várias linguagens**: C#, JavaScript, Python, Java, PowerShell.  

### 💡 Exemplos de uso:  
- APIs simples e endpoints RESTful.  
- Processamento de dados em background.  
- Automação de workflows.  
- Tarefas agendadas (ex: limpar bases de dados).  

### 📈 Benefícios:  
✔ **Custo eficiente**: paga apenas pelo tempo de execução.  
✔ **Rápida implementação**: foca só na lógica, sem infraestrutura.  
✔ **Flexível e escalável**: ideal para cargas variáveis.  

---  

## 🏗️ **Lift and Shift**  
- Migração de aplicações do ambiente local (**on-premises**) para a nuvem **sem mudanças significativas**.  

### 🔄 Como funciona?  
1️⃣ **Lift (levantar)**: pega a aplicação exatamente como está.  
2️⃣ **Shift (mover)**: muda para a nuvem (ex: VMs no Azure).  

### ✔ Prós:  
- Rápido e simples (não exige reescrever código).  
- Pode ser um primeiro passo para modernização futura.  

### ❌ Contras:  
- Nem sempre otimizado para a nuvem.  
- Pode gerar custos maiores ou desempenho subótimo.  

**Exemplo**: Mover um servidor físico para uma VM no Azure sem alterar o sistema.  

---  

## 🌐 **Principais Recursos de Rede do Azure**  

| Serviço                     | Função Principal                                      |
|----------------------------|------------------------------------------------------|
| **Virtual Network (VNet)** | Rede privada na nuvem para conectar recursos.         |
| **Load Balancer**          | Balanceamento de carga básico (TCP/UDP).             |
| **Application Gateway**    | Balanceamento HTTP/HTTPS + WAF + roteamento avançado.|
| **VPN Gateway**            | Conexão segura via VPN (IPsec/IKE).                  |
| **ExpressRoute**           | Conexão privada dedicada (baixa latência, mais cara).|
| **Azure DNS**              | Gerenciamento de domínios e resolução.               |
| **Azure Firewall**         | Firewall gerenciado para proteger redes Azure.       |
| **Azure Front Door**       | CDN + balanceamento global para aplicações web.      |
| **Azure DDoS Protection**  | Proteção contra ataques DDoS.                        |

---  

## 🛠️ **Criação de Máquinas Virtuais**  

### 01 - Encontre VMs na aba **"Computação"** no painel do Azure.  

### 02 - Escolha entre máquinas **predefinidas** ou **customizadas**:  
| Tipo                     | Descrição                                                                 |
|--------------------------|---------------------------------------------------------------------------|
| **Customizada**          | Escolha SO, tamanho (CPU, RAM), disco, rede. Flexível para cargas específicas. |
| **Predefinida (imagem)** | Imagens prontas (Windows Server, Ubuntu, SQL Server, etc.). Valores mais altos. |

### 03 - **Aba "Básico"**:  
- Nome da VM, grupo de recursos (obrigatório), região, zona de disponibilidade.  
- Imagem do SO ou app.  
- **Spot do Azure** (uso de capacidade ociosa, não recomendado para produção).  
- Tamanho da VM (CPU, RAM, disco).  
- Nome de usuário e senha.  
- Portas de entrada.  

### 04 - **Aba "Discos"**:  
- Tamanho e tipo de discos.  
- **"Excluir com VM"** (evita discos órfãos).  
- Adicionar/anexar discos novos ou existentes.  

### 05 - **Aba "Rede"**:  
- Configuração de rede virtual.  
- **"Excluir IP público e a NIC quando a VM for excluída"** (evita recursos órfãos).  

### 06 - **Aba "Gerenciamento"**:  
- Atribuições de identidade.  
- **Desligamento automático** (não há ligamento automático).  
- Backup (configurável separadamente).  

### 07 - **Aba "Monitoramento"**:  
- Alertas (notificações para eventos).  
- Diagnóstico (pode consumir recursos).  

### 08 - **Aba "Avançado"**:  
- Extensões, aplicativos de VM (opcional).  

### 09 - **Aba "Marcas"**:  
- Tags para classificar recursos (facilita gestão de custos).  

### 10 - **Aba "Revisar + criar"**:  
- Confirme as configurações antes de criar a VM.  

---

# Identidade, Acesso e Segurança 🔐

## Microsoft Entra ID

🔐 **O que é o Microsoft Entra ID?**

O Microsoft Entra ID é uma solução de gerenciamento de identidade e acesso (IAM) baseada em nuvem da Microsoft. Ele permite que organizações controlem o acesso a aplicativos e recursos, tanto na nuvem quanto locais, por meio de autenticação e autorização centralizadas. Isso inclui serviços como Microsoft 365, Azure, Dynamics 365 e milhares de outros aplicativos SaaS. 


🛡️ **Principais Funcionalidades**

**Autenticação Multifatorial (MFA):** Adiciona camadas extras de segurança ao exigir múltiplos métodos de verificação.

**Acesso Condicional:** Aplica políticas de acesso com base em condições como localização, dispositivo e risco do usuário.

**Single Sign-On (SSO):** Permite que usuários acessem múltiplos aplicativos com uma única autenticação.

**Gerenciamento de Identidade Privilegiada (PIM):** Controla e monitora o acesso de usuários com permissões elevadas.

**Provisionamento de Usuários:** Automatiza a criação, atualização e exclusão de contas de usuário em aplicativos conectados.

**Integração com Diretórios Locais:** Conecta-se ao Active Directory local por meio do Microsoft Entra Connect.


🧩 **Planos e Licenciamento**

O Microsoft Entra ID oferece diferentes planos para atender às necessidades das organizações:

**Gratuito:** Inclui recursos básicos como SSO e autenticação multifatorial.

**P1:** Adiciona recursos como acesso condicional e gerenciamento de identidade híbrida.

**P2:** Inclui funcionalidades avançadas como PIM e proteção de identidade.

**Governança:** Focado em governança de identidade e acesso, com recursos adicionais de auditoria e conformidade.


🌐 **Casos de Uso Comuns**

**Organizações Híbridas:** Gerenciar identidades em ambientes locais e na nuvem.

**Aplicações SaaS:** Integrar aplicativos de terceiros com autenticação centralizada.

**Colaboração Externa:** Permitir acesso seguro a parceiros e fornecedores.

**Segurança Zero Trust:** Implementar políticas de segurança baseadas em risco e identidade.

Ele traz recursos como autenticação, logon único (SSO), gerenciamento de aplicativos, negócios para negócios (B2B) e gerenciamento de dispositivos.
Isso significa que ele ajuda empresas a garantir que seus funcionários e parceiros possam acessar recursos com segurança, sem precisar de múltiplas senhas e gerenciando tudo de forma centralizada.


## Microsoft Entra Domain Services 

🔐 **O que é o Microsoft Entra Domain Services?**

O Microsoft Entra Domain Services (Entra DS) é um serviço gerenciado da Microsoft que oferece funcionalidades tradicionais de domínio do Active Directory (AD ou ambiente on premise), mas na nuvem, sem a necessidade de você gerenciar controladores de domínio (domain controllers) diretamente.

Ele faz parte do portfólio Microsoft Entra, que é o conjunto de soluções de identidade e acesso da Microsoft.


🛠️ **Para que serve o Entra Domain Services?**

Ele permite que máquinas virtuais (VMs) e serviços no Azure se autentiquem e façam uso de políticas de domínio, como:

- Autenticação LDAP e Kerberos
- Políticas de grupo (GPO)
- Administração baseada em grupos de segurança
- Integração com aplicações que dependem do LDAP/AD tradicional

Tudo isso sem que você precise instalar, configurar e manter servidores de Active Directory.


⚙️ **Como funciona na prática?**

- Você cria um domínio gerenciado no Azure, que é automaticamente replicado e gerenciado pela Microsoft.
- Você conecta suas VMs e recursos Azure a esse domínio para autenticação.
- Você pode sincronizar identidades do Azure AD para o Entra Domain Services, assim os usuários do Azure AD podem usar as mesmas credenciais.
- Isso facilita o uso de aplicações legadas e serviços que dependem do AD, mas dentro da infraestrutura cloud do Azure.


✅ **Principais benefícios**

- Zero gerenciamento de infraestrutura de domínio: sem servidores para manter, atualizar ou corrigir.
- Alta disponibilidade e escalabilidade: a Microsoft cuida da resiliência.
- Integração direta com Azure AD: simplifica o gerenciamento de identidades.
- Suporte a protocolos tradicionais: LDAP, Kerberos e NTLM.

🏢 **Casos de uso típicos**
- Aplicações legadas na nuvem que precisam de autenticação via AD.
- Cenários híbridos onde você quer estender o domínio para o Azure sem VPNs complicadas.
- Ambientes onde o cliente quer usar políticas de grupo e controles de acesso baseados em domínio sem a complexidade de gerenciar DCs.

### 🔒 Diferença Entre Autenticação e Autorização

**Autenticação:** é o processo de verificar quem você é — ou seja, confirmar sua identidade (login com usuário e senha, por exemplo).

**Autorização:** é o processo de determinar o que você pode fazer — ou seja, quais recursos ou ações você tem permissão para acessar ou executar.

No Azure, primeiro você se autentica (via Azure AD, por exemplo), depois o sistema verifica sua autorização para liberar acesso aos recursos.

### 🔐 Autenticação Multifator

**O que é Autenticação Multifator (MFA)?**

É uma camada extra de segurança na autenticação que exige mais de um método para provar sua identidade.

Em vez de só usar uma senha (fator único), o MFA pede pelo menos dois fatores diferentes, que podem ser:

- Algo que você sabe (senha, PIN)
- Algo que você tem (celular, token, app autenticador)
- Algo que você é (impressão digital, reconhecimento facial)

**Por que usar MFA no Azure?**
- Aumenta muito a segurança da conta.
- Mesmo que a senha seja roubada, o invasor não consegue entrar sem o segundo fator.
- É padrão em muitos serviços de identidade, incluindo o Azure AD.

### 🤝 B2B do Microsoft Entra External ID

O Entra External ID é uma solução da Microsoft para gerenciar identidades externas — ou seja, usuários que não fazem parte da sua organização, mas precisam acessar seus recursos de forma segura.

O B2B (Business-to-Business) do Entra External ID permite que você:

- Convide usuários externos (como parceiros, fornecedores, clientes) para acessar seus apps, dados ou serviços.
- Esses usuários usam suas próprias credenciais (Azure AD, Microsoft Accounts, Google, etc.) para se autenticar.
- Você mantém o controle do acesso, definindo permissões e políticas para esses usuários externos.


⚙️ **Como funciona na prática?**

1. Você convida um usuário externo para sua organização via B2B.
2. O usuário recebe um convite e usa sua conta externa para entrar.
3. O acesso é controlado pelo seu Azure AD, com políticas de segurança e conformidade.
4. Você pode monitorar e gerenciar esses usuários sem precisar criar contas internas para cada um.


✅ **Principais benefícios**

- Simplifica o acesso para parceiros sem complicar o gerenciamento de identidades.
- Mantém o ambiente seguro, com controles e auditorias.
- Integração fácil com múltiplos provedores de identidade.
- Escalável para grandes parcerias ou clientes.

### 🚦 Acesso Condicional

O Acesso Condicional é um mecanismo inteligente de controle de acesso que permite aplicar políticas com base em condições específicas, como:

- Quem está tentando acessar
- De onde (local, IP)
- De qual dispositivo
- Qual aplicativo
- Se passou pela MFA
- Se o dispositivo está em conformidade

Ele é dinâmico: em vez de simplesmente permitir ou bloquear acesso, ele avalia o contexto e toma decisões automatizadas.

🛡 **Exemplo simples**
Política: Se um usuário está tentando acessar fora do país e não passou pela MFA → bloquear ou exigir MFA.

Outro exemplo: Só permitir acesso ao portal do Azure se o usuário estiver com um dispositivo corporativo e registrado.

🔧 **Ações que o Acesso Condicional pode aplicar**
- Exigir MFA
- Exigir dispositivo em conformidade
- Exigir aplicativo aprovado
- Bloquear acesso
- Permitir acesso (com ou sem restrições)

🧠 **Como funciona?**
1. O usuário tenta acessar um recurso (por exemplo, o Microsoft Teams).
2. O Azure AD avalia a tentativa com base nas políticas de acesso condicional.
3. Com base nos critérios, ele decide se:
   - Permite o acesso
   - Bloqueia
   - Ou exige uma ação (como autenticação multifator)

⚙️ **Onde configurar?**
No portal do Azure: Azure Active Directory > Segurança > Acesso Condicional

### 👨‍💼 Controle de Acesso Baseado em Função

✅ **O que é RBAC?**
RBAC (Role-Based Access Control) é uma forma de controlar quem pode fazer o quê dentro do Azure, atribuindo funções (roles) a usuários, grupos ou identidades gerenciadas.

Em vez de dar permissões diretamente a cada usuário, você dá permissões a uma função, e depois atribui essa função ao usuário.

🧠 **Como funciona?**
1. Você define "quem" (usuário, grupo, aplicativo)
2. Atribui uma função (role) — que define as permissões (ex: leitura, gravação, gerenciamento)
3. Associa isso a um escopo (subscription, resource group ou recurso específico)

🔐 **Exemplo simples**

| Usuário       | Função atribuída           | Escopo                | Resultado                                      |
| ------------- | -------------------------- | --------------------- | ---------------------------------------------- |
| Maria         | `Reader`                   | Resource Group "App1" | Pode **ver**, mas não **editar** recursos      |
| Equipe DevOps | `Contributor`              | Subscription inteira  | Pode **criar e editar** recursos               |
| App Web XYZ   | `Storage Blob Data Reader` | Conta de Storage      | Pode **ler blobs** (acesso controlado por app) |


📋 **Tipos de funções comuns no Azure**
- **Owner:** controle total (inclusive delegar permissões)
- **Contributor:** pode criar e gerenciar recursos, mas não dar permissões
- **Reader:** só leitura
- **Funções específicas:** ex: Virtual Machine Contributor, Storage Blob Data Reader, etc.

Você também pode criar funções personalizadas, com permissões sob medida.

🔍 **Onde configurar?**
No portal do Azure:
Vá até o recurso → Controle de Acesso (IAM) → + Adicionar atribuição de função

🛡 **RBAC x Acesso Condicional**
- **RBAC** define o que o usuário pode fazer (permissões).
- **Acesso Condicional** define quando e como o usuário pode acessar (contexto de acesso).

### 🛡️ Modelo de Confiança Zero

🛡️ **O que é o Modelo de Confiança Zero?**
O Modelo de Confiança Zero parte do princípio de:

"Nunca confie, sempre verifique" — independentemente de onde venha a solicitação (interna ou externa da rede).

Ou seja, ninguém ou nenhum dispositivo tem acesso garantido por padrão, mesmo que já esteja "dentro" da rede corporativa.

🔑 **Princípios do Zero Trust**
1. **Verificar explicitamente**
   - Sempre autenticar e autorizar com base em identidade, localização, status do dispositivo, sensibilidade dos dados e outros sinais contextuais.
   - Ex: Acesso condicional + MFA + conformidade do dispositivo.

2. **Conceder acesso com o menor privilégio necessário**
   - Usar RBAC (controle baseado em função) e acesso Just-In-Time (JIT) para limitar o que o usuário pode fazer e por quanto tempo.
   - Ex: Azure Privileged Identity Management (PIM).

3. **Assumir violação**
   - Monitorar continuamente, registrar atividades e estar preparado para resposta rápida.
   - Ex: Microsoft Defender, Microsoft Sentinel, auditorias de acesso.

🧱 **Componentes em um ambiente Zero Trust (na Microsoft)**

| Componente         | Exemplo na Microsoft                           |
| ------------------ | ---------------------------------------------- |
| **Identidade**     | Azure AD, MFA, Acesso condicional              |
| **Dispositivo**    | Intune, Microsoft Defender for Endpoint        |
| **Aplicações**     | Proteção com autenticação, RBAC, tokens        |
| **Dados**          | Microsoft Purview, Sensitivity Labels          |
| **Infraestrutura** | Defender for Cloud, Just-in-Time VM Access     |
| **Rede**           | Azure Firewall, Private Link, VPN, Segmentação |

✅ **Benefícios do Zero Trust**
- Redução do risco de ataques de ransomware, phishing e acesso indevido.
- Melhor visibilidade e controle.
- Adaptação à força de trabalho híbrida/remota.
- Conformidade com normas como LGPD, ISO, NIST, etc.

🧭 **Resumo prático**
- Antes: usuário dentro da rede = confiável
- Agora (Zero Trust): usuário precisa provar constantemente que é confiável, mesmo dentro da rede

### 🛡️ Microsoft Defender for Cloud

🛡️ **O que é o Microsoft Defender for Cloud?**
O Microsoft Defender for Cloud é uma plataforma de proteção de carga de trabalho na nuvem (CWPP) + Postura de segurança (CSPM).

Ele ajuda você a:
- Avaliar e melhorar a segurança do seu ambiente (Azure, AWS, GCP, híbrido)
- Detectar ameaças em tempo real
- Proteger recursos como VMs, bancos de dados, storage, containers, etc.

🧩 **Componentes principais**

🔍 **Secure Score (CSPM)**
- Avalia sua postura de segurança e dá recomendações (ex: ativar MFA, criptografar discos).
- Pontuação baseada em conformidade com boas práticas.
- Ajuda a priorizar ações de segurança.

🛡 **Proteção ativa (Defender Plans – CWPP)**
Planos específicos que protegem cargas de trabalho diferentes, como:

| Plano                     | Protege...                                             |
| ------------------------- | ------------------------------------------------------ |
| Defender for Servers      | VMs (Windows/Linux), integra com Defender for Endpoint |
| Defender for SQL          | SQL Database, SQL Server on-premises e em VMs          |
| Defender for App Services | Web apps no Azure                                      |
| Defender for Containers   | AKS, Kubernetes e registries                           |
| Defender for Storage      | Blobs e arquivos contra malware e acessos suspeitos    |
| Defender for Key Vault    | Acesso anormal a chaves e segredos                     |
| Defender for ARM          | Atividades suspeitas no plano de controle do Azure     |

🔐 **Funcionalidades adicionais**
- Análise de conformidade regulatória (como ISO 27001, NIST, LGPD)
- Integração com SIEM/SOAR (ex: Microsoft Sentinel)
- Alertas de segurança e automação de resposta
- Workbooks e painéis personalizáveis

🌍 **Multicloud e Híbrido**
Você pode proteger recursos em outras nuvens (AWS, GCP) e on-premises, usando o Azure Arc.

📈 **Exemplo prático de uso**
Você ativa o Defender for Servers → Ele detecta que uma VM tem RDP exposto sem proteção → Gera alerta + sugere ação (fechar porta, exigir MFA, etc).

💵 **É gratuito?**
O Secure Score e recomendações básicas de segurança (CSPM) têm uma versão gratuita.

Os planos Defender (proteção ativa) são pagos por recurso protegido (ex: por VM/mês, por banco de dados/mês etc.).

✅ **Resumo rápido**

| Recurso               | O que faz                                        |
| --------------------- | ------------------------------------------------ |
| CSPM (Secure Score)   | Avalia e recomenda melhorias                     |
| CWPP (Defender Plans) | Protege cargas de trabalho específicas           |
| Multicloud            | Suporta Azure, AWS, GCP e ambientes híbridos     |
| Integrações           | Funciona com Sentinel, Arc, Intune, Defender XDR |

---

# AI-900: Conceitos Básicos de IA do Azure

## Conceitos Fundamentais de IA 🤖

1. **O que é Inteligência Artificial (IA)?**  
   Capacidade de uma máquina imitar funções humanas como raciocínio, aprendizado, percepção e tomada de decisão.  

   **Objetivo:** permitir que sistemas executem tarefas inteligentes com pouca ou nenhuma intervenção humana.  

2. **Principais tipos de IA**  
   | Tipo de IA                            | Descrição                                                                                  | Exemplo                                                |  
   | ------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------ |  
   | **IA fraca (Narrow AI)**              | Focada em tarefas específicas                                                              | Assistentes virtuais (Cortana, Siri)                   |  
   | **IA forte (General AI)**             | Teoricamente, executa qualquer tarefa humana                                               | Ainda em pesquisa                                      |  
   | **IA simbólica vs. baseada em dados** | IA tradicional baseada em regras (simbólica) vs. IA moderna baseada em aprendizado (dados) | Diagnóstico médico baseado em regras vs. modelos de ML |  

3. **Áreas da IA**  
   | Área                                         | O que faz                                   | Exemplo                                |  
   | -------------------------------------------- | ------------------------------------------- | -------------------------------------- |  
   | **Machine Learning (ML)**                    | Ensina a máquina a aprender com dados       | Previsão de vendas, análise de crédito |  
   | **Visão Computacional (CV)**                 | Interpreta imagens e vídeos                 | Reconhecimento facial, OCR             |  
   | **Processamento de Linguagem Natural (NLP)** | Entende e gera linguagem humana             | Chatbots, tradução automática          |  
   | **Sistemas de Recomendação**                 | Sugerem conteúdos com base em comportamento | Netflix, Spotify                       |  
   | **IA Conversacional**                        | Interage por voz ou texto                   | Chatbots, assistentes virtuais         |  

4. **O que é Machine Learning (ML)?**  
   Subcampo da IA que permite que modelos aprendam com dados sem serem programados explicitamente, modelos preditivos baseados em dados e estatísticas

   **Ciclo de vida básico:**  
   - Coleta de dados  
   - Preparação de dados  
   - Treinamento do modelo  
   - Avaliação  
   - Implantação  
   - Monitoramento  

5. **Tipos de Aprendizado de Máquina**  
   | Tipo                        | Descrição                                   | Exemplo                              |  
   | --------------------------- | ------------------------------------------- | ------------------------------------ |  
   | **Supervisionado**          | Dados rotulados (entrada + saída conhecida) | Classificação de e-mails como spam   |  
   | **Não supervisionado**      | Dados sem rótulos                           | Agrupamento de clientes (clustering) |  
   | **Aprendizado por reforço** | Baseado em recompensas                      | Robôs aprendendo a andar             |  

6. **Conceitos importantes**  
   - **Modelo:** resultado do aprendizado  
   - **Rótulo (Label):** valor conhecido usado em aprendizado supervisionado  
   - **Feature (atributo):** característica usada para treinar o modelo  
   - **Treinamento:** processo de ensinar o modelo  
   - **Inferência/predição:** uso do modelo treinado para prever resultados  

7. **Ética e Responsabilidade em IA**  
   - Imparcialidade (fairness)  
   - Privacidade e segurança  
   - Explicabilidade (por que o modelo tomou certa decisão?)  
   - Transparência  
   - Impacto social  

8. **Serviços de IA no Azure (visão geral)**  
   | Serviço                    | Função                                                             |  
   | -------------------------- | ------------------------------------------------------------------ |  
   | **Azure Machine Learning** | Plataforma completa de ML                                          |  
   | **Cognitive Services**     | APIs pré-treinadas para visão, linguagem, fala e tomada de decisão |  
   | **Azure OpenAI Service**   | Modelos avançados como GPT                                         |  
   | **Bot Framework**          | Criação de chatbots inteligentes                                   |  

### 🧾 Inteligência de Documentos

É o uso de IA para ler, entender e extrair informações de documentos não estruturados ou semiestruturados (como PDFs, imagens digitalizadas, formulários, notas fiscais, contratos etc.).

🧠 **O objetivo?**
Automatizar tarefas que antes eram feitas manualmente, como:

Digitar dados de notas fiscais

Ler e-mails com anexos

Processar contratos

Organizar formulários

🧩 **Onde isso se encaixa na IA?**
Faz parte da Visão Computacional + Processamento de Linguagem Natural (NLP), pois lida com:

Imagens (OCR)

Texto (compreensão e extração)

Estrutura de documentos (campos, tabelas, layout)

🔧 **No Azure: Azure AI Document Intelligence (antigo Form Recognizer)**
É o serviço da Microsoft criado para esse tipo de tarefa. Ele:

📌 **Funcionalidades principais:**
| Função                          | O que faz                                                     |
| ------------------------------- | ------------------------------------------------------------- |
| **Extração de texto com OCR**   | Lê texto de PDFs e imagens                                    |
| **Extração de layout**          | Detecta tabelas, colunas, posições                            |
| **Modelos pré-treinados**       | Para faturas, recibos, identidades, contratos, etc.           |
| **Modelos personalizados**      | Você treina um modelo com seus próprios documentos            |
| **Classificação de documentos** | Identifica o tipo de documento (ex: nota fiscal vs. contrato) |

⚙️ **Exemplo prático**
Você envia uma imagem de uma nota fiscal → O serviço detecta automaticamente:

Nome do fornecedor

Data de emissão

Valor total

Número da nota

E devolve isso em JSON estruturado, pronto para ser usado em um sistema.

✅ **Benefícios**
Reduz erro humano

Acelera processos manuais

Automatiza captura de dados

Funciona com documentos em massa

🛠 **Quando usar?**
Contas a pagar (AP automation)

Recursos Humanos (leitura de CVs, formulários)

Jurídico (extração de cláusulas de contratos)

Financeiro (processamento de extratos, recibos)


### 🧠 Mineração de Conhecimento

🧠 **O que é Mineração de Conhecimentos no Azure?**
No Azure, Mineração de Conhecimentos (Knowledge Mining) é o uso combinado de IA + busca inteligente para extrair informações úteis de conteúdos não estruturados, como PDFs, imagens, e-mails, contratos, etc.

📦 **Enquadramento no Azure**
A mineração de conhecimento é viabilizada principalmente por três serviços principais:

1. **Azure AI Search**
Um serviço de busca inteligente.

Indexa documentos e permite pesquisa com linguagem natural.

2. **Azure AI Vision + Document Intelligence**
Faz OCR (leitura de texto em imagens/PDFs).

Extrai texto, tabelas, formulários, entidades (como nomes, datas, valores).

3. **Cognitive Skills**
APIs de IA que enriquecem os dados durante a indexação:

Detecção de idioma

Extração de entidades (nomes, locais)

Análise de sentimento

Tradução automática

Classificação de texto

🔁 **Como funciona o pipeline no Azure?**
Você conecta os dados (Blob Storage, SharePoint, SQL, etc.)

Azure analisa e enriquece os dados com IA (OCR + NLP)

O conteúdo é indexado pelo Azure AI Search

Você faz buscas avançadas em uma interface (ex: portal, chatbot, app)

✅ **Resultado prático**
Um buscador inteligente que entende o conteúdo dos documentos

Respostas rápidas a perguntas complexas sobre seus dados

Possibilidade de integrar com chatbots, apps, dashboards

🧭 **Quando usar?**
Use Mineração de Conhecimentos no Azure quando você tem:

Muitos documentos não estruturados

Dificuldade em localizar informações críticas

Desejo de automatizar análise de documentos


### 🤖 IA Generativa

🤖 **O que é IA Generativa?**
IA Generativa é um tipo de inteligência artificial que cria novo conteúdo a partir de dados de entrada — como texto, imagem, áudio ou código.

Exemplos: gerar textos, responder perguntas, criar imagens, resumir documentos, escrever código, entre outros.

📦 **IA Generativa no Azure**
No Azure, a IA Generativa é oferecida principalmente por meio do:

🔹 **Azure OpenAI Service**
É a integração oficial da Microsoft com os modelos da OpenAI (como GPT-4, GPT-3.5, Codex, DALL·E).
Permite usar IA generativa de forma segura, escalável e corporativa.

📌 **Funcionalidades principais com Azure OpenAI:**
| Função                          | O que faz                                    |
| ------------------------------- | -------------------------------------------- |
| **Chatbot com GPT**             | Cria assistentes de conversação              |
| **Geração de texto**            | Completa, reescreve, resume, traduz          |
| **Análise de linguagem**        | Classificação, extração, insights            |
| **Geração de código**           | Gera scripts, funções, ajuda na programação  |
| **Criação de imagens (DALL·E)** | Gera imagens a partir de descrições em texto |

🧩 **Como a IA Generativa se encaixa no Azure?**
| Serviço                    | Papel                                                                                    |
| -------------------------- | ---------------------------------------------------------------------------------------- |
| **Azure OpenAI**           | Fornece os modelos (GPT, Codex, DALL·E)                                                  |
| **Azure AI Studio**        | Ambiente visual para construir soluções com IA generativa                                |
| **Azure Cognitive Search** | Pode ser combinado com IA generativa para fazer **RAG** (Retrieval-Augmented Generation) |
| **Azure Machine Learning** | Treinamento, tuning e monitoramento de modelos de IA generativa personalizados           |
| **Azure Content Safety**   | Avalia e modera o conteúdo gerado (toxicidade, violência, etc.)                          |

✅ **Exemplos de uso no Azure**
Copilot interno: Ajuda funcionários a buscar informações internas com linguagem natural

Geração automática de relatórios: A partir de dados e PDFs

Resumo de contratos: Para áreas jurídicas e compliance

Ajuda a programadores: Com sugestões de código e documentação

🔐 **Segurança e governança no Azure**
Controle de acesso via Azure Active Directory

Auditoria e monitoramento

Conformidade com padrões corporativos

Uso controlado de conteúdo sensível com Azure Content Safety

🧭 **Quando usar IA Generativa no Azure?**
Use IA Generativa no Azure quando você precisa:

Automatizar tarefas complexas de linguagem

Criar experiências conversacionais

Transformar texto, código ou imagens com alta qualidade

Ter controle seguro e governado da IA em ambientes corporativos


### ⚖️ Imparcialidade

⚖️ **O que é Imparcialidade em IA?**
Imparcialidade significa garantir que um sistema de IA trate todos os usuários de forma justa e equitativa, sem favorecer nem prejudicar grupos específicos com base em atributos como:

Gênero

Raça

Idade

Localização

Condições sociais

🚨 **Por que isso é importante?**
Modelos de IA aprendem com dados históricos — que muitas vezes contêm vieses humanos.
Se não forem tratados, esses vieses podem ser reproduzidos ou amplificados pelo sistema de IA.

Exemplo: Um modelo que aprova crédito pode negar mais frequentemente para certos grupos, mesmo que isso não seja intencional.

✅ **Boas práticas de imparcialidade em IA**
Analisar dados de entrada para possíveis vieses

Testar o modelo com diferentes grupos demográficos

Monitorar decisões automatizadas em produção

Ser transparente sobre os limites e riscos do sistema

Incluir diversidade na equipe de desenvolvimento

🧠 **Em resumo para o AI-900:**
Imparcialidade é um princípio ético da IA.

Evita discriminação e decisões injustas.

Azure oferece ferramentas práticas para medir e corrigir vieses.

Faz parte do esforço da Microsoft de promover IA confiável e responsável.

🧰 **Como a Microsoft e o Azure tratam a Imparcialidade?**
A Microsoft aplica princípios de IA Responsável em todos os seus serviços de IA. No Azure, isso se reflete em:

🛠️ **Ferramentas e práticas:**
| Recurso                                                 | Função                                                  |
| ------------------------------------------------------- | ------------------------------------------------------- |
| **Azure Machine Learning – Responsible AI dashboard**   | Permite visualizar, medir e mitigar vieses no modelo    |
| **Fairlearn toolkit (open-source)**                     | Usado para detectar e corrigir desigualdade em modelos  |
| **Model interpretability tools**                        | Ajudam a entender por que o modelo toma certas decisões |
| **Avaliação de métricas de justiça (fairness metrics)** | Permite comparar o desempenho entre grupos diferentes   |


### 🔒 Confiabilidade e Segurança

🔒 **Confiabilidade e Segurança em IA**
Confiabilidade significa que sistemas de IA devem funcionar de maneira consistente e previsível, entregando resultados corretos e que possam ser replicados, mesmo em situações novas ou inesperadas. É fundamental que a IA seja estável e que seus resultados possam ser confiados pelos usuários.

Segurança envolve proteger os sistemas de IA contra ataques e acessos não autorizados, garantindo a integridade dos dados e modelos, além de preservar a privacidade dos usuários e das informações processadas.

**Por que isso importa?**
Sistemas de IA podem ser alvos de tentativas de manipulação, como ataques adversariais que confundem o modelo, ou podem vazar dados sensíveis se não estiverem protegidos. Além disso, falhas no sistema podem causar danos, especialmente em aplicações críticas.

**Como o Azure ajuda?**
O Azure oferece controles rigorosos de segurança, incluindo autenticação forte via Azure Active Directory, criptografia de dados em repouso e em trânsito, monitoramento contínuo e ferramentas para proteger os modelos e dados usados pela IA. Além disso, o Azure fornece práticas para garantir a confiabilidade, como monitoramento de desempenho e testes regulares dos modelos para evitar erros.

**No AI-900, lembre-se:**
Confiabilidade garante que a IA funcione corretamente e consistentemente.

Segurança protege os dados, modelos e acesso ao sistema de IA.

Azure incorpora esses princípios para oferecer soluções de IA seguras e confiáveis.


### 🔐 Privacidade e Segurança

🔐 **Privacidade e Segurança em IA no Azure**
Privacidade significa proteger os dados pessoais e sensíveis das pessoas para que não sejam usados indevidamente ou expostos sem consentimento. Em IA, isso é crucial porque modelos aprendem com dados que podem conter informações pessoais.

Segurança é garantir que os sistemas de IA, os dados usados e os resultados gerados estejam protegidos contra acessos não autorizados, ataques cibernéticos, vazamentos e manipulações.

**Por que isso é importante?**
Dados pessoais expostos podem causar danos às pessoas e à reputação da empresa.

Violações de privacidade podem resultar em multas e problemas legais (ex: GDPR).

Sistemas inseguros podem ser alvo de ataques que prejudicam o funcionamento e a confiabilidade da IA.

**Como o Azure protege a privacidade e a segurança?**
Usa criptografia forte para proteger dados em trânsito e em repouso.

Implementa controle de acesso via Azure Active Directory para garantir que só pessoas autorizadas acessem dados e modelos.

Oferece monitoramento e auditoria para detectar acessos suspeitos.

Suporta políticas de conformidade com normas internacionais de privacidade e segurança.

Fornece ferramentas para anonimizar dados e garantir o uso responsável dos dados na IA.

**No AI-900, é importante entender que:**
Privacidade e segurança são pilares da IA responsável.

Azure oferece recursos integrados para proteger dados e sistemas.

Garantir a privacidade ajuda a manter a confiança dos usuários e cumprir a legislação.


### 🤝 Inclusão e Transparência

🤝 **Inclusão em IA**
Inclusão significa criar sistemas de IA que sejam acessíveis e úteis para todas as pessoas, independentemente de suas habilidades, idiomas, cultura ou condições. É garantir que a IA não exclua nenhum grupo, promovendo diversidade e equidade no uso e nos resultados da tecnologia.

No Azure, a inclusão é levada a sério, com ferramentas que suportam múltiplos idiomas, acessibilidade para pessoas com deficiência, e designs que consideram diferentes realidades culturais e sociais.

🔍 **Transparência em IA**
Transparência refere-se a tornar claro como os sistemas de IA funcionam — como eles tomam decisões, quais dados usam e quais limitações possuem. Isso ajuda usuários e organizações a confiar na tecnologia, compreender seus riscos e responsabilidades.

O Azure oferece ferramentas para interpretar modelos, explicar previsões e monitorar comportamento da IA, facilitando a transparência nos processos automatizados.

**Por que isso importa?**
A inclusão garante que a IA beneficie toda a sociedade.

A transparência cria confiança e responsabilidade no uso da IA.

Juntas, elas ajudam a construir sistemas de IA éticos e responsáveis.


### ⚖️ Responsabilidade

⚖️ **Responsabilidade em IA**
Responsabilidade significa que os desenvolvedores, organizações e usuários de IA devem ser responsáveis pelas ações e impactos dos sistemas de IA que criam e utilizam. Isso envolve garantir que a IA seja usada de forma ética, segura e em conformidade com leis e políticas.

**Por que é importante?**
Sistemas de IA podem afetar pessoas e negócios de formas significativas. A responsabilidade ajuda a prevenir danos, abusos ou usos indevidos, e assegura que haja prestação de contas quando algo sai errado.

**Como o Azure apoia a responsabilidade?**
Oferece ferramentas para monitorar, auditar e controlar o uso de modelos de IA.

Suporta práticas de IA responsável, incluindo mitigação de vieses, explicabilidade e conformidade regulatória.

Permite rastrear decisões feitas por IA para investigação e correção.

Incentiva a transparência e governança de dados.

**No AI-900, lembre-se:**
Responsabilidade é fundamental para construir IA confiável e ética.

Envolve garantir controle humano, monitoramento e conformidade.

Azure fornece recursos para apoiar essa responsabilidade.

2
## Processamento de Linguagem Natural

O que é Processamento de Linguagem Natural (PLN)?
Processamento de Linguagem Natural (PLN) é uma área da inteligência artificial que permite que computadores entendam, interpretem, gerem e respondam à linguagem humana — seja escrita ou falada.

Para que serve?
O PLN ajuda máquinas a lidar com textos e falas do jeito que as pessoas usam no dia a dia, possibilitando coisas como:

Traduzir idiomas automaticamente

Entender perguntas feitas em linguagem natural

Resumir textos longos

Analisar sentimentos em avaliações ou redes sociais

Reconhecer comandos de voz

Como funciona?
Ele combina várias técnicas, como:

Análise gramatical para entender estrutura das frases

Extração de significado para captar o sentido das palavras e frases

Modelos estatísticos e de aprendizado de máquina para interpretar contextos

Geração de texto para responder ou criar conteúdos coerentes

Processamento de Linguagem Natural (PLN) no Azure
No Azure, o PLN é oferecido principalmente por meio do Azure Cognitive Services - Language. Esse serviço permite que aplicações entendam e processem texto em linguagem natural. Ele inclui funcionalidades como:

Análise de sentimento

Reconhecimento de entidades (pessoas, lugares, datas)

Extração de frases-chave

Tradução automática

Resposta a perguntas (QnA)

Essas capacidades ajudam a transformar textos e conversas em dados estruturados e úteis.

**IA Conversacional no Azure**

A IA Conversacional é a aplicação prática do PLN para criar interfaces que interagem com humanos por meio de linguagem natural — como chatbots e assistentes virtuais.

No Azure, essa área é atendida pelo Azure Bot Service e pelo Azure Cognitive Services - Language, além da integração com o Azure OpenAI Service para capacidades avançadas, como o uso de modelos GPT.

Com essas ferramentas, você pode criar:

Chatbots para atendimento ao cliente

Assistentes virtuais internos

Interfaces conversacionais que entendem perguntas complexas e respondem de forma natural

Suporte automatizado para tarefas específicas

Em resumo
PLN no Azure processa e entende textos e linguagem natural.

IA Conversacional usa PLN para criar diálogos naturais entre humanos e máquinas.

Azure oferece serviços integrados para construir, treinar e implantar essas soluções de forma escalável e segura

### Reconhecimento de Entidade Nomeada

Imagine que uma imagem mostra uma frase:

"I had a wonderful trip to Seattle last week."

O Azure usa PLN para analisar esse texto e identificar entidades nomeadas, que são partes importantes da frase com significado específico. Esse processo é chamado de NER — Named Entity Recognition, ou em português, Reconhecimento de Entidade Nomeada.

🧩 Entidades identificadas
O Azure extrai e classifica três tipos de entidade no texto:

Event (Evento):

Palavra: trip

Confiança: 74%

Representa uma ação ou atividade (viagem, nesse caso).

Location (Localização):

Palavra: Seattle

Confiança: 100%

Reconhecida como uma cidade (GPE = geopolitical entity).

DateTime (Data/Tempo):

Expressão: last week

Confiança: 80%

Indica um intervalo de tempo recente.

🎯 Para que isso serve?
O NER é usado para estruturar informações em textos. Exemplos práticos:

Um chatbot que entende quando o usuário fala datas, locais ou eventos.

Um sistema que analisa e classifica e-mails, contratos ou mensagens automaticamente.

Ferramentas de busca que destacam entidades para melhorar os resultados.

🤖 No Azure
Esse tipo de análise pode ser feito com o Azure Cognitive Services – Language, usando o recurso de Named Entity Recognition. É muito útil em IA conversacional, pois permite que os sistemas entendam a intenção e o contexto de forma mais rica.

### Detecção de PII e PHI

🔐 O que é PII e PHI?
PII – Personally Identifiable Information
Informações de identificação pessoal. São dados que podem identificar uma pessoa diretamente ou indiretamente, como:

Nome completo

CPF / RG

Endereço

Telefone

Número de cartão de crédito

E-mail pessoal

PHI – Protected Health Information
Informações de saúde protegidas. São dados médicos vinculados a uma pessoa, como:

Diagnósticos

Resultados de exames

Históricos médicos

Dados de planos de saúde

Informações clínicas com identificação pessoal

🧠 Por que detectar isso?
Em aplicações de IA, como chatbots, análise de texto, e processamento de documentos, é comum trabalhar com dados sensíveis. A detecção automática de PII/PHI ajuda a:

Evitar vazamentos de dados

Cumprir leis de privacidade, como LGPD, GDPR, HIPAA

Reduzir riscos legais e reputacionais

Anonimizar dados antes de treinar modelos ou expor textos

🔍 Como o Azure ajuda?
O Azure Cognitive Services – Language inclui funcionalidades de detecção automática de PII e PHI. Ele consegue:

Identificar dados pessoais e de saúde em textos

Classificar os tipos de informação encontrados

Oferecer ferramentas para anonimização (ex: substituir por "
𝑅
𝐸
𝐷
𝐴
𝐶
𝑇
𝐸
𝐷
REDACTED")

Você pode usar isso para:

Processar textos médicos com segurança

Monitorar conteúdo sensível em documentos, e-mails, ou sistemas de atendimento

Exemplo prático
Texto:

“Maria Souza fez um exame de sangue no dia 15 de abril e seu CPF é 123.456.789-00.”

Resultado:

Nome: Maria Souza → PII

Data: 15 de abril → PII

CPF: 123.456.789-00 → PII

Tipo de exame: sangue → PHI


### Detecção de Idioma

🌍 O que é detecção de idioma?
Detecção de idioma (ou language detection) é a capacidade de um sistema identificar automaticamente em qual idioma um texto foi escrito.

Por exemplo, ao receber a frase:

"Bonjour, comment ça va?"

Um sistema de detecção de idioma reconhece que isso está em francês, mesmo sem ninguém dizer isso diretamente.

🤖 Como o Azure faz isso?
O Azure oferece essa funcionalidade através do:

Azure Cognitive Services – Language

Serviço de Tradução (Translator)

Esses serviços permitem:

Detectar automaticamente o idioma de qualquer texto enviado

Retornar o código do idioma (por exemplo, "fr" para francês ou "pt" para português)

Indicar um nível de confiança na detecção (ex: 99%)

📦 Para que serve?
Tradução automática (saber de onde para onde traduzir)

Chatbots multilíngues (responder no idioma do usuário)

Análise de sentimento por idioma

Organizar ou filtrar conteúdo com base em idioma


### Análise de Sentimentos

💬 O que é Análise de Sentimentos?
Análise de sentimentos é uma técnica de Processamento de Linguagem Natural (PLN) que permite que sistemas entendam a emoção ou opinião expressa em um texto.

Ela identifica se um texto é:

Positivo (ex: "Adorei o serviço!")

Negativo (ex: "Foi uma experiência terrível.")

Neutro (ex: "Recebi o pedido ontem.")

E, em alguns casos, misto (ex: "A comida era boa, mas o atendimento ruim.")

🧠 Como o Azure faz isso?
Através do serviço:

🔹 Azure Cognitive Services – Language, usando a funcionalidade de Sentiment Analysis

Esse serviço:

Analisa textos em vários idiomas

Retorna o sentimento geral e também por frase

Indica escores de confiança (ex: 85% de certeza de que o texto é positivo)

🧪 Exemplo
Texto:

"A entrega foi rápida, mas o produto veio quebrado."

Resultado:

Sentimento geral: Misto

Frase 1: "A entrega foi rápida." → Positivo

Frase 2: "O produto veio quebrado." → Negativo

📌 Para que serve?
Avaliar feedback de clientes

Monitorar redes sociais

Entender opiniões em pesquisas e comentários

Automatizar respostas (ex: alertar sobre críticas negativas)


### Respostas a Perguntas

❓ O que é o recurso de Respostas a Perguntas (Question Answering)?
É uma funcionalidade de IA que permite que um sistema encontre respostas exatas para perguntas feitas em linguagem natural, a partir de conteúdo já existente, como:

Documentos

FAQs

Manuais

Sites

🔍 Como funciona no Azure?
No Azure Cognitive Services – Language, esse recurso é chamado de:

👉 Azure Question Answering
Ele funciona assim:

Você envia uma pergunta (ex: "Qual o horário de funcionamento?")

O serviço procura nos conteúdos fornecidos (base de conhecimento)

Ele retorna a resposta mais relevante, com pontuação de confiança

🧠 Tipos de uso
Chatbots inteligentes que respondem dúvidas frequentes

Assistentes virtuais internos (RH, TI, suporte)

Sistemas de busca inteligente em bases de documentos

🧪 Exemplo
Pergunta:

"Como faço para redefinir minha senha?"

Resposta extraída do conteúdo:

"Você pode redefinir sua senha acessando o portal de segurança e clicando em 'Esqueci minha senha'."

✅ Benefícios
Respostas rápidas e consistentes

Redução da carga em atendentes humanos

Facilidade de integração com bots no Microsoft Teams, web e apps

### Recurso de Fala

🗣️ O que são os recursos de fala?
São serviços que permitem que os aplicativos ouçam, falem e entendam linguagem falada, usando inteligência artificial. Eles conectam a fala humana com sistemas computacionais.

🔧 Funcionalidades principais
Reconhecimento de fala (Speech to Text)
Converte fala em texto em tempo real ou a partir de gravações.
Ex: Transcrever reuniões ou comandos de voz.

Síntese de fala (Text to Speech)
Converte texto em voz natural.
Ex: Criar narradores virtuais, assistentes que falam, ou ler conteúdo para usuários.

Tradução de fala (Speech Translation)
Traduz a fala de um idioma para outro com voz ou texto.
Ex: Conversas multilíngues em tempo real.

Reconhecimento de fala personalizado
Treine modelos para entender sotaques, termos técnicos ou nomes próprios específicos.

Verificação e identificação de locutor (Speaker Recognition)
Verifica ou identifica quem está falando com base na voz.

🎯 Para que serve?
Chatbots por voz

Leitura automatizada de documentos

Acessibilidade (ex: leitores de tela)

Tradução em tempo real

Comandos de voz em apps e dispositivos

🧠 Integração com IA conversacional
Você pode combinar fala + linguagem natural no Azure para criar assistentes conversacionais completos, que entendem, falam e respondem em voz.


### Recurso de Tradução

🌍 O que é a tradução no Azure?
É um serviço de tradução automática oferecido pelo Azure Cognitive Services, chamado:

👉 Azure Translator
Ele permite que aplicativos e sistemas traduzam texto ou fala de um idioma para outro com rapidez e precisão.

🧠 O que ele faz?
Tradução de texto entre mais de 100 idiomas

Detecção automática do idioma original

Tradução de documentos inteiros (como PDFs, DOCX)

Tradução em tempo real de conversas faladas (Speech Translation)

Suporte a gírias, expressões locais e termos personalizados

🧪 Exemplo
Texto original:

"Olá, como você está?"

Tradução para inglês (usando o serviço):

"Hello, how are you?"

💡 Para que serve?
Sites multilíngues

Aplicativos globais

Chatbots que atendem em vários idiomas

Tradução de manuais, contratos e mensagens

Acessibilidade para pessoas de diferentes nacionalidades

📌 Como usar?
Você pode usar a tradução no Azure de três formas:

Via API REST (em apps e sistemas)

Pelo Azure Language Studio

Integrado com outros serviços, como bots, Power Automate e Microsoft 365