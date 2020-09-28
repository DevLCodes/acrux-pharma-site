<template>
  <div class="contact-component" id="contact-component">
      <div class="contact-header">
      </div>
      <div class="contact-form-container">
        <div class="contact-info-container">
          <h1 class="contact-heading-one">WE WANT TO HEAR FROM YOU</h1>
          <h1 class="contact-heading-two">CONTACT US</h1>
          <p>To answer the many questions we receive about our company and our products, we offer detailed information about common areas of interest on our Web site. Please take a look at the options below. They should help you find the information you're looking for.</p>
        </div>
        <div class="contact-form">
          <form id="contact-form" @submit.prevent="sendEmail">
            <div class="input-container">
              <label for="name1">Name</label>
              <input  name="name" id="name" type="text" />
            </div>
            
            <div class="input-container">
              <label for="phone1">Phone</label>
              <input  name="contact" id="contact" type="text" />
            </div>
            <div class="input-container">
              <label for="email1">Email</label>
              <input name="email" id="email" type="text" />
            </div>
            <div class="input-container">
              <label for="des1" required>Description</label>
              <textarea id="message" name="message"></textarea>
            </div>
            <div class="send-container">
              <button type="submit">Send</button>
             </div>
          </form>
       </div>
       
    </div>      
  </div>
</template>
<script>
import emailjs from 'emailjs-com';

export default {
  methods: {
    sendEmail: () => {
      var form = document.getElementById('contact-form');
      /*var formData= {
        name: form.name.value,
        contact: form.contact.value,
        email: form.email.value,
        message:form.message.value
      }*/
      emailjs.sendForm('service_slyuaff', 'template_1j9cpbq', form,'user_c808FMaWZu3rvFJCTDMwW')
        .then((result) => {
            console.log('SUCCESS!', result.status, result.text);
        }, (error) => {
            console.log('FAILED...', error);
        });
    }
  }
}
</script>

<style lang="scss">
  $lightgrey: #E5E5E5;
  $white: #FFFFFF;
  $darkblue: #172131;
.contact-component{
  background: $white;
  min-height: 900px;
  .contact-header{
    height: 300px;
    background: $white;
    height: 20%;
  }
  .contact-form-container{
    display: inline-flex;
    margin: 1% 10%;
    padding: 4% 2%;
    .contact-info-container{
      padding: 1% 1%;
      margin: 1% 6%;
      color: $darkblue;
      .contact-heading-one{
        display: block;
      }
      .contact-heading-two{
        display: none;
      }
      h1{
        font-family: Rubik Mono One;
        font-style: normal;
        font-weight: normal;
        font-size: 48px;
        line-height: 71px;
        text-align: right;
      }
      p{
        font-family: Quicksand;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 194%;
/* or 33px */

text-align: justify;
text-indent: 2px;
      }
    }
    .contact-form{
      form{
        margin: 10% 1%;
      }
       box-shadow: 0px 2px 5px 2px rgba(0, 0, 0, 0.25);
       min-width: 48%;
       background: #FFFFFF;
       border-radius: 32px;
          .input-container {
             padding: 3% 1%;
          label {
            display: block;
            padding: 3px 5%;
            margin-bottom: 8px;
            float:left;
            color: #4c4b4b;
            font-size: 16px;
            font-family: 'Quicksand', sans-serif;
          }
          input,
          textarea {
            width: 89%;
            padding: 5px 4% 5px;
            height: 48px;
            border-radius: 20px;
            border: none;
            background: #DADADA;
            box-shadow: 0 2px 0px #77bd7d00;
            font-family: 'Quicksand', sans-serif;
            font-size: 16px;
            color: #757575;
            &:focus {
              outline: none;
            
            }
          }
          textarea {
            height: 154px;
            width: 89%;
            padding: 5px 4% 5px;
            resize: none;
          }
         
        }
           .send-container {
            margin: 1%;
            button {
              background: #308dff;
              border: none;
              color: white;
              padding: 15px 30px;
              border-radius: 20px;
              font-size: 16px;
              cursor: pointer;
              &:hover {
                background: #1e74de;
              }
            }
        }
    }
    
  }
  @media only screen and (max-width: 600px) {
    .contact-form-container{
      display: inline-block;
      margin: 1% 1%;
      .contact-info-container{
        .contact-heading-one{
        display: none;
      }
      .contact-heading-two{
        display: block;
      }
        h1{
            font-size: 48px;
            line-height: 68px;
            text-align: center;
        }
      }
      .contact-form{
        margin: 0 3%;
        .send-container{
          margin: 2%;
          padding: 4%;
        }
      }
    }
  }
}
</style>