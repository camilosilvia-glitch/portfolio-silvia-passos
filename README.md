# portfolio-silvia-passos
Portfólio de análise de dados educacionais — Silvia Passos
<!DOCTYPE html>

<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Silvia Passos — Dados & Educação</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --navy:#0b1120;
  --navy2:#111827;
  --gold:#c9974a;
  --gold-light:#f0c97a;
  --teal:#1d8fa8;
  --teal-light:#4dc4de;
  --paper:#f7f5f0;
  --paper2:#efecea;
  --white:#ffffff;
  --gray:#9ca3af;
  --gray2:#6b7280;
  --ink:#1a1a2e;
  --shadow:0 2px 20px rgba(0,0,0,.07);
  --shadow-lg:0 12px 40px rgba(0,0,0,.12);
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'Inter',sans-serif;-webkit-font-smoothing:antialiased;overflow-x:hidden;}

/* ── HERO ── */
.hero{
min-height:100vh;
background:var(–navy);
display:flex;align-items:center;justify-content:center;
position:relative;overflow:hidden;
padding:6rem 2rem 4rem;
}
.hero-grid{
position:absolute;inset:0;
background-image:
linear-gradient(rgba(255,255,255,.025) 1px,transparent 1px),
linear-gradient(90deg,rgba(255,255,255,.025) 1px,transparent 1px);
background-size:60px 60px;
}
.hero-glow{
position:absolute;
left:10%;top:30%;
width:500px;height:400px;
border-radius:50%;
background:radial-gradient(ellipse,rgba(29,143,168,.18),transparent 70%);
filter:blur(40px);
pointer-events:none;
}
.hero-glow2{
position:absolute;
right:5%;bottom:20%;
width:350px;height:350px;
border-radius:50%;
background:radial-gradient(ellipse,rgba(201,151,74,.12),transparent 70%);
filter:blur(40px);
pointer-events:none;
}
.hero-content{position:relative;z-index:2;max-width:780px;text-align:center;}

.hero-tag{
display:inline-block;
font-family:‘JetBrains Mono’,monospace;
font-size:.7rem;letter-spacing:4px;text-transform:uppercase;
color:var(–gold);
margin-bottom:2rem;
}
.hero-tag span{margin:0 .75rem;opacity:.4;}

.hero h1{
font-family:‘Playfair Display’,serif;
font-size:clamp(3.2rem,8vw,5.8rem);
line-height:1.08;
color:var(–white);
margin-bottom:1.25rem;
}
.hero h1 em{
font-style:normal;
color:var(–gold);
}

.hero-sub{
font-size:1.05rem;font-weight:300;
color:rgba(255,255,255,.55);
max-width:520px;margin:0 auto 3.5rem;
line-height:1.8;
}

.hero-stats{
display:flex;flex-direction:column;align-items:center;gap:2.5rem;
margin-bottom:3rem;
}
.stat{text-align:center;}
.stat-num{
font-family:‘Playfair Display’,serif;
font-size:3.2rem;
color:var(–gold);
display:block;line-height:1;
}
.stat-lbl{
font-size:.68rem;letter-spacing:3px;text-transform:uppercase;
color:rgba(255,255,255,.3);margin-top:.5rem;
}

.scroll-hint{
display:flex;flex-direction:column;align-items:center;gap:.5rem;
color:rgba(255,255,255,.2);font-size:.68rem;letter-spacing:2px;text-transform:uppercase;
}
.scroll-ring{
width:28px;height:44px;border:1.5px solid rgba(255,255,255,.2);border-radius:14px;position:relative;
}
.scroll-ring::after{
content:’’;width:4px;height:8px;background:var(–gold);border-radius:2px;
position:absolute;top:8px;left:50%;transform:translateX(-50%);
animation:sd 2s ease infinite;
}
@keyframes sd{0%{opacity:1;transform:translateX(-50%) translateY(0);}100%{opacity:0;transform:translateX(-50%) translateY(16px);}}

/* ── NAV ── */
nav{
position:sticky;top:0;z-index:100;
background:rgba(247,245,240,.94);
backdrop-filter:blur(14px);
border-bottom:1px solid rgba(0,0,0,.07);
padding:0 2rem;
}
nav ul{
max-width:1100px;margin:0 auto;
display:flex;list-style:none;overflow-x:auto;
scrollbar-width:none;
}
nav ul::-webkit-scrollbar{display:none;}
nav a{
display:block;padding:.95rem 1.2rem;
text-decoration:none;color:var(–gray2);
font-size:.82rem;font-weight:500;white-space:nowrap;
border-bottom:2px solid transparent;
transition:all .3s;
}
nav a:hover,nav a.active{color:var(–teal);border-bottom-color:var(–teal);}

/* ── SECTIONS ── */
.section{padding:5.5rem 2rem;background:var(–paper);}
.section.dark{background:var(–navy);color:var(–white);}
.section-inner{max-width:1100px;margin:0 auto;}
.section-label{
font-family:‘JetBrains Mono’,monospace;
font-size:.68rem;letter-spacing:3px;text-transform:uppercase;
color:var(–gold);margin-bottom:.6rem;
}
.section-title{
font-family:‘Playfair Display’,serif;
font-size:clamp(1.9rem,4vw,2.8rem);
margin-bottom:.85rem;color:var(–ink);
}
.section.dark .section-title{color:var(–white);}
.section-desc{
color:var(–gray2);font-weight:300;line-height:1.8;
max-width:600px;margin-bottom:3rem;font-size:1rem;
}
.section.dark .section-desc{color:rgba(255,255,255,.45);}

/* ── PROJECT CARDS ── */
.cards-list{display:flex;flex-direction:column;gap:1.75rem;}

.p-card{
background:var(–white);
border-radius:20px;overflow:hidden;
box-shadow:var(–shadow);
transition:all .4s;
}
.p-card:hover{transform:translateY(-5px);box-shadow:var(–shadow-lg);}

.card-vis{height:210px;position:relative;overflow:hidden;}
.card-vis.c1{background:linear-gradient(135deg,#0b2d42 0%,#1d8fa8 60%,#4dc4de 100%);}
.card-vis.c2{background:linear-gradient(135deg,#2e0e0e 0%,#b44040 60%,#e07060 100%);}
.card-vis.c3{background:linear-gradient(135deg,#0a2818 0%,#1e6b38 60%,#4db870 100%);}
.card-vis.c4{background:linear-gradient(135deg,#1a0a2e 0%,#6b3fa0 60%,#a675d4 100%);}
.card-vis.c5{background:linear-gradient(135deg,#2e1a0a 0%,#c9974a 60%,#f0c97a 100%);}
.card-vis.c6{background:linear-gradient(135deg,#0b2d42 0%,#1d5080 60%,#4080c0 100%);}

.chip{
position:absolute;top:1.1rem;left:1.1rem;
font-family:‘JetBrains Mono’,monospace;
font-size:.65rem;letter-spacing:1px;text-transform:uppercase;
padding:.35rem .85rem;border-radius:100px;
background:rgba(0,0,0,.35);backdrop-filter:blur(6px);
color:rgba(255,255,255,.85);
}

/* bar chart inside vis */
.vis-bars{
position:absolute;bottom:0;left:0;right:0;
display:flex;align-items:flex-end;gap:7px;padding:0 1.5rem;
}
.vb{flex:1;border-radius:5px 5px 0 0;background:rgba(255,255,255,.2);}
.vb.hi{background:rgba(255,255,255,.65);}

/* scatter inside vis */
.vis-scatter{position:absolute;inset:0;}
.vs{position:absolute;width:9px;height:9px;border-radius:50%;background:rgba(255,255,255,.35);}
.vs.hi{background:rgba(255,255,255,.85);width:11px;height:11px;}

/* map icon */
.vis-map{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;}
.map-ring{
width:130px;height:130px;border-radius:50%;
border:1.5px solid rgba(255,255,255,.25);
display:flex;align-items:center;justify-content:center;
font-size:3rem;
}

/* gauge */
.vis-gauge{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;}
.gauge{
width:110px;height:110px;border-radius:50%;
border:7px solid rgba(255,255,255,.15);
border-top-color:rgba(255,255,255,.8);
border-right-color:rgba(255,255,255,.5);
display:flex;align-items:center;justify-content:center;
font-family:‘Playfair Display’,serif;font-size:1.9rem;color:white;
}

.card-body{padding:1.6rem 1.75rem;}
.card-title{
font-family:‘Playfair Display’,serif;
font-size:1.2rem;margin-bottom:.5rem;color:var(–ink);line-height:1.3;
}
.card-desc{
font-size:.88rem;color:var(–gray2);line-height:1.7;margin-bottom:1.1rem;
}
.tags{display:flex;flex-wrap:wrap;gap:.45rem;}
.tag{
font-family:‘JetBrains Mono’,monospace;font-size:.66rem;
padding:.3rem .75rem;border-radius:8px;
background:#e8f4f8;color:var(–teal);font-weight:500;
}
.tag.warm{background:#f5ebe0;color:#8b6340;}
.demo-btn{
display:inline-block;margin-top:1rem;
padding:.65rem 1.5rem;border-radius:8px;
background:var(–teal);color:white;
text-decoration:none;font-size:.82rem;font-weight:600;
transition:all .3s;
}
.demo-btn:hover{background:#17748a;transform:translateY(-2px);box-shadow:0 6px 20px rgba(29,143,168,.3);}

/* ── SKILLS (dark) ── */
.skills-cols{display:grid;grid-template-columns:repeat(3,1fr);gap:3rem;}
.sk-group h3{
font-size:.72rem;font-weight:600;letter-spacing:2px;text-transform:uppercase;
color:var(–gold);margin-bottom:1.5rem;padding-bottom:.75rem;
border-bottom:1px solid rgba(255,255,255,.07);
}
.sk{margin-bottom:1.1rem;}
.sk-row{display:flex;justify-content:space-between;margin-bottom:.45rem;}
.sk-name{font-size:.88rem;color:rgba(255,255,255,.75);}
.sk-pct{font-family:‘JetBrains Mono’,monospace;font-size:.7rem;color:var(–gold);}
.sk-track{height:3px;background:rgba(255,255,255,.08);border-radius:2px;overflow:hidden;}
.sk-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,var(–teal),var(–gold));}

/* ── TIMELINE ── */
.tl{position:relative;padding-left:2.25rem;}
.tl::before{
content:’’;position:absolute;left:0;top:.4rem;bottom:0;
width:1px;background:linear-gradient(to bottom,var(–gold),var(–teal),transparent);
}
.tl-item{position:relative;padding-bottom:3.5rem;}
.tl-item::before{
content:’’;position:absolute;left:-2.6rem;top:.35rem;
width:12px;height:12px;border-radius:50%;
background:var(–gold);box-shadow:0 0 0 4px rgba(201,151,74,.15);
}
.tl-date{font-family:‘JetBrains Mono’,monospace;font-size:.68rem;color:var(–gold);letter-spacing:1px;margin-bottom:.4rem;}
.tl-role{font-family:‘Playfair Display’,serif;font-size:1.4rem;margin-bottom:.3rem;}
.tl-org{font-size:.9rem;color:var(–teal-light);font-weight:500;margin-bottom:.75rem;}
.tl-desc{font-size:.88rem;color:rgba(255,255,255,.5);line-height:1.8;}

/* ── ACADEMIC ── */
.ac-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;}
.ac-card{
background:var(–white);border-radius:18px;
padding:1.75rem;box-shadow:var(–shadow);
border-top:3px solid var(–teal);
transition:all .4s;
}
.ac-card.gold-top{border-top-color:var(–gold);}
.ac-card:hover{transform:translateY(-4px);box-shadow:var(–shadow-lg);}
.ac-type{font-family:‘JetBrains Mono’,monospace;font-size:.65rem;letter-spacing:2px;text-transform:uppercase;color:var(–gray);margin-bottom:.7rem;}
.ac-title{font-family:‘Playfair Display’,serif;font-size:1.1rem;margin-bottom:.5rem;color:var(–ink);line-height:1.35;}
.ac-inst{font-size:.85rem;color:var(–teal);font-weight:500;margin-bottom:.75rem;}
.ac-desc{font-size:.84rem;color:var(–gray2);line-height:1.65;}

/* ── CONTACT ── */
.contact-wrap{text-align:center;}
.contact-desc{color:rgba(255,255,255,.45);max-width:480px;margin:0 auto 2.5rem;font-weight:300;line-height:1.8;}
.contact-links{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;}
.btn{
display:inline-block;padding:.85rem 2rem;border-radius:100px;
font-size:.85rem;font-weight:600;text-decoration:none;
transition:all .35s;
}
.btn-primary{background:linear-gradient(135deg,var(–gold),var(–gold-light));color:var(–navy);}
.btn-primary:hover{transform:translateY(-3px);box-shadow:0 10px 30px rgba(201,151,74,.3);}
.btn-outline{border:1px solid rgba(255,255,255,.2);color:var(–white);}
.btn-outline:hover{background:rgba(255,255,255,.08);transform:translateY(-3px);}

/* ── FOOTER ── */
footer{
background:var(–navy);border-top:1px solid rgba(255,255,255,.05);
padding:2rem;text-align:center;
font-size:.75rem;color:rgba(255,255,255,.2);
}

/* ── REVEAL ── */
.reveal{opacity:0;transform:translateY(30px);transition:opacity .7s ease,transform .7s ease;}
.reveal.visible{opacity:1;transform:none;}

/* ── RESPONSIVE ── */
@media(max-width:800px){
.skills-cols,.ac-grid{grid-template-columns:1fr;}
.hero-stats{gap:2rem;}
.stat-num{font-size:2.2rem;}
nav a{padding:.85rem .9rem;font-size:.78rem;}
}
</style>

</head>
<body>

<!-- HERO -->

<header class="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>
  <div class="hero-content">
    <p class="hero-tag">Dados<span>·</span>Educação<span>·</span>Inteligência</p>
    <h1>Silvia <em>Passos</em></h1>
    <p class="hero-sub">Transformo microdados educacionais em inteligência de gestão — dashboards, relatórios e análises para redes de ensino públicas.</p>
    <div class="hero-stats">
      <div class="stat"><span class="stat-num">67</span><div class="stat-lbl">Escolas Atendidas</div></div>
      <div class="stat"><span class="stat-num">6+</span><div class="stat-lbl">Anos em Dados Educacionais</div></div>
      <div class="stat"><span class="stat-num">4</span><div class="stat-lbl">Países na Rede de Pesquisa</div></div>
    </div>
    <div class="scroll-hint">
      <div class="scroll-ring"></div>
    </div>
  </div>
</header>

<!-- NAV -->

<nav>
  <ul>
    <li><a href="#projetos" class="active">Projetos</a></li>
    <li><a href="#competencias">Competências</a></li>
    <li><a href="#experiencia">Experiência</a></li>
    <li><a href="#academico">Formação & Pesquisa</a></li>
    <li><a href="#contato">Contato</a></li>
  </ul>
</nav>

<!-- PROJECTS -->

<div class="section" id="projetos">
  <div class="section-inner">
    <p class="section-label">Portfólio</p>
    <h2 class="section-title">Projetos em Destaque</h2>
    <p class="section-desc">Análises, dashboards e relatórios produzidos para apoiar a tomada de decisão baseada em evidências na educação pública.</p>

```
<div class="cards-list">

  <div class="p-card reveal">
    <div class="card-vis c1">
      <span class="chip">BI · Star Schema</span>
      <div class="vis-bars">
        <div class="vb" style="height:42px"></div>
        <div class="vb hi" style="height:78px"></div>
        <div class="vb" style="height:55px"></div>
        <div class="vb hi" style="height:95px"></div>
        <div class="vb" style="height:62px"></div>
        <div class="vb hi" style="height:85px"></div>
        <div class="vb" style="height:48px"></div>
        <div class="vb hi" style="height:70px"></div>
        <div class="vb" style="height:58px"></div>
        <div class="vb" style="height:38px"></div>
      </div>
    </div>
    <div class="card-body">
      <h3 class="card-title">Arquitetura BI — SARESP 2019–2025</h3>
      <p class="card-desc">Modelagem completa em star schema integrando 15+ fontes de dados (Excel multi-aba) para análise longitudinal de proficiência em LP e Matemática, 2º/5º/9º ano.</p>
      <div class="tags">
        <span class="tag">Power BI</span><span class="tag">Looker Studio</span><span class="tag">Star Schema</span><span class="tag warm">DAX</span><span class="tag warm">ETL</span>
      </div>
    </div>
  </div>

  <div class="p-card reveal">
    <div class="card-vis c2">
      <span class="chip">Análise Estatística</span>
      <div class="vis-scatter">
        <div class="vs hi" style="top:22%;left:28%"></div>
        <div class="vs" style="top:58%;left:18%"></div>
        <div class="vs hi" style="top:32%;left:62%"></div>
        <div class="vs" style="top:72%;left:52%"></div>
        <div class="vs hi" style="top:18%;left:75%"></div>
        <div class="vs" style="top:82%;left:38%"></div>
        <div class="vs hi" style="top:48%;left:82%"></div>
        <div class="vs" style="top:42%;left:8%"></div>
        <div class="vs hi" style="top:28%;left:48%"></div>
        <div class="vs" style="top:65%;left:70%"></div>
        <div class="vs hi" style="top:55%;left:35%"></div>
        <div class="vs" style="top:12%;left:55%"></div>
      </div>
    </div>
    <div class="card-body">
      <h3 class="card-title">Coerência Sistêmica — Avaliações Formativas × SARESP</h3>
      <p class="card-desc">Correlações de Spearman entre CNCA, PNRA e SARESP por escola, identificando padrões divergentes e escolas-referência de coerência avaliativa.</p>
      <div class="tags">
        <span class="tag">Python</span><span class="tag">pandas</span><span class="tag">Spearman</span><span class="tag warm">67 escolas</span>
      </div>
    </div>
  </div>

  <div class="p-card reveal">
    <div class="card-vis c3">
      <span class="chip">Rankings & Criticidade</span>
      <div class="vis-bars">
        <div class="vb hi" style="height:95px"></div>
        <div class="vb hi" style="height:85px"></div>
        <div class="vb" style="height:72px"></div>
        <div class="vb" style="height:58px"></div>
        <div class="vb" style="height:44px"></div>
        <div class="vb" style="height:32px"></div>
        <div class="vb" style="height:22px"></div>
      </div>
    </div>
    <div class="card-body">
      <h3 class="card-title">Mapa de Criticidade por Escola e Segmento</h3>
      <p class="card-desc">Rankings de proficiência por escola, componente e série, com identificação de 8 escolas com vulnerabilidade cross-segmento e análise de equidade (NEE, gênero).</p>
      <div class="tags">
        <span class="tag">Excel</span><span class="tag">Python</span><span class="tag">Microdados</span><span class="tag warm">CMA</span>
      </div>
    </div>
  </div>

  <div class="p-card reveal">
    <div class="card-vis c4">
      <span class="chip">Georreferenciamento</span>
      <div class="vis-map">
        <div class="map-ring">📍</div>
      </div>
    </div>
    <div class="card-body">
      <h3 class="card-title">Mapa de Fluência Leitora</h3>
      <p class="card-desc">Dashboard interativo com mapa georreferenciado de 67 escolas, 5.872 alunos avaliados, análise regional comparativa, ranking de fluência e decomposição de pré-leitores (N1–N4) para intervenção pedagógica.</p>
      <div class="tags">
        <span class="tag">Leaflet.js</span><span class="tag">Chart.js</span><span class="tag">HTML/CSS/JS</span><span class="tag warm">CAEd</span>
      </div>
      <a href="https://fluenciadash-qeguanjk.manus.space" target="_blank" class="demo-btn">Ver demo ao vivo →</a>
    </div>
  </div>

  <div class="p-card reveal">
    <div class="card-vis c5">
      <span class="chip">Projeções IDEB</span>
      <div class="vis-gauge">
        <div class="gauge">5.8</div>
      </div>
    </div>
    <div class="card-body">
      <h3 class="card-title">Projeções IDEB — 5º Ano por Escola</h3>
      <p class="card-desc">Cálculo de projeções IDEB utilizando fórmula oficial INEP, com comparativo escola × rede × meta, e dashboards interativos Chart.js para cada unidade.</p>
      <div class="tags">
        <span class="tag">INEP</span><span class="tag">Chart.js</span><span class="tag">HTML/JS</span><span class="tag warm">IDEB</span>
      </div>
    </div>
  </div>

  <div class="p-card reveal">
    <div class="card-vis c6">
      <span class="chip">Pesquisa Acadêmica</span>
      <div class="vis-bars">
        <div class="vb" style="height:12px"></div>
        <div class="vb" style="height:25px"></div>
        <div class="vb hi" style="height:78px"></div>
        <div class="vb" style="height:52px"></div>
        <div class="vb" style="height:28px"></div>
        <div class="vb" style="height:10px"></div>
      </div>
    </div>
    <div class="card-body">
      <h3 class="card-title">DigCompEdu — Perfis de Competência Digital Docente</h3>
      <p class="card-desc">Análise de 136 professores com SELFIEforTEACHERS (instrumento cuja adaptação brasileira coautorei). Perfil predominante: Integrador/B1 (33,82%). Cohen's d = −0,044.</p>
      <div class="tags">
        <span class="tag">DigCompEdu</span><span class="tag">SPSS</span><span class="tag">Mixed Methods</span><span class="tag warm">n=136</span>
      </div>
    </div>
  </div>

</div>
```

  </div>
</div>

<!-- SKILLS -->

<div class="section dark" id="competencias">
  <div class="section-inner">
    <p class="section-label">Stack Técnico</p>
    <h2 class="section-title">Competências</h2>
    <p class="section-desc">Ferramentas e habilidades que aplico no dia a dia da análise de dados educacionais.</p>
    <div class="skills-cols">
      <div class="sk-group reveal">
        <h3>BI & Visualização</h3>
        <div class="sk"><div class="sk-row"><span class="sk-name">Power BI</span><span class="sk-pct">90%</span></div><div class="sk-track"><div class="sk-fill" style="width:90%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Looker Studio</span><span class="sk-pct">92%</span></div><div class="sk-track"><div class="sk-fill" style="width:92%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Flourish</span><span class="sk-pct">88%</span></div><div class="sk-track"><div class="sk-fill" style="width:88%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Chart.js / Leaflet.js</span><span class="sk-pct">75%</span></div><div class="sk-track"><div class="sk-fill" style="width:75%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Excel Avançado</span><span class="sk-pct">95%</span></div><div class="sk-track"><div class="sk-fill" style="width:95%"></div></div></div>
      </div>
      <div class="sk-group reveal">
        <h3>Dados & Programação</h3>
        <div class="sk"><div class="sk-row"><span class="sk-name">Python / pandas</span><span class="sk-pct">78%</span></div><div class="sk-track"><div class="sk-fill" style="width:78%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">ETL & Limpeza de Dados</span><span class="sk-pct">90%</span></div><div class="sk-track"><div class="sk-fill" style="width:90%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">HTML / CSS / JavaScript</span><span class="sk-pct">72%</span></div><div class="sk-track"><div class="sk-fill" style="width:72%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Estatística Aplicada</span><span class="sk-pct">82%</span></div><div class="sk-track"><div class="sk-fill" style="width:82%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">openpyxl / Node.js docx</span><span class="sk-pct">70%</span></div><div class="sk-track"><div class="sk-fill" style="width:70%"></div></div></div>
      </div>
      <div class="sk-group reveal">
        <h3>Domínio Educacional</h3>
        <div class="sk"><div class="sk-row"><span class="sk-name">SARESP / SAEB / IDEB</span><span class="sk-pct">97%</span></div><div class="sk-track"><div class="sk-fill" style="width:97%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Microdados INEP</span><span class="sk-pct">93%</span></div><div class="sk-track"><div class="sk-fill" style="width:93%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Indicadores Educacionais</span><span class="sk-pct">95%</span></div><div class="sk-track"><div class="sk-fill" style="width:95%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">DigCompEdu / SELFIE</span><span class="sk-pct">96%</span></div><div class="sk-track"><div class="sk-fill" style="width:96%"></div></div></div>
        <div class="sk"><div class="sk-row"><span class="sk-name">Storytelling com Dados</span><span class="sk-pct">85%</span></div><div class="sk-track"><div class="sk-fill" style="width:85%"></div></div></div>
      </div>
    </div>
  </div>
</div>

<!-- EXPERIENCE -->

<div class="section" id="experiencia">
  <div class="section-inner">
    <p class="section-label">Trajetória</p>
    <h2 class="section-title">Experiência Profissional</h2>
    <p class="section-desc" style="color:var(--gray2)">Uma carreira construída na interseção entre educação pública, análise de dados e pesquisa aplicada.</p>
    <!-- reuse dark timeline on light bg -->
    <div style="color:var(--ink)">
      <div class="tl" style="--gold:#c9974a">
        <div class="tl-item reveal" style="padding-bottom:3rem">
          <p class="tl-date" style="color:var(--gold)">ATUAL</p>
          <h3 class="tl-role" style="color:var(--ink)">Analista de Dados e Indicadores Educacionais</h3>
          <p class="tl-org" style="color:var(--teal)">Secretaria Municipal de Educação — São José dos Campos, SP</p>
          <p class="tl-desc" style="color:var(--gray2)">Coordenadoria de Gestão da Aprendizagem. Produção de análises de desempenho, dashboards executivos e relatórios institucionais para rede de 67 escolas municipais. Processamento de microdados SARESP e SAEB, arquitetura BI star schema, correlações de coerência avaliativa, projeções IDEB, participação de alunos NEE e materiais formativos para gestores.</p>
        </div>
        <div class="tl-item reveal" style="padding-bottom:0">
          <p class="tl-date" style="color:var(--gold)">EM ANDAMENTO</p>
          <h3 class="tl-role" style="color:var(--ink)">Pesquisadora Doutoranda — Competências Digitais Docentes</h3>
          <p class="tl-org" style="color:var(--teal)">PUC-SP · Programa TIDD · Prof. Dr. João Augusto Mattar Neto</p>
          <p class="tl-desc" style="color:var(--gray2)">Investigação sobre formação continuada e desenvolvimento de competências digitais de professores da rede pública (DigCompEdu / SELFIEforTEACHERS). Rede internacional Brasil · Paraguai · Canadá · Portugal. Financiamento CNPq, CAPES e PIPEq/PUC-SP.</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ACADEMIC -->

<div class="section" id="academico" style="background:var(--paper2)">
  <div class="section-inner">
    <p class="section-label">Formação & Pesquisa</p>
    <h2 class="section-title">Base Acadêmica</h2>
    <p class="section-desc" style="color:var(--gray2)">Produção acadêmica com visibilidade e impacto internacional.</p>
    <div class="ac-grid">
      <div class="ac-card reveal">
        <p class="ac-type">Doutorado em Andamento</p>
        <h3 class="ac-title">Tecnologias da Inteligência e Design Digital</h3>
        <p class="ac-inst">PUC-SP · TIDD</p>
        <p class="ac-desc">Design Sequencial Explanatório, 136 participantes. Análise de casos contrastantes A1 vs. C2. Perfil predominante Integrador/B1 (33,82%). Cohen's d = −0,044.</p>
      </div>
      <div class="ac-card gold-top reveal">
        <p class="ac-type">Publicação / Instrumento</p>
        <h3 class="ac-title">SELFIEforTEACHERS — Adaptação Brasileira</h3>
        <p class="ac-inst">competenciasdigitais.net</p>
        <p class="ac-desc">Coautoria da adaptação ao português brasileiro do instrumento europeu de autoavaliação de competências digitais docentes.</p>
      </div>
      <div class="ac-card reveal">
        <p class="ac-type">Rede Internacional</p>
        <h3 class="ac-title">Pesquisa Multi-país em Competências Digitais</h3>
        <p class="ac-inst">Brasil · Paraguai · Canadá · Portugal</p>
        <p class="ac-desc">Colaboração internacional com financiamento PIPEq/PUC-SP, CNPq e CAPES, investigando competências digitais docentes em múltiplos contextos.</p>
      </div>
    </div>
  </div>
</div>

<!-- CONTACT -->

<div class="section dark" id="contato">
  <div class="section-inner contact-wrap">
    <p class="section-label">Vamos Conversar</p>
    <h2 class="section-title">Entre em Contato</h2>
    <p class="contact-desc">Disponível para oportunidades em Análise de Dados Educacionais, BI, Consultoria e Avaliação de Redes de Ensino.</p>
    <div class="contact-links">
      <a href="https://www.linkedin.com/in/silvia-regina-passos-08577768" target="_blank" class="btn btn-primary">LinkedIn →</a>
      <a href="mailto:Camilo.silvia@gmail.com" class="btn btn-outline">E-mail</a>
      <a href="https://competenciasdigitais.net" target="_blank" class="btn btn-outline">competenciasdigitais.net</a>
    </div>
  </div>
</div>

<footer>© 2026 Silvia Passos · Dados & Educação · São José dos Campos, SP</footer>

<script>
// Reveal on scroll
const obs = new IntersectionObserver(es=>{
  es.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('visible'); });
},{threshold:.1});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

// Active nav link
const secs = document.querySelectorAll('[id]');
const links = document.querySelectorAll('nav a');
window.addEventListener('scroll',()=>{
  let cur='';
  secs.forEach(s=>{ if(scrollY>=s.offsetTop-120) cur=s.id; });
  links.forEach(a=>{
    a.classList.remove('active');
    if(a.getAttribute('href')==='#'+cur) a.classList.add('active');
  });
});
</script>

</body>
</html>
