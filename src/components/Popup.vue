<template>
  <div class="window">
    <p class="title">
      Codecademy requires that you have a secure password. If your password is
      too weak, make sure you:
    </p>
    <ul>
      <li>Use at least 6 characters</li>
      <li>Use a mix of upper and lower case characters</li>
      <li>Use at least 1 number</li>
      <li>Use at least 1 special character like “.”, “&”, or “*”</li>
      <li>
        Do not use common words or simple passwords like “password”, “qwerty”,
        or “123456”
      </li>
    </ul>
  </div>
</template>

<style scoped>
.window {
  top: 34px;
  right: 10px;
  width: 450px;
  position: absolute;
  background-color: white;
  border: 1px solid black;
  border-radius: 3px;
  padding: 1rem;
  font-size: 0.875rem;
  line-height: 1.5;
  z-index: 1;
}

.title {
  font-size: 1.1rem;
}

ul {
  display: block;
  line-height: 1.5;

  margin: 1rem 0;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 40px;
}
li {
  display: list-item;
  margin-bottom: 0.5rem;
  font-size: 1.1rem;
  line-height: 1.6;
}
</style>
