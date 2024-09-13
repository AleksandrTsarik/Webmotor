<template>
  <button
    :type="type"
    :class="btnClass"
    class="btn"
  >
    <span v-if="svg" v-html="svg"></span>
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: {
      label: String,
      default: '',
      require: true
    },
    type: {
      type: String,
      dafault: ''
    },
    svg: {
      type: String,
      dafault: ''
    },
    btnClass: String
  }
}
</script>

<style lang="scss" scoped>
  .btn {
    font-size: 18px;
    font-weight: 400;
    border: solid 1px transparent;
    padding: 14px 20px;
    cursor: pointer;
    border-radius: 5px;
    transition: 0.3s;
    display: inline-block;
    &:active {
      background-color: tomato;
    }
    &:hover {
      @media(min-width: 1023px) {
        background: darken(#0078EE, 5%);
        box-shadow:0 0 0 5px rgba(#0078EE, 0.5);
      }
    }
  }
  .btn-dark {
    background-color: var(--primary);
    color: var(--bg);
  }
</style>