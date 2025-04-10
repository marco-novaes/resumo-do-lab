# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO sobre Microsoft Azure

# ⚙️ Configurações e Personalização do Portal

Este repositório contém informações e instruções sobre as **configurações do portal** e suas possibilidades de **personalização**. Aqui você encontra detalhes sobre como alterar idioma, aparência e visualizar as categorias de serviços disponíveis.

---

## 📌 Personalizações Possíveis

### 🌐 Idioma
É possível **alterar o idioma** do portal de acordo com a preferência do usuário.

### 🎨 Aparência e Inicialização
Também é possível modificar:
- O **tema/visual** do portal;
- As **exibições de inicialização**, que determinam como o conteúdo aparece ao carregar o portal.

---

## 📚 Navegação no Portal

### 🔎 Todos os Serviços

Na seção `Todos os serviços`, o usuário pode navegar por **diversas categorias**, facilitando a busca por funcionalidades específicas.

#### Exemplos:

- **🧮 Computação**  
  Dentro deste serviço, é possível visualizar:
  - Versões de **imagens de VM**;
  - Versões de **aplicativos de VM**;
  - Serviços baseados em **PaaS**;
  - Opções de **microserviços**.

- **🌐 Networking**  
  Um exemplo importante é o serviço **Bastions**, que permite **configurar uma rede segura**, ideal para acessos protegidos e gerenciamento de conexões.

---

## 🧪 Versões Prévias (Preview)

Alguns serviços são disponibilizados inicialmente como **versões prévias**, conhecidas como **preview**.

> ⚠️ Isso significa que o serviço está em fase de teste, e os usuários podem utilizá-lo e fornecer feedback sobre sua utilidade e desempenho.

---

# ☁️ SLA, Disponibilidade e Armazenamento em Ambientes de Nuvem

Este documento apresenta conceitos fundamentais sobre **SLA (Acordo de Nível de Serviço)**, disponibilidade de recursos e tipos de redundância em contas de armazenamento. Tudo isso é essencial para um bom planejamento de infraestrutura na nuvem e atendimento a requisitos de negócios.

---

## 📊 Tabela de SLA e Tempo de Inatividade

| **SLA**   | **Tempo de inatividade por semana** | **Tempo de inatividade por mês** | **Tempo de inatividade por ano** |
|----------|-------------------------------------|----------------------------------|----------------------------------|
| 99%      | 1,68 hora                           | 7,2 horas                        | 3,65 dias                        |
| 99,9%    | 10,1 minutos                         | 43,2 minutos                     | 8,76 horas                       |
| 99,95%   | 5 minutos                            | 21,6 minutos                     | 4,38 horas                       |
| 99,99%   | 1,01 minuto                          | 4,32 minutos                     | 52,56 minutos                    |
| 99,999%  | 6 segundos                           | 25,9 segundos                    | 5,26 minutos                     |

> 📌 **Quanto maior o número de noves no SLA, menor o tempo permitido de inatividade.**

---

## 📌 Por que o SLA é importante?

- Se você **criar um recurso** e ele ficar fora do ar por mais tempo do que o previsto no SLA, a **Microsoft precisa ressarcir** o cliente.
- Antes de implementar qualquer solução, é importante **verificar com a equipe qual SLA é necessário**.
- Isso se aplica a tudo: **produtos, serviços, máquinas virtuais, contas de armazenamento** e muito mais.

---

## 🖥️ Disponibilidade na Criação de Máquinas Virtuais

Durante a criação de uma VM, na seção **"Detalhes da Instância"**, é possível configurar opções de disponibilidade:

### ✅ Recursos disponíveis:

- **Zona de disponibilidade**
- **Conjunto de disponibilidade**
- **Conjunto de dimensionamento de máquinas virtuais (VMSS)**

> ℹ️ Ao posicionar o mouse sobre o ícone `i` ao lado da opção, aparece um resumo do recurso e um botão “**Saiba mais**” que leva direto para a documentação oficial no [Microsoft Docs](https://learn.microsoft.com/).

---

## 🗄️ Redundância em Contas de Armazenamento

A **redundância** define como os dados são replicados para garantir alta disponibilidade. Os principais tipos são:

| **Sigla** | **Descrição** |
|----------|----------------|
| **LRS**  | Armazenamento com Redundância Local (*Local Redundant Storage*) |
| **GRS**  | Armazenamento com Redundância Geográfica (*Geo Redundant Storage*) |
| **ZRS**  | Armazenamento com Redundância de Zona (*Zone Redundant Storage*) |
| **GZRS** | Armazenamento com Redundância de Zona Geográfica (*Geo-Zone Redundant Storage*) |

> 📌 Esses tipos de armazenamento influenciam diretamente no SLA, pois armazenam dados em **várias localidades** simultaneamente.

⚠️ **Importante:** Sempre verifique os **requisitos do projeto antes de aplicar uma solução**. Redundância e disponibilidade mais alta trazem custos adicionais na nuvem.

---

## ⚙️ Configurações de Máquina Virtual e Banco de Dados no Azure

### 💻 Imagem e Tamanho (Pay-as-you-go)

- Quando a configuração está como **Pay-as-you-go**, tudo o que for criado será de **responsabilidade do usuário**.
- É possível **adicionar discos** além dos que já vêm por padrão.

---

### 🌐 Rede

- Na seção de rede, é possível configurar **se a máquina estará exposta ou não à internet**.

---

### 🛠️ Gerenciamento

- Nessa etapa, já se configura como será o ambiente de **produção**, incluindo monitoramento, identidade, backup e outras opções relacionadas.

---

## 🗄️ Criação de Banco de Dados SQL

### 📍 Detalhes do Servidor

- Definir o **nome do servidor** e a **localização**.
- Escolher o tipo de **autenticação**: SQL ou Microsoft.
- Selecionar o **modelo de redundância do armazenamento de backup**, lembrando de considerar o **SLA (Acordo de Nível de Serviço)**.

---

### 💰 Estimativa de Custo

- Após preencher todas as configurações, o portal exibe o **custo mensal estimado** da solução.

---

### 📝 Observação

- Todo o **gerenciamento** está diretamente ligado ao **modelo de serviço** escolhido.
