<template>
  <Layout>
    <h1>Term</h1>
    <form action="https://formspree.io/mzbdzbra" method="POST">
  <input type="text" name="name">
  <input type="email" name="_replyto">
    <input type="submit" value="Send">
    </form>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </Layout>
</template>

<script>
  export default {
    metaInfo () {
      return {
        title: 'Terms and Condition',
        meta: [
          { name: 'description', content: 'Terms and Condition page' },
        ],
      }
    },

  }
</script>
