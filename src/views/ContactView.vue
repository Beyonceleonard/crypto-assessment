<template>
 <div class="container">
  <div class="row">
    <div class="left">
      <h3>NEED HELP <span>WE ARE HERE</span></h3>
    </div>
    <div class="text">
      <h4>CALL US</h4>
      <p>Contact us on +27 (0)21 700 4800</p>
      <p>Monday- Friday, 8am- 5pm</p>
    </div>
    <div class="msg">
      <h4>SEND US A MESSAGE</h4>
      <p>Contact our support centre and we'll get back to you as soon as possible. During business hours, we will respond within 48 hours. Email us on support@sharenet.co.za</p>
    </div>
    <div class="right">
      <img src="https://i.postimg.cc/QtXcYTsn/onur-binay-m-Vc-TLc-RAkn-M-unsplash.jpg">
    </div>
  </div>
 </div>
 <div class="background">
  <div class="content">
    <h3>TALK TO US ON <span>WhatsApp</span></h3>
    <div class="info">
      <p>Chat with us on <span>WhatsApp</span> by scanning the QR code to add Sharenet as a contact.</p><br>
      <h6>How it works</h6>
      <ul>
        <li>Open WhatsApp to chat with us on your computer, or scan the QR code to add Sharenet as a contact</li>
        <li>Say "Hi" to us in the WhatsApp chat to start the conversation</li>
        <li>Follow the prompts to complete your request</li>
      </ul>
      <div class="image">
        <img src="https://i.postimg.cc/05SyB9nY/Sharenet-Whats-App-1eb8ee79.png">
      </div>
    </div>
  </div>
  <div class="con">
            <div class="form">
            <div class="contact-form">
              <h3><span>COMPLETE THE FORM </span>BELOW AND WE WILL GET BACK TO YOU</h3>
                <form action="https://formspree.io/f/moqzlyyd" method="POST">
                    <div class="input-box">
                        <input type="text" name="name" class="input">
                        <label for="">FirstName:</label>
                    </div>
                    <div class="input-box">
                        <input type="text" name="name" class="input">
                        <label for="">LastName:</label>
                    </div>
                    <div class="input-box">
                        <input type="email" name="email" class="input">
                        <label for="">Email:</label>
                    </div>
                    <div class="input-box">
                        <input type="tel" name="phone" class="input">
                        <label for="">Cellphone:</label>
                    </div>
                    <div class="input-box textarea" >
                        <textarea name="message" class="input"></textarea>
                        <label for="">Message:</label>
                    </div>
                    <input type="submit" value="Send" class="btn-dark">
                </form>
            </div>
        </div>
     </div>
 </div>
 <div class="map">
  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3312.495128478417!2d18.627532675510697!3d-33.876900019478164!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1dcc41e6218f7ab3%3A0xbdd802ca53b92d43!2sSharenet%20(Pty)%20Ltd!5e0!3m2!1sen!2sza!4v1692958231649!5m2!1sen!2sza" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
 </div>
 <div class="subtitle">
  <h3>FIND US <span>HERE</span></h3>
 </div>
 <div class="heading">
  <p>Head Office</p>
  <p>301, 3rd Floor Imperial Terraces
    <br>
    Tyger Waterfront
    <br>
    Carl Cronje Drive
    <br>
    Bellville, Cape Town
    <br>
    7530
  </p>
 </div>
 <div class="tel">
  <p>Telephone</p>
  <p><a href="tel: +27217004800">(021) 700 4800</a>
    <br>
    <a href="tel: +27217004800"> +27 21 700 4800</a>
  </p>
 </div>
 <div class="email">
  <p>Email</p>
  <p>support@sharenet.co.za</p>
 </div>
</template>

<style scoped>
*{
  box-sizing: border-box;
}
.text h4{
  display: flex;
  margin-left: -50px;
  margin-top: 2rem;
  font-size: 22px;
  font-weight: 600;
  color: #000000;
}
.text p{
  display: flex;
  margin-left: -50px;
  margin-top: 0.9rem;
  font-size: 14px;
  font-family: Arial, Helvetica, sans-serif;
  color: black;
}
.msg h4{
  display: flex;
  margin-left: -50px;
  margin-top: 2rem;
  font-size: 22px;
  font-weight: 600;
  color: #000000;
}
.msg p{
  display: flex;
  margin-left: -55px;
  margin-top: 0.9rem;
  font-size: 14px;
  font-family: Arial, Helvetica, sans-serif;
  width: 395px;
  color: black;
}
.left h3{
  display: flex;
  margin-left: -50px;
  margin-top: 2rem;
  font-size: 30px;
  color: black;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.map{
  display: flex;
  margin-top: 5rem;
  margin-left: 20px;
  height: 400px;
}
.subtitle h3 span{
  color: #71b5fc;
}
.subtitle{
display: block;
float: right;
margin-right: 555px;
margin-top: -400px;
}
.heading {
display: flex;
float: right;
gap: 40px;
margin-right: 400px;
margin-top: -340px;
color: black;
}
.tel{
  display: flex;
  float: right;
  gap: 55px;
  margin-right: 500px;
  margin-top: -210px;
  color: black;
}
.email{
  display: flex;
  float: right;
  gap: 80px;
  margin-right: 450px;
  margin-top: -130px;
  color: black;
}
.container{
  width: 100%;
  height: 440px;
  padding-right: var(--bs-gutter-x,.75rem);
  padding-left: var(--bs-gutter-x,.75rem);
  margin-right: auto;
  margin-left: auto;
  margin-top: 5rem;
}
.row span{
  color: #71b5fc;
}
.right img{
  height: 425px;
  width: 650px;
  margin-left: 740px;
  position: relative;
  filter: blur(1.7px);
  margin-top: -370px;
}
.background{
  background: rgb(243, 244, 246);
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 70px;
  margin-top: -10px;
}
.content span{
  color: rgb(36, 220, 36);
  font-size: 30px;
  font-weight: bold;
}
.content h3{
  color: black;
  font-size: 28px;
  font-weight: bold;
  margin-right: 350px;
}
.info span{
  color: black;
  font-size: 14px;
}
.info p{
  margin-right: 130px;
  color: black;
}
.info h6{
  margin-right: 620px;
  color: black;
}
.info li{
  color: black;

}
.con{
    position: relative;
    width:600px;
    height: 500px;
    margin-right: 50px;
    border-radius: 5px;
    margin-bottom: 30px;
}
.form{
    padding: 3.3rem 2.2rem;
    z-index: 10;
    overflow: hidden;
    position:relative;
}
.input-box{
    position: relative;
    margin: 1rem 0;
}

.input{
   width: 500px;
   outline: none; 
   border: 2px solid #67eb50f2;
   background: none;
   padding: 0.6rem 5rem;
   color: #000000;
   font-size: 0.95rem;
   font-weight: 500;
   letter-spacing: 0.5px;
   border-radius: 10px;
   transition: 0.4s;
}
textarea.input{
    padding: 1.8rem 0.2rem;
    min-height: 60px;
    border-radius: 11px;
    resize: none;
    overflow-y: auto;
}
.input-box label{
    position: absolute;
    top: 50%;
    left: 15px;
    transform: translateY(-50%);
    padding: 0.0.4rem;
    color: #000000;
    font-size: 0.9rem;
    font-weight: 400;
    pointer-events: none;
    z-index: 1000;
    transition: 0.6s;
}
.input-box.textarea label{
    top: 1rem;
    transform: translateY(0);
}
.btn-dark{
  padding: 0.6rem 1.3rem;
    background-color: #113145;
    border: 2px solid #67eb50f2;
    font-size: 0.95rem;
    color: #fbf7f7;
    line-height: 1;
    border-radius: 15px;
    width: 180px;
    height: 35px;
    outline: none;
    cursor: pointer;
    transition: 0.3s;
    margin: 0;
}
.btn-dark:hover{
    background-color:#67eb50f2;
    color: #000000f2;
}
.contact-form h3 span{
  color: black;
}
.contact-form h3{
  color: #686363;
  font-size: 25px;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: 100;
}
.content {
  margin-right: 90px;
  margin-top: 110px;
}

</style>
