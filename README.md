<!DOCTYPE html>
<html>
<head>
<title>CBSE Result 2025-2026</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

<style>
body{font-family:'Roboto',sans-serif;margin:0;background:#eef2f7}

/* Header */
.top{
background:#0b5ed7;
color:white;
padding:10px;
text-align:center;
font-size:15px;
font-weight:500
}

.logo{
display:flex;
align-items:center;
gap:8px;
justify-content:center
}

.logo img{height:35px}

.container{
width:95%;
max-width:900px;
margin:auto;
background:white;
padding:15px;
margin-top:10px;
border:1px solid #ccc
}

input{
width:100%;
padding:10px;
margin-top:10px;
border:1px solid #ccc
}

button{
padding:10px;
width:100%;
background:#1a73e8;
color:white;
border:none;
margin-top:10px;
cursor:pointer;
}

/* Table */
table{
width:100%;
border-collapse:collapse;
margin-top:10px;
font-size:13px
}

th,td{
border:1px solid #999;
padding:4px;
text-align:center
}

th{
background:#2f4f8f;
color:white
}

tbody tr:nth-child(even){
background:#eef3ff;
}

p{margin:4px 0;font-size:14px}

.hidden{display:none}

.section-title{
margin-top:12px;
font-size:14px;
font-weight:bold
}

.spinner{
border:4px solid #f3f3f3;
border-top:4px solid #1a73e8;
border-radius:50%;
width:30px;
height:30px;
animation:spin 1s linear infinite;
margin:15px auto;
display:none;
}

@keyframes spin{
0%{transform:rotate(0deg);}
100%{transform:rotate(360deg);}
}
</style>
</head>

<body>

<div class="top">
<div class="logo">
<img src="https://upload.wikimedia.org/wikipedia/en/thumb/3/3c/CBSE_logo.svg/120px-CBSE_logo.svg.png">
<span>Senior School Certificate Examination (Class XII) Results 2026</span>
</div>
</div>

<!-- PAGE 1 -->
<div class="container" id="page1">
<h3>Enter Roll Number</h3>
<input type="text" id="roll" placeholder="Enter Roll Number">

<div class="spinner" id="spinner"></div>

<button onclick="showResult()">Submit</button>
</div>

<!-- PAGE 2 -->
<div class="container hidden" id="page2">

<h3 style="text-align:center;">Examination Results</h3>
<p style="text-align:center;">Senior School Certificate Examination (Class XII) Results 2026</p>

<p><b>Roll No:</b> <span id="rno"></span></p>
<p><b>Candidate Name:</b> <span id="name" style="font-weight:700"></span></p>
<p><b>Mother's Name:</b> <span id="mother"></span></p>
<p><b>Father's Name:</b> <span id="father"></span></p>
<p><b>School's Name:</b> <span id="school"></span></p>

<div class="section-title">Main Subjects</div>

<table>
<tr>
<th>SUB CODE</th>
<th>SUB NAME</th>
<th>THEORY</th>
<th>PRACTICAL</th>
<th>TOTAL</th>
<th>GRADE</th>
</tr>
<tbody id="mainMarks"></tbody>
</table>

<div class="section-title">Additional Subject</div>

<table>
<tr>
<th>SUB CODE</th>
<th>SUB NAME</th>
<th>THEORY</th>
<th>PRACTICAL</th>
<th>TOTAL</th>
<th>GRADE</th>
</tr>
<tbody id="addMarks"></tbody>
</table>

<h3 id="result"></h3>

<button onclick="goBack()">Check Another Result</button>

<!-- NOTE -->
<div style="margin-top:15px;color:#a94442;font-weight:600">
<b>Note:</b> R.L., N.E., R.W., ABST, COMP, UFM, SJD, N.R., R.T., R.P., R.B.
</div>

<!-- DISCLAIMER -->
<div style="margin-top:10px;font-size:13px;color:#333">
<b>Disclaimer:</b> Results shown are for immediate information only.
</div>

</div>

<script>

const data={
"2260695":{
name:"ABHINAV KUMAR",
mother:"NAMITA DEVI",
father:"HIMANSHU SHEKHAR",
school:"GURU GOBIND SINGH PUBLIC SCHOOL, BOKARO STEEL CITY",
subjects:[
["301","ENGLISH CORE",66,30,96,"A1","main"],
["041","MATHEMATICS",52,20,72,"B1","main"],
["042","PHYSICS",45,30,75,"B1","main"],
["043","CHEMISTRY",56,30,86,"A2","main"],
["034","HINDI MUSIC VOCAL",20,68,88,"A2","main"],

["500","WORK EXPERIENCE","--","--","--","A1","main"],
["502","HEALTH & PHYSICAL EDUCATION","--","--","--","A1","main"],
["503","GENERAL STUDIES","--","--","--","A1","main"],

["048","PHYSICAL EDUCATION",60,30,90,"A1","add"]
],
result:"PASS"
}
};

function showResult(){

let roll=document.getElementById("roll").value.trim();

if(!roll){
alert("Enter Roll Number");
return;
}

let spinner=document.getElementById("spinner");
spinner.style.display="block";

setTimeout(()=>{
if(!data[roll]){
spinner.style.display="none";
alert("Invalid Roll Number");
return;
}

let s=data[roll];

document.getElementById("page1").classList.add("hidden");
document.getElementById("page2").classList.remove("hidden");

document.getElementById("rno").innerText=roll;
document.getElementById("name").innerText=s.name;
document.getElementById("mother").innerText=s.mother;
document.getElementById("father").innerText=s.father;
document.getElementById("school").innerText=s.school;

let mainRows="", addRows="";

s.subjects.forEach(sub=>{
let row=`<tr>
<td>${sub[0]}</td>
<td>${sub[1]}</td>
<td>${sub[2]}</td>
<td>${sub[3]}</td>
<td>${sub[4]}</td>
<td>${sub[5]}</td>
</tr>`;
(sub[6]==="add") ? addRows+=row : mainRows+=row;
});

document.getElementById("mainMarks").innerHTML=mainRows;
document.getElementById("addMarks").innerHTML=addRows;
document.getElementById("result").innerText="Result: "+s.result;

spinner.style.display="none";

},1000);
}

function goBack(){
document.getElementById("page1").classList.remove("hidden");
document.getElementById("page2").classList.add("hidden");
document.getElementById("roll").value="";
}

</script>

</body>
</html>
