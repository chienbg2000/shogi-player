<template lang="pug">
.MainDocPlayDemo7.column
  b-message(type="is-info")
    | sp_human_side="white" và sp_viewpoint="white": Người chơi là bên Trắng (Gote) và bàn cờ tự động đảo ngược để thuận tiện quan sát.
  ShogiPlayer(
    sp_mode="play"
    sp_viewpoint="white"
    sp_human_side="white"
    sp_slider
    sp_controller
    sp_board_variant="wood_normal"
    )
</template>

<script>
export default {
  name: "MainDocPlayDemo7",
}
</script>

<style lang="sass">
@import "../support.sass"
.MainDocPlayDemo7
  __css_keep__: 0
</style>
