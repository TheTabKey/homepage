<template>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="mailto: contact@tab.cx">Contact</a></li>
      <li><a href="https://steamcommunity.com/id/tab-">Steam</a></li>
    </ul>
  </nav>
</template>

<style>
nav {
  background-color: #2c3e50;
  color: white;
}

ul {
  list-style: none;
  display: flex;
  justify-content: center;
  padding: 0;
}

li {
  margin: 0 10px;
}

a {
  color: white;
  text-decoration: none;
  padding: 10px;
}

a:hover {
  text-decoration: underline;
}
</style>

<script>
export default {
  name: 'AppNavbar',
};
</script>
