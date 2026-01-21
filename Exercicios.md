- Mostrar os dados do produto (nome, preço, quantidade no estoque, valor total no estoque).
- Realizar uma entrada no estoque e mostrar novamente os dados do produto
- Realizar uma saída no estoque e mostrar novamente os dados do produto

Classe: Product
- Name: String
- Price: double
- Quantity: int
--- 
+ TotalValueInStock(): double
+ AddProducts(quantity: int): void
+ RemoveProducts(quantity: int) void

```
package entities;

public class Product {
	
	public String name;
	public double price;
	public int quantity;
	
	public double totalValueInStock() {
		return price * quantity;
	}
	
	public void addProducts(int quantity) {
		this.quantity += quantity; // Acessando o atributo da classe, não o valor que chegou como parâmetro
	}
	
	public void removeProducts(int quantity) {
		this.quantity -= quantity;
	}
}
```



```
package application;

import java.util.Scanner;

import entities.Product;


public class Program {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		Product product = new Product();
		
		System.out.println("Enter product data: ");
		System.out.println("Name");
		product.name = sc.nextLine();
		
		System.out.println("Price");
		product.price = sc.nextDouble();
		
		System.out.println("Quantity in stock: ");
		product.quantity = sc.nextInt();
		
		
		System.out.println(product.name + ", " + product.price + ", " + product.quantity);
		
		sc.close();
	}
}
```




