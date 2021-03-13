<template>
  <header>
    <span>VIDEO PACHA TV</span>
    <nav>
        <ul>
            <li><a href="#" target="_blank" rel="noopener">Agregar Video</a></li>
        </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
header{
    background: red;
    display: flex;
    justify-content: space-between;
    padding: 10px 30px;
    font-weight: 700;
}
span{
    color: white;
    font-size: 30px;
    display: flex;
    align-items: center;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: white;
  text-decoration: none;
}
</style>
