<style>
  .tab {
    display: inline-block;
    margin-right: 10px;
    padding: 10px;
    border: 1px solid black;
    border-radius: 5px 5px 0 0;
    cursor: pointer;
  }
  .tab.active {
    background-color: white;
    border-bottom: none;
  }
  .tab-content {
    display: none;
    padding: 20px;
    border: 1px solid black;
    border-top: none;
  }
  .tab-content.active {
    display: block;
  }
</style>

<div style="display: flex; align-items: center;">
  <img src="./images/IMG_1352.JPG" alt="Adam Potter" style="width: 200px; height: 300px; border-radius: 50%;">
  <p style="margin-left: 20px;">Hello, my name is Adam Potter. I am a computer science student at UCSD. </p>
</div>

<div style="text-align: right;">
  <div class="tab active" onclick="openTab(event, 'tab1')">Tab 1</div>
  <div class="tab" onclick="openTab(event, 'tab2')">Tab 2</div>
  <div class="tab" onclick="openTab(event, 'tab3')">Tab 3</div>
</div>

<div id="tab1" class="tab-content active">
  <p>This is the content of tab 1.</p>
</div>

<div id="tab2" class="tab-content">
  <p>This is the content of tab 2.</p>
</div>

<div id="tab3" class="tab-content">
  <p>This is the content of tab 3.</p>
</div>

<script>
  function openTab(evt, tabName) {
    var i, tabcontent, tablinks;
    tabcontent = document.getElementsByClassName("tab-content");
    for (i = 0; i < tabcontent.length; i++) {
      tabcontent[i].style.display = "none";
    }
    tablinks = document.getElementsByClassName("tab");
    for (i = 0; i < tablinks.length; i++) {
      tablinks[i].classList.remove("active");
    }
    document.getElementById(tabName).style.display = "block";
    evt.currentTarget.classList.add("active");
  }
</script>
