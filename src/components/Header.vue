<template>
    <div class="header-topbar">
        <a href="/">
            <img alt="Vue logo" class="logo" src="../assets/logo.svg" />
        </a>
        <input type="text" placeholder="Search" value="">
        <div class="header-links">
            <a href="/news">News</a>
            <a href="/about us">About Us</a>
        </div>
    </div>
</template>

<style>
input {
    background: rgba(44, 44, 44, 1.0) url("assets/search-icon.svg") no-repeat 15px center;
    color: var(--color-heading);
    font-size: 16px;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px,
        rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
    background-size: 15px 15px;
    border-radius: 5px;
    border: none;
    margin: 20px;
    padding: 10px 45px;
}

@media (min-width: 1024px) {
    input {
        width: 350px;
    }
}

.header-topbar {
    position: sticky;
    top: 0px;
    left: 0px;
    display: flex;
    height: 80px;
    width: 100%;
    background: var(--color-background-soft);
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
  