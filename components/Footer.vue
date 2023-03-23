<template>
  <div class="container">
    <div class="footer__head">
      <div class="left__wrapper">
        <nuxt-link to="/">
          <img src="../assets/images/logo-tienda.png" alt="logo" />
        </nuxt-link>
        <p>
          Join our newsletter for deals, new drops and inspiration sent straight
          to your inbox.
        </p>
        <div class="box__wrapper">
          <input type="text" placeholder="Ingrese su correo" />
          <span>Mantente actualizado</span>
        </div>
      </div>
      <div class="right__wrapper">
        <div class="box__wrapper">
          <h3>Shop</h3>
          <a href="#" class="wrapper__link">Shop Live Plants</a>
          <a href="#" class="wrapper__link">Shop Live Fish</a>
          <a href="#" class="wrapper__link">Shop Hardscape</a>
        </div>

        <div class="box__wrapper">
          <h3>Compañia</h3>
          <a href="#" class="wrapper__link">Sobre nosotros</a>
          <a href="#" class="wrapper__link">Contactanos</a>
          <a href="#" class="wrapper__link">Carrera</a>
        </div>

        <div class="box__wrapper">
          <h3 class="direction-title">Direccion</h3>
          <p>123 Some St Name Tampa, FL USA 33605</p>
        </div>

        <div class="box__wrapper">
          <h3>Siguenos</h3>
          <a href="#" class="social-media">
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M16.5 6H13.5C12.9477 6 12.5 6.44772 12.5 7V10H16.5C16.6137 9.99748 16.7216 10.0504 16.7892 10.1419C16.8568 10.2334 16.8758 10.352 16.84 10.46L16.1 12.66C16.0318 12.8619 15.8431 12.9984 15.63 13H12.5V20.5C12.5 20.7761 12.2761 21 12 21H9.5C9.22386 21 9 20.7761 9 20.5V13H7.5C7.22386 13 7 12.7761 7 12.5V10.5C7 10.2239 7.22386 10 7.5 10H9V7C9 4.79086 10.7909 3 13 3H16.5C16.7761 3 17 3.22386 17 3.5V5.5C17 5.77614 16.7761 6 16.5 6Z"
                fill="CurrentColor"
              ></path>
            </svg>
            Facebook
          </a>
          <a
            href="#
"
            class="social-media"
          >
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M16 3H8C5.23858 3 3 5.23858 3 8V16C3 18.7614 5.23858 21 8 21H16C18.7614 21 21 18.7614 21 16V8C21 5.23858 18.7614 3 16 3ZM19.25 16C19.2445 17.7926 17.7926 19.2445 16 19.25H8C6.20735 19.2445 4.75549 17.7926 4.75 16V8C4.75549 6.20735 6.20735 4.75549 8 4.75H16C17.7926 4.75549 19.2445 6.20735 19.25 8V16ZM16.75 8.25C17.3023 8.25 17.75 7.80228 17.75 7.25C17.75 6.69772 17.3023 6.25 16.75 6.25C16.1977 6.25 15.75 6.69772 15.75 7.25C15.75 7.80228 16.1977 8.25 16.75 8.25ZM12 7.5C9.51472 7.5 7.5 9.51472 7.5 12C7.5 14.4853 9.51472 16.5 12 16.5C14.4853 16.5 16.5 14.4853 16.5 12C16.5027 10.8057 16.0294 9.65957 15.1849 8.81508C14.3404 7.97059 13.1943 7.49734 12 7.5ZM9.25 12C9.25 13.5188 10.4812 14.75 12 14.75C13.5188 14.75 14.75 13.5188 14.75 12C14.75 10.4812 13.5188 9.25 12 9.25C10.4812 9.25 9.25 10.4812 9.25 12Z"
                fill="CurrentColor"
              ></path>
            </svg>
            Instagram
          </a>
          <a href="#" class="social-media">
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M20.9728 6.7174C20.5084 7.33692 19.947 7.87733 19.3103 8.31776C19.3103 8.47959 19.3103 8.64142 19.3103 8.81225C19.3154 11.7511 18.1415 14.5691 16.0518 16.6345C13.962 18.6999 11.1312 19.8399 8.19405 19.7989C6.49599 19.8046 4.81967 19.4169 3.29642 18.6661C3.21428 18.6302 3.16131 18.549 3.16162 18.4593V18.3604C3.16162 18.2313 3.26623 18.1267 3.39527 18.1267C5.06442 18.0716 6.67402 17.4929 7.99634 16.4724C6.48553 16.4419 5.12619 15.5469 4.5006 14.1707C4.46901 14.0956 4.47884 14.0093 4.52657 13.9432C4.57429 13.8771 4.653 13.8407 4.73425 13.8471C5.19342 13.8932 5.65718 13.8505 6.1002 13.7212C4.43239 13.375 3.17921 11.9904 2.99986 10.2957C2.99349 10.2144 3.02992 10.1357 3.096 10.0879C3.16207 10.0402 3.24824 10.0303 3.32338 10.062C3.77094 10.2595 4.25409 10.3635 4.74324 10.3676C3.28184 9.40846 2.65061 7.58405 3.20655 5.92622C3.26394 5.76513 3.40181 5.64612 3.5695 5.61294C3.73718 5.57975 3.90996 5.63728 4.02432 5.76439C5.99639 7.86325 8.70604 9.11396 11.5819 9.25279C11.5083 8.95885 11.4721 8.65676 11.4741 8.35372C11.501 6.76472 12.4842 5.34921 13.9634 4.76987C15.4425 4.19054 17.1249 4.56203 18.223 5.71044C18.9714 5.56785 19.695 5.31645 20.3707 4.96421C20.4202 4.93331 20.483 4.93331 20.5325 4.96421C20.5634 5.01373 20.5634 5.07652 20.5325 5.12604C20.2052 5.87552 19.6523 6.50412 18.9509 6.92419C19.5651 6.85296 20.1685 6.70807 20.7482 6.49264C20.797 6.45942 20.8611 6.45942 20.9099 6.49264C20.9508 6.51134 20.9814 6.54711 20.9935 6.59042C21.0056 6.63373 20.998 6.68018 20.9728 6.7174Z"
                fill="CurrentColor"
              ></path>
            </svg>
            Twitter
          </a>
        </div>
      </div>
    </div>
    <div class="footer_body">
      <div>
        <span>© 2022 Habitat Scapes, LLC</span>
        <p>Crafted with ♥️ by DesignComet</p>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.container {
  font-family: "Manrope", sans-serif;
  color: #1b1b1b;
}
.footer__head {
  display: flex;
  justify-content: space-evenly;
  align-items: flex-start;
  padding-top: 3rem;
  padding-bottom: 4rem;

  background-color: #fafafa;
}
.left__wrapper {
  width: 28vw;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.left__wrapper img {
  width: 9rem;
  height: 4rem;
}
.left__wrapper p {
  font-size: 1.25rem;
  font-weight: 400;
  text-align: left;
  line-height: 2rem;
}
.left__wrapper .box__wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.left__wrapper .box__wrapper > input {
  min-height: 2.75rem;
  border-top: none;
  border-left: none;
  border-right: none;
  outline: 0;
  padding-left: 1rem;
  border-bottom: solid rgb(154, 154, 156) 1px;
}

.right__wrapper {
  display: flex;
  justify-content: space-between;
  width: 50vw;
  margin-left: 5rem;
}

.right__wrapper .box__wrapper {
  display: flex;
  flex-direction: column;
}

.right__wrapper .box__wrapper h3 {
  font-weight: 600;
  font-size: 1rem;
  padding-bottom: 1rem;
}

.right__wrapper .box__wrapper .direction-title {
  padding-bottom: 0rem;
}

.wrapper__link {
  font-weight: 300;
  font-size: 0.875rem;
  text-decoration: none;
  padding-bottom: 1.5rem;
  color: #1b1b1b;
}

.right__wrapper .box__wrapper svg {
  padding-right: 1rem;
  width: 1.5rem;
  height: 1.5rem;
}

.right__wrapper .box__wrapper .social-media {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: #1b1b1b;
  margin-bottom: 1rem;
  font-weight: 300;
  font-size: 0.875rem;
}

.right__wrapper .box__wrapper p {
  font-weight: 300;
  font-size: 0.875rem;
  width: 8rem;
}

.footer_body {
  padding-top: 1.05rem;
  padding-bottom: 1.05rem;
  background-color: #1b1b1b;
  color: whitesmoke;
  font-size: 1rem;
  font-weight: 400;
}
.footer_body div {
  padding-left: 5%;
  padding-right: 5%;
  display: flex;
  align-items: center;
  font-size: 0.875rem;
  font-weight: 300;
}
.footer_body span {
  margin-right: 1rem;
}
.footer_body p {
  margin-left: 20rem;
}
</style>
