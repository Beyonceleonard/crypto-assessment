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
    </div>
  </div>
  <div class="container">
    <form action="https://formspree.io/f/xlevpezg" method="post" role="form" class="formspree-form">
<label for="title">Title</label>
<select name="title" id="title">
  <option value="Mr">Mr</option>
  <option value="Mrs">Ms</option>
  <option value="Mx">Ms</option>
  <option value="Dr">Dr</option>
</select>
 <input type="text" name="name" class="form-control" placeholder="Your Name" required>
 <input type="email" name="email" class="form-control" placeholder="Your Email" required>
 <input type="text" name="subject" class="form-control" placeholder="Subject" required>
 <textarea name="message" rows="8" placeholder="Your Message" required></textarea>
 <div class="text-center"><button type="submit">Submit</button></div>
                  

  </form>
  </div>
 </div>
</template>

<style scoped>
*{
  box-sizing: border-box;

}
.container{
  width: 100%;
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
.container{
  display: flex;
  flex-direction: column;
  width: 100%;
}
.contact .formspree-form .form-group{
    padding-bottom: 8px;
}
.formspree-form input{
    height: 17px;
    border-radius: 6px;
} .formspree-form input,
 .formspree-form textarea{
    padding: 10px 12px;
}
 .formspree-form button[type="submit"]{
    background: #149ddd;
    border: 0;
    padding: 10px 12px;
    color: #fff;
    transition: 0.4s;
    border-radius: 4px;
}
.contact .formspree-form button[type="submit"]:hover{
    background: #004e72;
}

</style>
