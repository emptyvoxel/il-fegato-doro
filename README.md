# Premiação Fígado de Ouro
O Prêmio Fígado de Ouro de Alcoolismo Artístico é uma parceria entre o CABio-SPHN e Angela Hair, sempre uma mudança radical. 

## "Instalação"

Para calcular o Fígado de Ouro, primeiro tu precisa instalar uma porrada de coisas:
* O [Python](https://www.python.org/), caso tu ainda não o tenha.
* Uma vez que o Python estiver instalado, tu precisa instalar uns pacotes aí só usar: `pip install jupyterlab pandas matplotlib numpy`

Tu clona esse repositório (só baixar o arquivo `il fegato d'oro.ipynb`) e executar o jupyter lab na pasta onde tu baixou essa parada. Pra isso, é só abrir o cmd (na barra do Windows Explorer, já que tu provavelmente está usando Windows, tu digita `cmd` e ele já vai abrir um terminal na pasta onde tu está). No cmd, tu digita `jupyter-lab .`. Isso vai abrir teu navegador. Tu clica no arquivo do fígado e pronto, já pode brincar.

## Como usar
Pra calcular as paradas, tu precisa ter o extrato do Cora na mesma pasta do fígado (ou seja, só a gestão consegue fazer essa brincadeira). Com o extrato, tu inicializa ele em uma variável:
```python
extrato = inicializar_extrato('extrato.csv', 100)
```

O `100` ali na função é o limite de quanto tu considera. Um acima de R$100 vai ser desconsiderado, pois é improvável que seja uma pessoa comprando 30 por 100. Tu pode alterar esse limite.

Depois de inicializar o extrato, tu pode calcular o Top X usando 
```python
alcoolismo_global(extrato)[0:X]
```
substituindo X pelo top que tu quer (top 10, top 20, top 3.1415 etc.).

Uma vez com o nome do campeão, tu pode plotar o consumo semanal do querido usando 
```python
plotar_alcoolismo_semanal(extrato, 'NOME DA PESSOA')
```
substituindo `NOME DA PESSOA` pelo NOME DA PESSOA (meio óbvio isso, na real).

## Contribuir?
Se por algum motivo tu quiser implementar novas funções e novas estatísticas, sinta-se livre para clonar esse repositório e fazer sugestões. Não que alguém seja nerdola o suficiente para fazer isso, mas vai que.
