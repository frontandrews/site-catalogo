<template>
    <div class="q-pa-none bg-dark">
    <q-carousel
      animated
      v-model="slide"
    >

      <q-carousel-slide :name="1" img-src="~assets/images/carousel-2.jpg">
        <div class="absolute-center custom-caption text-center">
          <div class="text-h2 q-pa-md bg-red text-white">Marc Comércio</div>
          <div class="text-subtitle1 text-white">COMÉRCIO DE MATERIAIS, TECNOLOGIA E SERVIÇOS </div>
        </div>
      </q-carousel-slide>
    </q-carousel>
  <div class="row q-ma-md" id="catalogo">

    <q-card class="col-xs-12 col-sm-6 my-card catalog-item rounded q-pa-xs bg-dark"  v-for="(item, index) in items" :key="index">
      <a :href="item.download" target='_blank'>
      <q-img
        :src="item.img"
        :height="200"
        class="imagem-catalog"
      />

      <div class="text-h5 absolute-top text-subtitle2 text-center text-white">
         <div class="text-h6 q-pt-lg title absolute-right"><span class="q-pa-md bg-blue q-mr-md">{{ item.title }}</span></div>
        <!-- <div class="subtitle">{{ item.subtitle }}</div> -->
      </div>
        </a>
    </q-card>

  </div>

    <div class="row text-center">
      <div class="col-xs-12 col-sm-12  col-md-6 bg-dark text-white q-pa-xs q-py-md">
        <div class="text-h4 q-mb-md" style="align:center">Quem Somos</div>
        <p class="q-mx-md  text-justify subtitle">Nossa equipe é formada por profissionais experientes, com anos de vivência no mercado de comércio e distribuição de produtos, para atender nossos clientes com excelência e de maneira exclusiva.</p>
      </div>
      <div class="col-xs-12 col-sm-12  col-md-6 q-pa-xs  q-py-md bg-white">
        <div class="text-h4 q-mb-md" style="align:center">Nossos Valores</div>
       <p class="q-mx-md  text-justify subtitle"><b>Missão:</b>
Oferecer soluções em produtos com excelência, agregando valor e satisfação aos nossos Clientes, Fornecedores, Colaboradores e Comunidade.</p>
       <p class="q-mx-md  text-justify subtitle"><b>Visão:</b>
Buscar o reconhecimento nacional como parceiros valiosos para os nossos clientes, fornecedores, colaboradores e comunidade.</p>
        <p class="q-mx-md  text-justify subtitle"><b>Valores:</b> Ética, Comprometimento, Parcerias Estratégicas, Compromisso com Qualidade, Amizade e respeito.
</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      slide: 1,
      autoplay: true,
      items: [
        { title: 'Informática', subtitle: '', img: '/images/informatica.jpg', download: '/pdf/Informática.pdf' },
        { title: 'Ferramentas', subtitle: '', img: '/images/ferramentas.jpg', download: '/pdf/Ferramentas.pdf' },
        { title: 'Positivo', subtitle: '', img: '/images/positivo.png', download: '/pdf/Positivo.pdf' },
        { title: 'Vaio', subtitle: '', img: '/images/vaio.jpg', download: '/pdf/Vaio.pdf' }
      ]
    }
  },
  computed: {
    updatedSrc () {
      if (process.env.MODE === 'electron') {
        return '/' + this.src
      }
      return this.src
    }
  }
}
</script>

<style scoped>
* {
  font-family: 'Arial';
}
.catalog-item:hover {
  opacity: 0.80;
  cursor: pointer;

}

.imagem-catalog {
  height:300px;
}

.title {
  font-family: 'roboto';
  font-weight: bold;
}

* {
  font-family: 'roboto';
  font-weight: bold;
}

.subtitle {
  font-family: 'segoe ui light';
  font-weight: bold;
}
</style>
