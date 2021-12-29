<template>
  <div class="why_us">
    <div class="why_us-title">Чому обирають PlayRoom? Цінності та методика</div>
    <v-sheet
      class="mx-5"
      elevation="0"
      max-width="100%"
      height="300px"
      style="background-color: #ffffff"
    >
      <v-slide-group v-model="model" class="pa-0" height="300px" show-arrows>
        <v-slide-item v-for="item in items" :key="item.message">
          <v-card
            height="256"
            width="200"
            style="
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              align-items: center;
              margin: 10px 30px;
              background-color: #fff;"
          >
            <div
              class="card__title"
              style="margin-top: 12px;
                  text-align: center;
                  font-size: 15px;
                  font-weight: 600;
                  color: #BEA32E;"
            >
              {{ item.message }}
            </div>
            <div class="card__img"><img :src="item.img" alt="" /></div>
            <v-btn
              @click="openModal(item.modal)"
              style="
                margin-bottom: 12px;
                text-transform: capitalize;
                width: 130px;
                height: 30px;
                background: linear-gradient(90deg, #ECE9E6 0%, #FFFFFF 100%);
                box-shadow: 3px 3px 2px rgba(143, 176, 186, 0.8);
                border-radius: 2px;
                color: #79885C;
              "
            >Детальніше</v-btn
            >
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
    <v-overlay v-if="modalData" :z-index="99999" :value="overlay">
      <div class="overlay-bg" style="
        background-color: #fff;
        display: flex;
        flex-direction: column;
        color: black;
        margin: 0 auto;
        align-items: center;
        padding: 40px 20px;
        border-radius: 20px;
        ">
        <div class="overlay-title" style="
            font-size: 30px;
            font-weight: 600;
            color: #BEA32E;"
        >{{modalData.title}}</div>
        <div class="overlay-img" style="
            width: 302px;
            height: 245px;
            display: flex;
            justify-content: center;
          ">
          <img :src="modalData.img" alt="" style="
            width: 150px;
            "/>
        </div>
        <div class="overlay-text" style="
            max-width: 500px;
            text-align: center;
          ">
          {{modalData.text}}
        </div>
        <v-btn
          style="
                margin-top: 20px;
                text-transform: capitalize;
                width: 130px;
                height: 30px;
                background: linear-gradient(90deg, #ECE9E6 0%, #FFFFFF 100%);
                box-shadow: 3px 3px 2px rgba(143, 176, 186, 0.8);
                border-radius: 2px;
                color: #79885C;
          "
          @click="closeModal"
        >
          Закрити
        </v-btn>
      </div>
    </v-overlay>
  </div>
</template>

<script>
export default {
  name: "Why_us",
  data: () => ({
    overlay: false,
    zIndex: 0,
    model: null,
    modalData: null,
    items: [
      {
        message: "Circle Time",
        img: require("../../assets/Home/whyus/Circle.svg"),
        modal: {
          title: "Circle Time",
          img: require("../../assets/Home/whyus/Circle.svg"),
          text:
            "Привітання в колі, дискусії на теми погоди, емоцій та настрою,\n" +
            "розвиток комунікативних навичок за допомогою різних ігор. Виконання\n" +
            "фізичних вправ за допомогою активних рухливих ігор та пісень, вивчення\n" +
            "тематичних дитячих пісеньок англійською мовою.",
        },
      },
      {
        message: "Math and Logics",
        img: require("../../assets/Home/whyus/MAth.svg"),
        modal: {
          title: "Math and Logics",
          img: require("../../assets/Home/whyus/MAth.svg"),
          text:
            "Розвиток логіки, уваги,зорової пам’яті, дрібної моторики рук. A також, цифрових рядів від 1-5, 1-10, 1-15, 10-25 залежно від віку дитини. Навчання додаванню та відніманню, вивчення понять “один-багато”, “більше –менше”; вивчення назв фігур, кольорів, розміру та довжини предметів.",
        },
      },
      {
        message: "Letters and Sounds",
        img: require("../../assets/Home/whyus/Letters.svg"),
        modal: {
          title: "Letters and Sounds",
          img: require("../../assets/Home/whyus/Letters.svg"),
          text:
            "Вивчення звуків і літер англійського алфавіту, збагачення словникового запасу рядами слів. Розвиток  монологічного та діалогічного мовлення, Підготовка до читання та письма. Розвиток комунікативних навичок",
        },
      },
      {
        message: "Letter Craft",
        img: require("../../assets/Home/whyus/LetterCraft.svg"),
        modal: {
          title: "Letter Craft",
          img: require("../../assets/Home/whyus/LetterCraft.svg"),
          text:
            "Повторення та закріплення вивченого на уроках Letters and Sounds",
        },
      },
      {
        message: "Book Corner",
        img: require("../../assets/Home/whyus/BookCorner.svg"),
        modal: {
          title: "Book Corner",
          img: require("../../assets/Home/whyus/BookCorner.svg"),
          text:
            "Читання художніх творів світових дитячих авторів  та робота з книгою, виховання культури поведінки з книжками, розуміння їх цінності. Дискусії та обговорення сюжету книги, набуття і розвиток вміння вести короткий послідовний переказ її змісту .",
        },
      },
      {
        message: "English Language Arts ( з носієм мови )",
        img: require("../../assets/Home/whyus/LanguageArt.svg"),
        modal: {
          title: "English Language Arts ( з носієм мови",
          img: require("../../assets/Home/whyus/LanguageArt.svg"),
          text:
            "Розвиток комунікативних навичок, закладання основ граматики шляхом невимушеного спілкування та гри, активне поповнення словникового запасу, розвиток вміння сприймати мову на слух.",
        },
      },
      {
        message: "Story Time with Art  ( з носієм мови )",
        img: require("../../assets/Home/whyus/StoryTime.svg"),
        modal: {
          title: "Story Time with Art  ( з носієм мови )",
          img: require("../../assets/Home/whyus/StoryTime.svg"),
          text:
            "Читання і робота з книгою, обговорення сюжетів книг, розвиток вміння аналізувати та передбачати події, описувати головних героїв. Вивчення нових слів за допомогою їх візуалізації ( діти виготовляють тематичні поробки після прочитання книги).",
        },
      },
      {
        message: "Cooking",
        img: require("../../assets/Home/whyus/Cooking.svg"),
        modal: {
          title: "Cooking",
          img: require("../../assets/Home/whyus/Cooking.svg"),
          text:
            "Дітки мають можливість відчути себе справжніми кулінарами та засвоїти нову лексику, яка включає в себе назви різних продуктів-інгредієнтів, назви кухонного обладнання, назви технік і процесів приготування.",
        },
      },
      {
        message: "Drama play",
        img: require("../../assets/Home/whyus/Drama.svg"),
        modal: {
          title: "Drama play",
          img: require("../../assets/Home/whyus/Drama.svg"),
          text: "Заняття спрямовані на розвиток уяви, фантазії, уваги, творчих здібностей і ряд пунктів акторської техніки, адаптований для дітей молодшого шкільного віку",
        },
      },
      {
        message: "Dance",
        img: require("../../assets/Home/whyus/Dance.svg"),
        modal: {
          title: "Dance",
          img: require("../../assets/Home/whyus/Dance.svg"),
          text:
            "Курс занять, спрямований на розвиток координації, пластики, рухливості суглобів, еластичності м'язів та укріплення м'язового корсету. Діти навчаються чути музику, існувати в гармонії з нею, розвивають відчуття ритму.",
        },
      },
      {
        message: "Group Project",
        img: require("../../assets/Home/whyus/Groupe.svg"),
        modal: {
          title: "Group Project",
          img: require("../../assets/Home/whyus/Groupe.svg"),
          text:
            "Розвиток вміння працювати в команді, домовлятись і приймати спільні рішення, розвивати вміння працювати на результат внаслідок роботи над спільним проектом.",
        },
      },
      {
        message: "Smart Kid",
        img: require("../../assets/Home/whyus/SmartKid.svg"),
        modal: {
          title: "Smart Kid",
          img: require("../../assets/Home/whyus/SmartKid.svg"),
          text:
            "Підготовка та навчання читанню та письма українською мовою, закладання та розвиток основ математики та логіки.",
        },
      },
      {
        message: "Art",
        img: require("../../assets/Home/whyus/Art.svg"),
        modal: {
          title: "Art",
          img: require("../../assets/Home/whyus/Art.svg"),
          text:
            "Заняття знайомлять учнів із жанрами та видами мистецтва, та його майстрами. Діти отримують змогу мислити та творити як новатори.",
        },
      },
      {
        message: "Music",
        img: require("../../assets/Home/whyus/Music.svg"),
        modal: {
          title: "Music",
          img: require("../../assets/Home/whyus/Music.svg"),
          text:
            "Дітки не лише вивчають відомі музичні твори та вчаться співати, проте ознайомлюються з нотною грамотою, музичними інструментами.",
        },
      },
      {
        message: "Французька мова",
        img: require("../../assets/Home/whyus/Music.svg"),
        modal: {
          title: "Французька мова",
          img: require("../../assets/Home/whyus/Music.svg"),
          text:
            "Психологи рекомендують: вивчення декількох іноземних мов впливає на інтелектуальний розвиток дитини, соціальну адаптацію та самореалізацію. У веселій та дружній атмосфері, у поєднанні гри та навчання, наші студенти набудуть ефективних мовленнєвих навичок.",
        },
      },

    ],
  }),
  methods: {
    openModal(data) {
      this.modalData = data;
      this.overlay = true;
    },
    closeModal() {
      this.modalData = null;
      this.overlay = false;
    }
  },
};
</script>

<style scoped>
.why_us-title {
  margin: 50px auto;
  display: flex;
  justify-content: center;
  font-weight: 800;
  font-size: 40px;
  color: #7AD4CB;
  text-align: center;
}



</style>