# 1. Injetando o botão de busca por foto

### Injete o código javascript no seu site
Usamos um script Javascript para abrir o iframe do nosso widget em seu site.
Substitua o `<TENANT_ID>` pelo tenant id fornecido para você.

```
<script 
   src="https://widget.twiggys.cc/widget.js" 
   id="tw-widget-sb" 
   async="" 
   data-tenant-id="<TENANT_ID>" 
   data-target-sel='[data-tw-target="true"]'>
</script>
```

É possível injetar o script através de um gerenciador de scripts, porém até a finalização do loading do script, o botão estará inoperante.

## Crie o botão
Após injetar o código acima na página, você precisará criar um elemento `<button></button>` com um atributo `data-tw-target="true"`. Usamos esse atributo para saber qual é o elemento que irá abrir o widget.

```
<button data-tw-target="true">Buscar por foto</button>
```

### Isso é tudo
Pronto. O widget de busca por foto já foi criado em seu ecommerce!