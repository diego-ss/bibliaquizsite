<template>
<form id="contact-form" class="contact-form" @submit.prevent="sendEmail">
  <section class="hero is-fullheight">
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class="columns is-8 is-variable">
          <div class="column is-two-thirds has-text-left">
            <h1 class="title is-1">Fale Conosco!</h1>
            <p class="is-size-4">
              Aqui você pode nos enviar uma mensagem com feedbacks, dicas,
              observações, testemunhos e tudo mais que vier em sua mente!
            </p>
            <p class="is-size-4">Responderemos sempre que possível!</p>
          </div>
          <div class="column is-one-third has-text-left">
            <div class="field">
              <label class="label">Seu nome</label>
              <div class="control">
                <input
                  class="input is-medium"
                  type="text"
                  v-model="name"
                  name="name"
                  required
                />
              </div>
            </div>
            <div class="field">
              <label class="label">Email</label>
              <div class="control">
                <input name="email" class="input is-medium" v-model="email" type="email" required />
              </div>
            </div>
            <div class="field">
              <label class="label">Mensagem</label>
              <div class="control">
                <textarea
                  class="textarea is-medium" name="message"
                  v-model="message"
                ></textarea>
              </div>
            </div>
            <div class="control">
              <button
                type="submit"
                class="button is-info is-light is-fullwidth has-text-weight-medium is-medium"
              >
                enviar mensagem
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
    </form>
</template>

<script>
import emailjs from "emailjs-com";

export default {
  name: "Contact",
  data() {
    return {
      name: "",
      email: "",
      message: "",
    };
  },
  methods: {
    async sendEmail(e) {
        console.log(this.name);
        console.log(this.email);
        console.log(this.message);
      try {
        await emailjs.sendForm(
          "service_31s2y5f",
          "template_0t9bvy6",
          e.target,
          "user_x59jTuejUp0TiSUHRyXLC",
          {
            name: this.name,
            email: this.email,
            message: this.message,
          }
        );
        alert("E-mail enviado com sucesso!");
      } catch (error) {
        console.log({ error });
        alert("Ops! Falha ao enviar e-mail.");
      }
      // Reset form field
      this.name = "";
      this.email = "";
      this.message = "";
    },
  },
};
</script>

<style>
</style>