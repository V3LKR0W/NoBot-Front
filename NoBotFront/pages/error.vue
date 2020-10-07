<template>
  

<div>
    <h1 class='mainheader verifiedcolor'>
        Oh no! An error! :(
    </h1>
    <div class='center'>

    <svg width="118" id='main' height="94" viewBox="0 0 118 94" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M118 79.0697L77.1179 46.9178L117.435 14.4799L99.2577 0L58.882 32.5788L18.0245 0.450417L0 14.8089L40.9116 47.0823L0.565417 79.6415L18.5899 94L59.0885 61.4212L99.8231 93.5496L118 79.0697Z" fill="#D21919"/>
    </svg>


    </div>

    <h1 class='subheader burple'>Dont worry, help is on the way!</h1>
    <h1 class='hint burple'><i>Most likely we couldn't find your token in our database, please try again. <a href='https://crying.world/report-bug'>If the issue persists please report it.</a></i></h1>

</div>
</template>

<script>
export default {

};
</script>

<style>
#main {
    -webkit-animation: error 3s infinite ease-in-out;
    animation: error 3s infinite ease-in-out;
}

.subheader{
    padding-top: 50px;
    text-align: center;
}
.hint {
    font-size: 15px;
    padding-top: 10px;
    text-align: center;
}


@keyframes error{
    0% {
        -webkit-transform: scale(.5);
        transform: scale(.5);
    }
    50%{
        -webkit-transform: scale(1);
        transform: scale(1);
    }
    100% {
        -webkit-transform: scale(.5);
        transform: scale(.5);
    }
}

.mainheader {
    padding-top: 200px;
    font-size: 60px;
    text-align: center;
}

.center {
    padding-top: 100px;
    text-align: center;
}

.hint a{
    text-decoration: none;
}

.verifiedcolor {
    color: #D21919;
}

.burple {
  color: #7289DA;
}



</style>

