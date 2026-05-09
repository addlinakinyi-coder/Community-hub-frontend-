<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Community Hub Pro</title>

<style>

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:Arial;
}

body{
  background:#f4f7fb;
}

/* HEADER */

header{
  background:linear-gradient(135deg,#6C63FF,#8B5CF6);
  color:white;
  padding:15px;
}

.topbar{
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.logo{
  font-size:24px;
  font-weight:bold;
}

/* NOTIFICATIONS */

.notification-wrapper{
  position:relative;
}

.notification-btn{
  background:white;
  border:none;
  border-radius:50%;
  width:45px;
  height:45px;
  cursor:pointer;
  position:relative;
  font-size:18px;
}

#notificationCount{
  position:absolute;
  top:-5px;
  right:-5px;
  background:red;
  color:white;
  width:20px;
  height:20px;
  font-size:12px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
}

.notification-panel{
  position:absolute;
  right:0;
  top:55px;
  width:280px;
  background:white;
  box-shadow:0 5px 20px rgba(0,0,0,0.2);
  border-radius:12px;
  padding:10px;
  display:none;
}

.notification-item{
  background:#f1f5f9;
  padding:8px;
  border-radius:8px;
  margin-bottom:8px;
  font-size:13px;
}

/* LAYOUT */

.container{
  width:90%;
  max-width:1100px;
  margin:20px auto;
  display:grid;
  grid-template-columns:2fr 1fr;
  gap:15px;
}

.card{
  background:white;
  padding:15px;
  border-radius:12px;
  box-shadow:0 5px 15px rgba(0,0,0,0.08);
}

/* POSTS */

.post{
  border-bottom:1px solid #ddd;
  padding:15px 0;
}

.post:last-child{
  border:none;
}

.post-header{
  display:flex;
  align-items:center;
  gap:10px;
}

.avatar{
  width:50px;
  height:50px;
  border-radius:50%;
  object-fit:cover;
}

.post-actions button{
  margin-right:10px;
  margin-top:10px;
}

/* INPUT */

input, textarea{
  width:100%;
  padding:10px;
  margin-bottom:10px;
}

/* MODAL */

.auth-modal{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,0.6);
  display:flex;
  justify-content:center;
  align-items:center;
  z-index:999;
}

.auth-box{
  background:white;
  padding:20px;
  width:300px;
  border-radius:12px;
}

button{
  padding:10px;
  border:none;
  background:#6C63FF;
  color:white;
  cursor:pointer;
  border-radius:8px;
}

.comment-box{
  display:none;
  margin-top:10px;
}

.comment{
  background:#eef2ff;
  padding:8px;
  margin-top:5px;
  border-radius:6px;
}

.user-info{
  color:white;
  margin-left:10px;
}

</style>
</head>

<body>

<!-- AUTH -->

<div class="auth-modal" id="authModal">

  <div class="auth-box">

    <h3>Join Community</h3>

    <input id="name" placeholder="Name">
    <input id="email" placeholder="Email">
    <input id="password" placeholder="Password">

    <input type="file" id="profileUpload">

    <button onclick="joinCommunity()">Enter</button>

  </div>

</div>

<!-- HEADER -->

<header>

  <div class="topbar">

    <div class="logo">CommunityHub</div>

    <div class="notification-wrapper">

      <button class="notification-btn" onclick="toggleNotifications()">🔔
        <div id="notificationCount">0</div>
      </button>

      <div class="notification-panel" id="notificationPanel"></div>

    </div>

  </div>

</header>

<!-- MAIN -->

<div class="container">

  <div>

    <div class="card">

      <h3>Create Post</h3>

      <input id="title" placeholder="Title">
      <textarea id="content" placeholder="Write..."></textarea>

      <button onclick="addPost()">Post</button>

    </div>

    <div class="card" id="postList"></div>

  </div>

  <div class="card">
    <h3>Active Members</h3>
    <div id="memberList"></div>
  </div>

</div>

<script>

/* DATA */

let username = "";
let profileImage = "";
let notifications = [];

let members = [
  "Alice","John","Sophia","Daniel","Emma",
  "Michael","Grace","David","Olivia","James"
];

/* SHOW MEMBERS */

members.forEach(m => {

  let div = document.createElement("div");
  div.innerHTML = "👤 " + m;
  document.getElementById("memberList").appendChild(div);

});

/* AUTH */

function joinCommunity(){

  username = document.getElementById("name").value || "User";

  let file = document.getElementById("profileUpload").files[0];

  if(file){

    let reader = new FileReader();

    reader.onload = function(e){

      profileImage = e.target.result;

      login();

    };

    reader.readAsDataURL(file);

  }else{

    login();

  }

}

function login(){

  document.getElementById("authModal").style.display = "none";

}

/* POSTS */

function addPost(){

  let title = document.getElementById("title").value;
  let content = document.getElementById("content").value;

  let post = document.createElement("div");
  post.className = "post";

  post.innerHTML = `
    <div class="post-header">
      <img class="avatar" src="${profileImage || 'https://via.placeholder.com/50'}">
      <div><b>${username}</b> <p>${title}</p></div>
    </div>

    <p>${content}</p>

    <div class="post-actions">

      <button onclick="likePost(this)">👍 <span>0</span></button>

      <button onclick="toggleComment(this)">💬 Comment</button>

    </div>

    <div class="comment-box">
      <input placeholder="comment...">
      <button onclick="addComment(this)">Send</button>
      <div class="comments"></div>
    </div>
  `;

  document.getElementById("postList").prepend(post);

  notify("New post: " + title);

}

/* LIKE */

function likePost(btn){

  let span = btn.querySelector("span");
  span.innerText = parseInt(span.innerText) + 1;

  notify("Post liked");

}

/* COMMENT */

function toggleComment(btn){

  let box = btn.parentElement.nextElementSibling;

  box.style.display =
    box.style.display === "block" ? "none" : "block";

}

function addComment(btn){

  let box = btn.parentElement;
  let input = box.querySelector("input");

  let div = document.createElement("div");
  div.className = "comment";
  div.innerText = username + ": " + input.value;

  box.querySelector(".comments").prepend(div);

  input.value = "";

  notify("Comment added");

}

/* NOTIFICATIONS */

function notify(text){

  notifications.unshift(text);

  let list = document.getElementById("notificationPanel");
  let count = document.getElementById("notificationCount");

  list.innerHTML = "";

  notifications.forEach(n => {

    let div = document.createElement("div");
    div.className = "notification-item";
    div.innerText = n;

    list.appendChild(div);

  });

  count.innerText = notifications.length;

}

function toggleNotifications(){

  let panel = document.getElementById("notificationPanel");

  panel.style.display =
    panel.style.display === "block" ? "none" : "block";

}

/* AUTO POSTS FROM MEMBERS */

function autoPost(){

  let m = members[Math.floor(Math.random()*members.length)];

  let post = document.createElement("div");
  post.className = "post";

  post.innerHTML = `
    <div class="post-header">
      <img class="avatar" src="https://i.pravatar.cc/50?u=${m}">
      <div><b>${m}</b> <p>Auto post</p></div>
    </div>

    <p>This is an auto community update 🚀</p>

    <div class="post-actions">

      <button onclick="likePost(this)">👍 <span>${Math.floor(Math.random()*10)}</span></button>

      <button onclick="toggleComment(this)">💬 Comment</button>

    </div>

    <div class="comment-box"></div>
  `;

  document.getElementById("postList").prepend(post);

  notify(m + " posted");

}

/* START LIVE ACTIVITY */

setInterval(autoPost, 5000);

</script>

</body>
</html>
