<template>
  <div class="text-center">
    <form class="form-signin">
      <div v-if="showError">
        <div id="alert" class="alert alert-warning" role="alert">
          {{ errorMsg }}
        </div>
      </div>
      <img
        class="mb-4"
        src="../assets/person-bounding-box.svg"
        alt=""
        width="72"
        height="72"
      />
      <h1 class="h3 mb-3 font-weight-normal">Customer sign in</h1>
      <label for="email" class="sr-only">Email</label>
      <input
        type="email"
        id="email"
        class="form-control"
        placeholder="Email"
        required
        v-model="email"
      />
      <label for="inputPassword" class="sr-only">Password</label>
      <input
        type="password"
        id="inputPassword"
        class="form-control"
        placeholder="Password"
        required
        v-model="inputpassword"
      />
      <button class="btn btn-lg btn-primary btn-block" type="submit" @click="login(email, inputpassword)">
        Sign in
      </button>
      <p>Don't have an account? <a href="#/customer-register">Register now</a></p>
      <p class="mt-5 mb-3 text-muted">&copy; 2020</p>
    </form>
  </div>
</template>

<script src='./customerLoginPage.js'>

</script>

<style scoped>
.text-center {
  display: -ms-flexbox;
  display: flex;
  -ms-flex-align: center;
  align-items: center;
  padding-top: 100px;
  padding-bottom: 10px;
  background-color: #f5f5f5;
}
.form-signin {
  width: 100%;
  max-width: 330px;
  padding: 15px;
  margin: auto;
}
.form-signin .form-control {
  position: relative;
  box-sizing: border-box;
  height: auto;
  padding: 10px;
  font-size: 16px;
}
.form-signin .form-control:focus {
  z-index: 2;
}
.form-signin input[type="email"] {
  margin-bottom: 10px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.form-signin input[type="password"] {
  margin-bottom: 10px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
</style>