# 🛒 Sales Web MVC

Sistema de gerenciamento de vendas desenvolvido em ASP.NET Core MVC com Entity Framework Core e PostgreSQL.

> **Projeto educacional** baseado no curso de C# e .NET da Udemy, adaptado para .NET 8 e PostgreSQL.

---

## 🚀 Tecnologias

- **ASP.NET Core 8.0** - Framework web
- **Entity Framework Core 8.0** - ORM
- **PostgreSQL** - Banco de dados
- **C# 12** - Linguagem de programação
- **Bootstrap** - Framework CSS

---

## 📋 Pré-requisitos

Antes de começar, você precisa ter instalado:

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [PostgreSQL 12+](https://www.postgresql.org/download/)
- IDE de sua preferência:
  - [Visual Studio 2022](https://visualstudio.microsoft.com/) (Windows)
  - [JetBrains Rider](https://www.jetbrains.com/rider/) (Windows/Linux/Mac)
  - [Visual Studio Code](https://code.visualstudio.com/) + C# Extension

---

## ⚙️ Configuração do Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/SalesWebMvc.git
cd SalesWebMvc
```

### 2. Configure a Connection String

Edite o arquivo `appsettings.json` e ajuste a connection string do PostgreSQL:

```json
{
  "ConnectionStrings": {
    "SalesWebMvcContext": "Host=localhost;Port=5432;Database=saleswebmvc;Username=postgres;Password=SUA_SENHA"
  }
}
```

**⚠️ Importante:** Substitua `SUA_SENHA` pela senha do seu PostgreSQL.

### 3. Crie o banco de dados

Execute os comandos do Entity Framework:

```bash
# Criar a migration inicial
dotnet ef migrations add InitialCreate

# Criar/atualizar o banco de dados
dotnet ef database update
```

### 4. Execute o projeto

```bash
dotnet run
```

Acesse no navegador: `https://localhost:5001` ou `http://localhost:5000`

---

## 📁 Estrutura do Projeto

```
SalesWebMvc/
├── Controllers/        # Controllers MVC
├── Models/            # Modelos de domínio
├── Views/             # Views Razor
├── Data/              # DbContext e configurações do EF
├── Migrations/        # Migrations do Entity Framework
├── wwwroot/           # Arquivos estáticos (CSS, JS, imagens)
└── appsettings.json   # Configurações da aplicação
```

---

## 🎯 Funcionalidades

- ✅ Cadastro de vendedores
- ✅ Cadastro de departamentos
- ✅ Registro de vendas
- ✅ Relatórios de vendas por período
- ✅ Busca simples e agrupada
- ✅ Validação de dados
- ✅ Tratamento de erros

---

## 🗃️ Modelo de Dados

O sistema trabalha com as seguintes entidades principais:

- **Seller** (Vendedor)
- **Department** (Departamento)
- **SalesRecord** (Registro de Venda)

---

## 🛠️ Comandos Úteis

### Entity Framework

```bash
# Adicionar nova migration
dotnet ef migrations add NomeDaMigration

# Atualizar banco de dados
dotnet ef database update

# Reverter última migration
dotnet ef migrations remove

# Ver SQL que será executado
dotnet ef migrations script
```

### Execução

```bash
# Executar em modo de desenvolvimento
dotnet run

# Executar com hot reload
dotnet watch run

# Compilar o projeto
dotnet build

# Publicar para produção
dotnet publish -c Release
```

---

## 🔐 Segurança

**⚠️ NUNCA commite suas senhas!**

Para ambientes diferentes, use:

- `appsettings.Development.json` - Desenvolvimento (não commitado)
- `appsettings.json` - Configurações gerais
- Variáveis de ambiente em produção

Adicione no `.gitignore`:
```
appsettings.Development.json
```

---

## 📚 Recursos de Aprendizado

Este projeto foi desenvolvido seguindo o curso:

- **Curso:** C# COMPLETO Programação Orientada a Objetos + Projetos
- **Instrutor:** Nélio Alves
- **Plataforma:** Udemy

**Adaptações realizadas:**
- Migração de .NET Core 2.1 para .NET 8
- Substituição de SQL Server por PostgreSQL
- Atualização para práticas modernas do ASP.NET Core

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer um fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abrir um Pull Request

---

## 📝 Licença

Este projeto é de código aberto para fins educacionais.

---

## 👨‍💻 Autor

Desenvolvido durante estudos de ASP.NET Core MVC e Entity Framework.

- GitHub: [@seu-usuario](https://github.com/seu-usuario)

---

## 🙏 Agradecimentos

- Nélio Alves pelo excelente curso
- Comunidade .NET Brasil
- Microsoft Docs

---

**⭐ Se este projeto foi útil para você, considere dar uma estrela!**