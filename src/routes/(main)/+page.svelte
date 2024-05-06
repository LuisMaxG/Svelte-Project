<script>
    export let data;
    console.log(data);
    const MiPromesa = () => {
        return new Promise((resolve, reject) => {
            console.log("estoy haciendo algo mas")
            setTimeout(()=> {
                resolve("se ha terminado todo");
            }, 2000);
        })
    }

    const MiPromesa2 = new Promise((resolve,rejact) => {
        console.log("Estas haciendo algo");
        setTimeout(()=>{
            resolve(MiPromesa());
        }, 2000)
    })

    MiPromesa2.then((resultado) => {
        return resultado;
    }).then((mensaje)=> {
        console.log(mensaje);
    }).catch((err) => {
        console.err(err);
    })
</script>

<h1>Shop</h1>