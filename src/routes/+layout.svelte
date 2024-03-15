<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">Главная</a>
    </div>
</nav>

<div class="container">
    <slot></slot>
</div>
    
<style>
    .container {
        max-width: 1400px;
        margin: 50px auto;
    }
</style>