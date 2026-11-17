Baixe e extraia o Prova_Robson_Varela.zip 
# 🐾 Clínica Veterinária

### Sistema de Gerenciamento de Clínica Veterinária

Sistema web desenvolvido com **ASP.NET Core MVC (.NET 8)**, SQL Server e Entity Framework Core, com autenticação JWT, proteção de senhas utilizando BCrypt e criptografia AES-GCM para os CPFs dos tutores.

---

## 🚀 1. Como executar

Para iniciar o sistema, siga os passos abaixo.

**1. Abra o terminal do Visual Studio Code ou PowerShell.**

**2. Entre na pasta `sistema`:**

```powershell
cd .\sistema
```

**3. Execute o projeto:**

```powershell
dotnet run
```

**4. Acesse o endereço HTTPS** apresentado no terminal pelo navegador.

**5. Informe seu login e senha** na tela de autenticação.

---

## 🔐 2. Usuários de acesso

O sistema possui três contas de teste:

| Perfil | E-mail | Senha |
|---|---|---|
| Administrador | admin@clinica.com | Admin@123 |
| Recepção | ana@clinica.com | Ana@123 |
| Recepção | carlos@clinica.com | Carlos@123 |

As contas são criadas automaticamente pelo inicializador quando a tabela `Usuarios` está vazia.

As senhas são protegidas com hashes BCrypt.

---

## 🛠️ 3. Tecnologias utilizadas

| Tecnologia | Utilização |
|---|---|
| C# | Linguagem de programação |
| .NET 8 | Plataforma de desenvolvimento |
| ASP.NET Core MVC | Desenvolvimento web |
| SQL Server | Banco de dados |
| Entity Framework Core | Mapeamento e acesso aos dados |
| JWT | Autenticação |
| BCrypt | Proteção de senhas |
| AES-GCM | Criptografia dos CPFs |

---

## 💻 4. Requisitos para execução

- SDK do .NET 8 instalado.
- SQL Server Express instalado e em execução.
- Instância `localhost\SQLEXPRESS` configurada.
- Banco de dados `ClinicaVetDb` preparado.
- Migrations e tabelas aplicadas.
- Chaves `Jwt:Key` e `Encryption:Key` configuradas.

### Configuração de segurança

As chaves devem estar disponíveis por User Secrets ou variáveis de ambiente.

**Importante:** o arquivo ZIP não inclui os User Secrets do computador de desenvolvimento.

A chave AES deve ser a mesma utilizada para criptografar os CPFs já armazenados. Não compartilhe essas chaves publicamente.

---

## ⚙️ 5. Primeira execução

Caso seja a primeira execução no computador:

1. Instale e inicie o SQL Server Express.
2. Configure a conexão no `appsettings.json`.
3. Configure as chaves JWT e AES.
4. Crie o banco e aplique as migrations, caso necessário.
5. Configure o certificado HTTPS.

Para confiar no certificado de desenvolvimento, execute:

```powershell
dotnet dev-certs https --trust
```

Depois, inicie o projeto:

```powershell
dotnet run
```

---

## 📁 6. Estrutura do projeto

```text
Robson_Varela_Prova/
│
├── sistema/
│   ├── Controllers/
│   ├── Models/
│   ├── Views/
│   ├── Data/
│   ├── Services/
│   ├── wwwroot/
│   ├── appsettings.json
│   └── Program.cs
│
├── documentacao.pdf
├── diagrama_er.pdf
├── saep_db.sql
└── README.md
```

*Estrutura ilustrativa da entrega.*

---

## 📚 7. Roteiro de desenvolvimento

Projeto desenvolvido seguindo o roteiro de referência:

[Clínica Veterinária — .NET 8 MVC + JWT](https://devflexa.github.io/rotina/#step-23)

Etapas importantes:

| Etapa | Descrição |
|---|---|
| 05 | Configuração do banco, JWT e chave AES |
| 21 | Criação do banco de dados |
| 22 | Primeira execução em HTTPS |
| 23 | Geração e conferência do arquivo SQL |
| 25 | Testes e organização da entrega |

---

## ⏹️ 8. Como encerrar

Para finalizar a aplicação, pressione `Ctrl + C` no terminal onde o sistema está em execução.

---

## 👨‍💻 9. Informações do projeto

**Desenvolvedor:** Robson Varela

**Turma:** Desenvolvimento de Sistemas — Manhã

**Projeto:** Clínica Veterinária

**Plataforma:** ASP.NET Core MVC (.NET 8)

---

**Clínica Veterinária — Sistema de gerenciamento desenvolvido como projeto acadêmico.**
