<head>
  <title>File uploader</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" /> 
</head>
<body>
  <div class="rb">
    <div class="user">
      <img class="pfp" src="https://ratic.cc/cdn/users/pfp/octo.png" onclick="window.location.href='/cdn/users/pfp{{ pfp }}';" class="item1img" width="80" height="80">
      <h1 class="username">@octo</h1>
    </div>
    <div class="btns">
      <button class="fu">File Uploader</button>
      <button class="tu" onclick="window.location.href='/uploadtext';" >Text Uploader</button>
    </div>
  </div>
  <form action="/" method="post" enctype="multipart/form-data" id="upload-form" onsubmit="return checkFS();">
    <script>function checkFS() {
        return true;
    }</script>
    <div class="main">
        <h2>Self destructing file uploader</h2>
        <h>* After the file is accessed, the file will be removed from our servers.</h>
        <label>
            <input type="file" name="new-image" id="new-image" onchange="change()">
            Choose a file
          </label>
        <button id="sum" class="sumb">sumbit</button>
    </div>
</form>
</body>
<style>
body {
  background: url(/cdn/bg.svg) no-repeat;
  background-size: cover;
  font-family: 'Roboto', sans-serif;
}

.pfp {
  position:absolute;
  top:40%;
  left:50%;
  transform: translate(-50%,-50%);
  border-radius: 100%;
}
.user {
  position:absolute;
  top:0%;
  left:0%;
  width: 200px;
  height: 150px;
  background: hsla(0, 0%, 100%, 0.25);
  z-index: 1;
  -webkit-backdrop-filter: blur(12px);
  backdrop-filter: blur(12px);
  border-radius: 0.5rem;
  border-top-left-radius: 0px;
  border: 1px solid hsla(0, 0%, 100%, 0.25);
}

.username {
  color: #F9F6EF;
  font-size: 20px;
  position:absolute;
  top:70%;
  left:50%;
  transform: translate(-50%,-50%);
}

.rb {
  position:absolute;
  top:0%;
  left:0%;
  width: 200px;
  height: 100vh;
  background: hsla(0, 0%, 100%, 0.25);
  z-index: 1;
  -webkit-backdrop-filter: blur(12px);
  backdrop-filter: blur(12px);
  border-radius: 0.5rem;
  border: 1px solid hsla(0, 0%, 100%, 0.25);
  border-top-left-radius: 0px;
}


.fu {
  background: hsla(0, 0%, 100%, 0.514);
  width: 190px;
  border: none;
  color: #F9F6EF;
  position:absolute;
  top:19%;
  left:50%;
  transform: translate(-50%,-50%);
  font-size: 18px;
  border-radius: 10px;
  padding: 10px 20px; 
  height: 40px;
  transition: 0.2s;
  cursor: pointer;
}

.fu:hover {
  background: hsla(0, 0%, 100%, 0.514);
  width: 190px;
}

.tu {
  background: hsla(0, 0%, 100%, 0.25);
  border: none;
  color: #F9F6EF;
  position:absolute;
  top:24%;
  left:50%;
  transform: translate(-50%,-50%);
  font-size: 18px;
  border-radius: 10px;
  padding: 10px 20px; 
  width: 185px;
  height: 40px;
  transition: 0.2s;
  cursor: pointer;
}

.tu:hover {
  background: hsla(0, 0%, 100%, 0.514);
  width: 190px;
}

.main {
  height: 200px;
  width: 330px;
  position:absolute;
  top:50%;
  left:50%;
  transform: translate(-50%,-50%);
  background: hsla(0, 0%, 100%, 0.25);
  z-index: 1;
  -webkit-backdrop-filter: blur(12px);
  backdrop-filter: blur(12px);
  border-radius: 0.5rem;
  border: 1px solid hsla(0, 0%, 100%, 0.25);
}

h2 {
  color: #F9F6EF;
  font-size: 18px;
  text-align: center;
}

h {
  color: #F9F6EF;
  font-size: 10px;
  position:absolute;
  left: 15px;
}

.sumb {
  background: hsla(0, 0%, 100%, 0.25);
  border: 0.8px solid #ff4f4f;
  color: #ff4f4f;
  position:absolute;
  top:80%;
  left:50%;
  transform: translate(-50%,-50%);
  font-size: 18px;
  border-radius: 10px;
  padding: 10px 20px; 
  width: 300px;
  height: 45px;
  transition: 0.2s;
  cursor: not-allowed;
}

label > input {
  display: none;
}

label {
  text-align: center;
  background: hsla(0, 0%, 100%, 0.25);
  border: none;
  color: #F9F6EF;
  position:absolute;
  top:50%;
  left:50%;
  transform: translate(-50%,-50%);
  font-size: 18px;
  border-radius: 10px;
  padding: 10px 20px; 
  width: 260px;
  height: 25px;
  outline: none;
  transition: 0.2s;
  cursor: pointer;
}

label:hover {
  width: 265px;
  background: hsla(0, 0%, 100%, 0.514);
}

.sumb:hover {
  background: hsla(0, 0%, 100%, 0.514);
  width: 305px;
}

.exitbtn { 
  width: 32px;
  height: 32px;
  fill: red
}
</style>

<script>
    document.getElementById("sum").disabled = true;
    function change() {
        document.getElementById("sum").disabled = false;
        document.getElementById("sum").style.cursor = "pointer";
        document.getElementById("sum").style.color = "#baeeab";
        document.getElementById("sum").style.border = "0.8px solid #baeeab";
    } 
</script>
