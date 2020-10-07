<template>
  

<div>
    <h1 class='mainheader verifiedcolor'>
        Successfully verified! 
    </h1>
    <div class='center'>

        <svg width="100" height="94" viewBox="0 0 118 94" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path id='main' d="M99.7346 0L44.25 57.2262L18.2605 32.4349L0 50.8194L44.25 94L118 18.3795L99.7346 0Z" fill="#34CF46"/>
        </svg>


    </div>

    <h1 class='subheader burple'>You may close this window.</h1>
    <h1 class='hint burple'><i>Don't forget to click the (☑️) emote in discord</i></h1>

</div>
</template>

<script>
export default {

};
</script>

<style>
#main {
    -webkit-animation: check 3s infinite ease-in-out;
    animation: check 3s infinite ease-in-out;
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


@keyframes check{
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

.verifiedcolor {
    color: #34cf46;
}

.burple {
  color: #7289DA;
}



</style>

