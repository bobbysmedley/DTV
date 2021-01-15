<template>
  <iframe :src="url" width="75%" height="500" frameborder="0" scrolling="auto" allowtransparency="true"></iframe>
</template>

<script>
export default {
  name: "Bracket",
  props: {
    url: String
  },
}
</script>