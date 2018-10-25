<template>

<div class="flip flip-vertical">
    <div class="front"
    :style="{backgroundImage: 'url('+ thumbnail + ')'}">
       <h1 class="text-shadow">{{title}}</h1>
    </div>
    <div class="back">
       <h2>{{ title }}</h2>
       <p>{{ previewText }}</p>
        <div class="btn-bg bg-1">
    <div class="btn btn-1">
     <nuxt-link :to="'repo/asian/' + id" ><a>
        <button>เ ส พ</button></a>
    </nuxt-link>
    </div>
  </div>
    </div>
</div>

</template>

<script>
export default {
  name: "Mode",
  props: {
    id: {
      type: String,
      require: true
    },
    title: {
      type: String,
      require: true
    },
    previewText: {
      type: String,
      require: true
    },
    thumbnail: {
      type: String,
      require: true
    }
  }
};
</script>


<style scoped>
body .btn-bg.bg-1 .btn-1 button {
  color: #c7f8f9;
  font-size: 2.5rem;
  background: transparent;
  border: 3px solid #c7f8f9;
  border-radius: 5px;
  -webkit-transition: all 0.5s ease;
  transition: all 0.5s ease;
  -webkit-transform: translate(0, 0);
  transform: translate(0, 0);
}
body .btn-bg.bg-1 .btn-1 button a {
  color: #c7f8f9;
}
.btn .btn-1 {
  cursor: pointer;
}
body .btn-bg.bg-1 .btn-1 button:hover {
  background: #c7f8f9;
  color: #6ab1c9;
  border: 3px solid #6ab1c9;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}
body .btn-bg.bg-1 .btn-1 button:hover > a {
  color: #6ab1c9;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}
body .btn-bg.bg-1 .btn-1 button:active {
  -webkit-transform: translate(5px, 5px);
  transform: translate(5px, 5px);
}
h1 {
  font-size: 2.2em;
  text-align: center;
}

.flip {
  position: relative;
}
.flip > .front,
.flip > .back {
  display: block;
  transition-timing-function: cubic-bezier(0.175, 0.885, 1.32, 1.275);
  transition-duration: 0.5s;
  transition-property: transform, opacity;
}
.flip > .front {
  transform: rotateY(0deg);
}
.flip > .back {
  text-align: center;
  position: absolute;
  opacity: 0;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  transform: rotateY(-180deg);
}
.flip:hover > .front {
  transform: rotateY(180deg);
}
.flip:hover > .back {
  opacity: 1;
  transform: rotateY(0deg);
}
.flip.flip-vertical > .back {
  transform: rotateX(-180deg);
}
.flip.flip-vertical:hover > .front {
  transform: rotateX(180deg);
}
.flip.flip-vertical:hover > .back {
  transform: rotateX(0deg);
}

.flip {
  position: relative;
  display: inline-block;
  margin-right: 2px;
  margin-bottom: 1em;
  width: 400px;
}
.flip > .front,
.flip > .back {
  display: block;
  color: white;
  width: inherit;
  background-size: cover !important;
  background-position: center !important;
  height: 220px;
  padding: 1em 2em;
  background: #313131;
  border-radius: 10px;
}
.flip > .front p,
.flip > .back p {
  font-size: 0.9125rem;
  line-height: 160%;
  color: #fff;
}

.text-shadow {
  text-shadow: 1px 1px rgba(0, 0, 0, 0.04), 2px 2px rgba(0, 0, 0, 0.04),
    3px 3px rgba(0, 0, 0, 0.04), 4px 4px rgba(0, 0, 0, 0.04),
    0.125rem 0.125rem rgba(0, 0, 0, 0.04), 6px 6px rgba(0, 0, 0, 0.04),
    7px 7px rgba(0, 0, 0, 0.04), 8px 8px rgba(0, 0, 0, 0.04),
    9px 9px rgba(0, 0, 0, 0.04), 0.3125rem 0.3125rem rgba(0, 0, 0, 0.04),
    11px 11px rgba(0, 0, 0, 0.04), 12px 12px rgba(0, 0, 0, 0.04),
    13px 13px rgba(0, 0, 0, 0.04), 14px 14px rgba(0, 0, 0, 0.04),
    0.625rem 0.625rem rgba(0, 0, 0, 0.04), 16px 16px rgba(0, 0, 0, 0.04),
    17px 17px rgba(0, 0, 0, 0.04), 18px 18px rgba(0, 0, 0, 0.04),
    19px 19px rgba(0, 0, 0, 0.04), 1.25rem 1.25rem rgba(0, 0, 0, 0.04);
}
</style>
