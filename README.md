# Sistema de Gerenciamento de Estacionamento

Sistema desenvolvido como desafio da Trilha .NET Fundamentos da [Digital Innovation One](https://www.dio.me/).

## 📋 Descrição do Projeto

Sistema console interativo para gerenciamento de um estacionamento, permitindo cadastrar, remover e listar veículos. O programa calcula automaticamente a tarifa de estacionamento baseada no tempo de permanência do veículo.

## 🏗️ Estrutura do Projeto

```
Desafio-fundamentos-CShap/
│
├── README.md                          # Documentação do projeto
├── trilha-net-fundamentos-desafio.sln # Arquivo solução do Visual Studio
│
└── DesafioFundamentos/               # Pasta principal do projeto
    ├── DesafioFundamentos.csproj     # Arquivo de configuração do projeto
    ├── Program.cs                    # Arquivo principal (ponto de entrada)
    │
    ├── Models/                       # Pasta contendo as classes de modelo
    │   └── Estacionamento.cs         # Classe que implementa a lógica do estacionamento
    │
    ├── bin/                          # Pasta de saída compilada
    └── obj/                          # Pasta de arquivos de objeto compilados
```

## 🎯 Funcionalidades Implementadas

### 1. **Adicionar Veículo**
Permite cadastrar um novo veículo no estacionamento através da sua placa.
- Usuário digita a placa do veículo
- Veículo é armazenado em uma lista interna

### 2. **Remover Veículo**
Remove um veículo do estacionamento e calcula a tarifa total.
- Solicita a placa do veículo
- Verifica se o veículo está estacionado (busca case-insensitive)
- Solicita o tempo (em horas) que o veículo permaneceu estacionado
- Calcula e exibe o valor total: `preço inicial + (preço por hora × horas)`
- Remove o veículo da lista

### 3. **Listar Veículos**
Exibe todos os veículos atualmente estacionados.
- Se houver veículos: lista a placa de cada um
- Se não houver: exibe mensagem "Não há veículos estacionados"

### 4. **Menu Interativo**
Interface em loop que permite:
1. Cadastrar veículo
2. Remover veículo
3. Listar veículos
4. Encerrar programa

## 💻 Classe Principal: Estacionamento

### Variáveis de Instância

| Variável | Tipo | Descrição |
|----------|------|-----------|
| `precoInicial` | `decimal` | Preço fixo cobrado para qualquer veículo estacionado |
| `precoPorHora` | `decimal` | Preço adicional cobrado por cada hora de permanência |
| `veiculos` | `List<string>` | Lista das placas dos veículos estacionados |

### Métodos

#### `Estacionamento(decimal precoInicial, decimal precoPorHora)`
**Construtor** - Inicializa o estacionamento com os preços definidos pelo usuário.

#### `AdicionarVeiculo()`
Adiciona um novo veículo ao estacionamento.

#### `RemoverVeiculo()`
Remove um veículo e calcula a tarifa cobrada.

#### `ListarVeiculos()`
Exibe todos os veículos atualmente estacionados.

## 🚀 Como Usar

1. **Clone ou execute o projeto:**
   ```bash
   dotnet run
   ```

2. **Na inicialização:**
   - Digite o preço inicial para estacionar
   - Digite o preço por hora de permanência

3. **No menu:**
   - Selecione a opção desejada (1-4)
   - Siga as instruções na tela
   - Pressione uma tecla para continuar

### Exemplo de Uso

```
Seja bem vindo ao sistema de estacionamento!
Digite o preço inicial:
10.00

Agora digite o preço por hora:
5.00

[Menu interativo]
Digite a sua opção:
1 - Cadastrar veículo
2 - Remover veículo
3 - Listar veículos
4 - Encerrar
```

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** C# (.NET 6.0)
- **Tipo de Projeto:** Console Application
- **Paradigma:** Programação Orientada a Objetos (POO)

## 📌 Conceitos Aplicados

- ✅ Classes e Instanciação de Objetos
- ✅ Variáveis Privadas e Públicas
- ✅ Construtores
- ✅ Métodos
- ✅ Coleções (List<T>)
- ✅ LINQ (método `Any()` e `Remove()`)
- ✅ Entrada e Saída de Dados (Console)
- ✅ Estruturas de Controle (if/else, while, switch)
- ✅ Conversão de Tipos
- ✅ Tratamento de Strings (ToUpper())

## 👤 Autor

Desenvolvido como parte do desafio da Trilha .NET Fundamentos da DIO.

## 📚 Referências

- [DIO - Digital Innovation One](https://www.dio.me/)
- [Documentação .NET](https://docs.microsoft.com/dotnet/)
- [Documentação C#](https://docs.microsoft.com/pt-br/dotnet/csharp/)
