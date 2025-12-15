# 📦 Boxing, Unboxing e Wrapper Classes em Java

Este material explica de forma clara e prática os conceitos de **Wrapper Classes**, **Boxing** e **Unboxing** em Java, que são fundamentais para o uso de **Collections**, **Generics** e desenvolvimento **back-end**.

---

## 1️⃣ Wrapper Classes (Classes Wrapper)

Em Java, existem **tipos primitivos** e **objetos**.

### 🔹 Tipos Primitivos
```java
int, double, float, char, boolean, long, short, byte
Não são objetos

Não possuem métodos

🔹 Wrapper Classes
As wrapper classes são classes que representam os tipos primitivos como objetos.

Tipo Primitivo	Wrapper Class
int	Integer
double	Double
float	Float
char	Character
boolean	Boolean
long	Long
short	Short
byte	Byte

📌 Exemplo
java
Copiar código
int idade = 23;          // tipo primitivo
Integer idadeObj = 23;  // objeto (wrapper)
📍 Wrapper classes são necessárias porque:

Collections (List, Set, Map) não aceitam tipos primitivos

Generics trabalham apenas com objetos

Frameworks Java (Spring, Hibernate, etc.) usam objetos

2️⃣ Boxing
🔹 O que é Boxing?
Boxing é o processo de converter um tipo primitivo em um objeto wrapper.

Primitivo ➜ Objeto

🔹 Exemplo de Boxing Manual
java
Copiar código
int numero = 10;
Integer obj = Integer.valueOf(numero);
🔹 Exemplo de Autoboxing
java
Copiar código
int numero = 10;
Integer obj = numero; // Java faz o boxing automaticamente
📌 O Java executa o autoboxing sem necessidade de chamada explícita.

3️⃣ Unboxing
🔹 O que é Unboxing?
Unboxing é o processo inverso do boxing.

Objeto ➜ Primitivo

🔹 Exemplo de Unboxing Manual
java
Copiar código
Integer obj = Integer.valueOf(20);
int numero = obj.intValue();
🔹 Exemplo de Auto-unboxing
java
Copiar código
Integer obj = 20;
int numero = obj; // Java faz o unboxing automaticamente
4️⃣ Exemplo Prático com Collections
❌ Não é permitido usar tipos primitivos em Collections:

java
Copiar código
List<int> numeros = new ArrayList<>(); // ERRO
✅ Forma correta:

java
Copiar código
List<Integer> numeros = new ArrayList<>();

numeros.add(10); // autoboxing
numeros.add(20);

int soma = numeros.get(0) + numeros.get(1); // auto-unboxing
📌 O que acontece nos bastidores:

10 ➜ Boxing

numeros.get(0) ➜ Unboxing

5️⃣ Atenção: Comparação com Wrapper Classes
⚠️ Comparar objetos com == pode gerar comportamento inesperado.

🔹 Exemplo
java
Copiar código
Integer a = 100;
Integer b = 100;

System.out.println(a == b);      // true (cache)
System.out.println(a.equals(b)); // true
java
Copiar código
Integer x = 200;
Integer y = 200;

System.out.println(x == y);      // false
System.out.println(x.equals(y)); // true
📌 Regra de Ouro

Use == → para tipos primitivos

Use .equals() → para objetos (wrapper classes)

6️⃣ Resumo Geral
Conceito	Descrição
Wrapper Class	Classe que representa um tipo primitivo como objeto
Boxing	Conversão de primitivo para objeto
Autoboxing	Boxing automático
Unboxing	Conversão de objeto para primitivo
Auto-unboxing	Unboxing automático

7️⃣ Onde isso é muito usado?
Collections (List<Integer>, Map<Long, String>)

APIs Java

Spring Boot

Hibernate / JPA

Validações e conversões de dados

Integrações com banco de dados
