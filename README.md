<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Organiza+ Serviços Administrativos</title>

  <!-- FONTE -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <!-- ESTILO (TUDO EM UM BLOCO) -->
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
    body{background:#f4f4f4;color:#222}
    header{background:#000;padding:20px 40px;display:flex;justify-content:space-between;align-items:center}
    header img{height:45px}
    nav a{color:#fff;margin-left:25px;text-decoration:none;font-weight:500}
    nav a:hover{color:#3ccf4e}

    .hero{background:linear-gradient(to right,#000,#1a1a1a);color:#fff;padding:90px 20px;text-align:center}
    .hero h1{font-size:42px;margin-bottom:15px}
    .hero p{max-width:700px;margin:auto;margin-bottom:30px;font-size:18px}

    .btn{background:#3ccf4e;color:#000;padding:14px 32px;border:none;border-radius:30px;font-weight:600;cursor:pointer}

    section{padding:80px 20px;max-width:1200px;margin:auto}
    section h2{text-align:center;font-size:34px;margin-bottom:50px}

    .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:30px}
    .card{background:#fff;padding:35px;border-radius:16px;box-shadow:0 10px 30px rgba(0,0,0,.08)}

    .form-box{background:#fff;padding:50px;border-radius:20px;max-width:520px;margin:auto;box-shadow:0 15px 40px rgba(0,0,0,.1)}
    .form-box h3{text-align:center;margin-bottom:25px}
    form{display:flex;flex-direction:column;gap:15px}
    input{padding:14px;border-radius:8px;border:1px solid #ccc;font-size:15px}

    footer{background:#000;color:#fff;text-align:center;padding:40px}
    footer p{font-size:14px;margin-top:10px}
  </style>
</head>
<body>

<header>
  <img src="logoorganiza.png" alt="Organiza+">
  <nav>
    <a href="#">Home</a>
    <a href="#servicos">Serviços</a>
    <a href="#cadastro">Cadastro</a>
    <a href="#login">Login</a>
  </nav>
</header>

<section class="hero">
  <h1>Organiza+ Serviços Administrativos</h1>
  <p>Organização, eficiência e soluções administrativas para empresas que querem crescer com segurança.</p>
  <a href="#cadastro"><button class="btn">Cadastrar Empresa</button></a>
</section>

<section id="servicos">
  <h2>Nossos Serviços</h2>
  <div class="cards">
    <div class="card"><h3>Organização Administrativa</h3><p>Estruturamos processos e rotinas para eficiência total.</p></div>
    <div class="card"><h3>Apoio Financeiro</h3><p>Controle financeiro e organização empresarial.</p></div>
    <div class="card"><h3>Suporte Documental</h3><p>Regularizações, documentos e processos internos.</p></div>
  </div>
</section>

<section id="cadastro">
  <div class="form-box">
    <h3>Cadastro da Empresa</h3>
    <form id="cadastroForm">
      <input type="text" id="empresa" placeholder="Nome da Empresa" required>
      <input type="text" id="cnpj" placeholder="CNPJ" required>
      <input type="email" id="email" placeholder="Email" required>
      <input type="password" id="senha" placeholder="Senha" required>
      <button class="btn" type="submit">Cadastrar</button>
    </form>
  </div>
</section>

<section id="login">
  <div class="form-box">
    <h3>Login</h3>
    <form id="loginForm">
      <input type="email" id="loginEmail" placeholder="Email" required>
      <input type="password" id="loginSenha" placeholder="Senha" required>
      <button class="btn" type="submit">Entrar</button>
    </form>
  </div>
</section>

<footer>
  <strong>Organiza+ Serviços Administrativos</strong>
  <p>© 2025 - Todos os direitos reservados</p>
</footer>

<!-- SCRIPT (TUDO EM UM BLOCO) -->
<script>
  // VALIDAÇÃO SIMPLES DE CNPJ (BÁSICA)
  function validarCNPJ(cnpj){
    cnpj = cnpj.replace(/\D/g,'');
    return cnpj.length === 14;
  }

  document.getElementById('cadastroForm').addEventListener('submit', function(e){
    e.preventDefault();
    const cnpj = document.getElementById('cnpj').value;

    if(!validarCNPJ(cnpj)){
      alert('CNPJ inválido');
      return;
    }

    alert('Cadastro enviado! Entraremos em contato.');
    this.reset();
  });

  document.getElementById('loginForm').addEventListener('submit', function(e){
    e.preventDefault();
    alert('Login realizado (simulação).');
    this.reset();
  });
</script>

</body>
</html>
