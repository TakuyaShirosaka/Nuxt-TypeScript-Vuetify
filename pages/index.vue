<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-xs-center">
        <logo/>
        <vuetify-logo/>
      </div>
      <v-card>
        <v-card-title class="headline">Welcome to the Vuetify + Nuxt.js + TypeScript template</v-card-title>
        <v-card-text>
          <p>Vuetify + Nuxt.js + TypeScriptの組み合わせのテンプレートです。</p>
          <p>Vuetifyは何となくサンプルが格好良かったので採用しました。</p>
          <p>ライブラリはaxiosを入れてます。後は煮るなり焼くなりお好きにどうぞ。</p>
          <p>各モジュールはコミット時(19/4/16)時点でncuコマンドを実行してます。</p>
          <div class="text-xs-right">
            <em>
              <small>&mdash; 002418782</small>
            </em>
          </div>
          <hr class="my-3">
          <a href="https://nuxtjs.org/" target="_blank">Nuxt Documentation</a>
          <br>
          <a href="https://github.com/nuxt/nuxt.js" target="_blank">Nuxt GitHub</a>
        </v-card-text>
        <v-card-actions>
          <v-spacer/>
          <v-btn color="primary" flat nuxt to="/inspire">Continue</v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script lang="ts">
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

//letが使えるよ
let message: String = "Hello World";

//classも使える、C#とかJavaに感覚的に近い
class Person {
  name: String;
  age: Number;

  constructor(name: String, age: Number) {
    this.name = name;
    this.age = age;
  }

  public getName() {
    alert(
      "この画面は" +
        this.name +
        "プロジェクトの空き時間で考案しているものです。"
    );
  }
}

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  mounted() {
    const newPerson = new Person("どこかの", 11);
    newPerson.getName();
  }
};
</script>
