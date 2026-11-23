# Validade dos alimentos

Aplicação web que registra produtos e organiza os prazos de validade. Os dados são guardados no navegador. Para usar o sistema, informe o nome e a validade de cada produto.

## Executar

Extraia o ZIP e abra `index.html` no navegador. Se o navegador impedir a persistência ao abrir arquivos locais, abra um terminal na pasta do projeto e execute:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

No Windows, use `py -m http.server 8000 --bind 127.0.0.1` se o comando `python3` não estiver disponível. Em seguida, abra http://127.0.0.1:8000 no navegador. A aplicação usa apenas HTML, CSS e JavaScript e dispensa instalação de bibliotecas.

## Regras

- A lista é ordenada pela data de validade e, em caso de empate, pelo nome.
- Uma data anterior à data local do dispositivo aparece como vencida.
- O dia da validade aparece como vence hoje. De um a três dias, a lista informa quantos dias faltam.
- Acima de três dias, o produto aparece como dentro do prazo.
- O histórico fica restrito ao navegador e ao endereço usados. Limpar os dados do site elimina o histórico.

## Demonstração

Cadastre quatro produtos fictícios com validade ontem, hoje, daqui a três dias e daqui a quatro dias. Adicione-os fora de ordem para observar a ordenação. Recarregue a página, confira que os produtos continuam na lista e remova um deles.
