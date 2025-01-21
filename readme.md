
# Jogo de Quiz em Go

Este projeto é um jogo de quiz simples desenvolvido em Go. O jogo lê perguntas de um arquivo CSV e permite que os jogadores respondam, atribuindo pontos para respostas corretas.

## Funcionalidades
- Quiz interativo com perguntas e respostas de múltipla escolha.
- Leitura de perguntas de um arquivo CSV (`quiz-go.csv`).
- Controle de pontuação do jogador.
- Validação de entrada para respostas numéricas.

## Começando

### Pré-requisitos
- [Go](https://golang.org/doc/install) (recomenda-se a versão 1.23.5 ou superior).
- Um arquivo CSV chamado `quiz-go.csv` na mesma pasta do programa.

### Formato do Arquivo CSV
O arquivo CSV deve ter o seguinte formato:

| Pergunta          | Opção1 | Opção2 | Opção3 | Opção4 | Índice da Resposta Correta |
|--------------------|--------|--------|--------|--------|----------------------------|
| Exemplo de Pergunta 1 | A    | B      | C      | D      | 2                          |

- A coluna **Índice da Resposta Correta** deve conter o índice (baseado em 1) da resposta correta.

### Instalação
1. Clone o repositório ou baixe o código-fonte.
2. Navegue até o diretório do projeto:
   ```bash
   cd quiz-game
   ```
3. Certifique-se de que o arquivo `quiz-go.csv` está na mesma pasta do programa.

### Executando o Programa
Execute o programa com o seguinte comando:
```bash
go run main.go
```

### Como Jogar
1. Quando solicitado, insira seu nome.
2. O jogo exibirá uma série de perguntas com respostas de múltipla escolha.
3. Digite o número correspondente à sua resposta escolhida e pressione Enter.
4. O jogo informará se a sua resposta está correta e registrará seus pontos.
5. Ao final do quiz, sua pontuação total será exibida.

### Exemplo de Uso
```bash
Seja bem vindo(a) ao quiz.
Escreva o seu nome:
João
Vamos ao jogo João 

1. Qual é o resultado de 2 + 2?
[1] 3
[2] 4
[3] 5
[4] 6
Digite uma alternativa.
2
Resposta correta!
Fim do game, você fez 10 pontos
```

## Estrutura do Código
- **`Question` struct**: Representa uma pergunta do quiz.
- **`GameState` struct**: Gerencia o estado do jogo, incluindo informações do jogador, pontuação e perguntas.
- **Métodos principais**:
  - `Init()`: Inicializa o jogo.
  - `ProccessCSV()`: Lê e processa as perguntas do quiz a partir do arquivo CSV.
  - `Run()`: Executa o loop principal do jogo.
- Função utilitária: `toInt(string)`: Valida e converte entradas de string para números inteiros.

## Contribuindo
Sinta-se à vontade para enviar issues ou pull requests para melhorar o jogo!

## Licença
Este projeto está licenciado sob a licença MIT.
