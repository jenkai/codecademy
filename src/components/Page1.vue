<template>
  <div class="page1">
    <div class="container">
      <div class="page1-1">
        <div class="grid">
          <div class="gridLeft">
            <img
              style="max-width: 26rem; margin:auto;"
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
                  <input type="text" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

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
</style>
