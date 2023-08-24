<template>
 <div class="container">
  <div class="row">
    <div class="left">
      <h3>NEED HELP <span>WE ARE HERE</span></h3>
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
      <p>Chat with us on WhatsApp by scanning the QR code to add Sharenet as a contact.</p><br>
      <p>How it works</p>
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
  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3312.495128478341!2d18.627532676605476!3d-33.876900019480125!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1dcc41e6218f7ab3%3A0xbdd802ca53b92d43!2sSharenet%20(Pty)%20Ltd!5e0!3m2!1sen!2sza!4v1683021933066!5m2!1sen!2sza"></iframe>
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
  <p><a href="mailto: support@sharenet.co.za"> support@sharenet.co.za</a>
  </p>
 </div>
</template>

<style scoped>
*{
  box-sizing: border-box;
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
margin-right: -600px;
margin-top: -400px;
}
.heading {
display: flex;
justify-content: right;
gap: 40px;
margin-right: 210px;
}
.tel{
  display: flex;
  justify-content: right;
  gap: 55px;
  margin-right: 310px;
}
.email{
  display: flex;
  justify-content: right;
  gap: 80px;
  margin-right: 260px;
}
.container{
  width: 100%;
  height: 440px;
  padding-right: var(--bs-gutter-x,.75rem);
  padding-left: var(--bs-gutter-x,.75rem);
  margin-right: auto;
  margin-left: auto;

}
.row span{
  color: #71b5fc;
}
.right img{
  height: 400px;
  width: 650px;
  margin-left: 740px;
  position: relative;
  filter: blur(2px);
}
.background{
  background: rgb(243, 244, 246);
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 70px;
}
.content span{
  color: rgb(36, 220, 36);

}
.con{
    position: relative;
    width:600px;
    height: 500px;
    margin-right: 50px;
    border-radius: 5px;
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
}

</style>
