<script setup lang="ts"></script>

<template>
  <div class="abs-wrapper">
    <div class="header-wrapper">
      <div class="letter"><span>Thomas Thorstensson</span></div>
      <div class="msg">New portfolio coming soon</div>
      <div class="hover">
        <span class="hover-fx cursor"><a>hello@thomasjt.com</a></span>
        <span aria-hidden="true" class="hover-fx"><a>hello@thomasjt.com</a></span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
// TODO: Tidy up this landing page CSS, but really neeed to deepdive now into my next portfolio

.a {
  text-decoration: none;
}

.abs-wrapper {
  position: absolute;
  width: 100%;
}

.header-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 70px;
  padding: 0 $page-hpad 0 $page-hpad;
  user-select: none;
  font-display: fallback;
  font-family: $sans-ui;
  color: $secondary;
  font-size: 15px;
}

.cursor {
  cursor:pointer;
}

.letter span::after {
  content: "";
  display: inline-block;
  width: 4px;
  height: 4px;
  background-color: #fff;
  border-radius: 50%;
  margin: 0px 0 -1px 2px;
}

span {
  display: inline-block;
}

.msg {
  display: none;

  @include this-and-above('lg') {
    display: block;
  }
}
</style>