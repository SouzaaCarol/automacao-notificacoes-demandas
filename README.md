# 📧 Automação de Notificações por E-mail com Python

## 🎯 Sobre o Projeto

Projeto desenvolvido para automatizar etapas de um processo de acompanhamento de demandas a partir de planilhas Excel.

A proposta é utilizar Python para carregar uma planilha de demandas, validar as configurações de e-mail e preparar a integração com um serviço SMTP para o envio automatizado de notificações.

A solução busca reduzir atividades manuais, facilitar o acompanhamento de prazos e tornar a comunicação sobre demandas mais ágil.

## ⚙️ Funcionalidades

### 1. Seleção de Planilhas
- Abertura de uma janela para selecionar o arquivo diretamente no computador.
- Suporte a arquivos Excel nos formatos `.xlsx` e `.xls`.
- Validação para identificar quando nenhum arquivo é selecionado.

### 2. Leitura e Tratamento de Dados
- Importação da planilha utilizando Pandas.
- Carregamento dos dados para um DataFrame.
- Tratamento de erros durante a leitura do arquivo.
- Exibição de mensagens para acompanhar a execução do processo.

### 3. Configuração de E-mail
- Utilização de variáveis de ambiente para armazenar as configurações de e-mail.
- Integração com a biblioteca `smtplib`.
- Preparação de mensagens utilizando `MIMEText` e `MIMEMultipart`.
- Validação da existência das credenciais antes de prosseguir com a execução.

### 4. Validação e Monitoramento
- Verificação das configurações necessárias para a execução.
- Exibição de mensagens de sucesso e erro no terminal.
- Identificação de problemas relacionados à leitura da planilha e às configurações de e-mail.

## 🛠️ Tecnologias e Bibliotecas

| Tecnologia | Aplicação |
|---|---|
| Python | Linguagem principal do projeto. |
| Pandas | Leitura e manipulação de planilhas Excel. |
| Tkinter | Interface gráfica para seleção de arquivos. |
| SMTP | Estrutura de integração para envio de e-mails. |
| smtplib | Comunicação com servidores de e-mail. |
| python-dotenv | Carregamento de variáveis de ambiente. |
| MIME | Estruturação do conteúdo das mensagens. |

## 📂 Estrutura do Projeto

```text
automacao-notificacoes/
│
├── main.py
├── .env
├── .gitignore
├── requirements.txt
│
└── README.md
```

### Descrição dos Arquivos

| Arquivo | Descrição |
|---|---|
| `main.py` | Código principal responsável pela seleção e leitura da planilha e validação das configurações. |
| `.env` | Arquivo local com as credenciais e configurações de e-mail. |
| `.gitignore` | Arquivos e pastas que não devem ser enviados ao GitHub. |
| `requirements.txt` | Lista de dependências necessárias para executar o projeto. |

## 🚀 Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone URL_DO_REPOSITORIO
```

### 2. Acesse a pasta do projeto

```bash
cd automacao-notificacoes
```

### 3. Crie um ambiente virtual

```bash
python -m venv venv
```

Ative o ambiente virtual:

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### 4. Instale as dependências

```bash
pip install pandas openpyxl python-dotenv
```

### 5. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
EMAIL_REMETENTE=seu_email@gmail.com
EMAIL_DESTINATARIO=email_destinatario@gmail.com
SENHA_APP=sua_senha_de_aplicativo
```

**Importante:** para contas Gmail, utilize uma senha de aplicativo quando exigida, em vez da senha convencional da conta.

Nunca compartilhe suas credenciais ou envie o arquivo `.env` para o GitHub.

### 6. Execute o projeto

```bash
python main.py
```

Uma janela será aberta para selecionar a planilha Excel que contém as demandas.

## 🔐 Segurança

As credenciais de e-mail são armazenadas em variáveis de ambiente por meio do arquivo `.env`, evitando deixar informações sensíveis diretamente no código-fonte.

Certifique-se de incluir o arquivo `.env` no `.gitignore`:

```gitignore
.env
venv/
__pycache__/
*.pyc
```

## 📌 Próximas Melhorias

- Implementar o envio automático de e-mails via SMTP.
- Identificar demandas próximas do vencimento.
- Criar regras para notificar responsáveis conforme os prazos.
- Personalizar o conteúdo das mensagens com informações da planilha.
- Implementar logs para registrar os envios e possíveis falhas.
- Adicionar tratamento para planilhas com colunas obrigatórias ausentes.

## 👩‍💻 Autora

**Ana Carolina Martins Souza**

Projeto desenvolvido para praticar Python, manipulação de dados e automação de processos, explorando formas de reduzir atividades operacionais repetitivas.