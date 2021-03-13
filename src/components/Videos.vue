<template>
  <div>
    <h1>Lista de videos</h1>
    <div class="bloque">
        <article class="bloque__article" v-for='(db,id) in dbs' :key="id">
            <div class="bloque__article__options">                 
                <button title="delete" href="#" class="borrar-curso" data-id=${perro.id} @click="eliminar">X</button>
            </div>
            <div class="bloque__article__img">
                <iframe width="450" height="315"
            :src="db.urlVideo">
            </iframe>
            </div>
            <div class="bloque__article__mainInfo">
                <p class="title">{{db.titulo}}</p>
                <p class="desc">{{db.descripcion}}</p>
            </div>
        </article>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Videos',
  data() {
    return{
        dbs: 
        [
            {
                "id": 1,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 2,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 3,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 4,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 5,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 6,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 7,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            },
            {
                "id": 8,
                "titulo":"Tecnicas de programación",
                "urlVideo":"http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",
                "descripcion":"Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga saepe in minima odio, fugit ipsum assumenda animi itaque repellat sint quidem natus eius error, magnam, expedita deleniti iste. Sapiente, magni."
            }
        ]
    }
  },
  methods:{
      eliminar(){
          console.log('di click en eliminar');
        const carrito = document.querySelector(".bloque");
        console.log(carrito);



            carrito.addEventListener("click", eliminarCurso);

        function eliminarCurso(e) {

            e.preventDefault();
            if (e.target.classList.contains("borrar-curso")) {
                const cursoActual = e.target.parentElement;
                console.log(cursoActual);
                const cursoID = cursoActual.querySelector("button").getAttribute("data-id");

                e.target.parentElement.parentElement.remove();
            }
        }
      }
  }
}



</script>

<style scoped>
h1{
    padding: 0 40px;
}
.bloque{
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(2, 1fr);
    padding: 30px;
    gap: 10px;
}
.bloque__article {
  border: 1px solid;
  position: relative;
}
.bloque__article__options {
    position: absolute;
    display: none;
    justify-content: flex-end;
    width: 100%;
    top: -20px;
    left: -5px;
}

.bloque__article__options .borrar-curso {
  font-weight: bold;
  text-decoration: none;
}
:hover > .bloque__article__options {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}

.bloque__article__mainInfo{
    padding: 10px;
}

.title{
    font-weight: bold;
}
</style>
