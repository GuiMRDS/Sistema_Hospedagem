# 🏨 Sistema de Hospedagem — DIO .NET

![C#](https://img.shields.io/badge/C%23-239120?style=flat&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)
![DIO](https://img.shields.io/badge/DIO-Trilha_.NET-512BD4?style=flat)

Desafio de projeto desenvolvido como parte da **Trilha .NET** da [Digital Innovation One (DIO)](https://www.dio.me/), módulo **Explorando a linguagem C#**. O sistema simula o processo de reserva em um hotel, com validação de capacidade, cálculo de diárias e aplicação de desconto por fidelidade.

---

## 🧠 Sobre o Desafio

Modelar um sistema de hospedagem em C# com três classes principais — `Pessoa`, `Suite` e `Reserva` — aplicando orientação a objetos, encapsulamento, coleções (`List`) e regras de negócio reais como validação de lotação e desconto progressivo.

---

## 🏗️ Arquitetura de Classes

![Diagrama de classes](diagrama_classe_hotel.png)

```
Pessoa
 └── Nome, Sobrenome

Suite
 └── TipoSuite, Capacidade, ValorDiaria

Reserva
 ├── Hospedes (List<Pessoa>)
 ├── Suite
 ├── DiasReservados
 ├── CadastrarHospedes(List<Pessoa>)
 ├── CadastrarSuite(Suite)
 ├── ObterQuantidadeHospedes() → int
 └── CalcularValorDiaria() → decimal
```

### Descrição das classes

| Classe | Responsabilidade |
|---|---|
| `Pessoa` | Representa um hóspede com nome e sobrenome |
| `Suite` | Representa uma suíte com tipo, capacidade e valor da diária |
| `Reserva` | Gerencia o relacionamento entre hóspedes e suíte, valida capacidade e calcula o valor total |

---

## ✅ Funcionalidades

- 👤 Cadastro de hóspedes via `List<Pessoa>`
- 🛏️ Cadastro de suíte com tipo, capacidade e valor da diária
- 🚫 Validação: não permite reserva se a quantidade de hóspedes exceder a capacidade da suíte
- 💰 Cálculo do valor total da hospedagem
- 🎁 **10% de desconto** em reservas com **10 ou mais dias**
- 📋 Exibição da lista de hóspedes e quantidade de dias reservados

---

## 📌 Regras de Negócio

| Regra | Descrição |
|---|---|
| Validação de capacidade | Não é permitido reservar uma suíte com capacidade menor que a quantidade de hóspedes |
| Desconto por fidelidade | Reservas com 10 ou mais dias recebem **10% de desconto** no valor total |
| `ObterQuantidadeHospedes()` | Retorna o número de hóspedes cadastrados na reserva |
| `CalcularValorDiaria()` | Retorna o valor total com ou sem desconto conforme os dias reservados |

---

## 🗂️ Estrutura do Projeto

```
trilha-net-explorando-desafio/
├── Models/
│   ├── Pessoa.cs                    # Classe hóspede
│   ├── Suite.cs                     # Classe suíte
│   └── Reserva.cs                   # Classe reserva com regras de negócio
├── Program.cs                       # Ponto de entrada — simula uso do sistema
├── diagrama_classe_hotel.png        # Diagrama UML das classes
├── DesafioProjetoHospedagem.csproj
├── trilha-net-explorando-desafio.sln
└── README.md
```

---

## 🚀 Como Executar

### Pré-requisitos

- [.NET SDK 6+](https://dotnet.microsoft.com/download)
- Visual Studio 2022 ou VS Code

### Passo a passo

**1. Clone o repositório**
```bash
git clone https://github.com/GuiMRDS/trilha-net-explorando-desafio.git
cd trilha-net-explorando-desafio
```

**2. Execute**
```bash
dotnet run
```

> Ou abra o arquivo `trilha-net-explorando-desafio.sln` no Visual Studio e pressione `F5`.

---

## 🖥️ Exemplo de Saída

```
Hóspedes:
- Guilherme Marinho
- Maria Silva

Quantidade de hóspedes: 2
Dias reservados: 10
Valor total da diária: R$ 900,00 (com 10% de desconto)
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| C# | Linguagem principal de desenvolvimento |
| .NET 6+ | Plataforma de execução |
| Visual Studio | IDE utilizada |
| Git / GitHub | Versionamento de código |

---

## 📚 Conceitos Praticados

- **Orientação a Objetos** — classes, propriedades e métodos
- **Encapsulamento** — controle de acesso a atributos
- **Coleções** — uso de `List<T>` para gerenciar hóspedes
- **Estruturas de controle** — `if`, `foreach` para validações e iterações
- **Regras de negócio** — desconto progressivo e validação de capacidade
- **Diagrama de classes UML** — modelagem prévia da estrutura do sistema

---

## 🎓 Contexto Acadêmico

> Projeto desenvolvido como desafio da **Trilha .NET** da **Digital Innovation One (DIO)**, módulo Explorando a linguagem C#.
>
> Fork do repositório original: [digitalinnovationone/trilha-net-explorando-desafio](https://github.com/digitalinnovationone/trilha-net-explorando-desafio)

---

## 👨‍💻 Autor

**Guilherme Marinho**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-guilherme--marinho04-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/guilherme-marinho04/)
[![GitHub](https://img.shields.io/badge/GitHub-GuiMRDS-black?style=flat&logo=github)](https://github.com/GuiMRDS)
[![Email](https://img.shields.io/badge/Email-guimars22%40gmail.com-red?style=flat&logo=gmail)](mailto:guimars22@gmail.com)

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte de um desafio da DIO.
