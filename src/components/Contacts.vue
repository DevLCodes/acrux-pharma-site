<template>
  <div class="contact-component">
      <div class="contact-header">
      </div>
      <div class="contact-form-container">
        <div class="contact-info-container">
          <h1>WE WANT TO HEAR FROM YOU</h1>
          <p>To answer the many questions we receive about our company and our products, we offer detailed information about common areas of interest on our Web site. Please take a look at the options below. They should help you find the information you're looking for.</p>
        </div>
        <div class="contact-form">
          <form action="">
            <div class="input-container">
              <label for="name">Name</label>
              <input type="text" />
            </div>
            
            <div class="input-container">
              <label for="phone">Phone</label>
              <input type="text" />
            </div>
            <div class="input-container">
              <label for="email">Email</label>
              <input type="text" />
            </div>
            <div class="input-container">
              <label for="age" required>Description</label>
              <textarea name="comments" id=""></textarea>
            </div>
            <div class="send-container">
              <input type="submit" value="Send" onclick="return true"/>
             </div>
          </form>
       </div>
       
    </div>      
  </div>
</template>

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
            input {
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
}
</style>