---
layout: pages
title: Science Pulse Dispatches
description: "Automated newsletters with insights from our database."
social_description: "Automated newsletters with insights from our database."
---

<div class="tabset">
  <!-- Tab 1 -->
  <input type="radio" name="tabset" id="tab1" aria-controls="en" checked>
  <label for="tab1">Reports in English</label>

  <!-- Tab 2 -->
  <input type="radio" name="tabset" id="tab2" aria-controls="pt">
  <label for="tab2">Reports in Portuguese</label>

  <div class="tab-panels">
    <section id="marzen" class="tab-panel">
    <h2>Daily Dispatch</h2>
        <form action="https://sendy.voltdata.info/subscribe" method="POST" accept-charset="utf-8">
          <p>In the morning, know what the scientific community shared in Twitter in the last 24 hours.</p>
          <label for="name">Name</label><br/>
          <input type="text" name="name" id="name"/>
          <br/>
          <label for="email">Email</label><br/>
          <input type="email" name="email" id="email"/><br/><div style="display:none;">
          <label for="hp">HP</label><br/>
          <input type="text" name="hp" id="hp"/>
          </div>
          <input type="hidden" name="list" value="LJskW892Ny5Dr1oE4qSOepVw"/>
          <input type="hidden" name="subform" value="yes"/> <br>
          <input value="Subscribe to daily news" type="submit" name="submit" id="submit" style="background-color:#d91c5c !important;border:0px dashed #231f20;color:#fff"/>
      </form>


      <br/>
      <hr>

      <h2>Weekly Dispatch</h2>
      <form action="https://sendy.voltdata.info/subscribe" method="POST" accept-charset="utf-8">
        <p>Every Friday, know what the scientific community shared in Twitter in the last 7 days.</p>
        <label for="name">Name</label><br/>
        <input type="text" name="name" id="name"/>
        <br/>
        <label for="email">Email</label><br/>
        <input type="email" name="email" id="email"/><br/><div style="display:none;">
        <label for="hp">HP</label><br/>
        <input type="text" name="hp" id="hp"/>
        </div>
        <input type="hidden" name="list" value="ILmTZixssZ25zGmYWPztSg"/>
        <input type="hidden" name="subform" value="yes"/><br>
        <input value="Subscribe to weekly news" type="submit" name="submit" id="submit" style="background-color:#d91c5c !important;border:0px dashed #231f20;color:#fff"/>
        </form>

      <br/>
  </section>


    <section id="rauchbier" class="tab-panel">
    <h2>Daily Dispatch in Portuguese</h2>
    <form action="https://sendy.voltdata.info/subscribe" method="POST" accept-charset="utf-8">
        <p>In the morning, know what the Portuguese-language scientific community shared in Twitter in the last day.</p>
        <label for="name">Name</label><br/>
        <input type="text" name="name" id="name"/>
        <br/>
        <label for="email">Email</label><br/>
        <input type="email" name="email" id="email"/><br/><div style="display:none;">
        <label for="hp">HP</label><br/>
        <input type="text" name="hp" id="hp"/>
        </div>
        <input type="hidden" name="list" value="reKLi4A3xnM763ZFcG1h1kBg"/>
        <input type="hidden" name="subform" value="yes"/><br>
        <input value="Subscribe daily in Portuguese" type="submit" name="submit" id="submit" style="background-color:#d91c5c !important;border:0px dashed #231f20;color:#fff"/>
      </form>

        <br/>
        <hr>
        <h2>Weekly Dispatch in Portuguese</h2>
            <form action="https://sendy.voltdata.info/subscribe" method="POST" accept-charset="utf-8">
            <p>Every Friday, know what the Portuguese-language scientific community shared in Twitter in the last 7 days.</p>
            <label for="name">Name</label><br/>
            <input type="text" name="name" id="name"/>
            <br/>
            <label for="email">Email</label><br/>
            <input type="email" name="email" id="email"/><br/><div style="display:none;">
            <label for="hp">HP</label><br/>
            <input type="text" name="hp" id="hp"/>
            </div>
            <input type="hidden" name="list" value="FVDD892YnU1CQsb892892lz02ktA"/>
            <input type="hidden" name="subform" value="yes"/> <br>
            <input value="Subscribe weekly in Portuguese" type="submit" name="submit" id="submit" style="background-color:#d91c5c !important;border:0px dashed #231f20;color:#fff"/>
          </form>

        <br>
    </section>
  </div>

</div>

* * *

You can check how we will use this information in our [privacy policy page](../privacy).

Below you can read the main topics of our privacy policy:

*   If you choose to subscribe to our newsletter, your email will only be used for communication sent by the Science Pulse or Volt Data Lab;
*   We will not sell your email information to anyone, but we could share your email address with trusted partners;
*   We will not send you spam or harmful content;
*   We might integrate your email to other newsletters owned by Volt Data Lab, for strategic reasons;
*   We promise, within our power, to treat your information with zeal.

<style>
  form{
    max-width: 400px;
    margin: 0 auto;
  }
  h2{
    text-transform: uppercase
  }

  h2,h4{
    text-align: center
  }

.tabset > input[type="radio"] {
  position: absolute;
  left: -200vw;
}

.tabset .tab-panel {
  display: none;
}

.tabset > input:first-child:checked ~ .tab-panels > .tab-panel:first-child,
.tabset > input:nth-child(3):checked ~ .tab-panels > .tab-panel:nth-child(2),
.tabset > input:nth-child(5):checked ~ .tab-panels > .tab-panel:nth-child(3),
.tabset > input:nth-child(7):checked ~ .tab-panels > .tab-panel:nth-child(4),
.tabset > input:nth-child(9):checked ~ .tab-panels > .tab-panel:nth-child(5),
.tabset > input:nth-child(11):checked ~ .tab-panels > .tab-panel:nth-child(6) {
  display: block;
}

.tabset > label {
  position: relative;
  display: inline-block;
  padding: 5px 15px 20px;
  border: 0px solid transparent;
  border-bottom: 0;
  cursor: pointer;
  border-radius: 3px;
  font-weight: 600;
}

.tabset > label::after {
  content: "";
  position: absolute;
  left: 15px;
  bottom: 10px;
  width: 22px;
  height: 4px;
  background: #f4f4f4;
}

.tabset > label:hover,
.tabset > input:focus + label {
  color: #1cd999;
}

.tabset > label:hover::after,
.tabset > input:focus + label::after,
.tabset > input:checked + label::after {
  background: #1cd999;
}

.tabset > input:checked + label {
  border-color: #000;
  border-bottom: 1px solid #fff;
  margin-bottom: -1px;
}

.tab-panel {
  padding: 30px 0;
  border-top: 1px solid #d91c5c;
}
</style>
