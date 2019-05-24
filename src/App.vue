<template>
  <div id="app">
    <div class="header-banner col-xs-12 col-md-12">
      <div class="right-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
      </div>
      <div class="container">
        <div class="left-headers">
          <h1>{{finch.title}}</h1>
          <h2>{{finch.subtitle}}</h2>
          <a href="#">www.teste.com</a>
        </div>

      </div>
    </div>
    <nav class="navmae">
      <div class="container">

        <ul class="menu">
          <span class="brandzera">Teste.</span>
          <li><a class="active" href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Services</a></li>
          <li><a href="#">Team</a></li>
          <li><a href="#">Portfolio</a></li>
          <li><a href="#">Contact</a></li>
          <ul class="social-media">
            <li><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
          </ul>
        </ul>
      </div>
    </nav>

    <div class="about-content">
      <div class="container">
        <h2>{{finch.subtitle}}</h2>
        <h3>{{finch.text}}</h3>
        <div class="col-md-4 col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <h4>Some fancy <em>colors</em></h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae explicabo ea.</p>
        </div>
        <div class="col-md-4 col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <h4>Some fancy <em>colors</em></h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae explicabo ea.</p>
        </div>
        <div class="col-md-4 col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <h4>Some fancy <em>colors</em></h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae explicabo ea.</p>
        </div>
      </div>
    </div>
    <div class="random-counters">
      <div class="container">
        <div class="col-md-3 noPadd col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <span>
            <em>{{finch.emptyCups}}</em>
            <p>Empty cups</p>
          </span>
        </div>
        <div class="col-md-3 noPadd col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <span>
            <em>{{finch.HappyClients}}</em>
            <p>Happy Clients</p>
          </span>
        </div>
        <div class="col-md-3 noPadd col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <span>
            <em>{{finch.BBQMeetins}}</em>
            <p>BBQ Meetings</p>
          </span>
        </div>
        <div class="col-md-3 noPadd col-xs-12">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <span>
            <em>{{finch.cocktailParties}}</em>
            <p>cocktail Parties</p>
          </span>
        </div>
      </div>
    </div>
    <div class="services">
      <div class="container">
        <h2>Our Services</h2>
        <h3>With Passion & Experience</h3>
        <div class="col-md-4 col-xs-12" v-for="service in finch.services">
          <img src="/src/assets/images/placeholder.png" width="40px"/>
          <span>
            <h4>{{service.name}}</h4>
            <p>{{service.content}}</p>
          </span>
        </div>
    </div>
  </div>


    <div class="contact">
      <div class="container">
        <h3 class="session-title">Contact</h3>
        <h4 class="session-subtitle">We would really love to hear from you!</h4>
        <div class="form-content">
          <form id="contact-form" class="col-md-8 col-xs-12" name="contact-form" method="POST">
            <div class="col-md-12 noPadd col-xs-12">
              <label for="name" class="">Your name</label>
              <input type="text" id="name" name="name" class="form-control">
            </div>
            <div class="col-md-12 noPadd col-xs-12">
              <label for="email" class="">Your email</label>
              <input type="text" id="email" name="email" class="form-control">
            </div>
            <div class="col-md-12 noPadd col-xs-12">
              <label for="subject" class="">Subject</label>
              <input type="text" id="subject" name="subject" class="form-control">
            </div>
            <div class="col-md-12 noPadd">
              <label for="message">Your message</label>
              <textarea type="text" id="message" name="message" rows="2" class="form-control md-textarea"></textarea>

            </div>

            <button type="submit">Send</button>

          </form>
          <div class="col-md-4 col-xs-12 contact-info">
            <h3>Contactinfo</h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Possimus unde eos eligendi repellendus natus consectetur, at doloremque dicta, alias!<br><br> Vero temporibus tempore qui incidunt consequatur, alias ad earum eligendi ullam.</p>

            <ul class="contact-items">
              <li>
                <img src="/src/assets/images/placeholder.png" width="40px"/>
                <h4>Rue de Halle 245<br>1000 Brussels</h4>
              </li>
              <li>
                <img src="/src/assets/images/placeholder.png" width="40px"/>
                <h4>03 123 45 67<br>0412 345 678</h4>
              </li>
              <li>
                <img src="/src/assets/images/placeholder.png" width="40px"/>
                <h4><a href="mailto:info@roran.com">info@roran.com</a><br><a href="mailto:question@roran.com">question@roran.com</a></h4>
              </li>
            </ul>

          </div>
        </div>
      </div>
    </div>

    <div class="footer">
      <p>© 2018 Finch Soluções  All rights reserved</p>
    </div>


  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "app",
  data() {
    finch: {
    }
    return {
      subtitle: "",
      text: {},
      title: {},

      services: {
        name: "",
        content: "",
        }
    };
  },
  mounted() {
    axios
      .get("https://api.myjson.com/bins/15k3rg")
      .then(response => {
        this.finch = response.data;
      })
      .catch(error => {
        console.log(error);
        this.errored = true;
      })
      .finally(() => (this.loading = false));
  }
};
</script>

<style>
body {
  margin: 0;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

main {
  text-align: center;
  margin-top: 40px;
}

header {
  margin: 0;
  height: 56px;
  padding: 0 16px 0 24px;
  background-color: #35495e;
  color: #ffffff;
}

header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: 0.02em;
  font-weight: 400;
  box-sizing: border-box;
  padding-top: 16px;
}

button {
  background: #51b767;
  color: #ffffff;
  padding: 15px;
  border-radius: 0;
  font-weight: bold;
  font-size: 15px;
  border: 0;
}

.cards {
  background: #f5f5f5;
  height: 400px;
}
.cards:hover {
  transform: translateY(-0.5em);
  background: #ebebeb;
}

.cards {
  column-count: 1;
  column-gap: 1em;
  margin-top: 70px;
}
</style>
