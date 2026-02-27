<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Happy Birthday Didi!!!</title>
    <meta name="viewpoint" content="width=device-width, initial-scale=1" />
    <style>
        /*---Base Page---*/
        body{
            background: #000;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 
            'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans',
             'Helvetica Neue', sans-serif;
        }
        .quick-link {
            position: fixed;
            right: 10px;
            width: 35px;
            height: 35px;
            z-index: 999;
            background: #696969;
            border-radius: 50%;
            padding: 1px;
            text-align: center;
            color: #ddd;
            text-decoration: none;
            line-height: 35px;
            font-size: 13px;
            user-select: none;

        }
        .quick-link:nth-of-type(1) {top:10%;}
        .quick-link:nth-of-type(2) {top: 4%; z-index: 998;}
        .quick-link:nth-of-type(3) {top: 16%; z-index: 997;}
        .quick-link:nth-of-type(4) {top: 22%; z-index: 996;}

        #ui.love{
            position:absolute;
            top:50%;
            left:50%;
            margin: -225px 0 0 -225px;
            --i: 1;

        }

        #ui .love:last-child.love_word{
            color: #fff;
            font-size: 2rem;
            text-shadow: 0 0 10px #ea80b0;
        }

        #ui.love:last-child.love_word{
            color: #ea80b0;
            font-size: 1.4rem;
            text-shadow: 0 0 10px #fff;
        }

        #ui .love_word{
            color: #ea80b0;
            font-size: 1.4rem;
            transform: translateY(-100%) rotateZ(-30deg);
            text-shadow:0 0 10px #fff;
        letter-spacing: 2px;      
        white-space: nowrap;
        }

        #ui.love_horizontal{
            animation: horizontal 10000ms infinite alternate ease-in-out;
            animation-delay: calc(var(--i)*-300ms);
        }

        #ui.love_vertical{
            animation: vertical 20000ms infinite linear;
            animation-delay: calc(var(--i)*-300ms);
        }

        @keyframes horizontal {
            from{ transform: translateX(0px);}
            to{transform: translateX(450px);}
        }
        @keyframes vertical {
            0% {transform: translateY(180px);}
            10% {transform: translateY(45px);}
            15% {transform: translateY(4.5px);}
            18% {transform: translateY(0px);}
            20% {transform: translateY(4.5px);}
            22% {transform: translateY(34.61538px);}
            24% {transform: translateY(64.28571px);}
            25% {transform: translateY(112.5px);}
            26% {transform: translateY(64.28571px);}
            28% {transform: translateY(34.61538px);}
            30% {transform: translateY(4.5px);}
            32% {transform: translateY(0px);}
            35% {transform: translateY(4.5px);}
            40% {transform: translateY(45px);}
            50% {transform: translateY(180px);}
            71% {transform: translateY(428.57143px);}
            72.5% {transform: translateY(441.17647px);}
            75% {transform: translateY(450px);}
            77.5% {transform: translateY(441.17647px);}
            79% {transform: translateY(428.57143px);}
            100% {transform: translateY(180px);}
        }
        
    </style>
</head>

<body>   
    <!--Translated quick links--> 
    <a href="wishes.html"
    class="quick-link" title="Card">Card</a>
    <a href="cake.html"
    class="quick-link" title="Cake">Cake</a>


    <div id="ui"></div>

    <script>
        const N = 100;
        const ui = document.getElementById('ui');

        for (let i=1; i <=N; i++ ) {
            const love= document.createElement('div');
            love.className='love';
            love.style.setProperty('--i',i);
            
            const h= document.createElement('div');
            h.className='love_horizontal';

            const v= document.createElement('div');
            v.className='love_vertical';

            const word= document.createElement('div');
            word.className= 'love_word';
            word.textContent='Happy Birthday Didi!';

            v.appendChild(word);
            h.appendChild(v);
            love.appendChild(h);

            <svg class="heart-loader" xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#" xmlns:svg="http://www.w3.org/2000/svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 90 90" version="1.1">
  <g class="heart-loader__group">
    <path class="heart-loader__square" stroke-width="1" fill="none" d="M0,30 0,90 60,90 60,30z"/>
    <path class="heart-loader__circle m--left" stroke-width="1" fill="none" d="M60,60 a30,30 0 0,1 -60,0 a30,30 0 0,1 60,0"/>
    <path class="heart-loader__circle m--right" stroke-width="1" fill="none" d="M60,60 a30,30 0 0,1 -60,0 a30,30 0 0,1 60,0"/>
    <path class="heart-loader__heartPath" stroke-width="2" d="M60,30 a30,30 0 0,1 0,60 L0,90 0,30 a30,30 0 0,1 60,0" />
  </g>
</svg>

<style>
    body {background-color: black;}
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

$strokeColor: grey;
$heartColor: #db3434;
$size: 300px; // change this to manipulate overall size
$totalAnim: 7s;
$delay: .1s;
$squareLen: 240;
$circleLen: 188.522;
$heartLen: 308.522;
$svgSize: 90px;
$circleW: 60px;

.heart-loader {
  position: absolute;
  display: block;
  left: 50%;
  top: 50%;
  margin-top: $size/-2;
  width: $size;
  height: $size;
  overflow: visible;
  
  &__group {
    transform-origin: 0 $svgSize;
    animation: group-anim $totalAnim $delay infinite;
  }
  
  &__square {
    stroke: $strokeColor;
    stroke-dasharray: $squareLen, $squareLen;
    stroke-dashoffset: $squareLen;
    animation: square-anim $totalAnim $delay infinite;
  }
  
  &__circle {
    stroke: $strokeColor;
    stroke-dasharray: $circleLen, $circleLen;
    stroke-dashoffset: $circleLen;
    transform-origin: $circleW $circleW/2;
    
    &.m--left {
      animation: left-circle-anim $totalAnim $delay infinite;
    }
    
    &.m--right {
      animation: right-circle-anim $totalAnim $delay infinite;
    }
  }
  
  &__heartPath {
    stroke: $heartColor;
    fill: transparent;
    stroke-dasharray: $heartLen, $heartLen;
    stroke-dashoffset: $heartLen;
    animation: heart-anim $totalAnim $delay infinite;
  }
}
@keyframes square-anim {
  12% {
    stroke-dashoffset: 0;
  }
  43% {
    stroke-dashoffset: 0;
    opacity: 1;
  }
  85% {
    stroke-dashoffset: 0;
    opacity: 0;
  }
  100% {
    stroke-dashoffset: 0;
    opacity: 0;
  }
}
@keyframes left-circle-anim {
  12% {
    stroke-dashoffset: $circleLen;
  }
  31% {
    stroke-dashoffset: 0;
    transform: translateY(0);
  }
  41% {
    stroke-dashoffset: 0;
    transform: translateY($circleW/-2);
  }
  43% {
    stroke-dashoffset: 0;
    transform: translateY($circleW/-2);
    opacity: 1;
  }
  85% {
    stroke-dashoffset: 0;
    transform: translateY($circleW/-2);
    opacity: 0;
  }
  100% {
    stroke-dashoffset: 0;
    transform: translateY($circleW/-2);
    opacity: 0;
  }
}
@keyframes right-circle-anim {
  12% {
    stroke-dashoffset: $circleLen;
  }
  31% {
    stroke-dashoffset: 0;
    transform: translateX(0);
  }
  41% {
    stroke-dashoffset: 0;
    transform: translateX($circleW/2);
  }
  43% {
    stroke-dashoffset: 0;
    transform: translateX($circleW/2);
    opacity: 1;
  }
  85% {
    stroke-dashoffset: 0;
    transform: translateX($circleW/2);
    opacity: 0;
  }
  100% {
    stroke-dashoffset: 0;
    transform: translateX($circleW/2);
    opacity: 0;
  }
}
@keyframes group-anim {
  43% {
    transform: rotate(0);
  }
  54% {
    transform: rotate(-45deg);
  }
  90% {
    transform: rotate(-45deg);
    opacity: 1;
  }
  97% {
    transform: rotate(-45deg);
    opacity: 0;
  }
  100% {
    transform: rotate(-45deg);
    opacity: 0;
  }
}
@keyframes heart-anim {
  55% {
    stroke-dashoffset: $heartLen;
    fill: transparent;
  }
  70% {
    stroke-dashoffset: 0;
    fill: transparent;
  }
  87% {
    stroke-dashoffset: 0;
    fill: $heartColor;
  }
  100% {
    stroke-dashoffset: 0;
    fill: $heartColor;
  }
}

.other {
  position: absolute;
  left: 0;
  bottom: 0.5rem;
  width: 100%;
  text-align: right;
  
  &__link {
    font-size: 1.3rem;
    margin: 0 1rem;
  }
}
</style>
            ui.appendChild(love);

        }

    </script>
</body>
</html>
