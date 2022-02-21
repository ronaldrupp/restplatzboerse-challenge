<template>
  <div id="app">
    <teaser-slider :destinations="destinations" />
  </div>
</template>

<script>
import TeaserSlider from "@/components/TeaserSlider.vue";
export default {
  name: "App",
  components: { TeaserSlider },
  data() {
    return {
      destinations: [
        {
          text: "Ägypten",
          price: 1237,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
        {
          text: "Griechenland",
          price: 334,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
        {
          text: "Türkei",
          price: 237,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
        {
          text: "Italien",
          price: 237,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
        {
          text: "Spanien",
          price: 379,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
        {
          text: "Kroatien",
          price: 88,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
        {
          text: "Österreich",
          price: 0,
          image: "https://images.flux.reisen/hotel/1262/1/s",
          link: "https://google.com",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
  box-sizing: border-box;
  text-decoration: none;
}
/* HTML5 display-role reset for older browsers */
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}
body {
  line-height: 1;
}
ol,
ul {
  list-style: none;
}
blockquote,
q {
  quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}

:root {
  --aqua-color: #16828f;
  --greyish-color: #525252;
  --greenish-color: #d9e15f;
  --purple-color: #a11a79;
  --title-font-family: "Quicksand";
  --main-font-family: "Open Sans";
}
body {
  background-color: #fafafa;
}
#app {
  width: 375px;
  height: 812px;
  margin: 1em auto;
  padding-block: 5em;
  background-color: white;
}
</style>
