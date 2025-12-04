# 🧠 Fundamentos de Programação em Java  
**Guia de estudos completo com explicações, exemplos, exercícios práticos e um projeto unificado**

Este material foi criado para quem deseja aprender Java desde o zero ou reforçar os fundamentos da linguagem.  
Cada módulo contém:

- ✔️ Explicação clara e direta  
- ✔️ Exemplos reais em Java  
- ✔️ Exercícios práticos para fixação  
- ✔️ Tarefas para evoluir um **projeto unificado**

---

## 🚀 Projeto Unificado: TaskManager

Ao longo deste guia, você vai construir um projeto chamado **TaskManager**, um gerenciador de tarefas em linha de comando.

A ideia é que, a cada capítulo, você aplique o que aprendeu para deixar o projeto mais completo.

### 🎯 Objetivo do TaskManager

Criar um programa em Java que permita:

- Cadastrar tarefas  
- Listar tarefas  
- Marcar tarefas como concluídas  
- Remover tarefas  
- Filtrar e organizar tarefas (por status, prioridade, etc.)  
- Tratar erros de forma  
- Utilizar boas práticas de código

### 🧱 Estrutura inicial do projeto

- Clone o projeto inicial deste repositório
- No início, tudo será feito direto no `main`, e aos poucos vamos refatorar para algo mais organizado.

---

## 📌 Sumário

1. Variáveis  
2. Tipos Primitivos  
3. Operadores  
4. Estruturas Condicionais (if/else)  
5. Laços de Repetição (for, while)  
6. Métodos (Funções)  
7. Arrays  
8. Collections (List, Set, Map)  
9. Orientação a Objetos  
10. Tratamento de Exceções  
11. Streams  
12. Boas práticas

---

## 1️⃣ Variáveis

### 📘 O que é uma variável?
Uma variável é um espaço reservado na memória para armazenar dados.  
Em Java, você sempre precisa declarar o **tipo** da variável antes de usá-la.

Java é **estaticamente tipada**, então o tipo não pode mudar durante a execução.

### ✏️ Exemplo

```java
public class Main {
    public static void main(String[] args) {
        int idade = 25;
        double altura = 1.82;
        boolean programador = true;
        String nome = "Thalles";

        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("Altura: " + altura);
        System.out.println("É programador? " + programador);
    }
}
```

### 🏋️ Exercícios

1. Crie três variáveis: **nome**, **idade**, **cidade** e imprima tudo em uma única linha.  
2. Crie um `double precoProduto` e `double desconto`. Calcule o valor final do produto.  
3. Declare uma variável `boolean temCarteiraDeMotorista` e imprima mensagens diferentes dependendo do valor.

### 🧩 TaskManager — Aplicando este capítulo

- Crie a classe `TaskManagerApp` com o método `main`.  
- Crie variáveis para simular uma primeira tarefa:
  - `String titulo = "Estudar Java";`
  - `String descricao = "Estudar variáveis e tipos primitivos";`
  - `boolean concluida = false;`
- Imprima essas informações no console como se fosse um cartão de tarefa.

---

## 2️⃣ Tipos Primitivos

### 📘 O que são?

Java possui 8 tipos primitivos — os valores mais básicos e leves da linguagem.

| Tipo     | Descrição          | Exemplo                         |
|----------|--------------------|---------------------------------|
| byte     | números pequenos   | `byte b = 10;`                  |
| short    | números maiores    | `short s = 300;`                |
| int      | inteiros comuns    | `int idade = 29;`               |
| long     | inteiros grandes   | `long populacao = 8000000000L;` |
| float    | decimal simples    | `float peso = 70.5f;`           |
| double   | decimal preciso    | `double salario = 5000.99;`     |
| boolean  | verdadeiro/falso   | `boolean ativo = true;`         |
| char     | caractere único    | `char letra = 'A';`             |

### ✏️ Exemplo

```java
public class Main {
    public static void main(String[] args) {
        int quantidade = 15;
        double temperatura = 27.4;
        char letra = 'J';
        boolean ativo = false;

        System.out.println(quantidade);
        System.out.println(temperatura);
        System.out.println(letra);
        System.out.println(ativo);
    }
}
```

### 🏋️ Exercícios

1. Crie variáveis usando **todos os tipos primitivos** e imprima seus valores.  
2. Crie um `char` com sua inicial e imprima: `"Minha inicial é X"`.  
3. Crie um `float valor` e multiplique por 3, imprimindo o resultado.

### 🧩 TaskManager — Aplicando este capítulo

- Adicione uma variável `int prioridade` para representar a prioridade da tarefa (1 = baixa, 2 = média, 3 = alta).  
- Use um `char` para representar o status:
  - `'A'` = a fazer  
  - `'E'` = em andamento  
  - `'C'` = concluída  

Imprima a tarefa com essas informações adicionais.

---

## 3️⃣ Operadores

### 📘 O que são operadores?
Operadores são símbolos usados para realizar cálculos ou comparações entre valores.

### 🔢 Operadores aritméticos

| Operador | Significado  |
|----------|--------------|
| `+`      | Soma         |
| `-`      | Subtração    |
| `*`      | Multiplicação|
| `/`      | Divisão      |
| `%`      | Resto        |

### ✏️ Exemplo

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 3;

        System.out.println(a + b); // 13
        System.out.println(a - b); // 7
        System.out.println(a * b); // 30
        System.out.println(a / b); // 3
        System.out.println(a % b); // 1
    }
}
```

### 🏋️ Exercícios

1. Crie três variáveis `a`, `b` e `c` e calcule a **média** delas.  
2. Verifique se um número é **par ou ímpar** usando `%`.  
3. Converta `segundos = 3600` para **minutos e horas**.

### 🧩 TaskManager — Aplicando este capítulo

- Crie uma variável `int totalTarefas = 3;` e outra `int tarefasConcluidas = 1;`  
- Calcule a **porcentagem de tarefas concluídas**.  
- Imprima algo como: `"Progresso: 33% das tarefas concluídas."`

---

## 4️⃣ Estruturas Condicionais (if / else)

### 📘 O que é?
Uma estrutura condicional permite que você execute blocos de código dependendo de uma condição verdadeira ou falsa.

### ✏️ Exemplo

```java
public class Main {
    public static void main(String[] args) {
        int idade = 18;

        if (idade >= 18) {
            System.out.println("Maior de idade");
        } else {
            System.out.println("Menor de idade");
        }
    }
}
```

### 🏋️ Exercícios

1. Verifique se um número é **positivo**, **negativo** ou **zero**.  
2. Dado uma variável `nota`, imprima:
   - "Aprovado" (≥ 6)  
   - "Recuperação" (≥ 4)  
   - "Reprovado" (demais casos)  
3. Verifique se uma pessoa pode entrar em um evento:
   - Idade mínima: 16  
   - Pode entrar com responsável a partir de 14  

### 🧩 TaskManager — Aplicando este capítulo

- Dado o `char status` da tarefa (`'A'`, `'E'` ou `'C'`), imprima uma mensagem:
  - `"Tarefa ainda não iniciada"`  
  - `"Tarefa em andamento"`  
  - `"Tarefa concluída"`  
- Use `if/else if/else` para tratar os três casos.

---

## 5️⃣ Laços de Repetição (for, while)

### 📘 O que são?
Laços de repetição permitem executar um bloco de código várias vezes.

### ✏️ Exemplo com **for**

```java
for (int i = 0; i < 5; i++) {
    System.out.println("Contagem: " + i);
}
```

### ✏️ Exemplo com **while**

```java
int i = 0;
while (i < 5) {
    System.out.println("i = " + i);
    i++;
}
```

### 🏋️ Exercícios

1. Imprima todos os números de **1 a 100**.  
2. Imprima apenas os números **pares** de 1 a 50.  
3. Some todos os números de 1 a 100.  
4. Faça um contador regressivo de 10 a 0.

### 🧩 TaskManager — Aplicando este capítulo

- Simule várias tarefas usando contadores:
  - Use um `for` para imprimir `"Tarefa X"` de 1 a 5.  
- Crie uma variável `int tarefasPendentes = 5;` e use um `while` para ir decrementando até 0, imprimindo `"Restam N tarefas pendentes"`.

---

## 6️⃣ Métodos (Funções)

### 📘 O que é um método?

Um método é um bloco de código reutilizável que executa uma tarefa.  
Ele pode receber parâmetros e pode retornar um valor.

### ✏️ Exemplo

```java
public class Main {

    public static void saudacao(String nome) {
        System.out.println("Olá, " + nome + "!");
    }

    public static void main(String[] args) {
        saudacao("Thalles");
    }
}
```

### 🏋️ Exercícios

1. Crie um método que recebe um número e retorna o **dobro**.  
2. Crie um método que recebe a idade e retorna se a pessoa é **maior de idade**.  
3. Crie um método que recebe dois números e retorna a **soma** deles.

### 🧩 TaskManager — Aplicando este capítulo

- Crie um método `exibirTarefa(...)` que recebe os dados de uma tarefa (título, descrição, prioridade, status) e imprime de forma formatada.  
- Crie um método `calcularProgresso(int total, int concluidas)` que retorna a porcentagem de conclusão.

---

## 7️⃣ Arrays

### 📘 O que é um array?

Um array é uma **estrutura de dados** que armazena vários valores do mesmo tipo em uma única variável.

- Tem **tamanho fixo**
- Índices começam em **0**

### ✏️ Exemplo

```java
public class Main {
    public static void main(String[] args) {
        String[] nomes = new String[3];
        nomes[0] = "Ana";
        nomes[1] = "Bruno";
        nomes[2] = "Carlos";

        for (int i = 0; i < nomes.length; i++) {
            System.out.println("Nome: " + nomes[i]);
        }
    }
}
```

### 🏋️ Exercícios

1. Crie um array de `int` com 5 posições e preencha com valores. Imprima todos.  
2. Crie um array de `double` e calcule a média.  
3. Crie um array de `String` e procure um nome específico dentro dele.

### 🧩 TaskManager — Aplicando este capítulo

- Crie um array de `String` chamado `titulos` com tamanho 5.  
- Preencha com títulos de tarefas.  
- Use um `for` para listar todas as tarefas.  
- Depois, crie arrays paralelos:
  - `String[] descricoes`  
  - `int[] prioridades`  
  - `boolean[] concluidas`  

Use o índice para relacionar os dados.

---

## 8️⃣ Collections (List, Set, Map)

### 📘 O que são Collections?

O framework Collections oferece estruturas de dados mais flexíveis que arrays:

- `List` — lista ordenada, aceita repetição  
- `Set` — conjunto sem repetição  
- `Map` — pares chave/valor

### ✏️ Exemplo com `List`

```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<String> nomes = new ArrayList<>();

        nomes.add("Ana");
        nomes.add("Bruno");
        nomes.add("Carlos");

        for (String nome : nomes) {
            System.out.println(nome);
        }
    }
}
```

### ✏️ Exemplo com `Map`

```java
import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        Map<String, String> capitais = new HashMap<>();
        capitais.put("SP", "São Paulo");
        capitais.put("RJ", "Rio de Janeiro");

        System.out.println(capitais.get("SP"));
    }
}
```

### 🏋️ Exercícios

1. Crie uma `List<String>` com nomes e imprima todos com `for-each`.  
2. Crie uma `List<Integer>` e calcule a soma dos elementos.  
3. Crie um `Map<String, String>` representando sigla do estado → nome do estado.

### 🧩 TaskManager — Aplicando este capítulo

- Troque os arrays de tarefas por uma `List<String>` para títulos de tarefas.  
- Depois, comece a pensar em uma classe `Tarefa` (que vamos criar no próximo capítulo) e troque para `List<Tarefa>`.  
- Use uma `List` para armazenar todas as tarefas ativas no sistema.

---

## 9️⃣ Orientação a Objetos

### 📘 O que é OO?

Orientação a Objetos é um paradigma que organiza o código em **classes** e **objetos**.

Conceitos principais:

- **Classe**: modelo
- **Objeto**: instância
- **Encapsulamento**: esconder detalhes internos
- **Herança**: uma classe herda características de outra
- **Polimorfismo**: múltiplas formas de um mesmo comportamento

### ✏️ Exemplo de Classe e Objeto

```java
public class Pessoa {
    String nome;
    int idade;

    void apresentar() {
        System.out.println("Olá, meu nome é " + nome + " e tenho " + idade + " anos.");
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa p = new Pessoa();
        p.nome = "Ana";
        p.idade = 25;
        p.apresentar();
    }
}
```

### 🏋️ Exercícios

1. Crie uma classe `Aluno` com `nome`, `matricula` e `nota`. Crie um método para exibir os dados.  
2. Crie uma classe `Produto` com `nome`, `preco` e um método para aplicar desconto.  
3. Crie uma hierarquia simples: `Animal` (classe base) e `Cachorro` (subclasse) com um método `falar()`.

### 🧩 TaskManager — Aplicando este capítulo

- Crie uma classe `Tarefa` com:
  - `private String titulo;`
  - `private String descricao;`
  - `private int prioridade;`
  - `private boolean concluida;`
- Adicione:
  - Construtor(es)
  - Getters e setters
  - Método `exibir()` que imprime os dados da tarefa  
- Altere o código para usar `List<Tarefa>` em vez de arrays ou `List<String>`.

---

## 🔟 Tratamento de Exceções

### 📘 O que são exceções?

Exceções são problemas que acontecem em tempo de execução.  
Você pode **tratar** essas situações usando `try`, `catch` e `finally`.

### ✏️ Exemplo

```java
public class Main {
    public static void main(String[] args) {
        try {
            int resultado = 10 / 0;
            System.out.println(resultado);
        } catch (ArithmeticException e) {
            System.out.println("Erro: divisão por zero!");
        } finally {
            System.out.println("Bloco finally sempre é executado.");
        }
    }
}
```

### 🏋️ Exercícios

1. Faça uma divisão entre dois números, tratando a exceção de divisão por zero.  
2. Tente acessar um índice inválido em um array e trate a exceção.  
3. Crie um método que lança uma exceção customizada se um valor for negativo.

### 🧩 TaskManager — Aplicando este capítulo

- Se o usuário tentar acessar uma posição inválida de tarefa (no futuro, ao escolher por índice), trate a exceção e mostre uma mensagem amigável.  
- Prepare seu código para nunca quebrar o programa por erro simples de entrada.

---

## 1️⃣1️⃣ Streams

### 📘 O que são Streams?

Streams são uma forma moderna de trabalhar com coleções em Java, permitindo operações como:

- `filter`
- `map`
- `sorted`
- `collect`

De forma declarativa e expressiva.

### ✏️ Exemplo

```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<Integer> numeros = Arrays.asList(1, 2, 3, 4, 5);

        numeros.stream()
               .filter(n -> n % 2 == 0)
               .forEach(System.out::println);
    }
}
```

### 🏋️ Exercícios

1. Use Streams para filtrar apenas números pares de uma lista.  
2. Use Streams para transformar uma lista de strings em maiúsculas.  
3. Use Streams para calcular a soma dos números de uma lista.

### 🧩 TaskManager — Aplicando este capítulo

- Com `List<Tarefa>`:
  - Liste somente as tarefas concluídas usando `stream().filter(...)`.  
  - Liste somente as tarefas com prioridade alta.  
  - Conte quantas tarefas ainda não foram concluídas.

---

## 1️⃣2️⃣ Boas práticas

### 📘 Por que boas práticas importam?

Boas práticas deixam o código:

- Mais legível  
- Mais fácil de manter  
- Mais fácil de testar e evoluir

### ✅ Algumas boas práticas em Java

- Nomes de classes: `PascalCase` (ex: `TaskManagerApp`, `Tarefa`)  
- Nomes de métodos e variáveis: `camelCase` (ex: `calcularProgresso`, `totalTarefas`)  
- Uma classe por arquivo  
- Métodos pequenos, com uma única responsabilidade  
- Evitar duplicação de código (DRY)  
- Comentários apenas quando realmente agregam

### ✏️ Exemplo ruim

```java
public class t {
    public static void m(int a, int b, int c) {
        System.out.println(a + b + c);
    }
}
```

### ✏️ Exemplo melhor

```java
public class Calculadora {
    public static int somar(int primeiroNumero, int segundoNumero, int terceiroNumero) {
        return primeiroNumero + segundoNumero + terceiroNumero;
    }
}
```

### 🏋️ Exercícios

1. Revise um código seu antigo e renomeie variáveis e métodos para nomes mais significativos.  
2. Separe métodos grandes em métodos menores com responsabilidades claras.  
3. Remova comentários desnecessários que apenas repetem o que o código já diz.

### 🧩 TaskManager — Aplicando este capítulo

- Refatore o código do `TaskManager`:
  - Crie uma classe `TaskManagerService` para concentrar a lógica de negócio.  
  - Deixe `TaskManagerApp` apenas para lidar com entrada/saída (por enquanto, mensagens no console).  
  - Organize o projeto em pacotes:
    - `br.com.seuprojeto.taskmanager.app`  
    - `br.com.seuprojeto.taskmanager.model`  
    - `br.com.seuprojeto.taskmanager.service`  

---
