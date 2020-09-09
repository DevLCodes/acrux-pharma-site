<template>
  <div class="contact-component">
    <section class="left">
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
  </section>
      <section class="right">
        <div class='contact-details'>
          <h1>Reach us at</h1>
          <div class='inline-details'>
              <a> <i class="fas fa-phone-alt"></i></a>
              <p>(+91)9943887414</p>
          </div>
          <div class='inline-details'>
              <a> <i class="far fa-envelope"></i> </a> 
              <p>acruxpharmaceuticals@gmail.com</p>
          </div>
          <div class='inline-details'>
              <a> <i class="fas fa-address-card"></i></a>
              <div class='address'>Acrux Pharmaceuticals
                Old No.115, New No: 116/9 
                Hussaina Complex,
                Palakkarai
                Tricy-620008</div>
          </div>
        </div>
      </section>

  </div>
</template>

<style lang="scss">
.contact-details{
  display: inline-grid;
  .inline-details{
    display: inline-flex;
    margin: 3%;
    h1{
      font-size: 30px;
      float: left;
    }
    a{
      font-size: 27px;
      padding: 15px;
    }
    p{
         float: left;
        padding-left: 8%;
       font-size: 20px;
       
    }
    .address{
        float: left;
        padding-left: 8%;
        font-size: 20px;
        text-align: left;
        width: 41%;
       }
  }
}
.contact-component{
  color: black;
  height: 800px;
}

section {
    width: calc(50% - 90px);
    padding: 20px;
    margin: 20px;
    border-radius: 5px;
    &.left {
      float: left;
    }
    &.right {
      float: left;
    }
.input-container {
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
        height: 40px;
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
        height: 122px;
        width: 89%;
        padding: 5px 4% 5px;
        resize: none;
      }
      padding:10px;
    }
.contact-form {
  margin: 1% 10%;
  padding: 4% 2%;
  box-shadow: 0px 2px 5px 2px rgba(0, 0, 0, 0.25);
  border-radius: 25px;
    
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
  &:after {
    content: "";
    display: block;
    clear: both;
  }

  @media(max-width:768px) {
    margin-bottom:50px;
    width: calc(100% - 100px);
    section {
      width: 100%;
      margin: 0;
      &.left {
        margin-bottom: -30px;
      }
      &.right{
        float: left;
      }
    }
    .send-container {
      margin-right: 0;
      margin-top:15px;
      input{
        width:100%;
      }
    }
  }
}
</style>