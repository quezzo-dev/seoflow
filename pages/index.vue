<template lang="pug">
  .test
    script(
      src="https://telegram.org/js/telegram-widget.js?19"
      :data-telegram-login="BOT_USERNAME"
      data-size="large"
      :data-onauth="onTelegramAuth(user)"
      data-request-access="write"
      :data-auth-url="REDIRECT_URI")
      
</template>

<script>
export default {
  // name: "IndexPage",
  data() {
    return {
      BOT_USERNAME: "gerchik_login_bot",
      BOT_TOKEN: "5295915260:AAEnm4WCPpYdK7T6pIA8uaGfdhTrh7sogFY",
      REDIRECT_URI: "https://profound-babka-6a3346.netlify.app/",
    };
  },

  mounted() {
    alert("upd");
  },

  methods: {
    onTelegramAuth(user) {
      console.log(
        "Logged in as " +
          user.first_name +
          " " +
          user.last_name +
          " (" +
          user.id +
          (user.username ? ", @" + user.username : "") +
          ")"
      );
    },
  },
};
</script>
