<template>
  <q-item clickable :to="route" exact>
    <q-item-section v-if="props.icon" avatar>
      <q-icon :name="props.icon" style="font-size: 32px" />
    </q-item-section>

    <q-item-section>
      <q-item-label>{{ props.title }}</q-item-label>
      <q-item-label caption>{{ props.caption }}</q-item-label>
    </q-item-section>
  </q-item>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },

  caption: {
    type: String,
    default: '',
  },

  route: {
    type: [String, Object],
    default: '',
  },

  icon: {
    type: String,
    default: '',
  },
})
</script>
