<script>
import Dropdown from './widgets/Dropdown.vue';
export default {
    data() {
        return {
            options: ['Company', 'Careers']
        }
    },
    components: { Dropdown }
}
</script>

<template>
    <div class="header-topbar">
        <a href="/#/">
            <img alt="Vue logo" class="logo" src="https://www.fotmob.com/img/fotmob_icon_2017.png" />
        </a>
        <input type="text" placeholder="Search" value="">
        <div class="header-links">
            <!-- 5. change all href sources to start with /#/. You will have to do it for dropdown as well. -->
            <a href="/#/home">Home</a>
            <a href="/#/news">News</a>
            <a href="/#/cart">Cart</a>
            <Dropdown :options="options" text="About Us">
            </Dropdown>
        </div>
    </div>
</template>

<style>
input {
    background: rgba(44, 44, 44, 1.0) url("assets/search-icon.svg") no-repeat 15px center;
    color: var(--color-heading);
    font-size: 16px;
    box-shadow: r
    gba(50, 50, 93, 0.25) 0px 2px 5px -1px,
        rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
    background-size:40px 40px;
    border-radius: 16px;
    border: none;
    margin: 20px;
    padding: 10px 40px;
}

@media (min-width: 1024px) {
    input {
        width: 350px;
    }
}

.header-topbar {
    z-index: 1000;
    position: sticky;
    top: 0px;
    left: 0px;
    display: flex;
    background-color: rgb(236, 94, 177);
    align-items: center;
    justify-content: space-between;
    padding: 0 16px;
}

.header-links {
    display: flex;
    justify-content: flex-end;
}

.header-links>* {
    margin: 0 10px;
}
</style>
  