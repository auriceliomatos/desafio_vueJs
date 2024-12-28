<template>
    <footer id="social-links" class="p-5 mb-4 mt-4 rounded-3">
        <div class="nos-acompanhe">
            <ul class="social-links">
             
                <li>
                    <a href="https://github.com/auriceliomatos" title="Siga  no GitHub">
                        <img src="/src/img/github-icon.png" alt=" GitHub" />
                    </a>
                </li>
            </ul>
            <p>
               Auricélio Matos
            </p>
        </div>
        <div>
            <p> &copy; calculadora automatica </p>
        </div>
    </footer>
</template>

<style scoped>
footer {
    background-color: #27ae60;
    color: white;
    text-align: center;
    padding: 16px 0;
    margin-top: 32px;
    width: 700px;
}

.nos-acompanhe {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    margin-bottom: 20px;
    align-items: center;
}

.social-links img {
    height: 50px;
    margin-right: 8px;
}

.social-links li {
    display: inline;
    margin-right: 8px;
}

.social-links li a {
    text-decoration: none;
}
</style>