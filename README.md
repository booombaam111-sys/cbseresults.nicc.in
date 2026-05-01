<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

<title>CBSE Result</title>

<style>

body{
font-family:'Roboto',sans-serif;
margin:0;
background:#f1f1f1;
}

/* TOP */
.topbar{
background:#0099a8;
color:#fff;
padding:7px;
text-align:left; /* 🔥 LEFT */
font-size:14px;
}

/* HEADER */
.header{
background:#2f4f8f;
color:#fff;
padding:8px;
display:flex;
align-items:center;
justify-content:flex-start; /* 🔥 LEFT */
gap:8px;
font-size:14px;
font-weight:500;
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
}
@keyframes scrollText{
0%{transform:translateX(0)}
100%{transform:translateX(-100%)}
}

/* CONTAINER */
.container{
width:95%;
max-width:900px;
margin:10px auto;
background:#fff;
padding:10px;
border:1px solid #ccc;
}

/* FORM */
.form-group{
margin:8px 0;
font-size:13.5px;
}
.form-group label{
display:block;
margin-bottom:3px;
}
input{
width:100%;
padding:8px;
border:1px solid #bbb;
font-size:13px;
}

/* BUTTON */
button{
width:100%;
padding:9px;
margin-top:10px;
background:#1a73e8;
color:#fff;
border:none;
font-size:14px;
cursor:pointer;
}

/* CAPTCHA */
.captcha-box{
margin-top:10px;
padding:8px;
background:#f2f2f2;
font-weight:bold;
letter-spacing:2px;
font-size:18px;
text-align:center;
}

/* SPINNER */
.spinner{
border:4px solid #eee;
border-top:4px solid #1a73e8;
border-radius:50%;
width:28px;
height:28px;
animation:spin 1s linear infinite;
margin:10px auto;
display:none;
}
@keyframes spin{
0%{transform:rotate(0)}
100%{transform:rotate(360deg)}
}

/* DETAILS */
.details{
font-size:13.5px;
margin-top:8px;
}
.details div{
display:flex;
margin:3px 0;
}
.details .label{
min-width:180px;
font-weight:500;
}
.details .value{
flex:1;
}

/* TABLE */
.table-wrapper{
width:100%;
overflow-x:auto;
}
table{
width:100%;
min-width:650px;
border-collapse:collapse;
margin-top:8px;
font-size:12.8px;
}

th,td{
border:1px solid #b5b5b5;
padding:5px;
text-align:center;
}

th{
background:#2f4f8f;
color:#fff;
font-weight:500;
}

.highlight{
background:#eef3ff;
}

/* RESULT */
.result{
background:#2f4f8f;
color:#fff;
padding:5px;
margin-top:14px;
font-size:14px;
}

/* LINK */
.check{
text-align:center;
margin:15px 0;
}
.check a{
color:#1a0dab;
font-size:18px;
font-weight:600;
text-decoration:underline;
}

/* NOTE */
.note{
color:#a94442;
font-size:13px;
font-weight:600;
margin-top:12px;
line-height:1.5;
}

/* DISCLAIMER */
.disclaimer{
margin-top:12px;
font-size:12.5px;
color:#333;
}

.hidden{display:none}

</style>
</head>

<body>

<div class="topbar">केन्द्रीय माध्यमिक शिक्षा बोर्ड</div>

<div class="header">
<span>Central Board of Secondary Education</span>
</div>

<div class="marquee">
<span>Brought to you by National Informatics Centre</span>
</div>

<!-- PAGE 1 -->
<div class="container" id="page1">

<h3 style="text-align:center;margin:5px 0;">Examination Results</h3>
<p style="text-align:center;font-size:13px;margin:0;">
Senior School Certificate Examination (Class XII) Results 2026
</p>

<div class="form-group">
<label>Roll Number</label>
<input type="text" id="roll">
</div>

<div class="form-group">
<label>School Code</label>
<input type="text" id="school">
</div>

<div class="form-group">
<label>Date of Birth (dd/mm/yyyy)</label>
<input type="text" id="dob">
</div>

<div class="form-group">
<label>Admit Card ID</label>
<input type="text" id="admit">
</div>

<div class="captcha-box" id="captchaText"></div>
<input type="text" id="captchaInput" placeholder="Enter Captcha">

<div class="spinner" id="spinner"></div>

<button onclick="checkResult()">Submit</button>

</div>

<!-- PAGE 2 -->
<div class="container hidden" id="page2">

<h3 style="text-align:center;margin:5px 0;">Examination Results</h3>
<p style="text-align:center;font-size:13px;margin:0;">
Senior School Certificate Examination (Class XII) Results 2026
</p>

<div class="details">
<div><span class="label">Roll No:</span><span class="value">2260695</span></div>
<div><span class="label">Candidate Name:</span><span class="value">ABHINAV KUMAR</span></div>
<div><span class="label">Mother's Name:</span><span class="value">NAMITA DEVI</span></div>
<div><span class="label">Father's Name:</span><span class="value">HIMANSHU SHEKHAR</span></div>
<div><span class="label">School's Name:</span><span class="value">GURU GOBIND SINGH PUBLIC SCHOOL, BOKARO STEEL CITY</span></div>
</div>

<div class="table-wrapper">
<table>
<tr>
<th>SUB CODE</th>
<th>SUB NAME</th>
<th>THEORY</th>
<th>PRACTICAL</th>
<th>TOTAL</th>
<th>GRADE</th>
</tr>

<tr><td>301</td><td>ENGLISH CORE</td><td>66</td><td>30</td><td>96</td><td>A1</td></tr>
<tr class="highlight"><td>041</td><td>MATHEMATICS</td><td>52</td><td>20</td><td>72</td><td>B1</td></tr>
<tr><td>042</td><td>PHYSICS</td><td>45</td><td>30</td><td>75</td><td>B1</td></tr>
<tr class="highlight"><td>043</td><td>CHEMISTRY</td><td>56</td><td>30</td><td>86</td><td>A2</td></tr>
<tr><td>034</td><td>HINDI MUSIC VOCAL</td><td>20</td><td>68</td><td>88</td><td>A2</td></tr>
<tr><td>500</td><td>WORK EXPERIENCE</td><td>--</td><td>--</td><td>--</td><td>A1</td></tr>
<tr class="highlight"><td>502</td><td>HEALTH & PHYSICAL EDUCATION</td><td>--</td><td>--</td><td>--</td><td>A1</td></tr>
<tr><td>503</td><td>GENERAL STUDIES</td><td>--</td><td>--</td><td>--</td><td>A1</td></tr>

<tr class="highlight">
<td colspan="6" style="text-align:left;"><b>Additional Subject</b></td>
</tr>

<tr><td>048</td><td>PHYSICAL EDUCATION</td><td>60</td><td>30</td><td>90</td><td>A1</td></tr>

</table>
</div>

<div class="result">Result : PASS</div>

<div class="check">
<a href="#" onclick="goBack()">Check Another Result</a>
</div>

<div class="note">
Note: Abbreviations used against Result:<br>
R.L. - Result Later, N.E. - Not Eligible, R.W. - Result Withheld,
ABST - Absent, COMP - Compartment, UFM - Unfair means,
SJD - Subjudice, N.R. - Not Registered,
R.T. - Repeat in Theory, R.P. - Repeat in Practical, R.B. - Repeat in both
</div>

<div class="disclaimer">
<b>Disclaimer:</b> Neither NIC nor CBSE is responsible for any inadvertent error that may have crept in the results being published on NET. The results published on net are for Immediate information to the examinees. These cannot be treated as original mark sheets. Original mark sheets have been issued by the Board separately.
</div>

</div>

<script>
let captcha="";

function generateCaptcha(){
const chars="ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnpqrstuvwxyz23456789";
captcha="";
for(let i=0;i<6;i++){
captcha+=chars.charAt(Math.floor(Math.random()*chars.length));
}
document.getElementById("captchaText").innerText=captcha;
}
generateCaptcha();

function checkResult(){
let roll=document.getElementById("roll").value.trim();
let school=document.getElementById("school").value.trim();
let dob=document.getElementById("dob").value.trim();
let admit=document.getElementById("admit").value.trim();
let cap=document.getElementById("captchaInput").value.trim();

if(roll!=="2260695"||school!=="66242"||dob!=="23/11/2007"||admit!=="RJ765294"){
alert("Invalid Details");return;
}

if(cap!==captcha){
alert("Wrong Captcha");generateCaptcha();return;
}

document.getElementById("spinner").style.display="block";

setTimeout(()=>{
document.getElementById("page1").classList.add("hidden");
document.getElementById("page2").classList.remove("hidden");
document.getElementById("spinner").style.display="none";
},3000);
}

function goBack(){
document.getElementById("page1").classList.remove("hidden");
document.getElementById("page2").classList.add("hidden");
generateCaptcha();
}
</script>

</body>
</html>
