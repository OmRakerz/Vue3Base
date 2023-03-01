<script>
import Employee from "./components/Employee.vue";
export default {
  components: {
    Employee,
  },

  name: "App",
  data() {
    return {
      //Задание №1
    };
  },

  methods: {
    //Задание №1
  },
};
</script>

<template>
  <!-- <h1>Упражнение №64</h1>
  <br /> -->
  <i></i>
  <h1>Однонаправленный поток данных в Vue</h1>
  <br />

  <p>
    Все входные параметры образуют одностороннюю привязку между дочерним
    свойством и родительским: когда родительское свойство обновляется - оно
    будет передаваться дочернему, но не наоборот. Это предотвращает случайное
    изменение дочерними компонентами родительского состояния, что может
    затруднить понимание потока данных вашего приложения.
  </p>
  <br />
  <p>
    Кроме того, каждый раз, когда обновляется родительский компонент, все
    входные параметры дочернего компонента будут обновлены актуальными
    значениями. Это означает, что<i>
      вы не должны пытаться изменять входной параметр внутри дочернего
      компонента</i
    >. Если вы это сделаете, Vue отобразит предупреждение в консоли.
  </p>
  <br />
  <p>
    Обычно встречаются два случая, когда возникает соблазн изменять входной
    параметр. Давайте их рассмотрим.
  </p>

  <br />
  <br />

  <h1>Случай первый</h1>
  <p>
    Входной параметр используется для передачи начального значения; дочерний
    компонент хочет использовать его как локальное свойство данных в дальнейшем.
    В этом случае лучше всего определить локальное свойство в данных, которое
    использует значение входного параметра в качестве начального:
  </p>

  <p class="ul">
    props: ['initialCounter'], data() { return { counter: this.initialCounter };
    }
  </p>

  <br />
  <br />

  <h1>Случай второй</h1>

  <p>
    Входной параметр передаётся как необработанное значение, которое необходимо
    преобразовать. В этом случае лучше всего определить вычисляемое свойство с
    использованием входного параметра:
  </p>

  <p class="ul">
    props: ['size'], computed: { normalizedSize: function() { return
    this.size.trim().toLowerCase(); } }
  </p>

  <br />
  <br />

  <h2>Замечание</h2>
  <p>
    Обратите внимание, что объекты и массивы в JavaScript передаются по ссылке,
    поэтому если входной параметр массив или объект, то изменения внутри
    дочернего компонента этого объекта или массива будет влиять на состояние
    родителя и Vue не в состоянии предупредить об этом. Следует избегать любых
    мутаций входных параметров, в том числе объектов и массивов, так как
    игнорирование одностороннего связывания данных может привести к
    нежелательным результатам.
  </p>
  <!-- Задание №1 -->
  <!-- <h2>Задание №1</h2> -->

  <Employee />
</template>

<style>
/* Стиль упражнений */
body {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url(../background.png);
  background-position: 0 0;
  background-repeat: no-repeat;
  background-size: cover;
  font-family: sans-serif;
  background-attachment: fixed;
}

h1 {
  text-transform: uppercase;
  text-align: center;
  margin-top: 50px;
  font-size: 50px;
  color: #4682b4;
}

h2 {
  margin-top: 30px;
  margin-left: 10px;
  font-size: 35px;
  color: #008080;
}

p {
  font-size: 25px;
  display: block;
  width: 80%;
  color: white;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  margin: 10px;
}

.ul {
  color: #00bfff;
  font-size: 20px;
}

a {
  font-family: sans-serif;
  font-size: 20px;
  margin-left: 10px;
}
/* ---------------- */

.button {
  color: #4682b4;
  text-align: center;
  font-size: 20px;
  margin: 4px 0;
  border-radius: 40px;
}

span {
  color: #00bfff;
  font-size: 20px;
}

.input {
  color: #4682b4;

  font-size: 20px;
  text-align: center;
  border-radius: 40px;
  width: 100px;
}

table {
  color: aqua;
  border: 1px solid white;
  margin: 10px;
  font-size: 20px;
  text-align: center;
}

td,
th {
  padding: 5px;
}
</style>
