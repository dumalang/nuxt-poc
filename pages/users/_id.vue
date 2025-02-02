<template>
  <H1>Hi This is User with ID direct call: {{ $route.params.id }}</H1>
</template>

<script>

export default {
  async asyncData(context) {
    // Server-side console log
    console.log('Server-side log:', context.params.id);

    // Return data to the component
    return {};
  },
}
</script>
