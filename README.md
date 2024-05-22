# Projeto iPhone

Este projeto modela e implementa as funcionalidades de um iPhone, incluindo um reprodutor musical, um aparelho telefônico e um navegador na internet.

## Funcionalidades a Modelar

### Reprodutor Musical
- **Métodos**: 
  - `tocar()`
  - `pausar()`
  - `selecionarMusica(String musica)`

### Aparelho Telefônico
- **Métodos**:
  - `ligar(String numero)`
  - `atender()`
  - `iniciarCorreioVoz()`

### Navegador na Internet
- **Métodos**:
  - `exibirPagina(String url)`
  - `adicionarNovaAba()`
  - `atualizarPagina()`

## Diagrama UML

```mermaid
classDiagram
    class ReprodutorMusical {
        <<interface>>
        +tocar()
        +pausar()
        +selecionarMusica(String musica)
    }

    class AparelhoTelefonico {
        <<interface>>
        +ligar(String numero)
        +atender()
        +iniciarCorreioVoz()
    }

    class NavegadorInternet {
        <<interface>>
        +exibirPagina(String url)
        +adicionarNovaAba()
        +atualizarPagina()
    }

    class iPhone {
        +tocar()
        +pausar()
        +selecionarMusica(String musica)
        +ligar(String numero)
        +atender()
        +iniciarCorreioVoz()
        +exibirPagina(String url)
        +adicionarNovaAba()
        +atualizarPagina()
    }

    ReprodutorMusical <|-- iPhone
    AparelhoTelefonico <|-- iPhone
    NavegadorInternet <|-- iPhone
