# 🚀 Contador com Exceção Personalizada

![Java](https://img.shields.io/badge/Java-17+-blue)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📖 Sobre o Projeto

O **Contador com Exceção Personalizada** é uma aplicação desenvolvida em Java com finalidade educacional. O objetivo é demonstrar, de forma prática, conceitos fundamentais da linguagem, como:

- Validação de regras de negócio
- Criação de exceções personalizadas
- Uso de `throw`, `throws` e `try/catch`
- Estruturas de repetição (`for`)
- Entrada de dados com `Scanner`

O sistema solicita dois números inteiros ao usuário e realiza uma contagem baseada na diferença entre eles. Caso o primeiro número seja maior que o segundo, o programa lança uma exceção personalizada chamada `ParametrosInvalidosException`.

---

## 🧠 Regra de Negócio

- O segundo número deve ser maior que o primeiro.
- Se essa regra for violada, o sistema lança a exceção `ParametrosInvalidosException`.
- Se os valores forem válidos, o programa imprime a sequência correspondente à diferença entre os dois números.

---

## 🏗️ Estrutura do Projeto

Contador/
│
├── Contador.java
└── ParametrosInvalidosException.java


---

## ⚙️ Tecnologias e Conceitos Utilizados

- Java 17+
- Programação Orientada a Objetos (POO)
- Exceções Checked (`extends Exception`)
- Tratamento estruturado de erros
- Encapsulamento de regra de validação
- Controle de fluxo com `for`

---

## 📌 Implementação Técnica

### 🔹 Exceção Personalizada

```java
public class ParametrosInvalidosException extends Exception {

    public ParametrosInvalidosException(String mensagem) {
        super(mensagem);
    }
}
```

### Lançamento da Exceção
```java
static void contar(int parametroUm, int parametroDois)
        throws ParametrosInvalidosException {

    if (parametroUm > parametroDois) {
        throw new ParametrosInvalidosException(
            "O segundo parâmetro deve ser maior que o primeiro"
        );
    }

    int contagem = parametroDois - parametroUm;

    for (int i = 1; i <= contagem; i++) {
        System.out.println("Imprimindo o número " + i);
    }
}
```
### Compilar
javac Contador.java ParametrosInvalidosException.java
### Executar
java Contador

## Exemplo de Execução

### Entrada válida
Primeiro número: 3
Segundo número: 7

Saída:

Imprimindo o número 1
Imprimindo o número 2
Imprimindo o número 3
Imprimindo o número 4

### Entrada Inválida
Primeiro número: 10
Segundo número: 5

Saída:

Erro: O segundo parâmetro deve ser maior que o primeiro


## 👨‍💻 Autor

Matheus Rodrigues da Silva