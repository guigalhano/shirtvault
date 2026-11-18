# ShirtVault

Mapa-múndi e painel de coleções de camisas de futebol: Daniele Mureddu (663 camisas), Roberto Baigorria (5.931 camisas) e Anderson Borges (163 seleções não-FIFA e regionais).

Site: https://garrinchashirts.com/colecao (embutido) · https://guigalhano.github.io/shirtvault/

## O que tem
- **Mapa**: cada país pintado pela quantidade de camisas; clique para ver as camisas do país.
- **Painel**: totais e gráficos por continente, década, times, fornecedores, estilo, condição e tamanho.
- **Coleção**: busca, filtros, grade/tabela e ficha de cada camisa no formato do Hyfe.
- Idiomas: Português, English, Español, Italiano.

## Estrutura
- `index.html`: o app inteiro (HTML, CSS e JavaScript, sem build).
- `data/daniele.json`: coleção de Daniele Mureddu (663 camisas), da planilha `Collezione_Maglie_2026_Stats.xlsx`.
- `data/roberto.json`: coleção de Roberto Baigorria (5.931 camisas), da planilha `colección camis (Autoguardado).xlsx`. O país vem da coluna "País", que mistura países e ligas.
- `data/anderson.json`: coleção de Anderson Borges, da planilha `JERSEYS_gui.xlsx` (células verdes = camisas que ele tem; o resto é procura e ficou de fora). Cada seleção foi associada ao país onde fica, para aparecer no mapa.
- `data/countries.json`: nomes dos países em 4 idiomas e códigos ISO.
- `data/world.json`: geometria do mapa ([world-atlas](https://github.com/topojson/world-atlas), Natural Earth, domínio público).

## Rodar localmente
```bash
python3 -m http.server 8000
```
Abra http://localhost:8000.

## Publicação
GitHub Pages, branch `main`, pasta raiz, em https://guigalhano.github.io/shirtvault/.

Para mostrar dentro do site principal (garrinchashirts.com/colecao), crie uma página no construtor do site e embuta:

```html
<iframe src="https://guigalhano.github.io/shirtvault/" title="Coleção de camisas" style="width:100%;height:1400px;border:0" loading="lazy"></iframe>
```

## Páginas por país (Itália, Brasil, Argentina, Chile, Reino Unido, Espanha)
Clique no país no mapa-múndi para ver o mapa por região e o filtro por liga.
- `data/regions.json`: contornos das regiões ([Natural Earth](https://www.naturalearthdata.com/), domínio público) e a tabela time → região. Times que não estão na tabela aparecem como "região não identificada".
- As ligas vêm da coluna Serie (Daniele) ou da categoria da planilha (Roberto). Categorias genéricas, como "Italiano ascenso" e "Ascenso arg regional", ficam como divisões inferiores ou ligas regionais.
