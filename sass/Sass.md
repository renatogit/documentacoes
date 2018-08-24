# Sass (Udemy)

#### Indice
##### O que é e por que usar sass


### O que é e por que usar sass?

- "Linguagem de extensão CSS"
- Permite estender as capacidades nativas de CSS


### Por que usar Sass?

- Compatibilidade total com CSS nativo.
- Exelente documentação
- Possui mais capacidades que outros pré-processadores
- Aprovado pela indústria
- Grande comunidade
- Ecossistema (Compass, Bourbon, Susy etc.)


### Mixins ou Placeholders?

#### Mixin

```scss
/*DECLARAÇÃO*/

@mixin center() {
    display: block;
    margin-left: auto;
    margin-right: auto;
}

/*USO*/

.container {
    @include center();
}

.image-cover {
    @include center();
}

/*MIXIN COM PARÂMETRO*/

@mixin size($width, $height: $width) {
    $height: $width;
    $width: $width;
}

.icon(){
    @include size(30px);
}
```

#### Placeholders

```scss
%center {
    display: block;
    margin-left: auto;
    margin-right: auto;    
}

.container {
    @extend center();
}

.icon {
    @extend center();
}
```

#### É melhor usar Mixins ou Placeholders?

- Mixins 
    - Se precisar de variáveis (parãmetros)

- Placeholders
    - Se NÃO precisar de variáveis (parãmetros)


### Iniciando a biblioteca de utilitários

```scss
%u-bold { font-weight: bold; }
%u-no-bold { font-weight: normal; }
%u-italic { font-weight: italic; }
%u-no-italic { font-weight: normal; }

%u-text-align-left { text-align: left; }
%u-text-align-center { text-align: center; }
%u-text-align-right { text-align: right; }
%u-text-align-justify { text-align: justify; }

%u-underline { text-decoration: underline;}
%u-capitalize { text-decoration: line-through;}
%u-no-text-transform { text-decoration: none;}

%u-uppercase { text-transform: uppercase;}
%u-capitalize { text-transform: capitalize;}
%u-no-text-transform { text-transform: none;}

%u-position-absolute { position: absolute; }
%u-position-relative { position: relative; }
%u-position-fixed { position: fixed; }
%u-position-static { position: static; }
```