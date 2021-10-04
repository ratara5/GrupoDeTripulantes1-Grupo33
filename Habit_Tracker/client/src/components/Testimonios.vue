<template>
  <div>
    <h1>De nuestros visitantes</h1>
    <div class="ui grid">
      <div class="three wide column">
        <div class="ui comments">
          <div class="comment">
            <a class="avatar">
              <img src="../assets/Fulano.jpg" />
            </a>
            <div class="content">
              <a class="author">Fulano</a>
              <div class="metadata">
                <div class="date">Algún momento</div>
                <div class="rating">
                  <i class="star icon"></i>
                  5 Faves
                </div>
              </div>
              <div class="text">Hola, esto es muy bueno.</div>
            </div>
          </div>
        </div>
      </div>
      <div class="three wide column">
        <div class="ui comments">
          <div class="comment">
            <a class="avatar">
              <img src="../assets/Perano.png" />
            </a>
            <div class="content">
              <a class="author">Perano</a>
              <div class="metadata">
                <div class="date">Otro momento</div>
                <div class="rating">
                  <i class="star icon"></i>
                  4 Faves
                </div>
              </div>
              <div class="text">Saludos, esto es genial.</div>
            </div>
          </div>
        </div>
      </div>
      <div class="three wide column">
        <div class="ui comments">
          <div class="comment">
            <a class="avatar">
              <img src="../assets/Sultano.jpg" />
            </a>
            <div class="content">
              <a class="author">Sultano</a>
              <div class="metadata">
                <div class="date">Este momento</div>
                <div class="rating">
                  <i class="star icon"></i>
                  4.5 Faves
                </div>
              </div>
              <div class="text">Que hay, HT es excelente!</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "testimonios",
};
</script>

<style lang="scss" scoped>
.ui.grid {
  .ui.comments {
  }
}
</style>