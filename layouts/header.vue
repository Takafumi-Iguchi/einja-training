<template>
 <header class="header">
    <nav class="bc-black fc-white">
        <div class="menu">
            <button class="menu__button">
                <span class="menu__lineTop"></span>
                <span class="menu__lineMiddle"></span>
                <span class="menu__lineBottom"></span>
            </button>
        </div>
        <div class="logo">
            <nuxt-link to="/" class="logo text-lg">
                <img src="@/assets/img/logo-shoespicks.png" alt="">
            </nuxt-link>
        </div>　
    </nav>
  </header>
</template>

<script>
export default {
}
</script>

<style>
nav { 
    display: flex;
    justify-content: space-between;
    position: fixed;
    width: 100%;
    height: 63px;
    z-index: 998;
}
.menu {
    top: 0;
    right: 0;
    height: 100%;
    z-index: 998;
    transition: width .2s;
}

.menu--isOpen { width: 100vw; }/* メニューの範囲 */

.menu__button {
    position: fixed;
    left: 10px;
    top: 7px;
    width: 50px;
    height: 50px;
    z-index: 999;
    background-color: rgb(255, 255, 255, 0);
    border-radius: 5px;
    border: none;
  }

.menu__button:focus { outline: none; }

.menu span {
    display: block;
    width: 80%;
    margin: auto;
    height: 4px;
    background-color: #fff;
    position: absolute;
    left: 0;
    right: 0;
    top: calc((100% - 4px)/2);
    border-radius: 3px;
    transition: .2s;
}
.menu__lineTop { transform: translateY(-10px); }
.menu__lineBottom { transform: translateY(10px); }
.menu--isOpen .menu__lineTop { transform: rotate(45deg); }
.menu--isOpen .menu__lineMiddle { opacity: 0; }
.menu--isOpen .menu__lineBottom { transform: rotate(-45deg); }
.logo {
    height:100%;
}
.logo img {
    height: 100%;
    object-fit: contain;
}
</style>