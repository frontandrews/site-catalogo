<template>
<q-layout view="lHh Lpr lFf">

    <q-page-container class="text-justify">
        <transition
          appear
          duration-enter='1.5'
          duration-leave='2'
          enter-active-class='animated fadeIn'
          leave-active-class='animated fadeOut'
        >
          <router-view />
        </transition>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d918.8867324954912!2d-43.11999227080999!3d-22.893189299063643!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9983c3cf7d2745%3A0xf1f2950c77a3a41f!2sR.%20Luiz%20Leopoldo%20Fernandes%20Pinheiro%2C%20521%20-%20Centro%2C%20Niter%C3%B3i%20-%20RJ%2C%2024030-125!5e0!3m2!1sen!2sbr!4v1601164624876!5m2!1sen!2sbr" width="100%" height="300" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>

    </q-page-container>

    <q-footer class="absolute-bottom bg-dark q-pa-xl">
          <div class="container">
            <div class="row">
              <div class="col-6">
                <q-list>
                <q-item>
                    <q-item-section>Contato</q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section>Email: Comercial@marccomercio.com.br</q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section>Whatsapp: 21 97077-9851</q-item-section>
                  </q-item>
                </q-list>
              </div>
              <div class="col-xs-12 col-sm-12 col-md-6">
                <q-list>
                  <q-item>
                    <q-item-section>Endereço: RJ, Niterói, Centro, Rua Luís Leopoldo Fernandes Pinheiro, 521 - 2º Andar - 24030-121</q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section>Endereço: RJ, Parada de Lucas - Rua Saracá, 5 (Depósito)</q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section style="display: inline">Telefone: <a  class="link_style" target="_blank" href="+21964255128">(21) 96425-5128</a></q-item-section>
                  </q-item>
                </q-list>
              </div>
              <div class="col-xs-12 col-sm-12 col-md-6 q-pa-sm absolute-bottom" style="font-size: 10px">
                @ Todos os direitos reservados - MARC COMÉRCIO DE MATERIAIS, TECNOLOGIA E SERVIÇOS LTDA
                - Created by <a class="link_style" target="_blank" href="https://www.frontandrews.com.br">FrontAndrews</a>
              </div>
            </div>

          </div>
      </q-footer>

</q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  methods: {
    goBackHome () {
      this.$router.push('/')
    }
  }
}
</script>

<style scoped>

.link_style {
  color: white;
  text-decoration: none;
  text-transform: uppercase;
}

.link_style:hover {
  color: rgb(209, 202, 202);
  text-decoration: none;
  text-transform: uppercase;
}

.logo:hover {
  color: grey;
  cursor: pointer
}

</style>
