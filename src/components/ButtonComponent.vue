<template>
  <input type="submit" placeholder="Submit Log" v-on:submit="$emit('submit-log', $event)">
</template>

<script>
export default {
  name: 'ButtonComponent'
}
</script>
