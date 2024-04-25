# 1. Integrando o botão de busca por tamanho (Similar na medida)

## Injete o código javascript no seu site
Para incorporar a funcionalidade de busca por tamanho, insira o seguinte código JavaScript em seu site. Certifique-se de substituir `SEU_TENANT_ID` pelo tenant_id fornecido pela equipe da Twiggy.

```
<script 
   src="https://widget.twiggys.cc/widget.js" 
   id="tw-widget-sb" 
   async="" 
   data-tenant-id="SEU_TENANT_ID" 
   data-target-sel='[data-tw-target="true"]'>
</script>
```

** Não é necessário reinserir o script se já estiver presente.

## Crie o botão
Crie um elemento <button></button> conforme abaixo. Substitua `URL_DA_SUA_IMAGEM` pela URL da imagem do produto que deseja encontrar similares e `TAMANHO_SELECIONADO` pelo tamanho desejado.

```
<button 
    data-tw-image="URL_DA_SUA_IMAGEM" 
    data-tw-size="TAMANHO_SELECIONADO" 
    onclick="__TWIGGY__.widgetSizeSearch(event)">
    Buscar similar na medida
</button>
```
Você também pode implementar o botão usando a seguinte estrutura:

```
<button
    onclick="__TWIGGY__.widgetSizeSearch(event, 'URL_DA_SUA_IMAGEM', 'TAMANHO_SELECIONADO')">
    Buscar similar na medida
  </button>
```

Pronto! Com estas instruções, seus usuários poderão encontrar produtos similares com base em tamanho.