<template>
  <div class="container">
    <div class="row mt-4">
      <div class="col-md-8 offset-md-2">
        <h3>File a Complain</h3>
        <form>
          <div class="form-group">
            <label>Email address</label>
            <input type="email" v-model="userData.email" class="form-control" placeholder="Enter email">
          </div>

          <div class="form-group">
            <label>Password</label>
            <input type="password" v-model="userData.password" class="form-control" placeholder="Password">
          </div>

          <div class="form-group">
            <label>Age</label>
            <input type="number" v-model="userData.age" class="form-control" placeholder="Enter Age">
            <small class="form-text text-muted"></small>
          </div>

          <div class="form-group">
            <label>Message</label>
            <textarea class="form-control" cols="30" rows="5" placeholder="Enter Message"></textarea>
          </div>

          <div class="form-group form-inline">
            <div class="custom-control custom-checkbox my-1 mr-sm-2">
              <input type="checkbox" class="custom-control-input" id="mail">
              <label class="custom-control-label" for="mail">Send Mail</label>
            </div>
            <div class="custom-control custom-checkbox my-1 mr-sm-2">
              <input type="checkbox" class="custom-control-input" id="mailinfo">
              <label class="custom-control-label" for="mailinfo">Send Infomail</label>
            </div>
          </div>

          <div class="form-group">
            <div class="custom-control custom-radio custom-control-inline">
              <input type="radio" id="male" class="custom-control-input">
              <label class="custom-control-label" for="male">Male</label>
            </div>
            <div class="custom-control custom-radio custom-control-inline">
              <input type="radio" id="female" class="custom-control-input">
              <label class="custom-control-label" for="female">Female</label>
            </div>
          </div>

          <div class="form-group">
            <label class="mr-sm-2">Priority</label>
            <select class="custom-select mr-sm-2">
              <option selected>Choose...</option>
              <option value="1">One</option>
              <option value="2">Two</option>
              <option value="3">Three</option>
            </select>
          </div>

          <button type="submit" class="btn btn-primary">Submit</button>
        </form>
      </div>
    </div>

    <div class="row my-5">
      <div class="col-md-8 offset-md-2">
        <div class="card">
          <div class="card-header">
            Result
          </div>
          <div class="card-body">
            <p class="card-text">Email: {{ userData.email }}</p>
            <p class="card-text">Password: {{ userData.password }}</p>
            <p class="card-text">Age: {{ userData.age }}</p>
            <p class="card-text">Message</p>
            <p class="card-text">Send Mail ?</p>
            <ul>
              <li></li>
            </ul>
            <p class="card-text">Gender: </p>
            <p class="card-text">Priority: </p>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
        userData: {
          email: '',
          password: '',
          age: null
        }
    }
  }

}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
