<template>
  <div class="vue-tempalte">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- Navigation -->
    <nav class="navbar shadow bg-white rounded justify-content-between flex-nowrap flex-row fixed-top">
      <div class="container">

        <ul class="nav navbar-nav flex-row float-right">
          <li class="nav-item">
            <router-link class="btn btn-outline-primary" to="/">Sign in</router-link>
          </li>
          <li class="nav-item">
            <router-link class="btn btn-outline-primary" to="/signup">Sign up</router-link>
          </li>
          <!-- <li class="nav-item">
            <router-link class="btn btn-outline-primary" to="/forgot-password">forgot password</router-link>
          </li> -->
        </ul>
      </div>
    </nav>

    <!-- Main -->
    <div class="App">
      <div class="vertical-center">
        <div class="inner-block">
          <router-view />
        </div>
      </div>
    </div>
  </div>
</template>
