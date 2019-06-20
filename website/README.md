O site Libra Developer Docs foi criado com [Docusaurus](https://docusaurus.io/).
FontAwesome  ícones foram usados sob o
[Creative Commons Attribution 4.0 International](https://fontawesome.com/license).

## Construção

Você Precisa [Node](https://nodejs.org/en/) >= 8.x and
[Yarn](https://yarnpkg.com/en/) >= 1.5 para rodar o site da libra.

Mude para o diretorio `website` da raiz do projeto e inicie o servidor:
```bash
cd website
yarn start
```

Abra http://localhost:3000 (se não abrir automaticamente).

Sempre que você alterar o conteúdo da página, a página deverá ser atualizada automaticamente.

Observe que o acima não recria a referência da API (gerada automaticamente por
Rustdoc e Protogen). Para gerar essas páginas, você pode executar o seguinte:
```bash
./scripts/build_docs.sh
```


#### Gerando uma construção estática
Para gerar uma compilação estática do site no diretório `website / build`, execute
```bash
./scripts/build_docs.sh -b
```

#### Implementando para testes mais amplos

```bash
zip libra.zip -r website/build
scp -r website/build/ user@server:/path
```

no servidor:
```bash
unzip libra.zip
```

## Publicação

O site está hospedado nas páginas do GitHub, através do ramo `gh-pages` do `website'
[GitHub repo](https://github.com/libra/website).


O site é construído e publicado automaticamente a partir do CircleCI - veja o
[config file](https://github.com/libra/website/blob/master/.circleci/config.yml)
para detalhes.
