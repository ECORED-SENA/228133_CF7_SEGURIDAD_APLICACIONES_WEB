<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 4
      h1 Informes incidentes de seguridad en aplicaciones
    
    p Antes de iniciar este tema, es importante observar el siguiente video explicativo:

    figure.mb-4(data-aos="zoom-in")
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/Fnu6k-qrlGg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)

    .row.justify-content-star.align-items-center.mb-4
      .col-md-7.order-md-1.order-2
        .cajon-b.color-acento-botones.p-3
          p Los informes se deben presentar claros, concisos y ordenados, los mismos deben ser exhaustivos respecto de las técnicas forenses utilizadas con conclusiones lógicas, bien argumentadas y en un lenguaje técnico, legal y explicativo para los demás.
          p.mb-0 #[strong Lo anterior mediante el ASVS], que es un marco de referencia de requisitos de seguridad, controles funcionales y los no funcionales que se requieren al diseñar, desplegar y testear aplicaciones web. Así como con el OWASP top 10 que es el documento principal para tener en cuenta sobre los riesgos de seguridad más destacados en aplicaciones web, como se indica en la tabla a continuación:
      .col-md-5.col-10.order-md-2.order-2.mb-md-0.mb-4(data-aos="fade-left")
        img(src="@/assets/curso/tema4/img01.png")

    .titulo-sexto.color-acento-contenido.my-4
      h5 Figura 3
      span Metodología de clasificación de riesgo

    .tabla-a.color-acento-botones.mb-5
      table(data-aos="zoom-in")
        thead
          tr
            th(style="background-color: #FFF4D6;").text-center Agente de amenaza
            th(style="background-color: #FFF4D6;").text-center Explotabilidad
            th(style="background-color: #FFF4D6;").text-center Prevalencia de vulnerabilidad
            th(style="background-color: #FFF4D6;").text-center Detección de vulnerabilidad
            th(style="background-color: #FFF4D6;").text-center Impacto Técnico
            th(style="background-color: #FFF4D6;").text-center Impacto de Negocio
        tbody
          tr
            th(td rowspan="3") Específico de la aplicación.
            td(style="background-color: #E5FFF7;") 3 Fácil.
            td(style="background-color: #E5FFF7;") 3 Difundido.
            td(style="background-color: #E5FFF7;") 3 Fácil.
            td(style="background-color: #E5FFF7;") 3 Severo.
            th(td rowspan="3") Específico del negocio.
          tr
            td(style="background-color: #FFFAEF;") 2 Promedio.
            td(style="background-color: #FFFAEF;") 2 Común.
            td(style="background-color: #FFFAEF;") 2 Promedio.
            td(style="background-color: #FFFAEF;") 2 Moderado.
          tr
            th(style="background-color: #F3C035;") 1 Difícil.
            th(style="background-color: #F3C035;") 1 Poco común.
            th(style="background-color: #F3C035;") 1 Difícil.
            th(style="background-color: #F3C035;") 1 Mínimo.

    .row.justify-content-center.mb-4(data-aos="fade-right")
      .col-md-10.tarjeta.color-secundario.p-4
        .row.justify-content-around.align-items-center
          .col-3.col-sm-2.col-lg-1
            img(src="@/assets/curso/temas/img01.png")
          .col
            .row.justify-content-between.align-items-center
              .col.mb-3.mb-sm-0
                h4.text-white Factores de riesgo
                p.text-white.mb-0 Para conocer los factores de riesgo que se asocian a la anterior tabla, se invita a dar clic en:
              .col-sm-auto
                a.boton.color-acento-botones(:href="obtenerLink('downloads/anexo3.pdf')" target="_blank")
                  span Descargar
                  i.fas.fa-file-download
                
    p Según las tablas anteriores y los niveles de riesgos detectados por cada ítem de análisis en el informe, se debe especificar el tipo de amenaza según la aplicación, así:

    .titulo-sexto.color-acento-contenido.my-4(data-aos="fade-right")
      h5 Figura 5
      span Impacto vs. valoración

    .row.justify-content-center.mb-4
      .col-md-7
        table.mb-5(data-aos="zoom-in")
          thead
            tr
              th(style="background-color: #6ACEAE; border-width: 5px; border-color: #fff").text-center.text-center Impacto
              th(style="background-color: #6ACEAE; border-width: 5px; border-color: #fff").text-center.text-center Descripción
              th(style="background-color: #6ACEAE; border-width: 5px; border-color: #fff").text-center.text-center Valoración
          tbody
            tr
              td(style="background-color: #EA2440; border-width: 5px; border-color: #fff").text-center.text-white Catastrófico
              td(style="background-color: #F3F9FF; border-width: 5px; border-color: #fff").text-center Extremadamente dañino
              td(style="background-color: #EA2440; border-width: 5px; border-color: #fff" td rowspan="2").text-center.text-white Alto
            tr
              td(style="background-color: #F9943A; border-width: 5px; border-color: #fff").text-center Mayor
              td(style="background-color: #F3F9FF; border-width: 5px; border-color: #fff").text-center Dañino
            tr
              td(style="background-color: #F2E141; border-width: 5px; border-color: #fff").text-center Moderado
              td(style="background-color: #F3F9FF; border-width: 5px; border-color: #fff").text-center Moderado
              td(style="background-color: #F2E141; border-width: 5px; border-color: #fff").text-center Medio
            tr
              td(style="background-color: #B2C42D; border-width: 5px; border-color: #fff").text-center Menor
              td(style="background-color: #F3F9FF; border-width: 5px; border-color: #fff").text-center Menor
              td(style="background-color: #5EBF4A; border-width: 5px; border-color: #fff" td rowspan="2").text-center Baja
            tr
              td(style="background-color: #5EBF4A; border-width: 5px; border-color: #fff").text-center Insignificante
              td(style="background-color: #F3F9FF; border-width: 5px; border-color: #fff").text-center Ligeramente dañino

    p La descripción de la anterior tabla, se puede interpretar de la siguiente manera:

    .BGR01.p-4.mb-4(data-aos="zoom-in")
      SlyderA(tipo="b")
        .row.justify-content-center
          .col-md-6.order-md-1.order-2
            .h4 Impacto catastrófico y riesgo alto
            p La descripción es #[strong extremadamente dañina], en la misma en el informe se pone el valor de pérdidas superiores a 1.500 SMLV, la afectación de la imagen corporativa a nivel local, regional, nacional e internacional. 
            p Si llega a tener sanciones por entes de control como Fiscalía, Procuraduría y Contraloría, y también analizar si hay graves daños en la infraestructura y aplicaciones web de la organización.
          .col-md-4.col-8.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema4/img02.svg")
        .row.justify-content-center
          .col-md-6.order-md-1.order-2
            .h4 Impacto mayor y riesgo alto
            p Sería una descripción de #[strong tipo dañino] si existen pérdidas económicas entre 1.000 y 1.499 SMLV, si la afectación de la imagen corporativa es a nivel local, regional y nacional. Si llega a tener sanciones por entes de control como Fiscalía, Procuraduría y Contraloría y también analizar si hay graves daños en la infraestructura y aplicaciones web de la organización.
          .col-md-4.col-8.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema4/img03.svg")
        .row.justify-content-center
          .col-md-6.order-md-1.order-2
            .h4 Impacto moderado y riesgo medio
            p Sería una descripción de #[strong tipo moderado] si existen pérdidas económicas entre 600 y 999 SMLV, si la afectación de la imagen corporativa es a nivel local. Si llega a tener sanciones a nivel de la oficina de control interno o jurídico de la entidad, y también analizar si hay daños parciales en la infraestructura y aplicaciones web de la organización.
          .col-md-4.col-8.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema4/img04.svg")
        .row.justify-content-center
          .col-md-6.order-md-1.order-2
            .h4 Impacto es menor y el riesgo bajo
            p Sería una descripción de #[strong tipo menor] si existen pérdidas económicas entre 400 y 599 SMLV, si la afectación de la imagen corporativa es a nivel organizacional. Si llega a tener sanciones a nivel procesos, y también analizar si hay daños pequeños en la infraestructura y aplicaciones web de la organización.
          .col-md-4.col-8.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema4/img05.svg")
        .row.justify-content-center
          .col-md-6.order-md-1.order-2
            .h4 Impacto es insignificante y el riesgo bajo
            p Sería una descripción de tipo #[strong ligeramente dañino] si existen pérdidas económicas menores a 399 SMLV, si la afectación de la imagen corporativa es a nivel de área, si llega a tener sanciones a nivel área, y también analizar si hay daños pequeños en la infraestructura y aplicaciones web de la organización. Hay que revisar si se tiene llamados de atención a nivel grupo.
          .col-md-4.col-8.order-md-2.order-1.mb-md-0.mb-4
            img(src="@/assets/curso/tema4/img06.svg")
    
    p En la organización, y en este caso con las aplicaciones web, pueden ocurrir varios impactos y diferentes valoraciones que deben ser documentados y analizados en el informe, y de igual manera establecer un plan de mejora y control frente a incidentes informáticos. 
    p En cuanto a la urgencia frente a incidentes informáticos en aplicaciones web, se tienen de la siguiente manera:
    
    .row.justify-content-center.mb-4
      .col-md-10.BGR09.p-4
        .h4.text-center ATENCIÓN A LA URGENCIA
        .row.justify-content-center
          .col-md-4.col-10.mb-md-0.mb-4(data-aos="fade-right")
            .tarjeta-avatar
              img(src='@/assets/curso/tema4/img07.svg' alt='AvatarTop')
              .BGR10.p-4.pt-5
                p.mt-5.mb-0 El incidente de seguridad debe atenderse entre 0 y 120 minutos.
          .col-md-4.col-10.mb-md-0.mb-4(data-aos="zoom-in")
            .tarjeta-avatar
              img(src='@/assets/curso/tema4/img08.svg' alt='AvatarTop')
              .BGR11.p-4.pt-5
                p.mt-5.mb-0 El incidente de seguridad debe atenderse entre 0 y 240 minutos.
          .col-md-4.col-10(data-aos="fade-left")
            .tarjeta-avatar
              img(src='@/assets/curso/tema4/img09.svg' alt='AvatarTop')
              .BGR12.p-4.pt-5
                p.mt-5.mb-0 El incidente de seguridad debe atenderse entre 0 y 1.440 minutos.

    p Estos tiempos de respuestas también deben de ser tenidos en cuenta en la realización del informe, tener en cuenta los tiempos mínimos y máximo según el incidente informático en la aplicación web. Es importante establecer políticas de control en las aplicaciones web; la ISO 27001 juega un papel fundamental en ese plan de mejora.

  .container.BG13.p-4.p-md-5px(data-aos="fade-right")
    .row.justify-content-center.mb-4
      .col-md-9.order-1
        .h4 Un informe de auditoría debe contar con todas las evidencias recolectadas (#[i logs], errores humanos detectados, irregularidades) y el procedimiento es el siguiente:
      .col-md-6.order-md-2.order-3
        ul.lista-ul--color.ms-4
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Aplicar instrumentos de toma de información.
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Registrar las situaciones encontradas.
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Comentar las situaciones encontradas y sus posibles causas.
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Analizar y depurar las situaciones relevantes.
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Comentar las situaciones relevantes con gerente o directivos.
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Elaborar informe final con dictamen del auditor y plan de mejora.
          li
            <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
            | Sustentar informe final ante directivos o gerente.
      .col-md-3.col-6.order-md-3.order-2.mb-md-0.mb-4
        img(src='@/assets/curso/tema4/img10.png')
      
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    p En los <span style="background-color:#BBEFDE; padding: 5px;"><b>informes de incidentes de seguridad en aplicaciones</b>,</span> se incluyen los ajustes de controles que hacen referencia a los planes de mejora; así se detienen y previenen futuros incidentes informáticos, ya que los mismos buscan establecer mecanismos de prevención y control. Como política general de ajuste de control se debe contemplar las actualizaciones de #[i software] o parches de seguridad en la herramienta de aplicaciones web cada vez que se detecte una. A continuación, se conocerá los niveles de planes de mejora y tablero de control, básico, intermedio y avanzado:
  
    .row.justify-content-center.mb-4
      .col-lg-3.col-8(data-aos="fade-right")
        .BG14.p-5
          .h4.text-white.text-center.mb-0 Básico
        .BG03.p-4.mb-md-0.mb-4
          ul.lista-ul--color.mb-5
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Antivirus.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Contraseñas fuertes.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              p.mb-0 Realizar #[i backup] frecuentes.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Actualizar app.
      .col-lg-3.col-8(data-aos="zoom-in")
        .BG15.p-5
          .h4.text-white.text-center.mb-0 Intermedio
        .BG03.p-4.mb-md-0.mb-4
          ul.lista-ul--color.mb-0
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | No reciclar contraseñas.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Usar gestor de contraseñas.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Actualizar personal.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              p.mb-0 Utilizar #[i firewall].
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              p.mb-0 Proteger servidores web.
      .col-lg-3.col-8(data-aos="fade-left")
        .BG16.p-5
          .h4.text-white.text-center.mb-0 Avanzado
        .BG03.p-4
          ul.lista-ul--color.mb-4
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Utilizar cifrado. 
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Actualizar tableros de control de amenazas y riesgos.
            li
              <i class="fas fa-check-circle" style="color:#7FD8B8"></i>
              | Tener configuraciones avanzadas de seguridad web.

    p Los planes de mejora son las conclusiones que toda auditoría deja por defecto tomando correctivos para que los riesgos y amenazas no vuelvan a la aplicación web, con este tipo de control y seguimiento se previenen riesgos y amenazas.
    
</template>

<script>
export default {
  name: 'Tema4',
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
