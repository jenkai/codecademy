<template>
  <div class="page1">
    <div class="container">
      <div class="page1-1">
        <div class="grid">
          <div class="gridLeft">
            <img
              style="max-width: 27rem; margin-top:10px; margin-bottom:auto; margin-left:auto;margin-right:auto;"
              src="https://www.codecademy.com/webpack/01b4bd787ae0997f25109be2e7963559.png"
            />
          </div>
          <div class="gridRight">
            <div class="flexRight">
              <h1>
                Join the millions learning to code with Codecademy for free
              </h1>
              <div class="registerBox">
                <div class="inputBox">
                  <label>Email</label>
                  <input type="text" />
                </div>
                <div class="inputBox">
                  <label
                    >Password<svg
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 140 140"
                      fill="currentColor"
                      role="img"
                      aria-hidden="false"
                      @click="isPopup"
                    >
                      <title>Mini Info Outline Icon</title>
                      <g
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="10"
                      >
                        <path
                          d="M5 70a65 65 0 10130 0A65 65 0 105 70zm65 0v35"
                        ></path>
                        <path d="M65 45a5 5 0 1010 0 5 5 0 10-10 0z"></path>
                      </g></svg
                  ></label>
                  <Popup v-if="popup" />
                  <input type="password" />
                </div>

                <div class="signupBox">
                  <button>Sign up</button>
                </div>
                <small>
                  <p>
                    By signing up for Codecademy, you agree to <br />
                    Codecademy's <a href="/">Terms of Service</a> &amp;
                    <a href="/">Privacy Policy</a>.
                  </p>
                </small>
                <h2>Or sign up using:</h2>
                <div class="logoBox">
                  <div class="box1">
                    <svg
                      width="18"
                      height="18"
                      viewBox="0 0 980 980"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <title>LinkedIn</title>
                      <path
                        d="M882 0H98C44.1 0 0 44.1 0 98v784c0 53.9 44.1 98 98 98h784c53.9 0 98-44.1 98-98V98c0-53.9-44.1-98-98-98zM294 833H147V392h147v441zm-73.5-524.3c-49 0-88.2-39.2-88.2-88.2s39.2-88.2 88.2-88.2 88.2 39.2 88.2 88.2-39.2 88.2-88.2 88.2zM833 833H686V573.3c0-39.2-34.3-73.5-73.5-73.5S539 534.1 539 573.3V833H392V392h147v58.8c24.5-39.2 78.4-68.6 122.5-68.6 93.1 0 171.5 78.4 171.5 171.5V833z"
                        fill="#0E76A8"
                        fill-rule="nonzero"
                      ></path>
                    </svg>
                  </div>
                  <div class="box2">
                    <svg width="18" height="18">
                      <title>Google</title>
                      <g fill="none" fill-rule="evenodd">
                        <path
                          d="M9 3.48c1.69 0 2.83.73 3.48 1.34l2.54-2.48C13.46.89 11.43 0 9 0 5.48 0 2.44 2.02.96 4.96l2.91 2.26C4.6 5.05 6.62 3.48 9 3.48z"
                          fill="#EA4335"
                        ></path>
                        <path
                          d="M17.64 9.2c0-.74-.06-1.28-.19-1.84H9v3.34h4.96c-.1.83-.64 2.08-1.84 2.92l2.84 2.2c1.7-1.57 2.68-3.88 2.68-6.62z"
                          fill="#4285F4"
                        ></path>
                        <path
                          d="M3.88 10.78A5.54 5.54 0 0 1 3.58 9c0-.62.11-1.22.29-1.78L.96 4.96A9.008 9.008 0 0 0 0 9c0 1.45.35 2.82.96 4.04l2.92-2.26z"
                          fill="#FBBC05"
                        ></path>
                        <path
                          d="M9 18c2.43 0 4.47-.8 5.96-2.18l-2.84-2.2c-.76.53-1.78.9-3.12.9-2.38 0-4.4-1.57-5.12-3.74L.97 13.04C2.45 15.98 5.48 18 9 18z"
                          fill="#34A853"
                        ></path>
                        <path d="M0 0h18v18H0V0z"></path>
                      </g>
                    </svg>
                  </div>
                  <div class="box3">
                    <svg width="18" height="18">
                      <title>Facebook</title>
                      <path
                        d="M18 1v16c0 .5-.4 1-1 1h-4.6v-7h2.3l.3-2.7h-2.7V6.6c0-.8.2-1.3 1.4-1.3h1.4V2.8c-.2 0-1.1-.1-2.1-.1-2 0-3.4 1.3-3.4 3.6v2H7.3V11h2.3v7H1c-.5 0-1-.4-1-1V1c0-.5.4-1 1-1h16c.6 0 1 .4 1 1z"
                        fill="#3B5998"
                        fill-rule="evenodd"
                      ></path>
                    </svg>
                  </div>
                  <div class="box4">
                    <svg width="18" height="18">
                      <title>Github</title>
                      <path
                        d="M9 0C4.027 0 0 4.03 0 9a9 9 0 0 0 6.154 8.539c.45.084.615-.194.615-.433 0-.214-.008-.78-.011-1.53-2.504.543-3.032-1.208-3.032-1.208-.41-1.039-1.001-1.316-1.001-1.316-.816-.558.063-.546.063-.546.903.063 1.378.926 1.378.926.803 1.376 2.107.98 2.621.749.081-.582.313-.98.57-1.204-1.999-.225-4.099-1-4.099-4.447 0-.982.349-1.786.926-2.416-.101-.227-.405-1.141.079-2.381 0 0 .753-.242 2.475.922a8.66 8.66 0 0 1 2.25-.304 8.66 8.66 0 0 1 2.25.304c1.71-1.164 2.463-.922 2.463-.922.484 1.24.18 2.154.09 2.381.574.63.923 1.434.923 2.416 0 3.457-2.104 4.219-4.106 4.44.315.27.607.821.607 1.665 0 1.204-.011 2.171-.011 2.464 0 .236.157.517.619.427A8.968 8.968 0 0 0 18 9a9 9 0 0 0-9-9"
                        fill-rule="evenodd"
                      ></path>
                    </svg>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Popup from "./Popup.vue";

export default {
  components: {
    Popup,
  },
  created() {
    console.log(this.popup);
  },
  data() {
    return {
      popup: false,
    };
  },

  methods: {
    isPopup() {
      this.popup = !this.popup;
      console.log(this.popup);
    },
  },
};
</script>

<style scoped>
.page1 {
  height: 1000px;
  background-color: #fff0e6;
}
.container {
  height: 100%;
  padding: 0 6rem;
}

.page1-1 {
  height: 70%;
  padding-bottom: 2rem;
  padding-top: 1rem;
}

.grid {
  grid-template-columns: repeat(12, minmax(0, 1fr));
  display: grid;
  width: 100%;
  height: 100%;
  padding-top: 2rem;
  padding-bottom: 2rem;
  row-gap: 2rem;
}

.gridLeft {
  display: flex;
  justify-content: center;
  grid-column-end: span 6;
}

.gridRight {
  display: flex;
  justify-content: center;
  grid-column-end: span 6;
}

.flexRight {
  display: flex;
  flex-direction: column;

  max-width: 25rem;
}

.registerBox {
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
}

h1 {
  font-size: 1.625rem;
  margin: 0;
  padding-bottom: 1rem;
  line-height: 1.5;
}

.inputBox {
  width: 100%;
  margin-bottom: 30px;
  position: relative;
}

input {
  padding-left: 0.5rem;
  padding-top: 0.9rem;
  padding-bottom: 0.9rem;
  font-weight: 400;
  font-size: 1rem;
  width: 90%;
}

label {
  width: 90%;
  margin-bottom: 8px;
  display: flex;

  justify-content: space-between;
  align-items: center;
  font-size: 1rem;
  font-weight: normal;
}
label > svg {
  height: 12px;
  margin-right: 6px;
}
button {
  cursor: pointer;
  border-color: transparent;
  position: relative;
  border-radius: 4px;
  padding-left: 1rem;
  padding-right: 1rem;
  padding-top: 0.2rem;
  padding-bottom: 0.25rem;
  background-color: #3a10e5;
  font-weight: 700px;
  font-size: 16px;
  line-height: 24px;
  color: white;
  transition: all 0.2s ease-in-out;
  min-width: 40px;
  height: 40px;
}

button:hover {
  background-color: #5533ff;
}

small {
  color: #424242;
  margin-top: 4px;
  margin-bottom: 4px;
  font-weight: 400;
  line-height: 1.5;
  font-size: 0.875rem;
  display: inline-block;
}

h2 {
  font-weight: 700;
  font-size: 1rem;
  margin-bottom: 1rem;
  margin-top: 0;
}

.logoBox {
  display: flex;
  width: 100%;
}

.logoBox > div {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 60px;
  background-color: white;
  border: 1px solid #10162f;
  border-radius: 2px;
  margin-right: 10px;
  transition: all 0.2s;
}

.logoBox > div:hover {
  background-color: #f3f3f5;
  cursor: pointer;
}
</style>
