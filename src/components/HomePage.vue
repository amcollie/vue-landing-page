<script>
export default {
  data() {
    return {
      title: 'Travel Treasury',
      email: '',
      message: '',
    }
  },
  methods: {
    async addEmail(email) {
      const noticeMessage = '🎉 Your account has been reserved 🎉'
      await Auth
    },
  },
}
</script>

<template>
  <div class="container-fluid m-0 p-0">
    <div class="full-height p-4" id="home-page">
      <div class="container pt-3">
        <div class="row pb-5">
          <div class="col-12 pt-4 my-auto">
            <div class="text-center mb-3 d-block d-lg-none">
              <h1 class="display-3">{{ title }}</h1>
              <h3>Find the World</h3>
            </div>
          </div>

          <div class="col-12 col-lg-6 pt-4 pb-5 my-auto">
            <img
              id="iphone-img"
              src="../assets/travelTreasuryiPhone.png"
              alt="iphone"
              class="mx-auto d-block"
            />
          </div>

          <div class="col-12 col-lg-6 my-auto pt-4">
            <div class="text-center mb-3 d-none d-lg-block">
              <h1 class="display-3">{{ title }}</h1>
              <h3>Find the World</h3>
            </div>

            <div class="text-center border p-3 p-md-5 bg-white rounded shadow">
              <h2>Coming Soon</h2>
              <form @submit.prevent="addEmail(email)">
                <div class="form-group">
                  <label for="email"
                    >Reserve your account now, we'll contact you when it's
                    live</label
                  >
                  <input
                    class="form-control"
                    text="email"
                    id="email"
                    name="email"
                    placeholder="enter email"
                  />
                  <small id="emailHelp" class="form-text text-muted">
                    We will <strong>never</strong> share your email address
                  </small>
                </div>
                <button type="submit" class="btn btn-success mt-3">
                  Join waiting list
                </button>
                <div class="mt-4">
                  <p class="m-0">{{ message }}</p>
                </div>
              </form>
            </div>

            <div id="available" class="p-2">
              <h4 class="text-center mb-2 mt-3 text-lighter">Available On</h4>
              <div class="row">
                <div class="col my-auto">
                  <img
                    src="../assets/download_apple.png"
                    alt="App Store Logo"
                    class="float-right img-fluid app_store_img"
                  />
                </div>
                <div class="col my-auto">
                  <img
                    src="../assets/download_google.png"
                    alt="Play Store Logo"
                    class="float-left img-fluid app_store_img"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row bg-light p-3 p-md-5" id="about">
      <div class="row">
        <div class="col-lg">
          <!-- Icon made by Freepik perfect from www.flaticon.com -->
          <img
            src="../assets/icons/app.svg"
            alt="app image"
            class="m-4 mx-auto d-block"
            height="120"
          />
          <h5 class="ml-md-4 mr-md-4">
            Plan your next adventure by setting a daily spending budget. We make
            it easy to break your expenses down by category, giving you more
            time to plan the important tings!
          </h5>
        </div>
        <div class="col-lg">
          <!-- Icon made by Freepik perfect from www.flaticon.com -->
          <img
            src="../assets/icons/piggy-bank.svg"
            alt="piggy bank image"
            height="120"
            class="m-4 mx-auto d-block"
          />
          <h5 class="ml-md-4 mr-md-4">
            Use the app to track how much money you’ve saved towards your trips
            total budgeted goal. Know exactly how much more you need to save,
            and how much time you have left to save.
          </h5>
        </div>
        <div class="col-lg">
          <!-- Icon made by Freepik perfect from www.flaticon.com -->
          <img
            src="../assets/icons/passport.svg"
            alt="passport image"
            height="120"
            class="m-4 mx-auto d-block"
          />
          <h5 class="ml-md-4 mr-md-4">
            When the day of your trip comes, have the peace of mind that you
            planned out your expenses. Never worry about money on a trip again!
          </h5>
        </div>
      </div>
    </div>

    <div class="bg-info p-4" id="contact">
      <h2>Have Any Question</h2>
      <p>Contact us by filling out the information below</p>
      <form>
        <div class="form-group text-left">
          <input
            type="email"
            class="form-control"
            placeholder="Enter your Email"
          />
          <textarea
            class="form-control mt-3"
            name="message"
            id="message"
            cols="30"
            rows="10"
          >
          </textarea>
        </div>
        <button type="submit" class="btn btn-primary mt-3">Send Message</button>
      </form>
    </div>
    <div class="row p-4" id="footer">
      <footer class="text-center text-light p-4">
        <a
          href="http://www.youtube.com/1manstartup"
          target="_blank"
          class="text-warning"
          >Build This App</a
        >
        <a href="#" class="text-warning">Privacy Policy</a>
        <br />
        <small>&copy; 2020, TravelTreasury.app</small>
      </footer>
    </div>
  </div>
</template>

<style scoped>
#home-page {
  background-color: #92d2f2;
  background: url('../assets/bg_mt.jpg') no-repeat center center;
  --webkit-background-size: cover;
  --moz-background-size: cover;
  --o-background-size: cover;
}

#about {
  min-height: 40vh;
}

#iphone-img {
  max-height: 80vh;
}

#footer {
  background-color: #252223;
}
.app_store_img {
  max-height: 80px;
}
</style>
