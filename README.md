# Devtalks Testes de Integração

## Introdução

Mesmo em um software bem arquitetado, testando duas unidades que interagem entre si separadamente, e concluindo que ambas estão funcionando como esperado. Ainda assim, é possível que as duas unidades não funcionem bem em conjunto. Com isso, o principal objetivo dos testes de integração é garantir que duas ou mais unidades funcionem juntas.

- Testa grupos de unidades integradas para criar um sistema ou um subsistema;
- Geralmente são os testes mais lentos, pois possuem uma quantidade maior de componentes sendo testados de uma só vez, onde muitas vezes há persistência de dados e comunicação assíncrona;
- Os testes se concentram nas interfaces de comunicação entre unidades;

![Integration vs Unit Test](./.github/integration_vs_unit_test.gif)

## Feature que foi testada

- Endpoint para listar as postagens vindas da API [JSON Placeholder](https://jsonplaceholder.typicode.com/), expor as postagens em "/posts".

## Como foi testada a feature/componente RemoteFetchPosts

- 1ª - Mockando o módulo axios;
- 2ª - Mockando o componente de HttpClient (Injeção de dependência);
- 3ª - Interceptando as requisições HTTP utilizando Nock;

## Como o projeto foi desenvolvido

- Entities: responsável por concentrar os principais participantes das regras de negócio;
  - Objetos de negócio;
  - Aplicam regras que geralmente fazem parte apenas da entidade;
- Use Cases: realizam a orquestração das Entities na concepção das regras de negócio;
  - Representa as regras de negócio;
  - Lançam exceções de negócio;
- Adapters, Controllers, Presenters, Gateways, etc: fazem a tradução entre o mundo externo e as regras de negócio;
  - Fazem o intercâmbio de dados entre a base de dados, interface gráfica, aplicativo e/ou outros serviços utilizados pela aplicação;
- Devices, Web, UI, DB...:
  - Frameworks ou outras estruturas externas com fazem I/O com a aplicação;

![Clean Architecture Cone](./.github/clean_architecture_cone.jpg)

## Referências

- <https://homepages.dcc.ufmg.br/~figueiredo/disciplinas/aulas/testes-de-release_v01.pdf>
- <https://teses.usp.br/teses/disponiveis/55/55134/tde-01082017-155344/publico/MariaAdelinaSilvaBrito_revisada.pdf>
- <https://dev.to/joaosczip/clean-architecture-a-little-introduction-4ag6>
- <https://dev.to/pereiren/clean-architecture-series-part-3-2795>

----------
By [Victor B. Fiamoncini](https://github.com/Victor-Fiamoncini) ☕️
