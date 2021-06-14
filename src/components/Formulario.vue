<template>
<div class="container">
    <form class="text-left" action="mailto:felixbdev@gmail.com" id="contact-form" method="post" role="form" style="margin-top: 40px" enctype="text/plain">
    <h1>Contactame</h1>
      <div class="container mt-4">
        <div class="form-group ">
          <label for="name">Nombre</label>
          <input type="text" name="name" class="form-control" id="name" placeholder="Escribe tu nombre" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" name="email" class="form-control" id="email" aria-describedby="emailHelp" placeholder="Escribe tu correo" required>
        </div>
        <div class="form-group">
          <label for="message">Mensaje</label>
          <textarea class="form-control" name="message" id="message" rows="3" required placeholder="Escribe tu mensaje"></textarea>
        </div>
        <button type="submit" class="btn btn-primary btn-block">Enviar</button>
      </div>
  </form>
</div>

</template>

<script>
export default {
  name: "Formulario",
};
</script>

<style scoped>
  textarea{
    resize: none;
    height: 8.125rem;
  }
</style>
