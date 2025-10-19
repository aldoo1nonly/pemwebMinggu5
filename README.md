<!doctype html>
<html lang="id"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>Minggu 5</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<style>body{min-height:100vh;display:grid;place-items:center;background:#f6f8fb}.card{max-width:520px;width:100%}</style>
</head><body>
<div class="card shadow-sm"><div class="card-body">
<h1 class="h4 mb-3">Formulir Pendaftaran</h1>
<form id="form" novalidate>
<div class="mb-3"><label class="form-label" for="nama">Nama</label><input id="nama" class="form-control" required></div>
<div class="mb-3"><label class="form-label" for="email">Email</label><input id="email" type="email" class="form-control" required></div>
<div class="mb-3"><label class="form-label" for="password">Password</label><input id="password" type="password" minlength="8" class="form-control" required></div>
<button class="btn btn-primary">Kirim</button>
</form></div></div>
<script>
const f=document.getElementById('form');
f.addEventListener('submit',e=>{let v=true;
const nama=f.querySelector('#nama'),email=f.querySelector('#email'),pw=f.querySelector('#password');
const emailRegex=/^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/;
[nama,email,pw].forEach(el=>el.classList.remove('is-invalid'));
if(!nama.value.trim()){nama.classList.add('is-invalid');v=false;}
if(!email.value.trim()||!emailRegex.test(email.value)){email.classList.add('is-invalid');v=false;}
if(!pw.value.trim()||pw.value.length<8){pw.classList.add('is-invalid');v=false;}
if(!v){e.preventDefault();e.stopPropagation();}else{alert('Formulir valid dan siap dikirim!');}});
</script>

<p class="text-center text-muted small mt-3">Dikumpulkan oleh Febriano Aldo</p>
</body></html>
