<svelte:head>
    <title>Sneaker Store</title>
</svelte:head>

<body>
<main class="container">
    <section class="card">
      <div class="product-image">
        <img src="https://i.ibb.co/cNWqxGx/red.png" alt="OFF-white Red Edition" draggable="false" />
      </div>
      <div class="product-info">
        <h2>Nike X OFF-white</h2>
        <p>The 10: Air Jordan 1 off-white - Chicago</p>
        <div class="price">$999</div>
      </div>
      <div class="btn">
        <div class="buy-btn">
            {#each buy_1 as link}
                <a href={link.href} class="link">{link.title}</a> 
            {/each}
        </div>
        <button class="fav">
          <svg class="svg" id="i-star" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2">
            <path d="M16 2 L20 12 30 12 22 19 25 30 16 23 7 30 10 19 2 12 12 12 Z" />
          </svg>
        </button>
      </div>
    </section>
    <section class="card card-blue">
      <div class="product-image">
        <img src="https://i.ibb.co/0JKpmgd/blue.png" alt="OFF-white Blue Edition" draggable="false" />
      </div>
      <div class="product-info">
        <h2>Nike X OFF-white</h2>
        <p>Air Jordan 1 Retro High "Off-White - UNC" sneakers</p>
        <div class="price">$1599</div>
      </div>
      <div class="btn">
        <div class="buy-btn">
            {#each buy_2 as link}
                <a href={link.href} class="link">{link.title}</a> 
            {/each}
        </div>
        <button class="fav">
          <svg class="svg" id="i-star" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2">
            <path d="M16 2 L20 12 30 12 22 19 25 30 16 23 7 30 10 19 2 12 12 12 Z" />
          </svg>
        </button>
      </div>
    </section>
  </main>
</body>

<script>
    const buy_1 = [
        {
            title: 'Buy Now',
            href: '/buy_1',
        },
    ];
    const buy_2 = [
        {
            title: 'Buy Now',
            href: '/buy_2',
        },
    ];
</script>

<style>
:root {
  --dark-color-lighten: #f2f5ff;
  --red-card: #a62121;
  --blue-card: #4bb7e6;
  --btn: #141414;
  --btn-hover: #3a3a3a;
  --text: #fbf7f7;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  height: 80vh;
  width: 100vw;
  background-color: var(--dark-color-lighten);
  background-position: left top;
  font-family: 'Inter', sans-serif;
  background-repeat: no-repeat;
}
button {
  font-family: "Montserrat", sans-serif;
  display: inline-block;
  border: none;
  outline: none;
  border-radius: 0.2rem;
  color: var(--text);
  cursor: pointer;
}
img {
  max-width: 100%;
  height: 100%;
  user-select: none;
}
.container {
  height: 100%;
  width: 850px;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.card {
  position: relative;
  padding: 1rem;
  width: 350px;
  height: 450px;
  box-shadow: -1px 15px 30px -12px rgb(32, 32, 32);
  border-radius: 0.9rem;
  background-color: var(--red-card);
  color: var(--text);
  cursor: pointer;
}
.card-blue {
  background: var(--blue-card);
}
.product-image {
  height: 230px;
  width: 100%;
  transform: translate(0, -1.5rem);
  transition: transform 500ms ease-in-out;
  filter: drop-shadow(5px 10px 15px rgba(8, 9, 13, 0.4));
}
.product-info {
  text-align: center;
}
.card:hover .product-image {
  transform: translate(-1.5rem, -7rem) rotate(-20deg);
}
.product-info h2 {
  font-size: 1.4rem;
  font-weight: 600;
}
.product-info p {
  margin: 0.4rem;
  font-size: 0.8rem;
  font-weight: 600;
}
.price {
  font-size: 1.2rem;
  font-weight: 500;
}
.btn {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  margin-top: 0.8rem;
}
.buy-btn {
  background-color: var(--btn);
  padding: 0.6rem 3.5rem;
  font-weight: 600;
  font-size: 1rem;
  transition: 300ms ease;
}
.buy-btn:hover {
  background-color: var(--btn-hover);
}
.fav {
  box-sizing: border-box;
  background: #fff;
  padding: 0.5rem 0.5rem;
  border: 1px solid#000;
  display: grid;
  place-items: center;
}
.svg {
  height: 25px;
  width: 25px;
  fill: #fff;
  transition: all 500ms ease;
}
.fav:hover .svg {
  fill: #000;
}

@media screen and (max-width: 800px) {
  body {
    height: auto;
  }
  .container {
    padding: 2rem 0;
    width: 100%;
    flex-direction: column;
    gap: 3rem;
  }
}
</style>