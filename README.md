# Barbearia

## Descrição do Projeto

Este repositório contém um sistema de gerenciamento de barbearia desenvolvido em Java para a disciplina de Programação Orientada a Objetos. O sistema permite cadastrar clientes e funcionários, controlar serviços, estoque e agendamentos, registrar relatórios de venda e acompanhar extratos e balanço financeiro.

O objetivo do trabalho é praticar os conceitos de orientação a objetos, como classes, herança (`Cliente` e `Funcionario` estendem a classe abstrata `Pessoa`), enumerações, encapsulamento e interfaces (`Comparator`). Os dados são salvos em arquivos JSON, usando a biblioteca Gson, e a classe principal executa uma série de testes que demonstram as funcionalidades do sistema.

## Estrutura do Projeto

O código está organizado em pacotes dentro de `src/main/java`:

* `Model`: classes que representam os dados do sistema (`Pessoa`, `Cliente`, `Funcionario`, `Servico`, `Produto`, `Agendamento`, `RelatorioDeVenda`, `Extrato`, `Balanco` e `Estacoes`).
* `Controller`: lógica de negócio, com um gerenciador para cada área (clientes, funcionários, serviços, estoque, agendamentos, relatórios de venda, extratos, balanço e associações). A classe `SistemaBarbearia` reúne todos eles e também controla o login.
* `DAO`: leitura e gravação dos dados nos arquivos JSON.
* `Json`: arquivos onde os dados ficam armazenados.
* `Enums`: valores fixos usados no sistema (`Cargo`, `Estado`, `Status`, `StatusAgendamento` e `StatusRDV`).
* `Comparators`: comparadores usados para ordenar clientes, agendamentos, IDs e textos.
* `Testes`: testes que exercitam as funcionalidades do sistema.
* `Barbearia`: classe principal (`main`) que inicia o sistema e executa os testes.

Na raiz do repositório, a pasta `docs/` guarda o documento de modelagem.

## Modelagem

Antes da implementação, foi realizada a modelagem completa do sistema com UML. O documento reúne o diagrama de casos de uso, os fluxos de eventos, os diagramas de sequência, o diagrama de classes (modelos, controladores, DAOs, comparadores e enums) e o diagrama de estados. A estrutura de pacotes e classes do código foi construída a partir dessa modelagem.

* [Documento de modelagem (PDF)](docs/modelagem-uml.pdf)

## Requisitos

* Java 24 (JDK)
* Maven
* Gson 2.10.1 (baixada automaticamente pelo Maven)

## Funcionalidades do Sistema

* Cadastro e gerenciamento de clientes e funcionários, com login de usuário.
* Cadastro de serviços e controle de estoque de produtos.
* Agendamentos com status (preliminar, confirmado ou cancelado).
* Relatórios de venda com status (pendente, pago ou cancelado).
* Extratos e balanço financeiro.
* Controle de ocupação das estações de trabalho.
* Persistência dos dados em arquivos JSON.

## Como Rodar

1. Clone o repositório:

```
git clone https://github.com/thaiicarvalho/NOME_DO_REPOSITORIO.git
```

2. Entre na pasta do projeto, onde fica o arquivo `pom.xml`:

```
cd NOME_DO_REPOSITORIO
```

3. Compile e execute:

```
mvn compile exec:java
```

Também é possível abrir o projeto em uma IDE (NetBeans, IntelliJ ou VS Code) e executar a classe `Barbearia.Barbearia`.

## Observações

* Projeto desenvolvido para a disciplina de Programação Orientada a Objetos.
* Execute sempre a partir da pasta onde está o `pom.xml`, pois os arquivos JSON são acessados por caminho relativo (`src/main/java/Json/`).
* Os dados de clientes e demais registros nos arquivos JSON são fictícios.

## Licença

Projeto destinado apenas para fins educacionais.
