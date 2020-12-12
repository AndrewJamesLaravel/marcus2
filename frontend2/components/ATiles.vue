<template>
  <!--Tiles-->
  <section class="section">
    <div class="container">
      <div class="tile is-ancestor">
        <!-- first column -->
        <div class="tile is-8 is-vertical">
          <!--Our imagined subtitle-->
          <div class="tile">
            <div class="tile is-vertical is-parent">
              <div class="tile is-child box">
                <p class="title">
                  Vertical...
                </p>
              </div>
              <div class="tile is-child box">
                <p class="title">
                  ...tiles
                </p>
              </div>
            </div>
            <div class="tile is-parent">
              <div class="tile is-child box">
                <p class="title">
                  Middle tile
                </p>
              </div>
            </div>
          </div>
          <div class="tile is-parent">
            <!--The bottom tile in the first column-->
            <div class="tile is-child box">
              <p class="title">
                Wide title
              </p>
            </div>
          </div>
        </div>
        <div class="tile is-parent">
          <!-- second column -->
          <div class="tile is-child box">
            <p class="title">
              Tall tile
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ATiles'
}
</script>

<style scoped></style>
