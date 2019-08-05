# Afropython Conf 2019

Repositório para o site da Afropython Conf 2019

## Tecnologias

- HTML5
- CSS
- Github Pages

## Decisões Técnicas

É uma página única feita apenas com HTML5 e CSS onde se encontra as principais informações do evento.

O CSS foi dividido entre _estrutura_ e _tipografia_. Todo o css relacionado a estrutura e posicionamento do site está em `index-structure.css` já o css relacionando a tipografia, estilos e cores está em `index-typography.css`. Dessa forma, quando formos dar cores ao site, basta focar apenas em um arquivo css, sem medo de ~cagar tudo~ gerar problemas na estrutura da página.

## Mudando a aparência do site

Mudanças como cores, fontes, tamanho de fontes, espaçamento entre caracteres, estilos, etc __DEVEM SER FEITOS__ no arquivo `ndex-typography.css` para seguir o padrão escolhido.

## Adicionando Patrocinador

### CSS

- Remova o grupo de classes: `.sponsors-section .placeholder p` do arquivo [index-typography.css](css/index-structure.css)
- Remova o grupo de classes: `.sponsors-section .placeholder` do arquivo [index-structure.css](css/index-structure.css)
- Adicione o primeiro patrocinador descomentando a linha `display:flex` do grupo de classes `.sponsors-section .list .info` e excluir a linha `display:none` no aquivo [index-structure.css](css/index-structure.css):

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

## Adicionando Programação

### CSS

- Remova o grupo de classes: `.schedule-section .placeholder p` do arquivo [index-typography.css](css/index-structure.css)
- Remova o grupo de classes: `.schedule-section .placeholder` do arquivo [index-structure.css](css/index-structure.css)
- Adicione o primeiro patrocinador descomentando a linha `display:flex` do grupo de classes `.schedule-section .tables` e excluir a linha `display:none` no aquivo [index-structure.css](css/index-structure.css):

#### Antes

```css
.schedule-section .tables {
    /* display: flex; */
    display: none;
    margin-top: 40px;
    justify-content: space-between;
    flex-wrap: wrap;
    flex-flow: row wrap;
}
```

#### Depois

```css
.schedule-section .tables {
    display: flex;
    margin-top: 40px;
    justify-content: space-between;
    flex-wrap: wrap;
    flex-flow: row wrap;
}
```

### HTML

- Remova a div `<div class="placeholder">...</div>`
- Adicione um novo patrocinador replicando o seguinte trecho e código:

```html
<div class="attraction" >
    <p class="time">Horário 1</p>

    <div class="description">
        <p>Palestra Super Legal</p>
        <p>Autora muito massa</p>
    </div>
</div>
```

Onde:

- `Horário 1` é o horário da atração;
- `Palestra Super Legal` é o título da palestra;
- `Autora muita massa` é o nome da pessoa palestrante;

## Deploy

Para fazer o deploy basta mergear o pull request com a master e acessar: https://afropython.github.io/afropython-conf-2019/

## Como colaborar

- Clonando o repositório:

`https://github.com/AfroPython/afropython-conf-2019.git`

- Fazendo alterações de HTML em `index.html` e de CSS nos arquivos `index-structure.css` para mudanças em estrutura e `index-typography.css` para mudanças de estilo.
