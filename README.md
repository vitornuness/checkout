# Checkout Inteligente

## Instalação da API - Back-end

Abaixo estão os passos necessários, **exclusivamente para a instalação e execução do projeto**. Para mais detalhes sobre os endpoints e suas funcionalidades, consulte a documentação em seu repositório.

[Repositório](https://github.com/VitorNuness/checkout-inteligente-back)

### Pré-requisitos

Antes de começar, você precisa ter os seguintes itens instalados em sua máquina:

1. **[.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)**
2. **[MySQL Server](https://dev.mysql.com/downloads/mysql/)**
3. **[MySQL Workbench](https://dev.mysql.com/downloads/workbench/)** (opcional, mas recomendado para gerenciar o banco de dados)
4. **[Git](https://git-scm.com/downloads)**

### Clonando o Repositório

```bash
git clone https://github.com/VitorNuness/checkout-inteligente-back.git

cd checkout-inteligente-back/App
```

### Configurando o Banco de Dados

Após clonar o repositório, será necessário configurar a conexão com o banco em `appsettings.json`.

```json
"ConnectionStrings": {
    "DefaultConnection": "server=localhost;userid=root;password=root_password;database=checkout"
},
```

Altere o `userid` e `password` para o usuário e a senha com permissões do seu banco. A `database` é opcional, mas se necessário, poderá atualizar para um nome de sua preferência.

### Executando as Migrações

Navegue até o projeto de infraestrutura:

```bash
cd src/Checkout/Infra
```

Para criar as tabelas no banco de dados, utilize o comando:

```bash
dotnet ef database update -s ../Presentation
```

### Executando o Projeto

Navegue até o projeto de infraestrutura:

```bash
cd ../Presentation
```

Para executar o projeto, use o seguinte comando:

```bash
dotnet run
```

Ao executar o projeto, o Banco de Dados será atualizado com dados para demonstração.

O servidor deve iniciar e você verá uma mensagem indicando que a aplicação está rodando em http://localhost:5102.

## Instalação da Aplicação Front-end

Abaixo estão os passos necessários, **exclusivamente para a instalação e execução do projeto**. Para mais detalhes sobre as páginas, componentes e suas funcionalidades, consulte a documentação em seu repositório.

[Repositório](https://github.com/VitorNuness/checkout-inteligente-front)

### Pré-requisitos

Antes de começar, você precisa ter os seguintes itens instalados em sua máquina:

1. **[Node.js](https://nodejs.org/)**
2. **[Git](https://git-scm.com/downloads)**
3. **[API (Back-end)](#instalação-da-api---back-end)**

### Clonando o Repositório

```bash
git clone https://github.com/VitorNuness/checkout-inteligente-front.git

cd checkout-inteligente-front
```

### Instalando Dependências

Execute o seguinte comando para instalar as dependências do projeto:

```bash
npm install
```

### Executando a Aplicação

Para executar a aplicação, use o seguinte comando:

```bash
npm run dev
```

O servidor deve iniciar e você verá uma mensagem indicando que a aplicação está rodando em http://localhost:5173.

---

## Colaboradores

**@[AlexHPasquini](https://github.com/AlexHPasquini) | @[MayconMacedo23](https://github.com/MayconMacedo23) | @[vinirainho](https://github.com/vinirainho) | @[VitorNuness](https://github.com/VitorNuness)**
