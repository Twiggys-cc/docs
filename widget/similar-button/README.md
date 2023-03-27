# 1. Injetando o botão de busca por similares

## Injete o código javascript no seu site
Usamos um script Javascript para abrir o iframe do nosso widget em seu site.
Substitua o `<TENTANT_ID>` pelo tenant id forcedo para você.

```
<script 
   src="https://widget.twiggys.cc/widget.js" 
   id="tw-widget-sb" 
   async="" 
   data-tenant-id="<TENTANT_ID>" 
   data-target-sel='[data-tw-target="true"]'>
</script>
```

É possível injetar o script através de um gerenciador de scripts, porém até a finalização do loading do script, o botão irá estar inoperante.

## Crie o botão
Após injetar o código acima na página, você precisara criar um elemento `<button></button>` que irá disparar um evento para nosso widget com a URL da foto a ser usada como parâmetro de pesquisa.</br>
Substitua o `URL_DA_SUA_IMAGEM` dentro do `data-tw-image` pela URL da imagem mostrada ao usuário.
O clique irá dispoarar um evento que será recebido pelo nosso widget.

```
<button data-tw-image="URL_DA_SUA_IMAGEM" onclick="__TWIGGY__.widgetSearchByUrl(event)">
    Buscar similares
</button>
```
Você também pode implementar o botão no formato abaixo:
```
<button onclick="__TWIGGY__.widgetSearchByUrl(event, 'URL_DA_SUA_IMAGEM')">
    Similares
</button>
```

## Formatos aceitos
Nosso widget de busca por similares aceita as fotos em formato: .gif, .jpeg ou .webp.

## Confira o exemplo
[Codepen](https://codepen.io/AustinFelipe/pen/mdGpqbj)