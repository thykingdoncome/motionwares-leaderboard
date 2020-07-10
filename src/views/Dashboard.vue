<template>
  <div id="dashboard">
      <SideBar class="sideBar"/>
      <LeaderBoard />
  </div>
</template>

<script>
import SideBar from '../components/layout/SideBar'
import LeaderBoard from '../components/layout/LeaderBoard'


export default {
name: 'Dashboard',
components: {
    SideBar,
    LeaderBoard
}
}
</script>

<style scoped>

#dashboard {
    width: 100%;
    display: grid;
    grid-template-columns: 70px auto;
    background: #cbcbcc;
}

.sideBar {
    position: sticky;
    top: 0;
    left: 0;
}
</style>