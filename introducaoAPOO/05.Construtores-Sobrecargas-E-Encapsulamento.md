🔐 Construtores, Sobrecarga e Encapsulamento
📌 Construtores

São métodos especiais usados para inicializar objetos.

public Pessoa(String nome, int idade) {
    this.nome = nome;
    this.idade = idade;
}

📌 Sobrecarga

Ocorre quando existem vários métodos ou construtores com o mesmo nome, mas parâmetros diferentes.

public Pessoa() {}

public Pessoa(String nome) {
    this.nome = nome;
}

📌 Encapsulamento

Consiste em proteger os atributos e permitir acesso controlado por métodos.

private String nome;

public String getNome() {
    return nome;
}

public void setNome(String nome) {
    this.nome = nome;
}


Benefícios:

Segurança

Organização

Manutenção facilitada

📦 Estruturas de Dados: Arrays e Coleções
📌 Arrays

Estrutura de tamanho fixo.

int[] numeros = {1, 2, 3, 4};
System.out.println(numeros[0]);

Percorrendo um array
for (int n : numeros) {
    System.out.println(n);
}

📌 Coleções (Collections)

Mais flexíveis que arrays.

ArrayList
ArrayList<String> nomes = new ArrayList<>();
nomes.add("Ana");
nomes.add("João");

Percorrendo uma lista
for (String nome : nomes) {
    System.out.println(nome);
}


Vantagens:

Tamanho dinâmico

Métodos prontos

Melhor para aplicações reais
