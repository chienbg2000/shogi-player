<template lang="pug">
.MainDocViewDemoWhite.column
  b-message(type="is-info")
    | sp_viewpoint="white": Chế độ xem (Playback) từ góc nhìn bên Trắng (Gote). Bàn cờ được lật ngược 180 độ ngay khi khởi tạo.
  .has-text-centered
    .title.is-4 {{kifu_book_info.name}} (Góc nhìn bên Trắng)
  ShogiPlayer(
    :sp_body="kifu_book_info.sp_body"
    :sp_turn="4"
    :sp_player_info="sp_player_info"
    sp_viewpoint="white"
    sp_board_variant="wood_normal"
    sp_piece_variant="portella"
    sp_layout="horizontal"
    sp_controller
    sp_slider
  )
</template>

<script>
import { KifuBookInfo } from "../models/kifu_book_info.js"

export default {
  name: "MainDocViewDemoWhite",
  data() {
    return {
      kifu_book_info: KifuBookInfo.fetch("KIF_15733"),
      sp_player_info: {
        black: { name: "六代大橋宗銀", },
        white: { name: "伊藤印達",     },
      },
    }
  },
}
</script>

<style lang="sass">
@import "./support.sass"
.MainDocViewDemoWhite
  __css_keep__: 0
</style>
