# Afropython Conf 2019

Repositório para o site da Afropython Conf 2019

## Tecnologias

- HTML5
- CSS
- Github Pages

## Decisões Técnicas

É uma página única feita apenas com HTML5 e CSS onde se encontra as principais informações do evento.

O CSS foi dividido entre _estrutura_ e _tipografia_. Todo o css relacionado a estrutura e posicionamento do site está em `index-structure.css` já o css relacionando a tipografia, estilos e cores está em `index-typography.css`. Dessa forma, quando formos dar cores ao site, basta focar apenas em um arquivo css, sem medo de ~cagar tudo~ gerar problemas na estrutura da página.

## Adicionando Patrocinador

### CSS

- Remova o grupo de classes: `.sponsors-section .placeholder p` do arquivo [index-typography.css](css/index-structure.css)
- Remova o grupo de classes: `.sponsors-section .placeholder` do arquivo [index-structure.css](css/index-structure.css)
- Adicione o primeiro patrocinador descomentando a linha `display:flex` do grupo de classes `.sponsors-section .list .info` e excluir a linha `display:none` do aquivo [index-structure.css](css/index-structure.css):

#### Antes

```css
.sponsors-section .list .info {
     /* display: flex; */
    display: none;
    flex-direction: column;
    width: 33%;
    text-align: center;
}
```

#### Depois

```css
.sponsors-section .list .info {
    display: flex;
    flex-direction: column;
    width: 33%;
    text-align: center;
```

### HTML

- Remova a div `<div class="placeholder">...</div>`
- Adicione um novo patrocinador replicando o seguinte trecho e código:

```html
<div class="info">
    <img src="img/default.png">
    <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras semper diam vel pulvinar ultrices.
    </p>
</div>
```

Onde:

- `"img/default.png"` deve substituído pelo nome da imagem que contém o logo do patrocinador (previamente colocado na pasta `img`)
- `Lorem ipsum dolor sit amet...` é uma breve bio/descrição/slogan do patrocinador;

*_OBS.:_* é importante que a `<div class="info">...</div>` esteja dentro da `<div class="list">...</div>` ~~se não vai cagar o css tudo~~ não vai funcionar.

## Como colaborar

- Clonando o repositório:

`https://github.com/AfroPython/afropython-conf-2019.git`

- Fazendo alterações de HTML em `index.html` e de CSS nos arquivos `index-structure.css` para mudanças em estrutura e `index-typography.css` para mudanças de estilo.
