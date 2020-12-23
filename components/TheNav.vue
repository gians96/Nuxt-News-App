<template>
  <b-navbar>
    <template slot="brand">
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <img
          src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR34dyR4PdRqvfNi_QIruoGyjHihGJrL98VuA&usqp=CAU"
          alt="Lightweight UI components for Vue.js based on Bulma"
        />
      </b-navbar-item>
    </template>
    <template slot="start">
      <b-navbar-item v-for="link in links" :key="link.name" :href="link.href">
        {{ link.name }}
      </b-navbar-item>
      <b-navbar-item href="#"> Documentation </b-navbar-item>
      <b-navbar-dropdown label="Info">
        <b-navbar-item href="#"> About </b-navbar-item>
        <b-navbar-item href="#"> Contact </b-navbar-item>
      </b-navbar-dropdown>
    </template>

    <template slot="end">
      <b-navbar-item tag="div">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light"> Log in </a>
        </div>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          name: "link1",
          href: "#",
        },
        {
          name: "link2",
          href: "#",
          sublinks: [
            { name: "sublink 1", href: "#" },
            { name: "sublink 2", href: "#" },
            { name: "sublink 3", href: "#" },
          ],
        },
        {
          name: "link2",
          href: "#",
          sublink: [
            { name: "sublink 1", href: "#" },
            { name: "sublink 2", href: "#" },
            { name: "sublink 3", href: "#" },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>