<template>
<div id="app">

  <b-container class="bv-example-row">
    <!-- <b-row class="text-center"> -->
    <b-card no-body>
      <b-tabs pills card vertical>
        <b-tab title="课文" active>
          <b-tabs>
            <b-tab title="Uno(1)" active>
              <br>
              <h4>¿Cómote llamas?</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class001_s}}</b-col>
                  <b-col cols="6">{{class001_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse1  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse1" class="mt-2">
                  <b-card class="text-left">
                    <!-- <p class="card-text">class001_point</p> -->
                    <div>
                     <!-- Main UI -->
                     <!-- <p class="card-text">class001_point</p> -->
                     <div class="mt-3 mb-3">
                       class001_point:
                       <ul>
                         <li v-for="n in points">{{n}}</li>
                       </ul>
                     </div>
                     <b-btn v-b-modal.modalPrevent>Edición</b-btn>

                     <!-- Modal Component -->
                     <b-modal id="modalPrevent"
                              ref="modal"
                              title="Edición"
                              @ok="handleOk"
                              @shown="clearPoint">
                       <form @submit.stop.prevent="handleSubmit">
                         <b-form-input type="text"
                                       placeholder="Enter new point"
                                       v-model="point"></b-form-input>
                       </form>
                     </b-modal>
                   </div>
                  </b-card>
                </b-collapse>
              </div>
            </b-tab>
            <b-tab title="Uno(2)">
              <br>
              <h4>¿Quién es el chico?</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class002_s}}</b-col>
                  <b-col cols="6">{{class002_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse2  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse2" class="mt-2">
                  <b-card>
                    <p class="card-text">class002_point</p>

                  </b-card>
                </b-collapse>
              </div>
            </b-tab>
            <b-tab title="Dos(1)">
              <br>
              <h4>¿Cómo estás?</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class003_s}}</b-col>
                  <b-col cols="6">{{class003_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse3  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse3" class="mt-2">
                  <b-card>
                    <p class="card-text">class003_point</p>

                  </b-card>
                </b-collapse>
              </div>

            </b-tab>
            <b-tab title="Dos(2)">
              <br>
              <h4>Ocupados, ¡pero contentos!</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class004_s}}</b-col>
                  <b-col cols="6">{{class004_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse4  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse4" class="mt-2">
                  <b-card>
                    <p class="card-text">class004_point</p>

                  </b-card>
                </b-collapse>
              </div>

            </b-tab>
            <b-tab title="Tres(1)">
              <br>
              <h4>La casa de Juan</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class005_s}}</b-col>
                  <b-col cols="6">{{class005_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse5  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse5" class="mt-2">
                  <b-card>
                    <p class="card-text">class005_point</p>

                  </b-card>
                </b-collapse>
              </div>
            </b-tab>
            <b-tab title="Tres(2)">
              <br>
              <h4>¿Cuántos son en tu familia?</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class006_s}}</b-col>
                  <b-col cols="6">{{class006_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse6  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse6" class="mt-2">
                  <b-card>
                    <p class="card-text">class006_point</p>

                  </b-card>
                </b-collapse>
              </div>
            </b-tab>
            <b-tab title="Cuatro(1)">
              <br>
              <h4>¿Por qué no me hablas más de tu vida?</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class007_s}}</b-col>
                  <b-col cols="6">{{class007_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse7  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse7" class="mt-2">
                  <b-card>
                    <p class="card-text">class007_point</p>

                  </b-card>
                </b-collapse>
              </div>
            </b-tab>
            <b-tab title="Cuatro(2)">
              <br>
              <h4> Tenemos un horario muy apretado</h4>
              <br>
              <div class="">
                <b-row class="text-left">
                  <b-col cols="6">{{class008_s}}</b-col>
                  <b-col cols="6">{{class008_c}}</b-col>
                </b-row>
              </div>
              <div>
                <b-btn v-b-toggle.collapse8  variant="info" size="sm" style="float: right">Point</b-btn>
                <br>
                <br>

                <b-collapse id="collapse8" class="mt-2">
                  <b-card>
                    <p class="card-text">class008_point</p>

                  </b-card>
                </b-collapse>
              </div>
            </b-tab>
          </b-tabs>
        </b-tab>
        <b-tab title="单词">
          <div class="text-left">
            <b-btn v-b-toggle.collapse_word1  variant="success" >Uno</b-btn>
            <b-btn v-b-toggle.collapse_word2  variant="success" >Dos</b-btn>
            <b-btn v-b-toggle.collapse_word3  variant="success" >Tres</b-btn>
            <b-btn v-b-toggle.collapse_word4  variant="success" >Cuatro</b-btn>

            <br>
          </div>
          <div>
            <b-collapse id="collapse_word1" class="mt-2">
              <b-card class="text-left">
                 <div class="mt-3 mb-3 sm-6">
                   <b-row class="text-left">
                     <b-col  sm="6" md="6" lg="3">
                        <b-table striped hover :items="items1"></b-table>
                     </b-col>
                     <b-col  sm="6" md="6" lg="3">
                        <b-table striped hover :items="items1"></b-table>
                      </b-col>
                      <b-col  sm="6" md="6" lg="3">
                         <b-table striped hover :items="items1"></b-table>
                       </b-col>
                       <b-col  sm="6" md="6" lg="3">
                          <b-table striped hover :items="items1"></b-table>
                        </b-col>
                   </b-row>
                 </div>
              </b-card>
            </b-collapse>
          </div>
          <div>
            <b-collapse id="collapse_word2" class="mt-2">
              <b-card class="text-left">
                <div class="mt-3 mb-3 sm-6">
                  <b-row class="text-left">
                    <b-col  sm="6" md="6" lg="3">
                       <b-table bordered small  :items="items201"></b-table>
                    </b-col>
                    <b-col  sm="6" md="6" lg="3">
                       <b-table bordered small :items="items202"></b-table>
                     </b-col>
                     <b-col  sm="6" md="6" lg="3">
                        <b-table bordered small :items="items203"></b-table>
                      </b-col>
                      <b-col  sm="6" md="6" lg="3">
                         <b-table bordered small :items="items204"></b-table>
                       </b-col>
                  </b-row>
                </div>
              </b-card>
            </b-collapse>
          </div>
          <div>
            <b-collapse id="collapse_word3" class="mt-2">
              <b-card class="text-left">
                 <div class="mt-3 mb-3">
                   danci 03
                 </div>
              </b-card>
            </b-collapse>
          </div>
          <div>
            <b-collapse id="collapse_word4" class="mt-2">
              <b-card class="text-left">
                <div class="mt-3 mb-3 sm-6">
                  <b-row class="text-left">
                    <b-col  sm="6" md="6" lg="3">
                       <b-table bordered small  :items="items401"></b-table>
                    </b-col>
                    <b-col  sm="6" md="6" lg="3">
                       <b-table bordered small :items="items402"></b-table>
                     </b-col>
                     <b-col  sm="6" md="6" lg="3">
                        <b-table bordered small :items="items403"></b-table>
                      </b-col>
                      <b-col  sm="6" md="6" lg="3">
                         <b-table bordered small :items="items404"></b-table>
                       </b-col>
                  </b-row>
                </div>
              </b-card>
            </b-collapse>
          </div>
          <!-- <b-table :items="items" :fields="fields">
            <template slot="show_details" slot-scope="row">
              we use @click.stop here to prevent emitting of a 'row-clicked' event
              <b-button size="sm" @click.stop="row.toggleDetails" class="mr-2">
               {{ row.detailsShowing ? 'Hide' : 'Show'}} Details
              </b-button>
            </template>
            <template slot="row-details" slot-scope="row">
              <b-card>
                <b-row class="mb-2">
                  <b-col sm="3" class="text-sm-right"><b>Age:</b></b-col>
                  <b-col>{{ row.item.age }}</b-col>
                </b-row>
                <b-row class="mb-2">
                  <b-col sm="3" class="text-sm-right"><b>Is Active:</b></b-col>
                  <b-col>{{ row.item.isActive }}</b-col>
                </b-row>
                <b-button size="sm" @click="row.toggleDetails">Hide Details</b-button>
              </b-card>
            </template>
          </b-table> -->
        </b-tab>
        <b-tab title="变位">
          <!-- {{tab03Text}} -->

        </b-tab>
        <b-tab title="">

        </b-tab>
      </b-tabs>
    </b-card>

  </b-container>

</div>
</template>

<script>
let class001_s=`
  Ana:Hola, buenos días.
  Paco:Buenos días.Yo soy Paco. Y tú,¿cómo te llamas?
  Ana:Yo me llamo Ana. Ellos son mis amigos, ella se llama Susana y él se llama Tomás.
  Paco:¿Son ustedes españoles?
  Ana:Yo soy española.Susana es cubana y Tomás,chileno.
  Paco:Encantado de conocerlos.
  Ana:Mucho gusto. ¿Es usted profesor?
  Paco:Sí.soy profesor de chino.
  Ana:Ah. usted es nuestro profesor de chino. Entonces, somos sus alumnos.

`;
let class001_c=`
  你好，早上好。
  早上好。我是巴科。你呢？你叫什么名字？
  我叫安娜。他们是我的朋友们，她叫苏珊娜，他叫托马斯。
  您们是西班牙人吗？
  我是西班牙人。苏珊娜是古巴人，托马斯是智利人。
  很高兴认识您们。
  很高兴认识您。您是老师吗？
  是的，我是中文老师。
  哦，您是我们的中文老师。那么，我们就是您的学生。

`;
let class002_s=`
  Ana y Li Meilan son amigas. Ana es mexicana y Li Meilan es china. Las dos son estudiantes.
  Ana:Meilan, ¿eres amiga de esos jóvenes?
  Li:Sí,soy amiga de ellos.
  Ana:¿Quiénes ese chico? ¿Se llama Manolo?
  Li:Sí,élse llama Manolo.
  Ana:¿Es cubano?
  Li:No. no es cubano. Es panameño.
  Ana:¿No se llama Elena esa chica?
  Li:No, no se llama Elena. Ella es Susana.
  Ana:¿Son novios?
  Li:¿Quiénes?¿Elena y Manolo? ¡Quéva! Solo son amigos.
`
let class002_c=`
  安娜和李美兰是朋友。安娜是墨西哥人，李美兰是中国人。她们俩都是学生。
  美兰，你是那些年轻人的朋友吗？
  是的，我是他们的朋友。
  那个小伙子是谁？他是叫马诺罗吗？
  是的，他叫马诺罗。
  他是古巴人吗？
  不是，他不是古巴人。他是巴拿马人。
  那个女孩是叫艾琳娜吗？
  不是，她不叫艾琳娜。她是苏珊娜。
  他们是男女朋友吗？
  谁们？艾琳娜和马诺罗？什么呀！他们只是普通朋友。
`
let class003_s=`
  Mario, Carmen y Fernando son tres chicos latinoamericanos.
  Mario es mexicano. Carmen es argentina y Fernando es de Cuba.
  Éles el novio de la chica. Los tres son estudiantes. Su profesor se llama Carlos Ramírez.
  Mario:Buenas tardes, profesor Ramírez.
  Ramírez:Buenas tardes. Mario. ¿Cómoestás?
  Mario:Bien, gracias. Le presento a mis amigos:Carmen y Fernando.
  Ramírez:Mucho gusto.
  Fernando:Mucho gusto.
  Carmen:Encantada.
  Ramírez:¿De dónde son ustedes? ¿Son tambiénmexicanos?
  Fernando:No. Carmen es argentina y yo soy de Cuba. Los tres somos latinoamericanos.
  Pero ahora estamos en China. Estudiamos chino. Profesor, ¿es usted también latinoamericano?
  Ramírez:No. soy español.Enseño nuestra lengua en una universidad de este país.Pero también enseño chino a los hispanohablantes.
`
let class003_c=`
  马里奥，卡门和费尔南多是三个拉丁美洲的孩子。
  马里奥是墨西哥人。卡门是阿根廷人，费尔南多来自古巴。
  他是这个女孩的男朋友。他们三个都是学生。他们的老师叫卡洛斯. 拉米雷斯。
  马里奥：拉米雷斯老师，下午好。
  下午好。马里奥，你好吗？
  我很好，谢谢。我向您介绍我的朋友们：卡门和费尔南多。
  很高兴认识你们。
  认识您很高兴。
  很高兴认识您。
  各位都来自哪？你们都是墨西哥人吗？
  不是的。卡门是阿根廷人，我来自古巴。我们三个都是拉丁美洲人。
  但是现在我们都在中国。我们在学习中文。老师，您也是拉美人吗？
  不是，我是西班牙人。我在这个国家的一所大学里教西班牙语。但是我也教说西语的人中文。
`
let class004_s=`
    Víctor,Pablo y Pilar son latinoamericanos.
    Yo soy china. Los cuatro somos amigos. Ahora estamos en Alemania.
    Somos estudiantes. Estudiamos alemán.
    Tenemos muchas clases todos los díasy estamos siempre muy ocupados, pero contentos.
    ¿Me preguntas quiénes nuestro profesor? Pues tenemos varios:tres hombres y cuatro mujeres.
`
let class004_c=`
  维克托，巴布罗和皮拉尔是拉丁美洲人。
  我是中国人。我们四个是朋友。现在我们都在德国。
  我们都是学生。我们在学习德语。
  我们每天都有很多课，我们总是非常忙，但是我们很开心。
  你问我谁是我们的老师？我们有好几个老师：三个男老师和四个女老师。
`
let class005_s=`
    La casa de Juan tiene muchas habitaciones y estáen Lima, Perú.Toda su familia vive en ella.
    El padre de Juan es médico.Trabaja en un hospital. Su madre es profesora. Enseña inglés en un colegio.
    Juan tiene dos hermanos:una chica y un chico. Son menores que él.
    Van al colegio. Los abuelos, ya muy mayores, no trabajan.
    Juan estudia bachillerato (lasecundaria). Todos los días se levanta muy temprano.
    Se baña,se cepilla los dientes y se peina.
    Después de desayunar, primero lleva a sus hermanos al colegio (la escuela) y luego toma un autobús para ir al instituto (a su centro de estudios).
    Por la mañana tiene cuatro clases y por la tarde, también cuatro.
    Todo el día está muy ocupado, por eso regresa a casa muy tarde.
`
let class005_c=`
    胡安的家在秘鲁的利马，有很多房间。他们一家人都住在那。
    胡安的爸爸是医生。他爸爸在一家医院工作。他妈妈是老师，在学校里教英语。
    胡安有两个兄弟：一个妹妹，一个弟弟。他们都比胡安小。
    他们上学。他们的祖父母现在都很老了，已经不工作了。
    胡安在读高中（中学）。他每天都起得很早。
    洗澡，刷牙，梳头。
    吃过早饭后，他首先要送弟弟妹妹上学（小学），然后再乘坐公交车去上学（去他的学习中心）。
    上午有四节课，下午也是有四节课。
    他一整天都很忙，因此很晚才回家。
`
let class006_s=`
    Señora:Hola, chico, eres José,¿no?
    José:Sí,señora,buenos días.Soy José.
    Señora:¿De dónde eres? Pareces latinoamericano.
    José:Sí,soy peruano y vivo en Lima.
    Señora:¿Es grande la ciudad de Lima?
    José:Sí.es una ciudad bastante grande.
    Señora:Vives allí con tu familia, ¿verdad?
    José:Sí.señora.
    Señora:¿Cuántos son?
    José:Somos siete:mis abuelos, mis padres, mis hermanos y yo.
    Señora:Supongo que tu casa es grande.
    José:Sí,tenemos una casa con una sala de estar, cuatro dormitorios, una cocina y dos cuartos de baño.
    Señora:¿Estudias en la universidad?
    José:¡Quéva! Estoy todavía en el bachillerato. Mis hermanos van a un colegio.
    Todos los días me levanto muy temprano, tomo el desayuno y llevo a mis hermanos a su colegio.
    Luego, tomo un autobús y me voy a mi instituto.
    Señora:¡Qué día tan recargado! Todo el tiempo estás ocupado.
`
let class006_c=`
    孩子你好，你是何塞，对吗？
    是的，女士。早上好。我是何塞。
    你是从哪来的 ? 你看起来像拉美人。
    是的,我是秘鲁人,住在利马。
    利马这座城市大吗?
    大,利马是一座相当大的城市。
    你和你的家人住在那,对吗?
    是的,女士。
    几口人啊?
    我们有七口人:我的祖父母,我的父母,我的兄弟们和我。
    我想你家一定很大。
    是的,我们家有一个客厅,四间卧室,一个厨房和两个卫生间。
    你在上大学吗?
    哪里呀!我还在读高中。我的弟弟们在读小学。
    我每天起得都很早,吃早饭然后送我的弟弟们上学。
    然后我乘坐公交车去学校。
    多充实的一天啊!你总是那么忙。
`
let class007_s=`
    Yolanda:Hola, José.¡Tú también en España!¡Qué casualidad!
    José:¡Qué alegría de volver a verte! ¿Qué haces por aquí?
    Yolanda:Vengo a un curso de verano. España organiza estos cursos todos los años.¿Y tú?¿Llevas mucho tiempo aquí?
    José:Sí,llevo año y medio en una universidad del país.Estoy en un curso de doctorado.
    Yolanda:¡Doctorado! ¡Y yo sin saberlo! ¿Por qué no me hablas más de tu vida?
    José:En realidad no hay mucho que decir.
    Todos los días hago lo mismo:me levanto a las siete en punto, me baño,me cepillo los dientes, me peino y luego voy al comedor de estudiantes a tomar el desayuno.
    Como las clases no comienzan hasta las nueve, todavía tengo tiempo para leer.
    Repaso las lecciones estudiadas y me preparo para las nuevas.
    A las ocho y media salgo de la residencia y voy a la facultad en metro.
    Yolanda:¡Vaya horario más apretado! ¡Y eso, antes de comenzar la jornada real!
    José:Pues ya ves. Al mediodía,almuerzo en un comedor del campus. Despuésme quedo en la biblioteca casi toda la tarde para estudiar.
`
let class007_c=`
    尤兰达:何塞你好。你也在西班牙,多巧啊!
    何塞:很高兴又看见你了!你在这干什么呢?
    尤兰达:我来上一个暑期班。 西班牙每年都组织这种培训班, 你呢?你在这很长时间了吗?
    何塞:是的,我在这个国家上大学一年半了。我在读一个博士培训班。
    尤兰达:博士!我都不知道这事!你怎么不和我多说说你的生活呢?
    何塞:事实上没什么好说的。
    我每天做的事都一样:我七点钟准时起床,洗澡,刷牙,梳头,然后去学生食堂吃早餐。
    因为直到九点才开始上课,所以我还有时间读读书。
    我复习学过的课程,还预习新课。
    八点半我从住处出来,坐地铁去系里。
    尤兰达:多紧张的时间表啊!这还是在正式日程之前的安排。
    何塞:你都知道了。中午的时候我在校园的食堂吃午饭。然后,几乎整个下午我都待在图书 馆里学习。
`
let class008_s=`
  Los estudiantes universitarios tenemos un horario muy apretado.
  Nos levantamos muy temrano. Después de bañarnos, si todavía nos quedo tiempo, leemos algo antes del dasayuno.
  Al comenzar las clases, ya apenas tenemos tiempo para respirar. Por eso, después del almuerzo, tenemos que descansar una hora.
  Por la tarde, muchos de nosotros siempre hacemos algo de deporte.
  Por la noche, hacmos los trabajos de casa. Nos acostamos a las once.
  ¿ Estamos contentos con nuestra vida estudiantil ?
  Aunque terminamos la jornada muy cansados, yo algo que sí.
`
let class008_c=``


let class001_point='';

const items1 = [
  {key: 'Dickerson', value: 'Macdonald' },
  {key: 'Larsen', value: 'Shaw' },
  {key: 'Geneva', value: 'Wilson' },
  {key: 'Jami', value: 'Carney' }
]
const items401 = [
  {key: 'por qué', value: '为什么' },
  {key: 'hablar', value: '谈论' },
  {key: 'más', value: '更多的' },
  {key: 'vida', value: '生活' },
  {key: 'Yolanda', value: '约岚达' },
  {key: 'España', value: '西班牙' },
  {key: 'casualidad', value: '偶然性' },
  {key: 'alegría', value: '欢乐，欢喜' },
  {key: 'volver a', value: '再一次，重新' },
  {key: 'ver', value: '看见' },
  {key: 'te', value: '你（二单与格代词）' },
  {key: 'qué', value: '什么' },
  {key: 'hacer', value: '做，干' },
  {key: 'por', value: '在... & 为了...' },
  {key: 'aquí', value: '这里' },
  {key: 'venir', value: '来' },
  {key: 'curso', value: '学年，教程' },
  {key: 'verano', value: '夏天' },
  {key: 'organizar', value: '组织' },
  {key: 'estos,tas', value: '这些' },
  {key: 'año', value: '年' }

]
const items402 =[
  {key: 'llevar + 表示时间的名词+地点', value: '呆在...地方...时间' },
  {key: 'medio', value: '半' },
  {key: 'doctorado', value: '博士学位' },
  {key: 'sin', value: '没有' },
  {key: 'saber', value: '知道' },
  {key: 'lo,la', value: '您（三单宾格代词）' },
  {key: 'en realidad', value: '实际上' },
  {key: 'haber', value: '有' },
  {key: 'decir', value: '说' },
  {key: 'lo mismo', value: '同样的事情' },
  {key: 'en punto', value: '整点' },
  {key: 'comedor', value: '饭厅，食堂' },
  {key: 'no...hasta', value: '直到...才' },
  {key: 'comenzar', value: '开始' },
  {key: 'nueve', value: '九' },
  {key: 'leer', value: '读，看' },
  {key: 'repasar', value: '复习' },
  {key: 'lección', value: '功课' },
  {key: 'estudiado,da', value: '学过的' }
]
const items403 =[
  {key: 'prepararse', value: '准备' },
  {key: 'nuevo,va', value: '新' },
  {key: 'ocho', value: '八' },
  {key: 'salir', value: '离开' },
  {key: 'residencia', value: '公寓' },
  {key: 'facultad', value: '（院）系' },
  {key: 'metro', value: '地铁' },
  {key: 'horario', value: '作息时间' },
  {key: 'apretado,da', value: '挤压的，紧凑的' },
  {key: 'eso', value: '那' },
  {key: 'antes de', value: '在..之前' },
  {key: 'jornada', value: '工作日' },
  {key: 'real', value: '真正的' },
  {key: 'al mediodía', value: '中午' },
  {key: 'almorzar', value: '吃午饭' },
  {key: 'campus', value: '大学校园' },
  {key: 'quedarse', value: '呆，留在' },
  {key: 'biblioteca', value: '图书馆' },
  {key: 'casi', value: '几乎' },
  {key: 'universitario,ria', value: '大学的' },
  {key: 'si', value: '如果' },
  {key: 'nos', value: '我们（一复与格代词）' }
]
const items404=[
  {key: 'quedar', value: '剩下，还有' },
  {key: 'algo', value: '一点，一些' },
  {key: 'al ', value: '当...时候，一..就' },
  {key: 'apenas', value: '几乎没有，几乎不' },
  {key: 'respirar', value: '呼吸' },
  {key: 'almuerzo', value: '午餐' },
  {key: 'tener que', value: '必须' },
  {key: 'descansar', value: '休息' },
  {key: 'hora', value: '小时' },
  {key: 'por la tarde', value: '下午' },
  {key: 'deporte', value: '运动' },
  {key: 'por la noche', value: '晚上' },
  {key: 'trabajo de casa', value: '作业' },
  {key: 'acostarse', value: '上床睡觉' },
  {key: 'once', value: '十一' },
  {key: 'estudiantil', value: '学生的' },
  {key: 'aunque', value: '虽然' },
  {key: 'terminar', value: '结束' },
  {key: 'cansado,da', value: '累的，疲惫的' }
]


export default {
  name: 'app',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      modalShow: false,
      point: '',
     points: [],
      class001_s: class001_s,
      class001_c: class001_c,
      class002_s: class002_s,
      class002_c: class002_c,
      class003_s: class003_s,
      class003_c: class003_c,
      class004_s: class004_s,
      class004_c: class004_c,
      class005_s: class005_s,
      class005_c: class005_c,
      class006_s: class006_s,
      class006_c: class006_c,
      class007_s: class007_s,
      class007_c: class007_c,
      class008_s: class008_s,
      class008_c: class008_c,
      class001_point:class001_point,
      slide: 0,
      sliding: null,
      items1: items1,
      items401: items401,
      items402: items402,
      items403: items403,
      items404: items404

    }
  },
  methods: {
    clearPoint () {
      this.point = ''
    },
    handleOk (evt) {
      // Prevent modal from closing
      evt.preventDefault()
      if (!this.point) {
        alert('Please enter your new point')
      } else {
        this.handleSubmit()
      }
    },
    handleSubmit () {
      this.points.push(this.point)
      this.clearPoint()
      this.$refs.modal.hide()
    },
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = true
    }
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  /* list-style-type: none; */
  padding: 0;
}

li {
  /* display: inline-block; */
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
