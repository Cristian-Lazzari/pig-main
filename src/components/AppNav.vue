<script>

</script>

<template>
    <div class="header">
        <div class="logo">
            <span class="logo-up">federalist</span>
            <span class="logo-down">pig</span>
        </div>
        <ul class="nav">
            <li class="menu"> <span>menu</span></li>
            <li class="menu"><span>catering</span> </li>
            <li class="menu">locations</li>
            <li class="menu">bbq box</li>
            <li class="menu">supper club</li>
            <li class="menu">gift cards</li>
            <li class="orders-online">orders online</li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
*{
    text-transform: uppercase;
}
.header{
    background-color: #ffd700;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.logo{
   display: flex;
   flex-direction: column;
   font-size: 45px;
   padding: 5px 30px;
   
}

.nav{
    padding: 0px 30px;
    height: 100%;
    display: flex;
    gap: 20px;
    font-size: 16px;
}

.menu, .catering, .locations, .bbq-box, .supper-club, .gift-cards, .orders-online{
    padding: 7px 5px;
    position: relative;

}

.menu::after  {
    content: ' ';
    background-color: black;
    width: 0%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    transition: all linear 2s;
    z-index: 1;
    display: block;
}
.menu:hover::after{
    content: ' ';
    background-color: black;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    transition: all 2s linear  ;
    z-index: 1;
    display: block;
} 

.nav{
    .menu{
        span{
            color: black;
            padding: 5px;
            
            transition: all 2s linear  2s;
            display: block;
            position: relative;
            z-index: 3;
        }
        span:hover{
            color: #ffd700;
            padding: 5px;
        
            display: block;
            position: relative;
            z-index: 3;
        }
    }
}
.orders-online{
    border: 2px solid black;
    padding: 5px 10px;
}
.orders-online:hover{
    padding: 5px 10px;
    background-color: black;
    color: #ffd700;
    transition: all  linear 0.2s ;
}
</style>