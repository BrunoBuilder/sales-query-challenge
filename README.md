<p align="center">
  <a href="https://devsuperior.com.br">
    <img src="https://github.com/BrunoBuilder/customer_crud_challenge/assets/84381502/6b8cb2ad-5e4b-450b-a788-cd6c2d43a3c3" alt="DevSuperior Logo">
  </a>
</p>

<h1 align="center">Formação Desenvolvedor Moderno</h1>

<h2 align="center">Módulo: Back End</h2>

<h3 align="center">Capítulo: JPA, consultas SQL e JPQL</h3>

### DESAFIO: Consulta vendas

Forma de entrega: link do projeto no seu Github
Você deverá forkar o projeto abaixo e implementar as consultas como se pede a seguir.
[Projeto a ser forkado](https://github.com/devsuperior/desafio-consulta-vendas)

## (ATENÇÃO: não é para enviar pull request!)

Trata-se de um sistema de vendas (Sale) e vendedores (Seller). Cada venda está para um vendedor, e um
vendedor pode ter várias vendas.

<p align="center">
  <img src="https://github.com/BrunoBuilder/sales-query-challenge/assets/84381502/d1845256-8476-45ba-880f-5ca43859e78e" alt="Client Entity">
</p>

Você deverá implementar as seguintes consultas (ambas deverão estar corretas):

### Relatório de vendas
1. [IN] O usuário informa, opcionalmente, data inicial, data final e um trecho do nome do vendedor.
2. [OUT] O sistema informa uma listagem paginada contendo id, data, quantia vendida e nome do
vendedor, das vendas que se enquadrem nos dados informados.

Informações complementares:
- Se a data final não for informada, considerar a data atual do sistema. Para instanciar a data atual,
utilize o comando:

    LocalDate today = LocalDate.ofInstant(Instant.now(), ZoneId.systemDefault());

- Se a data inicial não for informada, considerar a data de 1 ano antes da data final. Para instanciar
uma data com um ano a menos, use a função minusYears:

    LocalDate result = minhaData.minusYears(1L);

- Se o nome não for informado, considerar o texto vazio.
  
- Dica: receba todos os dados como String no controller, e faça os tratamentos das datas acima,
instanciando os objetos LocalDate, no service.

Sumário de vendas por vendedor

1. [IN] O usuário informa, opcionalmente, data inicial, data final.
2. [OUT] O sistema informa uma listagem contendo nome do vendedor e soma de vendas deste vendedor
no período informado.

Informações complementares:
    
 - As mesmas do caso de uso Relatório de vendas
