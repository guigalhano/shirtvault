# ShirtVault

Mapa-múndi e painel da coleção de camisas de futebol de Daniele Mureddu (663 camisas, 156 países).

Site: https://garrinchashirts.com/colecao (embutido) · https://guigalhano.github.io/shirtvault/

## O que tem
- **Mapa**: cada país pintado pela quantidade de camisas; clique para ver as camisas do país.
- **Painel**: totais e gráficos por continente, década, times, fornecedores, estilo, condição e tamanho.
- **Coleção**: busca, filtros, grade/tabela e ficha de cada camisa no formato do Hyfe.
- Idiomas: Português, English, Español, Italiano.

## Estrutura
- `index.html`: o app inteiro (HTML, CSS e JavaScript, sem build).
- `data/daniele.json`: a coleção, convertida da planilha `Collezione_Maglie_2026_Stats.xlsx`.
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
