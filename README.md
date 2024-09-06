# My-Portfolio
My Portfolio using HTML, CSS and Javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="portfolio.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
        <script defer src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>    
    <style>
        .fixed-page {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: rgb(198, 198, 198);
}

.navbar {
  height: 8%;
  position: relative;
  top: 2%;
  background: rgba(255, 255, 255, 0.984);
  border-radius: 10vw;
}

.leftnav {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.logo {
  position: relative;
  left: 1vw;
  border-radius: 10vw;
}

.txtcontact {
  position: relative;
  right: 20%;
  transition: font-family 0.5s ease;
  /* font-weight: 1000; */
}
.contact{
  font-weight: 600;
  position: relative;
  right:  2%;
}

.contact:hover {
  font-weight: 1000;
  cursor: pointer;
}

#hidden-div {
  height: 10vh;
  /* width: 80vw; */
  background: rgba(255, 253, 253, 0);
  position: absolute;
  z-index: 1;
  border-radius: 1vw;
  display: none;
  /* transition: opacity 0.5s ease-in-out, visibility 0.5s ease-in-out; */

}
#hidden-div {
  animation: fadeIn 1s ease-in-out;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
    visibility: hidden;
    /* transform: translateX(100%); */

  }
  100% {
    opacity: 1;
    visibility: visible;
    /* transform: translateX(0%); */

  }
}


@media (max-width: 768px) {
  #hidden-div {
    height: 8vh;
    width: 91.3%;
    transform: translateX(8.33%);

  }
}

.socials {
  height: 100%;
  width: 20.5vw;
  background: rgb(255, 255, 255);
}
.social-transition{
  position: relative;
  background-color: white; 
  color: black; 
  transition: background-color 0.3s, color 0.3s;
  /* font-size: medium;  */
}

.social-transition::before {
  /* background-color: black;  */
  
  cursor: pointer;
  font-weight: 1000;
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 0;
  height: 100%;
  background-color: #000000;
  transition: width 0.5s;

  /* font-size: larger; */
}
.social-transition:hover{
    color: #ffffff;
    font-weight: 1000;
    font-style: italic;
}
.social-transition:hover::before {
  width: 100%;
  
}

.border-socials{
  width: 80%;
  height: 60%;
  border: 100% solid black;
  z-index: 1;
}
.textnav {
  font-family: "Courier New", Courier, monospace;
}

.text-loop {
  overflow: hidden;
  white-space: nowrap;
}

.looping-text {
  display: inline-block;
  animation: loop-text 8s linear infinite;
  font-size: 30vh;
  font-family: "Lucida Handwriting", cursive;
  color: black;
}

@keyframes loop-text {
  0% {
    transform: translatex(100%);
  }
  100% {
    transform: translateX(-98%);
  }
}

.myphoto{
  position: absolute;
  bottom: 0%;
  transition: width 0.5s ease-in-out;

}
.gif{
  position: absolute;
  left: 2%;
  bottom: 3%;
}
.scrolldown{
  position: absolute;
  left: 2%;
  bottom: 0%;
  color: rgb(0, 0, 0);
  font-weight: 1000;
}

.copyright-box {
  position: fixed;
  bottom: 0;
  right: 2%;
  bottom: 2%;
  background-color: rgb(255, 255, 255);
  /* padding: 2px; */
  height: 32px;
  border-radius: 5px;
  font-size: 20px;
  width: fit-content;
  font-weight: 1000;
  /* margin: 1vh; */
}




.scrolling-page {
  /* margin: 0,0,5%,0; */
  position: absolute;
  top: 100vh;
  left: 0;
  width: 100%;
  height: fit-content;
  overflow-y: scroll;
  scrollbar-width: none;
  -ms-overflow-style: none;
  transition: top 0.5s ease-in-out;
  background: rgb(255, 255, 255);
  border-radius: 5vh;
}

.scrolling-page::-webkit-scrollbar {
  display: none;
}

.scrolling-page.scrolled {
  top: 0;
}

.about{
  height: 65vh;
  border-radius: 2vw;
  /* border: rebeccapurple 2px solid; */
  opacity: 0; 
  transform: translateX(10%);
  transition: opacity 0.1s, transform 0.1s;
  color: rgb(0, 0, 0);
  z-index: 0;
  position: relative;
}
.about:hover{
  opacity: 1;
  color: rgb(255, 255, 255);
  z-index: 1;
    transform: translateX(0%);

}
.left-about{
  height: 100%;
  border: rgb(0, 0, 0) 2px solid;
  /* margin-top: 5%; */
}
.about-heading{
  font-size: 10vh;
  /* color: #ffffff; */
  font-family: Poppins, sans-serif;
}
.about-text{
  font-size: 5vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
}
.right-about{
  height: 100%;
  /* border: rgb(0, 0, 0) 2px solid; */
  position: relative;
  opacity: 0;
  transform: translateX(20%);
  transition: opacity 0.5s, transform 2s;
 
  /* z-index: 0; */
  z-index: 1;
}
.right-about:hover{
  opacity: 1;
  transform: translateX(0%);
  /* z-index: 1; */
}

.bg-about{
  position: absolute;
  top: 0vh;
  /* font-size: 45vh; */
  height: auto;
  transition: 1s;
  /* z-index: -1; border: rebeccapurple 2px solid; */
}
.bg-about:hover{
  z-index: -1;
}
.softskills{
  /* font-size: 11vh; */
  font-weight: 500;
  height: 55vh;
  color: #000000;
  background: #ffffff;
}
.right-arrow{
  font-family: "Playfair Display", serif;
  font-weight: 1000;
}

.list-softskill{
  font-family: "Playfair Display", serif;
  height:fit-content;
  font-weight: 0;
}
.list-softskill li:hover{
  font-weight: 1000;
  font-style: italic;
  cursor: pointer;
}
 
.hardskills{
  height: 10vh;
  position: relative;
  top: 0vh;
  /* background: #ffffff; */
  margin-top: 5vh  ;
  /* border-radius: 2vw; */
  /* border: 2vh groove rgb(213, 213, 213); */
}
.hardskill-text{ 
   font-family: "Playfair Display", serif;
  position: absolute;
  /* font-size: 10vh; */
  
}

.skills{
  /* background: rgb(255, 255, 255); */
  /* gap: 5%; */
  position: relative;
  top: 3vh;
  height: auto;
  /* min-height: calc(100% + 2vh); */
}
.skill-box{
  padding: 2%;
  /* background: rgb(255, 253, 252); */
  /* box-shadow: 1vw -2vh 2vh 0vh rgba(0, 0, 0, 0.411); */
  transition: transform 0.3s ease;
  /* border: #000000 1px solid; */
  

}
.skill-box:hover{
  transform: translate(2vw, -2vh);
}
.skill-box-container {
  flex-wrap: wrap;
  justify-content: space-around;
  column-gap: 5%;
  row-gap: 5vh;
  background: rgb(255, 255, 255);
  margin-top: 5vh;
  /* box-shadow: -1vw 2vh 1vh  0vh rgba(0, 0, 0, 0.411);/ */
  /* position: relative;
  top: 3vh; */
}
.skill-box-icon{
  display: grid;
  justify-content:center;
  background: rgb(255, 255, 255);
  align-items: center;
 
}
.skill-box-text{
  display: flex;
  justify-content:center;
  background: rgb(255, 255, 255);
  align-items: center;
 /* width: 100; */
 font-family: Playfair Display, serif;
  /* font-weight: 1000; */
  font-size: 3vh;
}
.experience{
  background: rgb(0, 0, 0) ;
  color: #ffffff;
  width: 100%;
  position: relative;
  left: 0;
  top: 10vh;
  border-radius: 1vh;
  box-shadow: -1vw 2vh 2vh 0vh rgba(0, 0, 0, 0.411);
  padding: 2vh;

}
.exp-heading{
  font-size: larger;
  font-weight: 1000;
}
.quest{
  font-weight: 600;
}
.blackline{
  background: #000000;
  height: 0.2vh;
  margin: 15vh;
}
.projects{
  margin-top: 5vh;
}
.projects-heading{
  font-weight: 1000;
  font-family: "Playfair Display", serif;
  font-size: 10vh;
  text-align: center;
}
.project-elements{

}
.project-row{
  /* width: 100%; */
  height: 10vh;
  /* background: rgb(157, 157, 157); */
  display: flex;
  /* justify-content: space-evenly; */
  /* border-radius: 2vh; */
  margin: 3%;
  background: rgb(0, 0, 0) ;
  /* box-shadow: -1vw 2vh 2vh 0vh rgba(0, 0, 0, 0.411); */
  color: white;
}
.pro-row-heading{
  /* width: 50%; */
  /* background: wheat; */
  display: flex;
  align-items: center;
  font-size: 3vh;
  font-weight: 1000;
  
}

.lock-contact-container{
  /* background: #0400f4; */
}
.lock-contact{
  background:white;
  color: black;
}

.lock img{
  height: 5vh;
  /* width:  ; */
}

.project-1-image{
  opacity: 0;
  transition: opacity 1s ease;
  /* position: relative;
  bottom: 10vh; */
}
.pro-1-eCommerce:hover .project-1-image{
  opacity: 1;
} 
.pro-2 img{
  height: 50vh;
  width: 25vw;
  z-index: 1;
}

.link-tree-container{
  margin-top: 15vh;
  height:fit-content
  /* background: rgb(198, 198, 198); */
}
.linktree-heading-text{


}
.linktree-heading{
  margin-top: 2vh;
  display: flex;
  align-items: center;
  justify-content: center;
  /* height: 15vh; */
}
.linktree-heading-photo img{
  margin-left: 2vw;
  height: 10vh;
  border-radius: 100vh;
}
.linktree-row{
    /* width: 100%; */
    height: 10vh;
    /* background: rgb(157, 157, 157); */
    display: flex;
    justify-content:center;
    align-items: center;
    /* border-radius: 2vh; */
    margin: 3%;
    background: rgb(0, 0, 0) ;
    /* box-shadow: -1vw 2vh 2vh 0vh rgba(0, 0, 0, 0.411); */
    position: relative;
    color: white;
}
.linktree-row img{
  border-radius: 100vh;
  margin-left: 1vw;
  z-index: 1;
}
.linktree-row h3{
  z-index: 1;
}
.linktree-row::before {
  /* background-color: black;  */
  
  cursor: pointer;
  font-weight: 1000;
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  background: rgb(255, 255, 255);
  transition: width 0.5s;

  /* font-size: larger; */
}

.linktree-row:hover{
    color: #000000;
    font-weight: 1000;
    font-style: italic;
    /* z-index: -1; */
  border: #000000 solid;
}
.linktree-row:hover::before {
  width: 100%;
  
}
.long-blackline{
  height: 0.5vh; 
  background: black;
  margin-top: 0vh;
}
.text-loop-bottom{
  overflow: hidden;
  white-space: nowrap;
  margin-top: 20vh;

}
.looping-text-bottom {
  display: inline-block;
  animation: looping-text-bottom 10s linear infinite;
  font-size: 10vh;
  /* font-family: "Playfair Display", serif; */
  color: black;
  /* margin-top: 5vh */
}
.looping-text-bottom img{
  filter: grayscale(90%);
  height: 18vh;
  width: 10vw;
  margin-RIGHT: 5VW;
}

@keyframes looping-text-bottom {
  0% {
    transform: translatex(100%);
  }
  100% {
    transform: translateX(-220%);
  }
}

.conclution{
  margin-top: 0VH;
  height: 100vh;
  width: 100vw;
}
.con-name{
  /* height: 15vh; */
  margin: 10vh;
  border: #000000 solid;
}
.con-name h1{
  font-size: 12vh;
  font-family: "Lucida Handwriting", cursive;
  margin: 1vh;
 
}
.con-border{
  
  height:  80vh;
  position: relative;
  top: 5vh;
}
.con-love{
  font-size: 4vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
  font-weight: 900;
}
.con-quotes{
  font-size: 3vh;
  /* display: flex; */
  /* display: flex; */
  position: absolute;
  bottom: 0vh;
}
.con-quotes span{
  display: flex;
  /* align-items: end; */
  justify-content: center;
  font-weight: 600;
}
.con-copy-right{
  display: flex;
  /* align-items: end; */
  justify-content: end;
  position: absolute;
  bottom: 0%;
  right: 0;
  /* font-weight: 600; */
}

#clock {
  font-size: 24px;
  font-family: Arial, sans-serif;
}
.con-img img{
  border-radius: 100%;
  position: absolute;
  right: 5vw;
  bottom: 15vh;
  height: 30vh;
  border: #000000 solid 1px;
}







.bottom-navbar{
  /* width: 30%; */
  height: 6vh;
  background: #fffdfdb2;
  position:fixed;
  top: 90vh;
  /* z-index: 1; */
  border-radius: 4vw;
  justify-content:space-around;
}
.logo-nav{
  border-radius: 10vw;
}

.nav-elements{
  width: 20%;
  /* border: #000000 2px solid; */
  height: 100%;
}
.nav-elements:hover{
  font-weight: 1000;
  cursor:grab;
}




/* Extra Large (xl) - 1200px and up */
@media (min-width: 1200px) {
  .about-text {
    font-size: 5vh;
  }
  .bg-about{
    font-size: 45vh;
  }
  .hardskill-text, .projects-heading, .right-arrow{
    font-size: 10vh;
    font-weight: 1000;
  }
  
  .list-softskill{
    font-size: 5vh;
 
  }
  .skill-box{
      height: 25vh;
  width: 20%;
  }
  .lock-contact{
    position: relative;
    left: 45%;
    top: 15%;
    width: 50%;
    /* background: rgb(255, 255, 255); */
    height: 70%;
    border-radius: 2vh;
    align-items: center;
    justify-content: center;
    font-weight: 1000;
  }
    .project-1-image{
  position: relative;
  left: -1%;
  /* bottom: 1000%; */
  z-index: 1;
}
.project-1-image img{
  height: 40vh;
  width: 35vw;

}
.pro-2 img{
  height: 50vh;
  width: 25vw;
}
.con-name{
  /* height: 15vh; */
  margin: 10vh;
  border: #000000 solid;
}
.con-name h1{
  font-size: 6.5vh;
  font-family: "Lucida Handwriting", cursive;
  margin: 1vh;
 
}
.con-border{
  
  height:  80vh;
  position: relative;
  top: 5vh;
}
.con-love{
  font-size: 4vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
  font-weight: 900;
  position: absolute;
  /* top: 55vh; */
}
.con-quotes{
  font-size: 3vh;
  /* display: flex; */
  /* display: flex; */
  position: absolute;
  bottom: 10vh;
}
.con-quotes span{
  display: flex;
  /* align-items: end; */
  justify-content: center;
  font-weight: 600;
}
.con-copy-right{
  display: flex;
  /* align-items: end; */
  justify-content: end;
  position: absolute;
  bottom: 0%;
  right: 0;
  /* font-weight: 600; */
}

#clock {
  font-size: 24px;
  font-family: Arial, sans-serif;
}
.con-img img{
  border-radius: 100%;
  position: absolute;
  right: 10%;
  /* bottom: 15vh; */
  top: 25vh;
  height: 30vh;
  border: #000000 solid 1px;
  display: flex;
  align-items: center;
}



  
}

/* Large (lg) - 992px to 1199px */
@media (min-width: 992px) and (max-width: 1199px) {
  .about-text {
    font-size:3.9vh;
  }
  .bg-about{
    font-size: 23vh;
  }
  .hardskill-text, .projects-heading, .right-arrow{
    font-size: 10vh;
    font-weight: 1000;
  }

  .list-softskill{
    font-size: 4vh;

  }
  .skill-box{
      height: 20vh;
  width: 20%;
  }
  .lock-contact, .pro-row-heading{
    font-size: 1.7vh;
  }
  .lock-contact{
    position: relative;
    left: 45%;
    top: 15%;
    width: 50%;
    /* background: rgb(129, 40, 40); */
    height: 70%;
    border-radius: 2vh;
    align-items: center;
    justify-content: center;
    font-weight: 1000;
    /* font-size: 1vh; */
  }
  .project-row{
    height: 8vh;
  }
  .lock img{
    height: 4vh;
    /* width:  ; */
  }
    .project-1-image{
  position: relative;
  left: -5%;
  z-index: 1;
}
.project-1-image img{
  height: 40vh;
  width: 40vw;
}
.pro-2 img{
  height: 50vh;
  width: 35vw;
}
.con-name{
  /* height: 15vh; */
  margin: 10vh;
  border: #000000 solid;
}
.con-name h1{
  font-size: 8.5vh;
  font-family: "Lucida Handwriting", cursive;
  margin: 1vh;
 
}
.con-border{
  
  height:  110vh;
  position: relative;
  top: 5vh;
}
.con-love{
  font-size: 4vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
  font-weight: 900;
  position: absolute;
  top: 55vh;
}
.con-quotes{
  font-size: 3vh;
  /* display: flex; */
  /* display: flex; */
  position: absolute;
  bottom: 10vh;
}
.con-quotes span{
  display: flex;
  /* align-items: end; */
  justify-content: center;
  font-weight: 600;
}
.con-copy-right{
  display: flex;
  /* align-items: end; */
  justify-content: end;
  position: absolute;
  bottom: 0%;
  right: 0;
  /* font-weight: 600; */
}

#clock {
  font-size: 24px;
  font-family: Arial, sans-serif;
}
.con-img img{
  border-radius: 100%;
  position: absolute;
  right: 35%;
  /* bottom: 15vh; */
  top: 25vh;
  height: 30vh;
  border: #000000 solid 1px;
  display: flex;
  align-items: center;
}
    
}

/* Medium (md) - 768px to 991px */
@media (min-width: 768px) and (max-width: 991px) {
  .about-text {
    font-size: 4vh;
  }
  .bg-about{
    font-size: 30vh;
  }
  .hardskill-text, .projects-heading, .right-arrow{
    font-size: 9vh;
    font-weight: 1000;
  }

  .list-softskill{
    font-size: 5vh;
  
  }
  .skill-box{
      height: 20vh;
  width: 20%;
  }
  
  .lock-contact, .pro-row-heading{
    font-size: 1.56vh;
  }
  .lock-contact{
    position: relative;
    left: 45%;
    top: 15%;
    width: 50%;
    /* background: rgb(129, 40, 40); */
    height: 70%;
    border-radius: 2vh;
    align-items: center;
    justify-content: center;
    font-weight: 1000;
    /* font-size: 1vh; */
  }
  .project-row{
    height: 8vh;
  }
  .lock img{
    height: 2.5vh;
    /* width:  ; */
  }
    .project-1-image{
  position: relative;
  left: -8%;
  z-index: 1;
}
.project-1-image img{
  height: 40vh;
  width: 40vw;
}
.pro-2 img{
  height: 50vh;
  width: 45vw;
}
.con-name{
  /* height: 15vh; */
  margin: 10vh;
  border: #000000 solid;
}
.con-name h1{
  font-size: 6.5vh;
  font-family: "Lucida Handwriting", cursive;
  margin: 1vh;
 
}
.con-border{
  
  height:  110vh;
  position: relative;
  top: 5vh;
}
.con-love{
  font-size: 4vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
  font-weight: 900;
  position: absolute;
  top: 55vh;
}
.con-quotes{
  font-size: 3vh;
  /* display: flex; */
  /* display: flex; */
  position: absolute;
  bottom: 10vh;
}
.con-quotes span{
  display: flex;
  /* align-items: end; */
  justify-content: center;
  font-weight: 600;
}
.con-copy-right{
  display: flex;
  /* align-items: end; */
  justify-content: end;
  position: absolute;
  bottom: 0%;
  right: 0;
  /* font-weight: 600; */
}

#clock {
  font-size: 24px;
  font-family: Arial, sans-serif;
}
.con-img img{
  border-radius: 100%;
  position: absolute;
  right: 35%;
  /* bottom: 15vh; */
  top: 25vh;
  height: 30vh;
  border: #000000 solid 1px;
  display: flex;
  align-items: center;
}
    
  
}

/* Small (sm) - 576px to 767px */
@media (min-width: 576px) and (max-width: 767px) {
  .about-text {
    font-size: 3vh;
  }
  .bg-about{
    font-size: 20vh;
  } 
  .hardskill-text, .projects-heading, .right-arrow{
    font-size: 7vh;
    font-weight: 1000;
  }

  .list-softskill{
    font-size: 4vh;
 
  }
  .skill-box{
      height: 20vh;
  width: 26.6%;
  }
    
   .pro-row-heading{
    font-size: 1.56vh;
  }
  .lock-contact{
    position: relative;
    left: 45%;
    top: 25%;
    width: 50%;
    /* background: rgb(129, 40, 40); */
    height: 50%;
    border-radius: 2vh;
    align-items: center;
    justify-content: center;
    font-weight: 1000;
    font-size: 1vh;
  }
  .project-row{
    height: 6vh;
  }
  .lock img{
    height: 2.5vh;
    /* width:  ; */
  }
  .project-1-image{
  position: relative;
  left: -8%;
  z-index: 1;
}
.project-1-image img{
  height: 30vh;
  width: 45vw;
}
.pro-2 img{
  height: 50vh;
  width: 45vw;
}

.con-name{
  /* height: 15vh; */
  margin: 10vh;
  border: #000000 solid;
}
.con-name h1{
  font-size: 4.5vh;
  font-family: "Lucida Handwriting", cursive;
  margin: 1vh;
 
}
.con-border{
  
  height:  110vh;
  position: relative;
  top: 5vh;
}
.con-love{
  font-size: 4vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
  font-weight: 900;
  position: absolute;
  top: 55vh;
}
.con-quotes{
  font-size: 3vh;
  /* display: flex; */
  /* display: flex; */
  position: absolute;
  bottom: 10vh;
}
.con-quotes span{
  display: flex;
  /* align-items: end; */
  justify-content: center;
  font-weight: 600;
}
.con-copy-right{
  display: flex;
  /* align-items: end; */
  justify-content: end;
  position: absolute;
  bottom: 0%;
  right: 0;
  /* font-weight: 600; */
}

#clock {
  font-size: 24px;
  font-family: Arial, sans-serif;
}
.con-img img{
  border-radius: 100%;
  position: absolute;
  right: 25%;
  /* bottom: 15vh; */
  top: 25vh;
  height: 30vh;
  border: #000000 solid 1px;
  display: flex;
  align-items: center;
}

    
}

/* Extra Small (xs) - 575px and down */
@media (max-width: 575px) {
  .about-text {
    font-size: 3vh;
  }
  .bg-about{
    font-size: 12vh;
  }
  .hardskill-text, .projects-heading, .right-arrow{
    font-size: 5vh;
    font-weight: 1000;
  }
  /* .hardskills{
    position: absolute;
  top: 100vh;
  } */
  .softskills{
    font-size: 6vh;
    height: 45vh;
  }
  .list-softskill{
    font-size: 2vh;
    /* width: 100%; */
    font-family: "Courier New", Courier, monospace;
  }

  .skill-box{
      height: 20vh;
  width: 40%;
  }

  .pro-row-heading{
    font-size: 1.3vh;
  }
  .lock-contact{
    position: relative;
    left: 14%;
    top: 25%;
    width: 80%;
    /* background: rgb(129, 40, 40); */
    height: 50%;
    border-radius: 2vh;
    align-items: center;
    justify-content: center;
    font-weight: 1000;
    font-size: 0.8vh;
  }
  .project-row{
    height: 6vh;
  }
  .lock img{
    height: 1.9vh;
    /* width:  ; */
  }
  .project-1-image{
  position: relative;
  left: -32%;
  z-index: 1;
  position: relative;
  bottom: 0vh;
}
.project-1-image img{
  height: 30vh;
  width: 45vw;

}
.pro-2 img{
  height: 50vh;
  width: 45vw;
}

.con-name{
  /* height: 15vh; */
  margin: 10vh;
  border: #000000 solid;
}
.con-name h1{
  font-size: 4.5vh;
  font-family: "Lucida Handwriting", cursive;
  margin: 1vh;
 
}
.con-border{
  
  height:  100vh;
  position: relative;
  top: 5vh;
}
.con-love{
  font-size: 4vh;
  /* color: #ffffff; */
  font-family: Playfair Display, serif;
  font-weight: 900;
  position: absolute;
  top: 45vh;
}
.con-quotes{
  font-size: 3vh;
  /* display: flex; */
  /* display: flex; */
  position: absolute;
  bottom: 10vh;
}
.con-quotes span{
  display: flex;
  /* align-items: end; */
  justify-content: center;
  font-weight: 600;
}
.con-copy-right{
  display: flex;
  /* align-items: end; */
  justify-content: end;
  position: absolute;
  bottom: 0%;
  right: 0;
  /* font-weight: 600; */
}

#clock {
  font-size: 24px;
  font-family: Arial, sans-serif;
}
.con-img img{
  border-radius: 100%;
  position: absolute;
  right: 10%;
  /* bottom: 15vh; */
  top: 15vh;
  height: 30vh;
  border: #000000 solid 1px;
}


  
}
    </style>
    <!-- <script src="test.js"></script> -->
</head>
<body>
<section id="rp">
<div class="fixed-page">
  <div class="navbar col-xs-10 offset-xs-1 col-sm-10 offset-sm-1 col-md-10 offset-md-1 col-lg-10 offset-lg-1 col-xl-10 offset-xl-1">
      <div class="leftnav 0">
        <div class="logodiv">
          <img src="images/logo rp.png" height="100%" alt="" class="logo ">
        </div>
        <div class="textnavd  d-flex justify-content-center  h-100  ">
          <p class="textnav  my-auto text-breakpoint-xs fs-1 text-breakpoint-sm fs-2 text-breakpoint-md fs-3 text-breakpoint-lg fs-4 text-breakpoint-xl fs-5">
            INNOVATE CREATE REPEAT </p>
        </div>
        <div class="contact  d-flex align-items-center justify-content-center">
          <span id="click-text"><p class="my-auto">
           <u> CONTACT</u></p>
          </span>
        </div>
      </div>
  </div>
  <!-- <section id="hiddendiv"> -->
  <div id="hidden-div" class=" col-sm-10 offset-sm-1 col-md-10 offset-md-1 col-lg-10 offset-lg-1 col-xl-10 offset-xl-1  " >
    <a href="https://www.instagram.com/rhishikesh_prince/" style="text-decoration: none; color: inherit;">
    <div class="instagram social-transition border border-black socials  d-flex align-items-center justify-content-center my-auto text-breakpoint-xs fs-1 text-breakpoint-sm fs-2 text-breakpoint-md fs-3 text-breakpoint-lg fs-4 text-breakpoint-xl fs-5 border">
        <div class="border-socials border d-flex align-items-center justify-content-center"><p class="my-auto">Instagram</p>
        </div>      
    </div></a>
    <a href="https://github.com/Rhishikesh-Prince/Rhishikesh_Prince"style="text-decoration: none; color: inherit">
    <div class="github social-transition border border-black socials d-flex align-items-center justify-content-center my-auto text-breakpoint-xs fs-1 text-breakpoint-sm fs-2 text-breakpoint-md fs-3 text-breakpoint-lg fs-4 text-breakpoint-xl fs-5">
        <div class="border-socials border d-flex align-items-center justify-content-center"><p class="my-auto">  Github</p>
        </div>
    </div></a>
    <a href="https://www.linkedin.com/in/rhishikesh-prince-8ab923240/"style="text-decoration: none; color: inherit">
    <div class="linkedin social-transition border border-black socials d-flex align-items-center justify-content-center my-auto text-breakpoint-xs fs-1 text-breakpoint-sm fs-2 text-breakpoint-md fs-3 text-breakpoint-lg fs-4 text-breakpoint-xl fs-5">
          <div class="border-socials border d-flex align-items-center justify-content-center"><p class="my-auto"> LinkedIn</p>
          </div>
    </div></a>
    <a href="mailto:rhishikeshprince32@gmail.com"style="text-decoration: none; color: inherit">
    <div class="mail social-transition border border-black socials d-flex align-items-center justify-content-center my-auto text-breakpoint-xs fs-1 text-breakpoint-sm fs-2 text-breakpoint-md fs-3 text-breakpoint-lg fs-4 text-breakpoint-xl fs-5">
          <div class="border-socials border d-flex align-items-center justify-content-center"><p class="my-auto">Email</p>
          </div>
    </div></a>
  </div>
<!-- </section> -->
  <div class="text-loop">
    <span class="looping-text  fst-italic ">
      RHISHIKESH PRINCE
    </span>
  </div>
  <div class="myphoto col-xl-6 offset-xl-3 col-xs-12 col-lg-6 offset-lg-3 col-md-8 offset-md-2 col-sm-8 offset-sm-2" >
    <img src="images/my photo.png" alt="" height="100%" width="100%">
  </div>
  <div class="gif col-xl-1 offset-xl-0 col-3 offset-0 col-sm-2 offset-sm-0 col-md-2 offset-md-0 col-lg-1 offset-lg-0">
    <img src="images/scroll.gif" alt="" width="100%" height="100%">
  </div>
  <div class="scrolldown"><p>SCROLL DOWN!</p>
  </div>
  <div class="copyright-box d-flex">
    <p>&#x24B8;2024</p>
  </div>
</div></section>
<div class="scrolling-page  ">
    <section id="about">
    <div class="about bg-black d-xl-flex  ">
      <div class="left-about  h-auto col-xl-4 mt-xl-5 mb-xl-5 col-md-12">
        <span class="about-heading ">
          About!
        </span>
      </div>
      <div class="right-about h-auto  col-xl-8 mt-xl-5 col-md-12 fs-xs-1  ">
        <span class="about-text">
        Rhishikesh Prince is a young and ambitious Python full-stack web developer from Kerala, with a strong desire 
        to work hard and explore the world of web development and ready to bring his skills to work on exciting projects.
        <br>
        I'm primed to take on new opportunities and make a meaningful impact in the web development world!
        </span>
        <!-- <div class="about-logo w-100  ">
          <img src="images/logo rp.png" width="100" alt=""> -->
        <!-- </div> --> 
      </div>
    </div>
  </section>
    <div class="bg-about col-12">
      ABOUT!
    </div>
    <div class="softskills ">
      <div class="right-arrow d-flex   justify-content-center" >	  Abilities</div>
      <br>
      <div class="list-softskill d-flex  justify-content-around   ">
        <div class="left-ss-list">
          <ul>
            <a href="https://in.pinterest.com/pin/318629742405844913/" style="text-decoration: none; color: inherit">
              <li>Communication
              </li>
            </a>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills"  style="text-decoration: none; color: inherit">
              <li>Teamwork
              </li>
            </a>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills"  style="text-decoration: none; color: inherit">
              <li>Adaptability</li>
            </a>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills"  style="text-decoration: none; color: inherit">
              <li>Patience
              </li>
            </a>
          </ul>
        </div>
        <div class="right-ss-list">
          <ul>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills "style="text-decoration: none; color: inherit">
              <li>Leadership
              </li>
            </a>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills "  style="text-decoration: none; color: inherit">
              <li>Creativity
              </li>
            </a>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills "  style="text-decoration: none; color: inherit">
              <li>Flexibility
              </li>
            </a>
            <a href="https://www.theforage.com/blog/basics/what-are-soft-skills-definition-and-examples#h-communication-skills "  style="text-decoration: none; color: inherit">
              <li>Critical thinking
              </li>
            </a>
          </ul>
        </div>
      </div>
    </div>
    <div class="blackline col-10 offset-1">
    </div>
    <div class="hardskills w-100 d-flex align-items-center justify-content-center">
      <div class="hardskill-text">
        Skills
      </div>
    </div>
    <div class="skills position-relative ">
      <div class="skill-box-container col-10 offset-1  d-flex  ">
        <div class="skill-box   ">
          <div class="skill-box-icon"><img src="images/python icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">Python</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/django icon.jpg" alt="" height="80" class="my-auto"></div>
          <div class="skill-box-text">Django</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/html icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">HTML</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/css icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">CSS</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/bootstrap icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">Bootstrap</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/javascript icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">JavaScript</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/mongo db icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">Mongo DB</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/Sqlite-square-icon.svg.png" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">SQLite</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/mysql icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">MySQL</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/jquery icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">JQuery</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/angular icon.jpg" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">Angular</div>
        </div>
        <div class="skill-box  ">
          <div class="skill-box-icon"><img src="images/flask cion.png" alt="" height="100" class="my-auto"></div>
          <div class="skill-box-text">Flask</div>
        </div>
    </div>
  </div>
  <div class="experience col-10 offset-1">
    <SPAN class="exp-heading ">EXPERIENCE&#8594; </SPAN><br> PYTHON FULL STACK WEB DEVELOPER - TRAINEE AT <br> <SPAn class="quest">
      QUEST INNOVATIVE SOLUTIONS PVT LTD (2023-present)
    </SPAn>
  </div>
  <div class="blackline col-10 offset-1">
  </div>
  <section id="work">
  <div class="projects col-10 offset-1">
    <div class="projects-heading">
       PROJECTS
    </div>

    <div class="project-elements ">

 <div class="pro-1-eCommerce project-row ">
        <div class="pro-row-heading col-4">
          <p style="margin-left: 5%">Try to remember!</p> 
        </div>
        <div class="pro-3 project-1-image  col-5">
          <img src="images/try to remember.gif" width="100%"  alt="">
        </div>
        <div class="lock-contact-container col-3">
          <a href="#contact" style="text-decoration: none; color: inherit">
          <div class="lock-contact d-flex ">
            <div class="pro-contact">
              CONTACT-
            </div>
            <div class="lock">
              <img src="images/lock icon.png" alt="">
            </div>
          </div></a>
        </div>
      </div>


      <div class="pro-1-eCommerce project-row ">
        <div class="pro-row-heading col-4">
          <p style="margin-left: 5%">E-commerce Website</p> 
        </div>
        <div class="project-1-image col-5">
          <img src="images/RedStore_EcommerceWebsiteDesign-GoogleChrome2024-09-0417-41-34-ezgif.com-video-to-gif-converter (1).gif"   alt="">
        </div>
        <div class="lock-contact-container col-3">
          <a href="#contact" style="text-decoration: none; color: inherit">
          <div class="lock-contact d-flex ">
            <div class="pro-contact">
              CONTACT-
            </div>
            <div class="lock">
              <img src="images/lock icon.png" alt="">
            </div>
          </div>
        </a>
        </div>
      </div>

      <div class="pro-1-eCommerce project-row ">
        <div class="pro-row-heading col-4">
          <p style="margin-left: 5%">Calculator using JavaScript</p> 
        </div>
        <div class="project-1-image pro-2 col-5">
          <img src="images/calculator js gif.gif" width="100%"  alt="">
        </div>
        <div class="lock-contact-container col-3">
          <a href="#contact" style="text-decoration: none; color: inherit">
          <div class="lock-contact d-flex ">
            <div class="pro-contact">
              CONTACT-
            </div>
            <div class="lock">
              <img src="images/lock icon.png" alt="">
            </div>
          </div></a>
        </div>
      </div>

      <!-- <div class="pro-1-eCommerce project-row ">
        <div class="pro-row-heading col-4">
          <p style="margin-left: 5%">E-commerce</p> 
        </div>
        <div class="project-1-image col-5">
          <img src="images/RedStore - Ecommerce Website Design -.png" width="100%"  alt="">
        </div>
        <div class="lock-contact-container col-3">
          <a href="#contact" style="text-decoration: none; color: inherit">
          <div class="lock-contact d-flex ">
            <div class="pro-contact">
              CONTACT-
            </div>
            <div class="lock">
              <img src="images/lock icon.png" alt="">
            </div>
          </div></a>
        </div>
      </div>

      <div class="pro-1-eCommerce project-row ">
        <div class="pro-row-heading col-4">
          <p style="margin-left: 5%">E-commerce</p> 
        </div>
        <div class="project-1-image col-5">
          <img src="images/RedStore - Ecommerce Website Design -.png" width="100%"  alt="">
        </div>
        <div class="lock-contact-container col-3">
          <a href="#contact" style="text-decoration: none; color: inherit">
          <div class="lock-contact d-flex ">
            <div class="pro-contact">
              CONTACT-
            </div>
            <div class="lock">
              <img src="images/lock icon.png" alt="">
            </div>
          </div></a>
        </div>
      </div> -->

     
      
    </div> 
  </div>
</section>

  <div class="blackline col-10 offset-1">
  </div>

<section id="contact">
  <div class="link-tree-container col-10 offset-1 border border-black">

    <div class="linktree-heading">
      <div class="linktree-heading-text">
        <h1 style="font-weight: 1000; font-family: Playfair Display, serif;">LINK TREE</h1>
      </div>
      <div class="linktree-heading-photo">
        <img src="images/smiling-removebg b.png" alt="">
      </div>
    </div>

    
     <a href="tel:+918606358367"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">Phone</h3>
      <img src="images/phone o.jpg" height="70%" alt="">
    </div></a>
    
     <a href="mailto:rhishikeshprince32@gmail.com"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">E-mail</h3>
      <img src="images/email.png" height="75%" alt="">
    </div></a>
    
     <a href="https://www.instagram.com/rhishikesh_prince/"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">Instagram</h3>
      <img src="images/instagram_1400829.png" height="90%" alt="">
    </div></a>
    
     <a href="https://github.com/Rhishikesh-Prince"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">Github</h3>
      <img src="images/github_5968866.png" height="90%" alt="">
    </div></a>
    
     <a href="https://www.linkedin.com/in/rhishikesh-prince-8ab923240/"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">LinkedIn</h3>
      <img src="images/linked inn.png" height="60%" alt="">
    </div></a>
    
     <a href="https://twitter.com/RhishikeshPrice"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">Twitter/X</h3>
      <img src="images/x.avif" height="60%" alt="">
    </div></a>
    
     <a href="images/Rhishikesh prince cv.pdf"style="text-decoration: none; color: inherit">
    <div class="linktree-row">
      <h3 style="font-weight: 1000; font-family: Playfair Display, serif;">Facebook</h3>
      <img src="images/face book.jpg" height="60%" alt="">
    </div></a>

  </div>
</section>

  <div class="text-loop-bottom">
    <!-- <span class="looping-text-bottom  fst-italic d-flex ">
      Thankfull <img src="images/minions.gif" alt="" style="margin-left:5%; ; border-radius: 50vh;">
      Greatfull <img src="images/MINIONS-2.gif" alt="" style="margin-left:5%; ; border-radius: 50vh;">
      Blessed <img src="images/minons-3.gif" alt="" style="margin-left:5%; ; border-radius: 50vh;">
    </span> -->
  </div>
  <div class="long-blackline  col-12 "></div>

  <div class="conclution  ">
    <div class="con-border  col-10 offset-1">
      <div class="con-name col-10 offset-1  d-flex align-items-center justify-content-center">
        <h1 >RHISHIKESH PRINCE</h1>
      </div> <div class="con-img col-xl-6 offset-xl-6"><img src="images/smiling-removebg w.png" alt=""></div>
      <div class="con-love col-xl-6">
        Made using HTML, CSS, JavaScript and love in Kerala, India! <div id="clock" class="d-flex justify-content-end"></div>
      </div>
     
      <div class="con-quotes col-xl-6">
        "I have not failed. I've just found 10,000 ways that won't work. At the end, I will win." <br> <span>-Thomas Edison</span>
      </div>
       <div class="con-copy-right">© 2024 Rhishikesh Prince. All right reserved.
      </div>
      
      

    </div>
   

  </div>


</div>



    <div class="bottom-navbar d-flex col-8 offset-2 col-md-6 offset-md-3 col-lg-4 offset-lg-4 col-xl-4 offset-xl-4">
      <a href="#rp"style="text-decoration: none; color: inherit">
        <div class="nav-elements">
          <img src="images/logo rp.png" height="100%" class="logo-nav" alt="">
        </div>
      </a>
      <a href="images/Rhishikesh prince cv.pdf"style="text-decoration: none; color: inherit">
        <div class="nav-elements  d-flex align-items-center justify-content-center">
          Bio
        </div>
      </a>
      <a href="#about " style="text-decoration: none; color: inherit">
        <div class="nav-elements  d-flex align-items-center justify-content-center">
          About
        </div>
      </a>
      <a href="#contact"style="text-decoration: none; color: inherit">
        <div class="nav-elements  d-flex align-items-center justify-content-center">
          Contact
        </div>
      </a>
      <a href="#work"style="text-decoration: none; color: inherit">
        <div class="nav-elements  d-flex align-items-center justify-content-center">
          Work
        </div>
      </a>
    </div>
   <script defer src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>    
    <script src="portfolio.js"></script>
</body>
</html>
