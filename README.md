# AveDex

A AveDex é um catálogo interativo de aves desenvolvido na disciplina de **Boas Práticas de Programação**.

O sistema permite consultar informações sobre aves cadastradas em um dataset JSON, realizar buscas, visualizar detalhes, comparar aves e consultar fontes relacionadas aos dados.

## Funcionalidades

* Listagem das aves cadastradas.
* Busca por nome popular.
* Busca por nome científico.
* Busca por família.
* Busca por ordem.
* Busca por tipo de dieta.
* Busca ignorando acentos.
* Exibição de detalhes de uma ave por ID.
* Comparação entre duas aves.
* Exibição de informações de conservação.
* Exibição de habitat, alimentação e curiosidades.
* Consulta de créditos e fontes.
* Carregamento dos dados a partir de arquivo JSON.
* Tratamento de entradas inválidas.
* Verificação do ambiente e das dependências opcionais.
* Validação defensiva dos dados do dataset.

## Como executar

Na raiz do projeto, execute:

```bash
python main.py
```

O programa será iniciado no terminal e apresentará o menu principal da AveDex.

## Instalação das dependências opcionais

Para instalar as dependências opcionais utilizadas pelo projeto, execute:

```bash
pip install -r requirements.txt
```

As bibliotecas opcionais são utilizadas para possíveis funcionalidades relacionadas a imagens e sons:

* `requests`: download de imagens e sons.
* `pygame`: reprodução de sons.
* `term_image`: exibição de imagens no terminal.

## Estrutura do projeto

```text
AveDex/
│
├── main.py
│
├── data/
│   └── avedex_dataset_midias.json
│
├── src/
│   └── avedex/
│       ├── app.py
│       ├── ambiente.py
│       ├── catalogo.py
│       ├── comparacao.py
│       ├── creditos.py
│       ├── dados.py
│       ├── interface.py
│       └── utils.py
│
├── docs/
│   └── testes_manuais.md
│
├── requirements.txt
└── README.md
```

### Principais arquivos

* `main.py`: ponto de entrada do programa.
* `src/avedex/app.py`: controla o fluxo principal e o menu.
* `src/avedex/interface.py`: exibe a abertura e o menu principal.
* `src/avedex/catalogo.py`: realiza a listagem, busca e exibição dos detalhes das aves.
* `src/avedex/comparacao.py`: realiza a comparação entre duas aves.
* `src/avedex/creditos.py`: exibe informações do projeto e suas fontes.
* `src/avedex/dados.py`: carrega o dataset JSON.
* `src/avedex/ambiente.py`: verifica as bibliotecas opcionais instaladas.
* `src/avedex/utils.py`: reúne funções auxiliares de formatação, mensagens e normalização de texto.
* `data/avedex_dataset_midias.json`: contém os dados das aves.
* `docs/testes_manuais.md`: documentação dos testes manuais.
* `requirements.txt`: lista as dependências opcionais do projeto.

## Dataset

Os dados utilizados pela AveDex estão armazenados em:

```text
data/avedex_dataset_midias.json
```

O dataset contém informações como:

* ID;
* nome popular;
* nome científico;
* ordem;
* família;
* dieta;
* comprimento;
* peso;
* status de conservação;
* índice de conservação;
* descrição;
* habitat;
* alimentação;
* curiosidade;
* informações de mídia.

Atualmente, o dataset contém **3 aves cadastradas**.

## Testes manuais

Foram realizados testes manuais das principais funcionalidades do sistema.

### Menu e navegação

* [x] Execução com `python main.py`
* [x] Exibição da abertura do sistema
* [x] Exibição do menu principal
* [x] Listagem das aves
* [x] Seleção de ave por ID existente
* [x] Seleção de ave por ID inexistente
* [x] Tratamento de opção inválida
* [x] Encerramento do programa

### Busca

* [x] Busca por parte do nome popular
* [x] Busca ignorando acentos
* [x] Busca por família
* [x] Busca por ordem
* [x] Busca por dieta
* [x] Busca sem resultados
* [x] Busca com entrada vazia
* [x] Tentativa de abrir ID fora dos resultados

### Detalhes das aves

* [x] Exibição dos detalhes por ID
* [x] Exibição do nome científico
* [x] Exibição de família e ordem
* [x] Exibição da dieta
* [x] Exibição de comprimento e peso
* [x] Exibição do status de conservação
* [x] Exibição do índice de conservação
* [x] Exibição do habitat
* [x] Exibição da alimentação
* [x] Exibição da curiosidade

### Comparação

* [x] Comparação entre duas aves existentes
* [x] Comparação exibindo família, dieta e habitat
* [x] Comparação exibindo peso e comprimento
* [x] Comparação exibindo status e índice de conservação
* [x] Tratamento de ID inexistente na comparação
* [x] Comparação da mesma ave com ela mesma

### Créditos e fontes

* [x] Exibição dos créditos do projeto
* [x] Exibição das fontes globais cadastradas no dataset

## Testes defensivos

Foram realizados testes para verificar o comportamento do programa diante de situações inválidas ou problemas nos dados:

* [x] JSON carregado corretamente
* [x] Arquivo JSON ausente
* [x] JSON mal formatado
* [x] Campo obrigatório ausente
* [x] ID duplicado
* [x] Campo numérico inválido
* [x] Entrada inválida no ID
* [x] Verificação das bibliotecas do ambiente

## Testes de regressão

Após as alterações no projeto, as principais funcionalidades foram testadas novamente para garantir que continuavam funcionando corretamente:

* [x] Listar aves
* [x] Buscar por parte do nome
* [x] Buscar por família
* [x] Buscar por ordem
* [x] Buscar por dieta
* [x] Ver detalhes por ID
* [x] Comparar duas aves
* [x] Tratar ID inexistente
* [x] Tratar opção inválida no menu
* [x] Encerrar o programa

## Fontes

As fontes utilizadas como referência para o dataset incluem:

* Guia de Aves Funed
* WikiAves
* IUCN Red List

As informações e URLs das fontes globais estão cadastradas no dataset da AveDex.

## Autor

**Luiz Henrique da Silva**

