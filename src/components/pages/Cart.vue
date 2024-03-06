<script>
import Header from '../Header.vue'
import Footer from '../Footer.vue'

</script>

<style scoped>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
    }

    header {
      background-color: #2c3e50;
      color: #ecf0f1;
      text-align: center;
      padding: 1em 0;
    }

    main {
      max-width: 800px;
      margin: 20px auto;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      border-radius: 8px;
    }

    .cart-item {
      border-bottom: 1px solid #ddd;
      padding: 15px 0;
      display: flex;
      align-items: center;
    }

    .cart-item img {
      width: 80px;
      height: 80px;
      border-radius: 4px;
      margin-right: 15px;
    }

    .cart-item-details {
      flex-grow: 1;
    }

    .cart-item-details h3 {
      margin: 0;
      font-size: 1.2em;
    }

    .cart-item-details p {
      color: #888;
      margin: 5px 0;
    }

    .cart-total {
      margin-top: 20px;
      text-align: right;
    }

    .cart-actions {
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
    }

    .cart-actions a {
      background-color: #3498db;
      color: #fff;
      text-decoration: none;
      padding: 10px 20px;
      border-radius: 4px;
      transition: background-color 0.3s ease;
    }

    .cart-actions a:hover {
      background-color: #2980b9;
    }
</style>
<template>
    <header>
    <h1>FootMob Shop</h1>
  </header>
    <div class="cart-item">
      <img src="https://pbs.twimg.com/media/EW8DRS3WsAY4gIT.jpg" alt="Product 1">
      <div class="cart-item-details">
        <h3>FootMob Shirt</h3>
        <p>Price: $25.00</p>
        <p>2 Left In Stock!! Buy Fast!</p>
      </div>
    </div>

    <div class="cart-item">
      <img src="https://play-lh.googleusercontent.com/6L1u_v2JGG4Rpkh6UuHD8m5xNDMddxUTp6lcO86fgTzJ-SC8Fphgz7CkLZklnS8Dfjs=s256-rw" alt="Product 2">
      <div class="cart-item-details">
        <h3>FootMob Premium App</h3>
        <p>Price: $5.50 </p>
      </div>
    </div>

    <div class="cart-total">
      <p>Total: $69.97</p>
    </div>

    <div class="cart-actions">
      <a href="#">Continue Shopping</a>
      <a href="#">Checkout</a>
    </div>
</template>