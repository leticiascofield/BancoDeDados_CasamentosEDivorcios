# Dados de Casamentos, Divorcios e relacionados

## Introdução
 Este projeto de banco de dados visa analisar e explorar dados relacionados a Divórcios, Casamentos, População e Índice de Desenvolvimento Humano (IDH) por estado no Brasil. Os dados foram obtidos de fontes confiáveis, como o Instituto Brasileiro de Geografia e Estatística (IBGE), o Programa das Nações Unidas para o Desenvolvimento (Pnud Brasil), o Instituto de Pesquisa Econômica Aplicada (Ipea) e a Fundação João Pinheiro (FJP).

## Fontes de Dados
 As fontes de dados escolhidas para este projeto incluem:
- **Divórcios e Casamentos:** Dados do IBGE, coletados em 18/06/2023, referentes ao ano de 2021.
- **População:** Prévia do censo 2022 do IBGE.
- **IDH:** Dados de 2021 fornecidos pelo Pnud Brasil, Ipea e FJP.

## Estrutura do Banco de Dados
 O banco de dados foi modelado utilizando PostgreSQL e consiste em cinco tabelas principais:

1. **Casamento:**
    - **idC (Chave Primária):** Identificador único para cada entrada de dados de casamento.
    - **SiglaEstado:** Sigla do estado onde o casamento ocorreu.
    - **Total:** Número total de casamentos no estado.

2. **Estado:**
    - **SiglaEstado (Chave Primária):** Sigla do estado.
    - **NomeEstado:** Nome completo do estado.
    - **Regiao:** Região do país a que o estado pertence.
    - **Populacao:** População do estado.
    - **IDH:** Índice de Desenvolvimento Humano do estado.

3. **FamiliaDivorciada:**
    - **idTF (Chave Primária):** Identificador único para cada entrada de dados de família divorciada.
    - **SiglaEstado:** Sigla do estado em que a família se divorciou.
    - **SemFilhos:** Número de famílias sem filhos.
    - **SomenteComFilhosMaioresDeIdade:** Número de famílias com filhos maiores de idade.
    - **SomenteComFilhosMenoresDeIdade:** Número de famílias com filhos menores de idade.
    - **ComFilhosMaioresEMenoresDeIdade:** Número de famílias com filhos de ambas as idades.
    - **SemDeclaracao:** Número de famílias sem informação sobre filhos.
    - **TotalFilhos:** Número total de filhos nas famílias divorciadas.

4. **GuardaDivorcio:**
    - **idRGF (Chave Primária):** Identificador único para cada entrada de dados de guarda de divórcio.
    - **SiglaEstado:** Sigla do estado onde a guarda de divórcio foi estabelecida.
    - **Marido:** Número de casos em que o marido ficou responsável pela guarda.
    - **Mulher:** Número de casos em que a mulher ficou responsável pela guarda.
    - **AmbosConjuges:** Número de casos em que ambos os cônjuges compartilham a guarda.
    - **Outro:** Número de casos em que outra parte ficou responsável pela guarda.
    - **SemDeclaracao:** Número de casos em que não há declaração sobre a guarda.

5. **TipoDivorcio:**
    - **idTD (Chave Primária):** Identificador único para cada tipo de divórcio.
    - **SiglaEstado:** Sigla do estado onde o divórcio ocorreu.
    - **Total:** Número total de divórcios no estado.
    - **Consensual:** Número de divórcios consensuais.
    - **NaoConsensual:** Número de divórcios não consensuais.
    - **ComunhaoUniversal:** Número de divórcios com comunhão universal de bens.
    - **ComunhaoParcial:** Número de divórcios com comunhão parcial de bens.
    - **Separacao:** Número de divórcios por separação.
    - **SemDeclaracao:** Número de divórcios sem declaração sobre o tipo.

## Dependências e Restrições
 O banco de dados inclui chaves primárias em todas as tabelas para garantir unicidade nas entradas. Além disso, foram estabelecidas restrições de chave estrangeira (FK) para manter a integridade referencial entre as tabelas "Casamento," "FamiliaDivorciada," "GuardaDivorcio," e "TipoDivorcio" com a tabela "Estado."

## Utilização do Código SQL
 O código SQL fornecido no dump pode ser utilizado para criar o banco de dados e suas tabelas. As consultas SQL podem ser elaboradas para explorar os dados e extrair informações relevantes.

