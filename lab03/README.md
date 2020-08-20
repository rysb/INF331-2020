# INF331-2020

**Rodrigo Yokoo Siqueira Bueno**

# Orquestração e Coreografia

# Lab03 - Model-View-Controller

## Tarefa 1

![Diagrama de Orquestração](images/tarefa1.png)

## Tarefa 2
![Diagrama de Coreografia](images/tarefa2.png)
1. O componente Cliente posta uma mensagem com o tópico *cotar/#* (por exemplo, cotar/liquidificador);
2. O componente Leilão assina o tópico *cotar* e publica uma mensagem com o tópico *leiloar*;
3. Os componentes do tipo Fornecedor assinam o tópico *leiloar* e publicam mensagens com o tópico *preço*;
4. O componente Agregador assina o tópico *preço* e publica uma mensagem com o tópico *agregado*;
5. Os componentes do tipo Cliente assinam o tópico *agregado* e apresentam os melhores preços para os clientes.


## Tarefa 3

> ![tela 1](images/tela1.png)
> ![tela 2](images/tela2.png)
> ![tela 3](images/tela3.png)
> ![tela 4](images/tela4.png) 
![blocks](images/blocks.png)
[Link para o arquivo do aplicativo](app/Tarefa_3.aia)
