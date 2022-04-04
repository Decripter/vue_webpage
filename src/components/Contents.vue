<template>

<div class="column is-7">
    <div class="pt-3 pl-4 block " >
        Mussum Ipsum, cacilds vidis litro abertis. Interagi no mé, cursus quis, vehicula ac nisi.Delegadis gente finis, bibendum egestas augue arcu ut est. Pra lá , depois divoltis porris, paradis.Quem num gosta di mé, boa gentis num é.
A ordem dos tratores não altera o pão duris.Si num tem leite então bota uma pinga aí cumpadi!Atirei o pau no gatis, per gatis num morreus.Todo mundo vê os porris que eu tomo, mas ninguém vê os tombis que eu levo!
     
</div>
</div>
<div class="tile is-ancestor pl-5 pr-5" style="transition: background-color 500ms ease-out 50ms;">
  <BoxContent :themeIsDark="[themeDark[0] ? true : false]" content="Não sou faixa preta cumpadi, sou preto inteiris, inteiris. Suco de cevadiss, é um leite divinis, qui tem lupuliz, matis, aguis e fermentis. Aenean aliquam molestie leo, vitae iaculis nisl.Cevadis im ampola pa arma uma pindureta."/>
  <BoxContent :themeIsDark="[themeDark[0] ? true : false]" content="Não sou faixa preta cumpadi, sou preto inteiris, inteiris. Suco de cevadiss, é um leite divinis, qui tem lupuliz, matis, aguis e fermentis. Aenean aliquam molestie leo, vitae iaculis nisl.Cevadis im ampola pa arma uma pindureta."/>
</div>

</template>

<script>
import BoxContent from '@/components/BoxContent.vue'

export default {
    name: 'contents',
    props:['themeDark'],
    components: {
    BoxContent

  },
    data(){
        return{
            
        }
    },
    
}
</script>