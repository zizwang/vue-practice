<template>
  <div>
    <p>
      User name: 
      <strong>{{ user.firstName }} {{ user.lastName }}</strong>
    </p>
  </div>
</template>
<script>
export default {
  name: "Props",
  props: { 
    user: {
      type: Object,
      required: true,
    },
  },
}
</script>