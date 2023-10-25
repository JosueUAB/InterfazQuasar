<template>
  <q-page padding>
    <!-- content -->
    
    <div class="row justiy-center flex-center">
    
    <div class="q-pa-md ">
      <div class="q-gutter-y-md column justiy-center">
        
        <h1>gatos</h1>
        
      </div>
    </div>
    </div>


    <div class="row justiy-center flex-center content-center">
  <div class="col flex-center">
    <p>
    Se ha comprobado que tener un gato reduce el estrés. Normalmente los dueños de gatos tienen una tensión arterial más baja que las personas sin mascotas. Puedes beneficiarte de un sistema inmunológico más fuerte y recuperarte de las enfermedades antes que las personas que no tienen animales de compañía.
  </p></div>
  
  <!--
     we have 3 children, so equivalent
     to above would be to use `col-4`
     on each of the children
  -->
</div>

  <div class="q-pa-md">
    <q-parallax>
      <template v-slot:media>
        <img src="https://thecatapi.com/api/images/get?format=src&type=gif?results_per_page=img+1">
      </template>

      <template v-slot:content="scope">
        <div
          class="absolute column items-center"
          :style="{
            opacity: 0.45 + (1 - scope.percentScrolled) * 0.55,
            top: (scope.percentScrolled * 60) + '%',
            left: 0,
            right: 0
          }"
        >
          <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" style="width: 150px; height: 150px">
          <div class="text-h3 text-white text-center">Bienvenido a mi Sitio</div>
          <div class="text-h6 text-grey-3 text-center">
            v{{ $q.version }}
          </div>
        </div>
  
      </template>
    </q-parallax>
  </div>

  <div class="row justiy-center flex-center">
    
  <div class="q-pa-md ">
    <div class="q-gutter-y-md column justiy-center">
      
      <q-rating
        v-model="ratingModel"
        size="3em"
        color="brown-5"
        icon="pets"
      />
      
    </div>
  </div>
  </div>


  <div class="row justiy-center flex-center">
    
    <div class="q-pa-md ">
      <div class="q-gutter-y-md column justiy-center">
        
        <h3>curiosidades</h3>
        
      </div>
    </div>
    </div>

  <div>
    <q-splitter
      v-model="splitterModel"
      style="height: 400px"
    >

      <template v-slot:before>
        <div class="q-pa-md">
          <div class="text-h4 q-mb-md">Cosas que no sabias de los gatos</div>

          <ul>
            
           <li><p>1. Existen más de 500 millones de gatos domésticos en el mundo de 40 razas.</p></li>

           <li><p>2. Los gatos hacen unos 100 sonidos y los perros solamente 10.</p></li>

           <li><p>3. Son los animales con mayor oído.</p></li>

           <li><p>4. Un gato que nace con un ojo azul normalmente es sordo de la oreja más cercana.</p></li>

           <li><p>5. El gato más longevo vivió 34 años.</p></li>

           <li><p>6. Pasan el 70% de su vida durmiendo.</p></li>

           <li><p>7. La orina de tu gato brilla en la oscuridad cuando la iluminas con luz negra.</p></li>

           <li><p>Si crees que tu gato está marcando territorio -más allá del tremendo olor- puedes hacerle a la CSI y buscar la ﬂuorescencia.</p></li>

           <li><p>8. Los gatos se comunican con el movimiento de sus colas. Por ejemplo: si un gato está cerca de ti y agita su cola, es la mayor expresión de cariño que puede hacer. En cambio si la agita demasiado fuerte, tanto que golpea con ella, está de pésimo humor, es mejor que lo dejes solo un rato.</p></li>

           <li><p>9. Pueden sentir el peligro... incluso durmiendo.</p></li>

           <li><p>10. Pueden ver en la oscuridad, pero no pueden reconocer colores diferentes.</p></li>

           <li><p>11. No les gustan los dulces.</p></li>

           <li><p>12. En el Antiguo Egipto cuando un gato doméstico fallecía todos los miembros de la casa se depilaban las cejas y lamentaban su pérdida.</p></li>

           <li><p>13. Normalmente tienen cinco dedos en cada pata delantera y cuatro en cada pata trasera.</p></li>

           <li><p>14. Cuando los gatos están muy contentos cierran los ojos bien fuerte.</p></li>

           <li><p>15. Los gatos, con el paso de los años, se vuelven intolerantes a la lactosa.</p></li>

           <li><p>16. Isaac Newton, entre sus muchos logros, inventó las puertas abatibles para gatos. Así evitaba que sus mascotas le distrajeran.</p></li>

           <li><p>17. En 1879 se usaron 37 gatos para entregar et correo a algunos pueblos. Sin embargo, se dieron cuenta de que no eran los suficientemente disciplinados
             para continuar la tarea y se abandonó el proyecto.</p></li>

           <li><p>18. Un gato puede saltar hasta 5 veces su altura de una sola vez.</p></li>

           <li><p>19. Los gatos sudan. Así es, pero no donde crees, en realidad el sudor aparece a través de las almohadillas de sus patas.</p></li>
           <li><p>20. La mayoría de las hembras son diestras, mientras que los gatos machos suelen ser zurdos</p></li>
          
          </ul>
</div>
      </template>

      

    </q-splitter>
  </div>
  <div class="row justiy-center flex-center">
    
    <div class="q-pa-md ">
      <div class="q-gutter-y-md column justiy-center">
        
        
  <div class="q-pa-md q-gutter-xs">
    <div class="q-gutter-md row justify-center">
      <div>
        <q-spinner-audio
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerAudio</q-tooltip>
      </div>
      <div>
        <q-spinner-ball
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerBall</q-tooltip>
      </div>
      <div>
        <q-spinner-bars
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerBars</q-tooltip>
      </div>
      <div>
        <q-spinner-box
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerBox</q-tooltip>
      </div>
      <div>
        <q-spinner-clock
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerClock</q-tooltip>
      </div>
      <div>
        <q-spinner-comment
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerComment</q-tooltip>
      </div>
      <div>
        <q-spinner-cube
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerCube</q-tooltip>
      </div>
      <div>
        <q-spinner-dots
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerDots</q-tooltip>
      </div>
      <div>
        <q-spinner-facebook
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerFacebook</q-tooltip>
      </div>
      <div>
        <q-spinner-gears
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerGears</q-tooltip>
      </div>
      <div>
        <q-spinner-grid
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerGrid</q-tooltip>
      </div>
      <div>
        <q-spinner-hearts
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerHearts</q-tooltip>
      </div>
      <div>
        <q-spinner-hourglass
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerHourglass</q-tooltip>
      </div>
      <div>
        <q-spinner-infinity
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerInfinity</q-tooltip>
      </div>
      <div>
        <q-spinner-ios
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerIos</q-tooltip>
      </div>
      <div>
        <q-spinner-orbit
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerOrbit</q-tooltip>
      </div>
      <div>
        <q-spinner-oval
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerOval</q-tooltip>
      </div>
      <div>
        <q-spinner-pie
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerPie</q-tooltip>
      </div>
      <div>
        <q-spinner-puff
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerPuff</q-tooltip>
      </div>
      <div>
        <q-spinner-radio
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerRadio</q-tooltip>
      </div>
      <div>
        <q-spinner-rings
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerRings</q-tooltip>
      </div>
      <div>
        <q-spinner-tail
          color="primary"
          size="2em"
        />
        <q-tooltip :offset="[0, 8]">QSpinnerTail</q-tooltip>
      </div>
    </div>
  </div>
        
      </div>
    </div>
    </div>
  
  </q-page>
  
</template>




<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  // name: 'PageName'
})
</script>
