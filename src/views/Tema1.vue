<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 1
      h1 Incidentes informáticos
    
    .row.justify-content-center.align-items-center.mb-4
      .col-md-8.order-md-1.order-2
        p Dentro del tratamiento de incidentes de seguridad digital en las aplicaciones web, parte de la normatividad la establece el Ministerio de Tecnologías de Información y las Comunicaciones de Colombia mediante la Resolución 500 del año 2021 Por la cual se establecen los lineamientos y estándares para la estrategia de seguridad digital y se adopta el modelo de seguridad y privacidad como habilitador de la política de gobierno digital”; por ello se debe recordar que al existir incidentes informáticos el Código Penal establece sanciones legales mediante la #[strong Ley 1273 de 2009].
        p.mb-0 Igualmente, hay que tener en cuenta los marcos de referencia ante un incidente de seguridad de la información guiándose con la #[strong ISO 27035] que es la norma de gestión de incidentes de seguridad de la información, el ciclo de vida de la gestión y contradicción de un incidente informático, así:
      .col-md-4.col-8.order-md-2.order-1.mb-md-0.mb-4(data-aos="fade-left")
        img(src="@/assets/curso/tema1/img01.png")

    .titulo-sexto.color-acento-contenido.my-4(data-aos="fade-right")
      h5 Figura 1
      span Ciclos incidentes informáticos
    
    .row.justify-content-center.mb-4
      .col-lg-10.BG01.p-5(data-aos="fade-right")
        img(src="@/assets/curso/tema1/img02.svg")
      .col-lg-10.BG02.p-4(data-aos="fade-right")
        p El ciclo siempre será repetitivo, el mismo puede controlarse o auditarse mediante políticas de seguridad de la información y que la organización tenga un departamento en atención frente a los diferentes incidentes de seguridad como un CSIRT como lo indica el Conpes 3701 de 2011; es necesario recordar que dentro los pilares de la información están:
        ul.lista-ul--color.ms-4
          li
            <i class="fas fa-check-circle" style="color:#F38E1E"></i>
            | Confidencialidad.
          li
            <i class="fas fa-check-circle" style="color:#F38E1E"></i>
            | Integridad.
          li
            <i class="fas fa-check-circle" style="color:#F38E1E"></i>
            p.mb-0 Disponibilidad.  

    p.mb-5 Los incidentes informáticos de seguridad en aplicaciones web pueden darse mediante técnicas de ingeniera social o #[i hacking] no autorizados, #[i malware] y SQL #[i injection], como puede verse a continuación:

    .row.justify-content-center.mb-5(data-aos="zoom-in")
      .col-md-8.BG13.p-4
        img(src="@/assets/curso/tema1/img03.svg")

    p.mb-5 Se invita a conocer algunos conceptos importantes que identificará en el transcurso de este componente:

    TabsA.color-acento-contenido.mb-5
      .tarjeta.color-acento-contenido--borde.p-4(titulo="<em>Malware]</em>")
        .row.justify-content-center
          .col-md-8.order-md-1.order-2
            h4 #[i Malware]
            p Programas maliciosos que realizan acciones dañinas en un sistema informático.
          .col-md-2.col-4.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema1/img04.png")
      .tarjeta.color-acento-contenido--borde.p-4(titulo="Ingeniería social")
        .row.justify-content-center
          .col-md-8.order-md-1.order-2
            h4 Ingeniería social
            p Técnicas usadas por organizaciones cibercriminales donde utilizan técnicas de engaño para que usuarios con desconocimiento o incautos envíen con facilidad datos confidenciales.
          .col-md-2.col-4.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema1/img05.png")
      .tarjeta.color-acento-contenido--borde.p-4(titulo="SQL <em>Injection</em>")
        .row.justify-content-center
          .col-md-8.order-md-1.order-2
            h4 SQL #[i Injection]
            p Técnicas donde se usa código fuente realizando infiltraciones.
          .col-md-2.col-4.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema1/img06.png")
      
</template>

<script>
export default {
  name: 'Tema1',
  components: {},
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
