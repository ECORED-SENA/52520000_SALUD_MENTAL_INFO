<template lang="pug">
section
  BannerPrincipal.mb-5


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p Estimado aprendiz sea bienvenido al curso de “Actividad física para la salud mental” en el cual se trabaja uno de los mayores problemas de salud en el mundo y es el estrés que junto con el sedentarismo se pueden convertir en una de las mayores causas de problemas mentales en los colombianos y en general en la población mundial con índices altos y preocupantes.
      br
      br
      |Es por eso que este curso evidencia en tres momentos la importancia de la actividad física para los distintos ámbitos mentales trabajando desde la personalidad hasta los parámetros ideales antes del planteamiento de una rutina de ejercicio, es así como se pretende crear conciencia de la importancia de la actividad física en los temas de la salud mental y no cualquier actividad física, la actividad física ideal para la población objetivo desde niños hasta adultos mayores.
      br
      br
      |Sea bienvenido a este curso complementario virtual y esté pendiente de las plataformas y el correo electrónico registrado con el Sena para que no pierda detalle de estas cuatro semanas de trabajo inmersivo. 

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa

    p El curso complementario en Actividad Física para la salud mental, está dirigido a personas y profesionales de las áreas de la actividad física, deportiva, recreativa, social y educativa, que trabajan con población aparentemente sana, diagnosticadas con enfermedades no transmisibles, y con factores de vulnerabilidad en salud mental. Formación mediante la cual los aprendices caracterizaran la población o usuarios desde su estado de salud mental con el fin de recomendar prácticas de actividad física que contribuyan al bienestar físico, psicológico y social.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Población<br>objetivo

    p Este programa está dirigido a la ciudadanía en general que tenga acceso a internet y a un equipo de cómputo sin importar su área de formación, ocupación o perfil.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4. Estrategia<br>metodológica

    p Centrada en la construcción de autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en el utilización de las tecnologías de la información y la comunicación, integradas, en ambientes virtuales de aprendizaje, que en todo caso recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias. 

    | Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el que hacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:
    .ms-3.mt-2
      li El instructor - Tutor
      li El entorno
      li las TIC
      li El trabajo colaborativo



  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>

<style lang="sass" scoped>
.resultados-aprendizaje
  &__item
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0

.desarrollo-contenidos
  &__item
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 25px
    padding: 5px
    border-radius: $base-border-radius

    &__texto
      display: flex
      align-items: center

    &__icono
      display: block
      background-color: $color-sistema-g
      font-size: 20px
      font-weight: $base-black-font-weight
      text-align: center
      padding: 10px
      line-height: 1em
      width: 40px
      margin-right: 15px

    &:last-child
      margin-bottom: 0

    &:hover
      background-color: $color-sistema-g
      font-weight: $base-black-font-weight
      color: $color-sistema-a
</style>
