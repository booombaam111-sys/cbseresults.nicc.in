<!DOCTYPE html>
<html>
<head>
<title>CBSE Result 2025-2026</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

<style>
body{
font-family:'Roboto',sans-serif;
margin:0;
background:#f1f1f1;
}

/* TOP BAR */
.top{
background:#0099a8;
color:white;
padding:8px;
text-align:center;
font-size:15px;
font-weight:500;
}

.logo{
display:flex;
align-items:center;
gap:6px;
justify-content:center;
}

.logo img{
height:28px; /* FIXED SIZE */
}

/* MARQUEE */
.marquee{
background:#f5f5f5;
overflow:hidden;
white-space:nowrap;
border-bottom:1px solid #ccc;
}

.marquee span{
display:inline-block;
padding-left:100%;
animation:scrollText 12s linear infinite;
font-size:12px;
color:#333;
}

@keyframes scrollText{
0%{transform:translateX(0);}
100%{transform:translateX(-100%);}
}

/* CONTAINER */
.container{
width:95%;
max-width:950px;
margin:auto;
background:white;
padding:12px; /* LESS SPACING */
margin-top:8px;
border:1px solid #ccc;
}

/* INPUT */
input{
width:100%;
padding:8px;
margin-top:8px;
border:1px solid #ccc;
}

/* BUTTON */
button{
padding:9px;
width:100%;
background:#1a73e8;
color:white;
border:none;
margin-top:10px;
cursor:pointer;
font-weight:500;
}

/* TABLE */
table{
width:100%;
border-collapse:collapse;
margin-top:8px;
font-size:12.5px;
}

th,td{
border:1px solid #b5b5b5;
padding:5px; /* tighter */
text-align:center;
}

th{
background:#2f4f8f;
color:white;
}

tbody tr:nth-child(even){
background:#eef3ff;
}

/* TEXT SPACING FIX */
p{
margin:2px 0;  /* VERY IMPORTANT FIX */
font-size:13.5px;
line-height:1.3;
}

.hidden{display:none}

.section-title{
margin-top:10px;
font-size:13.5px;
font-weight:600;
}

/* RESULT BAR */
#result{
background:#2f4f8f;
color:white;
padding:5px;
margin-top:8px;
font-size:14px;
}

/* SPINNER */
.spinner{
border:4px solid #f3f3f3;
border-top:4px solid #1a73e8;
border-radius:50%;
width:28px;
height:28px;
animation:spin 1s linear infinite;
margin:10px auto;
display:none;
}

@keyframes spin{
0%{transform:rotate(0deg);}
100%{transform:rotate(360deg);}
}

@media(max-width:600px){
th,td{
font-size:11px;
padding:4px;
}
}

</style>
</head>

<body>

<div class="top">
<div class="logo">
<!-- ✅ FIXED LOGO (WORKING LINK) -->
<img src="https://cbse.gov.in/newsite/images/cbse-logo.png">
<span>Senior School Certificate Examination (Class XII) Results 2026</span>
</div>
</div>

<div class="marquee">
<span>Brought to you by National Informatics Centre</span>
</div>

<!-- PAGE 1 -->
<div class="container" id="page1">
<h3>Enter Roll Number</h3>
<input type="text" id="roll" placeholder="Enter Roll Number">

<div class="spinner" id="spinner"></div>
<button id="submitBtn">Submit</button>
</div>

<!-- PAGE 2 -->
<div class="container hidden" id="page2">

<h3 style="text-align:center;margin-bottom:3px;">Examination Results</h3>
<p style="text-align:center;font-size:13px;margin-top:0;">
Senior School Certificate Examination (Class XII) Results 2026
</p>

<p><b>Roll No:</b> <span id="rno"></span></p>
<p><b>Candidate Name:</b> <span id="name" style="font-weight:700"></span></p>
<p><b>Mother's Name:</b> <span id="mother"></span></p>
<p><b>Father's Name:</b> <span id="father"></span></p>
<p><b>School's Name:</b> <span id="school"></span></p>

<div class="section-title">Main Subjects</div>

<table>
<thead>
<tr>
<th>SUB CODE</th>
<th>SUB NAME</th>
<th>THEORY</th>
<th>PRACTICAL</th>
<th>TOTAL</th>
<th>GRADE</th>
</tr>
</thead>
<tbody id="mainMarks"></tbody>
</table>

<div class="section-title">Additional Subject</div>

<table>
<thead>
<tr>
<th>SUB CODE</th>
<th>SUB NAME</th>
<th>THEORY</th>
<th>PRACTICAL</th>
<th>TOTAL</th>
<th>GRADE</th>
</tr>
</thead>
<tbody id="addMarks"></tbody>
</table>

<h3 id="result"></h3>

<button onclick="goBack()">Check Another Result</button>

<div style="margin-top:12px;line-height:1.4">

<p style="color:#a94442;font-size:13px;font-weight:600">
<b>Note: Abbreviations used against Result:</b>
</p>

<p style="color:#a94442;font-size:13px;font-weight:600">
R.L. - Result Later, N.E. - Not Eligible, R.W. - Result Withheld, ABST - Absent, COMP - Compartment,
UFM - Unfair means, SJD - Subjudice, N.R. - Not Registered,
R.T. - Repeat in Theory, R.P. - Repeat in Practical, R.B. - Repeat in both
</p>

<br>

<p style="font-size:12.5px;color:#333">
<b>Disclaimer:</b> Neither NIC nor CBSE is responsible for any error.
</p>

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

document.getElementById("submitBtn").addEventListener("click", showResult);

function showResult(){
let roll=document.getElementById("roll").value.trim();

if(roll===""){
alert("Enter Roll Number");
return;
}

let btn=document.getElementById("submitBtn");
let spin=document.getElementById("spinner");

btn.disabled=true;
spin.style.display="block";

setTimeout(()=>{
processResult(roll);
btn.disabled=false;
spin.style.display="none";
},1200);
}

function processResult(roll){

if(!data[roll]){
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
}

function goBack(){
document.getElementById("page1").classList.remove("hidden");
document.getElementById("page2").classList.add("hidden");
document.getElementById("roll").value="";
}

</script>

</body>
</html>
