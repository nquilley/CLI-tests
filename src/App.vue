<template>
  <div id="app">
    
    <app-header :title="title" @changeTitle="updateTitle($event)"></app-header>
    <app-ninjas :ninjas="ninjas"></app-ninjas>   
    <app-footer :title="title"></app-footer>
  </div>
</template>

<script>
import Ninjas from './components/Ninjas.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    'app-ninjas':Ninjas,
    'app-header':Header,
    'app-footer':Footer
  },
  data(){
    return{
      ninjas: [
                {name: 'Ryu', speciality: 'Vue Components', show: false},
                {name: 'Crystal', speciality: 'HTML Wizardry', show: false},
                {name: 'Hitoshi', speciality: 'Click Events', show: false},
                {name: 'Tango', speciality: 'Conditionals', show: false},
                {name: 'Kami', speciality: 'Webpack', show: false},
                {name: 'Yoshi', speciality: 'Data Diggin', show: false}
          ],
      title: 'Vue Ninjas'
    }
  },
  methods: {
    updateTitle: function(updatedTitle){
      this.title = updatedTitle
    }
  }
}
</script>

<style>

</style>
