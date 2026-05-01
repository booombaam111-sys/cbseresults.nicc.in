<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>CBSE Result</title>

<style>
body{font-family:Arial;margin:0;background:#fff}

.topbar{background:#0099a8;color:#fff;padding:6px 10px;font-size:13px}

.header{
background:linear-gradient(to right,#1bb1b3,#3b4db7);
color:#fff;padding:7px 8px;display:flex;align-items:center;gap:6px;font-size:12.5px
}
.header img{height:24px}

/* FIRST PAGE */
.container{width:95%;max-width:600px;margin:20px auto}

.form-group{
display:flex;
align-items:center;
margin:10px 0;
font-size:14px;
}

.form-group label{
width:160px;
font-weight:bold;
}

.form-group input{
flex:1;
padding:6px;
border:1px solid #999;
}

.hint{font-size:12px;color:#555;margin-left:160px;}
.red{color:red;font-size:13px;margin-left:160px;}

button{padding:6px 14px;margin:10px 5px;}

.center{text-align:center}

/* CAPTCHA */
.captcha-box{
margin-top:12px;padding:7px;background:#f2f2f2;
font-weight:bold;letter-spacing:2px;font-size:18px;text-align:center;
}

.spinner{
border:4px solid #eee;border-top:4px solid #1a73e8;border-radius:50%;
width:28px;height:28px;animation:spin 1s linear infinite;margin:10px auto;display:none
}
@keyframes spin{0%{transform:rotate(0)}100%{transform:rotate(360deg)}}

/* SECOND PAGE */
.details{font-size:13px;margin-top:6px;margin-bottom:10px;}
.details div{display:flex;margin:4px 0;}
.details .label{min-width:170px;font-weight:bold;}
.details .value{flex:1;}

table{width:100%;border-collapse:collapse;font-size:12px;margin-top:6px}
th,td{border:1px solid #999;padding:4px;text-align:center}
th{background:#3b4db7;color:#fff;font-size:12px}

.highlight{background:#d9dcf7;}

.result{
background:#3b4db7;
color:#fff;
padding:4px;
margin-top:14px;
font-size:13px
}

.check{text-align:center;margin:14px 0}
.check a{color:#2b4ecf;font-size:18px;font-weight:bold;text-decoration:underline}

.note{
color:#a94442;font-size:12.8px;font-weight:600;line-height:1.6;margin-top:12px;
}

.disclaimer{margin-top:14px;font-size:12.5px;color:#333;line-height:1.5;}

.hidden{display:none}
</style>
</head>

<body>

<div class="topbar">केन्द्रीय माध्यमिक शिक्षा बोर्ड</div>

<div class="header">
<img src="https://upload.wikimedia.org/wikipedia/en/thumb/2/2d/CBSE_logo.svg/512px-CBSE_logo.svg.png">
<span>Central Board of Secondary Education</span>
</div>

<!-- FIRST PAGE -->
<div class="container" id="page1">

<h3 class="center">Senior School Certificate Examination (Class XII) Results 2026</h3>

<div class="form-group">
<label>Enter your Roll Number</label>
<input type="text" id="roll">
</div>

<div class="form-group">
<label>Enter School No.</label>
<input type="text" id="school">
</div>

<div class="form-group">
<label>Enter Date of Birth</label>
<input type="text" id="dob">
</div>
<div class="hint">(Type DOB in dd/mm/yyyy format)</div>

<div class="form-group">
<label>Enter Admit Card ID</label>
<input type="text" id="admit">
</div>
<div class="red">(as given on your admit card)</div>

<div class="captcha-box" id="captchaText"></div>

<div class="form-group">
<label>Enter Captcha</label>
<input type="text" id="captchaInput">
</div>

<div class="spinner" id="spinner"></div>

<div class="center">
<button onclick="checkResult()">Submit</button>
<button onclick="resetForm()">Reset</button>
</div>

</div>

<!-- SECOND PAGE (TERA SAME) -->
<div class="container hidden" id="page2">

<h3 style="text-align:center;margin:4px 0;font-size:15px;">Examination Results</h3>
<p style="text-align:center;font-size:12.5px;margin:0;">
Senior School Certificate Examination (Class XII) Results 2026
</p>

<div class="details">
<div><span class="label">Roll No:</span><span class="value">2260695</span></div>
<div><span class="label">Candidate Name:</span><span class="value">ABHINAV KUMAR</span></div>
<div><span class="label">Mother's Name:</span><span class="value">NAMITA DEVI</span></div>
<div><span class="label">Father's Name:</span><span class="value">HIMANSHU SHEKHAR</span></div>
<div><span class="label">School's Name:</span><span class="value">GURU GOBIND SINGH PUBLIC SCHOOL, BOKARO STEEL CITY</span></div>
</div>

<table>
<tr>
<th>SUB CODE</th>
<th>SUB NAME</th>
<th>THEORY</th>
<th>Prac/IA/Proj</th>
<th>MARKS</th>
<th>POSITIONAL GRADE</th>
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

<div class="result">Result : PASS</div>

<div class="check">
<a href="#" onclick="goBack()">Check Another Result</a>
</div>

<div class="note">
<p><b>Note: Abbreviations used against Result:</b></p>
<p>
R.L. - Result Later, N.E. - Not Eligible, R.W. - Result Withheld, ABST - Absent,
COMP - Compartment, UFM - Unfair means, SJD - Subjudice, N.R. - Not Registered,
R.T. - Repeat in Theory, R.P. - Repeat in Practical, R.B. - Repeat in both
</p>
</div>

<div class="disclaimer">
<b>Disclaimer:</b> Neither NIC nor CBSE is responsible for any inadvertent error.
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

if(roll!=="2260695"){alert("Invalid Roll Number");return;}
if(school!=="66242"){alert("Invalid School No.");return;}
if(dob!=="23/11/2007"){alert("Invalid DOB");return;}
if(admit!=="RJ765294"){alert("Invalid Admit Card ID");return;}
if(cap!==captcha){alert("Wrong Captcha");generateCaptcha();return;}

document.getElementById("spinner").style.display="block";

setTimeout(()=>{
document.getElementById("page1").classList.add("hidden");
document.getElementById("page2").classList.remove("hidden");
document.getElementById("spinner").style.display="none";
},3000);
}

function resetForm(){
document.getElementById("roll").value="";
document.getElementById("school").value="";
document.getElementById("dob").value="";
document.getElementById("admit").value="";
document.getElementById("captchaInput").value="";
generateCaptcha();
}

function goBack(){
document.getElementById("page1").classList.remove("hidden");
document.getElementById("page2").classList.add("hidden");
generateCaptcha();
}
</script>

</body>
</html>
