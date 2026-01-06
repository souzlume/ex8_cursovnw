<script setup></script>

<template>
    <footer>
        <section class="footer_geral">
            <div class="newsletter">
                <h2>Assine nossa Newsletter</h2>
                <form>
                    <label for="email"></label>
                    <input type="email" id="email" placeholder="Seu email" />
                </form>
                <button class="btn_newsletter">Inscrever-se</button>
            </div>
            <div class="info">
                <article class="contato">
                    <h3>Contato</h3>
                    <p>contato@inspiralens.com</p>
                    <p>Central de ajuda</p>
                    <p>Rio de Janeiro - Brasil</p>
                </article>
                <section class="sobre">
                    <h3>Sobre</h3>
                    <ul>
                        <li><a href="">Políticas</a></li>
                        <li><a href="">Politicas de privacidade</a></li>
                        <li><a href="">Blog</a></li>
                    </ul>
                </section>
            </div>
        </section>
        <section class="redes">
            <img src="../assets/facebook.svg" alt="Facebook" />
            <img src="../assets/linkedin.svg" alt="LinkedIn" />
            <img src="../assets/instagram.svg" alt="Instagram" />
            <img src="../assets/twitter.svg" alt="Twitter" />
        </section>
    </footer>
</template>

<style scoped lang="scss">
footer {
    display: flex;
    box-shadow: 1px 1px 5px #262626;
    flex-direction: column;
    align-items: center;
}

.newsletter {
    margin: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;

    h2 {
        padding: 1rem;
        font-weight: 500;
        font-size: 20px;
    }

    input {
        width: 320px;
        height: 45px;
        background-color: #e6e6e63b;
        border: none;
        padding: 1rem;
        border-radius: 5px;
        font-weight: 500;
    }

    .btn_newsletter {
        background-color: #e1306c;
        color: #ffffff;
        border: none;
        font-weight: 700;
        margin: 1rem;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 5px;
        padding: 0.5rem 1.5rem;
        cursor: pointer;

        &:hover {
            background-color: #e7a4ba;
            transition: 0.3s;
        }
    }
}

.contato {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.8rem;
    margin-bottom: 2rem;
}

h3 {
    font-size: 20px;
    font-weight: 600;
}

.sobre {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 2rem;
    gap: 0.8rem;

    ul {
        display: flex;
        flex-direction: column;
        gap: 0.7rem;
        align-items: center;
    }

    li {
        list-style: none;
    }

    a {
        text-decoration: none;
        color: #262626;

        &:hover {
            color: #e1306c;
            transition: 0.3s;
        }
    }
}

.redes {
    display: flex;
    gap: 1rem;
    padding: 0 0 2rem;

    img {
        cursor: pointer;
    }
}

@media (min-width: 769px) {
    footer {
        flex-direction: column;
        padding: 0 2rem;
    }

    .footer_geral {
        display: flex;
        width: 100%;
        flex-direction: row-reverse;
        align-items: center;
        justify-content: space-between;
    }

    .info {
        display: flex;
        gap: 3rem;
    }
}
</style>