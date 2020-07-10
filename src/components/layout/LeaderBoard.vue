<template>
  <div class="leaderboard">
    <div class="main-header">
      <div>
        <h3>Community Leaderboards</h3>
      </div>
      <div class="main-header-icons">
        <span
          >{{ userRank }} <i class="fas fa-user"></i>
          <i class="fas fa-chevron-down"></i
        ></span>
        <span><i class="fas fa-arrow-right"></i></span>
        <span><i class="fas fa-bell"></i></span>
      </div>
    </div>

    <div class="leaderboard-fl white-box">
      <span>Forum</span> <span class="tab-active">Leaderboards</span>
    </div>

    <div class="white-box topic-percentage">
      <div>
        <div class="ten-place">
          <span>{{ tenPlace }}</span
          >%
        </div>
        <p class="pt-1">
          You have more total points than <span class="b-txt">{{ tenPlace }}%</span> of all
          other students
        </p>
      </div>
      <div>
        <p class="b-txt">Your primary topic percentile rankings</p>
        <div>
          <div class="two-place">
            <span>{{ twoPlace }}</span
            >%
          </div>
          <p class="pt-1">HTML</p>
        </div>
      </div>
    </div>
    <div class="lead-section">
      <h3>Badges Leaderboard</h3>
    </div>

    <div>
      <div class="badges-header">
        <span class="tab-active">This Week</span>
        <span>This Month</span>
        <span>All Time</span>
      </div>
      <Card />
    </div>
    <!-- <div class="lead-footer">
      <p>
        This week you're ranked 5815 out of 10720 students for badges earned!
      </p>
    </div> -->

    <div class="lead-section">
      <h3>Points Leaderboard</h3>
    </div>

    <div>
      <div class="badges-header points-header">
        <div>
          <span class="tab-active">This Week</span>
          <span>This Month</span>
          <span>All Time</span>
        </div>

        <div>
          <multiselect
            v-model="value"
            :options="options"
            :custom-label="nameWithLang"
            placeholder="Select one"
            label="name"
            track-by="name"
          ></multiselect>
        </div>
      </div>
      <Card />
    </div>
    <!-- <div class="lead-footer">
      <p>
        This week you're ranked 5815 out of 10720 students for points earned!
      </p>
    </div> -->

    <Footer class="footer" />
  </div>
</template>

<script>
import Card from "../Card";
import Footer from "../layout/Footer";
import Multiselect from "vue-multiselect";
export default {
  name: "LeaderBoard",
  components: {
    Card,
    Footer,
    Multiselect,
  },
  data() {
    return {
      userRank: 39,
      tenPlace: 10,
      twoPlace: 2,
      value: { topic: "All topics" },
      options: [
        { topic: "All topics" },
        { topic: "Rails" },
        { topic: "JavaScript" },
        { topic: "Laravel" },
        { topic: "HTML" },
      ],
    };
  },
  methods: {
    nameWithLang({ topic }) {
      return `${topic}`;
    },
  },
};
</script>

<style src="vue-multiselect/dist/vue-multiselect.min.css"></style>

<style scoped>
.leaderboard {
  padding: 1rem 2rem;
  font-weight: 600;
}

.main-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.main-header-icons {
  display: grid;
  grid-template-columns: auto auto auto;
  justify-content: space-evenly;
  align-items: center;
}

.main-header-icons span {
  padding: 0 1rem;
  display: flex;
  align-items: center;
  border-right: 1px solid black;
  color: #555555;
}

.main-header-icons span:last-of-type {
  padding-right: 0;
  border-right: none;
}

.fa-user {
  background: white;
  padding: 0.3rem;
  margin: 0 0.5rem;
  border-radius: 50%;
  border: 2px solid blue;
  color: #cbcbcc;
}

.white-box {
  background: white;
  margin: 2rem 0;
  padding: 1.5rem;
  border-radius: 4px;
  box-shadow: 0 0 1px 2px rgba(0, 0, 0, 0.05);
}

.leaderboard-fl, .badges-header {
  color: #cbcbcb;
}

.leaderboard-fl span:nth-of-type(1) {
  margin-right: 2rem;
}

.tab-active {
  color: #555555;
}

.topic-percentage {
  display: grid;
  grid-template-columns: 40% 60%;
}

.topic-percentage > div:nth-of-type(1) {
  border-right: 1px solid #cbcbcc;
  padding-right: .5rem;
}

.topic-percentage > div:nth-of-type(2) {
  padding-left: 10%;
}

.topic-percentage > div:nth-of-type(2) > div {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: fit-content;
}

.topic-percentage > div:nth-of-type(2) > p {
  text-align: center;
}

.pt-1 {
  padding: 1rem 0 0;
  color: #cbcbcb;
}

.b-txt {
  color: #555555;
}

.ten-place {
  display: flex;
  align-items: center;
  font-weight: 600;
  color: white;
  background: #cbcbcc;
  padding: 2rem;
  border-radius: 50%;
  width: fit-content;
  margin-left: 10%;
}

.ten-place span {
  font-size: 3rem;
}

.two-place {
  display: flex;
  align-items: center;
  font-weight: 600;
  color: blue;
  padding: 1.5rem;
  border-radius: 50%;
  width: fit-content;
  border: 4px solid #cbcbcc;
}

.two-place span {
  font-size: 2.5rem;
}

.lead-section {
  margin: 2rem 0 1.5rem;
  color: #555555;
}

.lead-footer {
  background: white;
  padding: 2rem 1rem;
  text-align: center;
  font-weight: 600;
  color:  #555555;
}

.badges-header {
  background: white;
  padding: 1.5rem;
  margin-top: 1rem;
}

.badges-header span {
  padding-right: 3rem;
  font-weight: 700;
  /* color: #555555; */
}

.points-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.footer {
  margin: 8rem 0 0;
}
</style>
