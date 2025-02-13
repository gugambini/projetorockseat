# projetorockseat

<!DOCTYPE html>
<html lang="pt-br" class="">
<head>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&display=swap" rel="stylesheet"/>


    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DevLinks</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>


    <div id="container">
        <div id="profile">
         <img src="assets/banda.jpg" alt="  Logo do perfil da banda."/>

         <p>BANDA HARMONIZE</p>

    <div>
        <div id="switch" onclick="toggleMode()">
            <button></button>
            <span></span>
        </div>
        <ul>
            <li>
                <a href="#">Nossa história</a>
            </li>
            <li>
                <a href="https://www.instagram.com/banda.harmonize/">Perfil</a>
            </li>
            <li>
                <a href="#">Músicas</a>
            </li>
        </ul>
        <div id="social-links">
            <a href="https://wa.me/11991671080?text=Ol%C3%A1%2C%20tudo%20bem%3F%20Quero%20fazer%20parte%20da%20banda!!%20%F0%9F%91%91%E2%9C%9D%EF%B8%8F" target="_blank">
            <ion-icon name="logo-whatsapp"></ion-icon>
            </a>

            <a href="https://www.instagram.com/banda.harmonize/" target="_blank">
            <ion-icon name="logo-instagram"></ion-icon>
            </a>

            <a href=""> 
            <ion-icon name="musical-notes-outline"></ion-icon>
            </a>
            <a href="">
            <ion-icon name="logo-youtube"></ion-icon>
            </a>
     </div>
     <footer>
        by <a href="https://www.instagram.com/gambinigustavo/"
            >@gambinigustavo</a>
     </footer>
    </div>

    <script
    type = "module"  
    src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"
    ></script> 
    <script 
     nomodule  
     src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"
    ></script>

    <script src="./script.js"></script>
    
</body>
</html>














CSS

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
:root {
    --text-color: white;
    --bg-url: url(./assets/bg-mobile.jpg);
    --stroke-color: rgba(255, 255, 255, 0.5);
    --surface-color: rgba(255, 255, 255, 0.2);
    --surface-color-hover: rgba(0, 0, 0, 0.02);
    --highlight-color: rgba(255, 255, 255, 0.2);
    --switch-bg-url: url(./assets/moon-star.svg);
}

.light {
    --text-color: black;
    --bg-url: url(./assets/bg-mobile-light.jpg);
    --stroke-color: rgba(0,0,0,0.5);
    --surface-color: rgba(0, 0, 0, 0.05);
    --surface-color-hover: rgba(0, 0, 0, 0.02);
    --highlight-color: rgba(0,0,0,0.1);
    --switch-bg-url: url(./assets/sun.svg);

}



body {
    
    background: var(--bg-url) no-repeat top center/cover;
}


    body * {
        font-family: "Oswald", serif;
        font-optical-sizing: auto;
        font-weight: weight;
        font-style: normal;
        color: var(--text-color);  
        justify-content: center; /* Centraliza horizontalmente */
        align-items: center; /* Centraliza verticalmente */
        text-align: center;

    }

#container{
    width: 360px;
    margin: 20px auto 0px;
    padding: 0 24px;
    
    
    
}

#profile{
    text-align: center;
    padding: 1px;
 
}



#profile img{
    display: block;
    width: 100px;
    margin: auto;
    border-radius: 50%
    
}

#profile p {
    font-weight: 500;
    line-height: 24px;
    margin-top: 10px;
    margin-bottom: 70px;

}
#swtich{
    border: 1px solid red;
    position: relative;
}


#switch button{
    width: 32px;
    height: 32px;
    background: white var(--switch-bg-url) no-repeat center;
    border: 0;
    border-radius: 50%;
    position: absolute;
    right: 671px;
    bottom: 385px;
    z-index: 1;
    transform: translate(-50%);
    animation: slide-back 0.2s;
    
}

   .light #switch button{
    animation: slide-in 0.4s forwards;
    right: 648px;
    bottom: 387px;
   }

   #swtich button:hover {
    outline: 8px solid var(--highlight-color);
   }

    #switch span{
        display: block;
        width: 64px;
        height: 24px;
        background: var(--surface-color);
        border: 1px solid var(--stroke-color);
        backdrop-filter: blur(4px);
        -webkit-backdrop-filter: blur(4px);
        border-radius: 9999px;
        position: center;
        margin: auto;
        margin-bottom: 20px;
        margin-top: -10;
    }




ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 0;
    margin: 0;
    width: 100%;
}

ul li {
    width: 100%;
}

ul li a {
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    font-size: 1rem;
    font-weight: 500;
    color: var(--text-color);

    padding: 1rem 1.5rem;
    width: 100%; 
    box-sizing: border-box; /* Garante que padding e border não aumentem o tamanho total */
    
    background: var(--surface-color);
    border: 1px solid var(--stroke-color);
    border-radius: 8px;
    
    backdrop-filter: blur(4px);
    -webkit-backdrop-filter: blur(4px);
    
    transition: all 0.2s ease-in-out;
}

/* Efeito de hover para uma melhor experiência */
ul li a:hover {
    background: var(--surface-color-hover);
    border-color: var(--text-color);
    transform: scale(1.05);
}

#social-links {
    display: flex;
    justify-content: center;
    gap: 12px; /* Adiciona espaçamento entre os ícones */
    padding: 24px 0;
    font-size: 24px;
}

#social-links a {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 12px;
    transition: background 0.3s ease-in-out, transform 0.2s ease-in-out;
    border-radius: 50%; /* Garante um formato circular */
}

#social-links a:hover {
    background: var(--highlight-color);
    transform: scale(1.1); /* Efeito de leve crescimento ao passar o mouse */
}

footer{
    padding: 24px 0;
    text-align: center;
    margin-top: -20px;
    font-size: 14px;

}

@keyframes slide-in {
    from {
        transform: translateX(-100%);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-back {
    from {
        transform: translateX(0%);
    }
    to {
        transform: translateX(-100);
    }
}






JS

 const html = document.documentElement
    html.classList.toggle("light")

   const img = document.querySelector("#profile img")


   if(html.classList.contains('light')){

    img.setAttribute("src", "./assets/banda-light.jpg")

   }else{

    img.setAttribute("src", "./assets/banda.jpg")

   }



}
