# Modelagem e Diagramação de um Componente iPhone

## Descrição
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![UML](https://img.shields.io/badge/UML-FABD14.svg?style=for-the-badge&logo=UML&logoColor=black)

Este repositório contém o diagrama UML do componente iPhone e o código em Java para as classes e interfaces apresentadas.

Através do diagrama UML mapeamos a estrutura do sistema do iPhone. Esse dispositivo contém funcionalidades do reprodutor musical, aparelho telefônico e navegador de internet.


## Diagrama UML

```mermaid
classDiagram

    class ReprodutorMusical {
        <<interface>>
        + tocar()
        + pausar()
        + selecionarMusica(String musica)
    }
    iPhone ..> ReprodutorMusical 
    
    class AparelhoTelefonico {
        <<interface>>
        + ligar(String numero) 
        + atender() 
        + iniciarCorreioVoz()
    }
    iPhone ..> AparelhoTelefonico 

    class NavegadorInternet{
        <<interface>>
        + exibirPagina(String url) 
        + adicionarNovaAba()
        + atualizarPagina()
    }
    iPhone ..> NavegadorInternet

    class GoogleChrome{

    }
    NavegadorInternet <.. GoogleChrome

    class iPhone {

    }

    class iPod{

    }
    ReprodutorMusical <.. iPod

    class BlackBerry8800{

    }
    AparelhoTelefonico <..BlackBerry8800
    

    style ReprodutorMusical fill:#9ff,stroke:#369,stroke-width:2px,color:#000,stroke-dasharray: 5 5
    style AparelhoTelefonico fill:#9ff,stroke:#369,stroke-width:2px,color:#000,stroke-dasharray: 5 5
    style NavegadorInternet fill:#9ff,stroke:#369,stroke-width:2px,color:#000,stroke-dasharray: 5 5
```

## Classes e interfaces

### iPhone (classe):

Esta classe implementa as interfaces `ReprodutorMusical`, `AparelhoTelefonico` e `NavegadorInternet`, assim ela define o comportamento dos métodos de acordo com suas necessidades e desempenha o papel das três interfaces.

### iPod (classe):

Esta classe implementa a interface `ReprodutorMusical`, assim ela define o comportamento dos métodos de acordo com suas necessidades e desempenha o papel desta interface. Esta classe foi criada apenas para exemplificar uma classe que implementa apenas a interface `ReprodutorMusical`.

### BlackBerry8800 (classe):

Esta classe implementa a interface `AparelhoTelefonico`, assim ela define o comportamento dos métodos de acordo com suas necessidades e desempenha o papel desta interface. Esta classe foi criada apenas para exemplificar uma classe que implementa apenas a interface `AparelhoTelefonico`.

### GoogleChrome (classe):

Esta classe implementa a interface `NavegadorInternet`, assim ela define o comportamento dos métodos de acordo com suas necessidades e desempenha o papel desta interface. Esta classe foi criada apenas para exemplificar uma classe que implementa apenas a interface `NavegadorInternet`.

### ReprodutorMusical (interface):

A interface `ReprodutorMusical`é resposável pela definição dos métodos `tocar()`, `pausar()` e `selecionarMusica(String musica)`. Classes que implementam esta interface necessitam realizar a sobrescrita dos métodos dela. Desta forma, as classes que implementam esta interface podem funcionar como um reprodutor musical.

### AparelhoTelefonico (interface):

A interface `AparelhoTelefonico` é responsável pela definição dos métodos `ligar(String numero)`, `atender()` e `iniciarCorreioVoz()`. Classes que implementam esta interface necessistam realizar a sobrescrita dos métodos dela. Desta forma, as classes que implementam esta interface podem funcionar como um aparelho telefônico.

### NavegadorInternet (interface):

A interface `NavegadorInternet` é responsável pela definição dos métodos `exibirPagina(String url)`, `adicionarNovaAba()` e `atualizarPagina()`. Classes que implementam esta interface necessitam realizar a sobrescrita dos métodos dela. Desta forma, as classes que implementam esta interface podem funcionar como um navegador de internet.



