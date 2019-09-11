<template>
  <div id="app">
    
    <b-navbar toggleable="md" type="dark" variant="info">

  <b-container>
    <b-navbar-toggle target = "nav_collapse"></b-navbar-toggle>
    <b-nav-brand href="#">NavBar</b-nav-brand>
    <b-collapse is-nav id="nav_collapse">
        <b-navbar-nav style="width: 100%" justified  class="mt-4">
          <b-nav-item :to="{name:'home'}" exact>Home</b-nav-item>
          <b-nav-item :to="{name:'about'}" >About</b-nav-item>
          <b-nav-item :to="{name:'grid'}" >Grid</b-nav-item>
          <b-nav-item :to="{name:'card'}" >Card</b-nav-item>
          <b-nav-item :to="{name:'form'}" >Form</b-nav-item>
        </b-navbar-nav>
    </b-collapse>    
  </b-container>

</b-navbar>
  <b-container>
    <router-view/>
  </b-container>
  
  </div>
</template>