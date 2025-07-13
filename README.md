# Chess System Java
[![License](https://img.shields.io/npm/l/react)](https://github.com/rodrigobarr0s/chess-system-java/blob/main/LICENSE)

## Sobre o projeto

Este repositório contém uma aplicação em Java puro que simula um **sistema completo de jogo de xadrez**. O projeto foi desenvolvido durante o curso de **Programação Orientada a Objetos com Java**, ministrado pelo Prof. Dr. Nélio Alves. O foco é aplicar os principais conceitos da **POO** em um cenário real e desafiador.

## Tecnologias e Conceitos Utilizados

- **Java 8+**
- **Programação Orientada a Objetos**
- **Tratamento de exceções personalizadas**
- **Matriz como estrutura de tabuleiro**
- **Camadas de aplicação (UI, lógica de negócio, entidades)**
- **Regras do jogo de xadrez (movimentos, xeque, xeque-mate, captura, roque, promoção, en passant)**

## Como Executar o Projeto

### Pré-requisitos

- Java JDK 8 ou superior
- IDE que suporte projetos Java (IntelliJ, Eclipse, VS Code...)

### Passos para execução

```bash
# Clonar o repositório
git clone https://github.com/rodrigobarr0s/chess-system-java.git

# Acessar o diretório
cd chess-system-java

# Compilar e rodar a aplicação
javac application/Program.java
java application.Program
```

A interface é via terminal e exibe o tabuleiro com os movimentos permitidos e jogadas realizadas.

## Estrutura do Projeto

* `board/` → Classes genéricas como Piece, Board, Position, BoardException  
* `chess/` → Classes específicas do xadrez como ChessPiece, ChessMatch, King, Rook, etc.  
* `application/` → Programa principal e interface (UI)

## Principais Funcionalidades

- Validação de posições e jogadas
- Alternância entre jogadores
- Impressão dinâmica do tabuleiro
- Controle de peças capturadas
- Regras de xeque, xeque-mate e jogadas especiais
- Programação defensiva com tratamento de exceções

## Movimentos Possíveis das Peças

Cada peça possui uma lógica própria de movimentação, implementada com métodos abstratos e sobrescritos nas classes específicas. O sistema calcula e exibe os movimentos válidos dinamicamente no terminal, destacando as casas disponíveis para cada peça.

![Movimentos Possíveis](https://raw.githubusercontent.com/rodrigobarr0s/chess-system-java/main/img/possible-moves.png)


## Regras Especiais do Xadrez

O projeto implementa as principais **regras especiais do jogo de xadrez**, respeitando a lógica oficial de movimentação e comportamento das peças. Essas funcionalidades tornam a aplicação mais realista e desafiadora, revelando atenção aos detalhes e aplicação de conceitos avançados da programação orientada a objetos.

### Roque (Castling)

O roque é uma jogada especial entre o rei e a torre, que envolve movimentação dupla. O sistema valida as condições do roque, como:
- Rei e torre não movidos anteriormente
- Nenhuma peça entre rei e torre
- Rei não pode estar em xeque nem passar por casas sob ataque

![Roque](https://raw.githubusercontent.com/rodrigobarr0s/chess-system-java/main/img/castling.png)

---

### En Passant

O en passant permite que um peão capture outro que tenha avançado duas casas a partir da posição inicial, como se tivesse avançado apenas uma.

A lógica do sistema:
- Identifica o peão vulnerável à captura
- Permite a captura válida somente no turno seguinte
- Atualiza corretamente as listas de peças capturadas e movimento do peão

![En Passant](https://raw.githubusercontent.com/rodrigobarr0s/chess-system-java/main/img/en-passant.png)

---

### Promoção de Peão

Quando um peão alcança a última fileira, ele pode ser promovido a qualquer outra peça (geralmente a dama).

A funcionalidade implementa:
- Detecção automática da condição de promoção
- Substituição dinâmica da peça
- Atualização do estado da partida e possível novo xeque

![Promoção](https://raw.githubusercontent.com/rodrigobarr0s/chess-system-java/main/img/promotion.png)

---

Essas regras foram cuidadosamente programadas, respeitando as **regras oficiais do xadrez**, com uso de **polimorfismo, encapsulamento, exceções customizadas e lógica defensiva**. Demonstram o comprometimento com a fidelidade do jogo e a aplicação madura dos conceitos de engenharia de software.

## Autor

**Rodrigo Barros**  
[LinkedIn](https://www.linkedin.com/in/rodrigobarr0s)