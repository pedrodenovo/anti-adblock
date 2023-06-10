# anti-adblock
Essa é uma forma/conceito de como usar o adblock contra o próprio adblock e forçar o usuário a desativa-lo. Pode ser extremamente eficiente em site onde o usuário entra unicamente com o intuito de fazer alguma coisa e sair rapidamente do site, como pagina de download ou outros. Isso é só uma ideia e pode ser escalada e usada de outras formas.

# Conceito
O adblock bloqueia anuncios, então uma forma de burlar o adblock é colocar o conteudo da pagina como se fosse um ad. Por exemplo:

```
<!--- Aqui tem um codigo que simula um ad do google --->
<ins class="adsbygoogle adsbygoogle-noablate" data-adsbygoogle-status="done" style="!important;">
   <div id="aswift_0_host" tabindex="0" title="Advertisement" aria-label="Advertisement">
      <!--- Aqui fica o conteudo que vai ser escondido --->
      <a target="_blank" onclick="redirecionar(); this.innerHTML = 'Hold on again...';">Download</a>
   </div>
</ins>
```
Tente executar esse codigo e veja o que acontece. Mas resumindo com o adblock ligado tudo dentro da `<div>` não fica visivel a menos que o usuario deslique o adblock.

Dessa forma é possivel deixar um pequeno aviso junto ao conteudo dizendo que a conteudo não visivel e pedindo que ele desligue o adblock. Como esse que uso em meu site:

```
<div>
  <img src="..." alt="...">
   <div>
     <h5>Can't see the download button?</h5>
     <p>Disable your adblocker or switch browsers.
     Unfortunately, ads are necessary for me to sustain myself, so for now, please be a good person and help me continue providing this content 100% for free.</p>
  </div>
</div>
```

# Atenção
Apesar disso realmente funcionar, não tenho como ter certeza se ira funcionar contra todo adblock. Porem testei com o Brave e a extensão adblock de navegador e funcionou com ambos.
