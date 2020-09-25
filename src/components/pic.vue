<template>
  <onDisplay>
    <strong class="display-2">Space Trip</strong><br>
    <input class="ml-1" type="text" placeholder="Year " v-model="YearID" />
    <input class="ml-1" type="text" placeholder="Month " v-model="MonthID" />
    <input class="ml-1" type="text" placeholder="Day " v-model="DayID" />
    <button class="ml-1" @click="searchData()">Search</button>
    <br />
    <br />

    <!---{{playList}}--->
     <a-card
      v-for="l in ID"
      :key="l.date"
      :title="l.title"
      :img-src="l.hdurl"
      :explanation="l.explanation"
      >
      <b-card class="row">
        <img style="max-width:50%" :src="l.hdurl" />
        <div class="col">
          {{ l.date }}
          <br />
          {{ l.title }}
          <br />
         {{ l.explanation }}
        </div>
      </b-card>

    </a-card>
  </onDisplay>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      ID: null,
      DayID: "",
      MonthID: "",
      YearID: "",
      DateID: "",
    };
  },
  methods: {
    searchData() {
      this.DateID = this.YearID + "-" + this.MonthID + "-" + this.DayID;
      axios
        .get(
          "https://api.nasa.gov/planetary/apod?date="+this.DateID+"&hd=true&api_key=iK6QWVlZ9w0RUsSNWob3UL5KcXFehRlXBHvKuW6p"
        )
        .then((response) => {
          this.ID = response;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style>
input {
  width: 115px;
}
.ml-1{
    font-family: 'Titillium Web', sans-serif;
    text-align: center;
}
</style>