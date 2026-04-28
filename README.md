[index.html](https://github.com/user-attachments/files/27179339/index.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Consultoria Primeiro Imóvel — Juliana Moura</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --creme: #F5EFE4;
    --areia: #E8DCCA;
    --terra: #B5895A;
    --terracota: #C4714A;
    --marrom: #6B3F28;
    --escuro: #2C1810;
    --branco: #FDFAF6;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--creme);
    color: var(--escuro);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  .hero {
    min-height: 100vh;
    background: var(--marrom);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 60px 48px;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 420px; height: 420px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(196,113,74,0.35) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -60px;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(181,137,90,0.2) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-tag {
    display: inline-block;
    background: rgba(255,255,255,0.1);
    color: var(--areia);
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 6px 14px;
    border-radius: 20px;
    margin-bottom: 32px;
    border: 1px solid rgba(255,255,255,0.15);
    animation: fadeUp 0.8s ease both;
  }

  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.6rem, 8vw, 4.5rem);
    color: var(--branco);
    line-height: 1.1;
    margin-bottom: 24px;
    max-width: 600px;
    animation: fadeUp 0.8s 0.1s ease both;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--terra);
  }

  .hero p {
    font-size: 1.1rem;
    color: var(--areia);
    max-width: 480px;
    margin-bottom: 40px;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .hero-cta {
    display: inline-block;
    background: var(--terracota);
    color: var(--branco);
    font-family: 'DM Sans', sans-serif;
    font-size: 0.95rem;
    font-weight: 600;
    padding: 16px 36px;
    border-radius: 50px;
    text-decoration: none;
    letter-spacing: 0.5px;
    transition: transform 0.2s, background 0.2s;
    animation: fadeUp 0.8s 0.3s ease both;
  }

  .hero-cta:hover {
    background: var(--terra);
    transform: translateY(-2px);
  }

  .hero-scroll {
    position: absolute;
    bottom: 32px;
    left: 50%;
    transform: translateX(-50%);
    color: rgba(255,255,255,0.3);
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    animation: fadeUp 1s 0.6s ease both;
  }

  .hero-scroll::after {
    content: '';
    display: block;
    width: 1px;
    height: 40px;
    background: rgba(255,255,255,0.2);
    animation: scrollLine 1.5s ease-in-out infinite;
  }

  .intro {
    padding: 80px 48px;
    max-width: 760px;
    margin: 0 auto;
  }

  .intro-label {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--terracota);
    margin-bottom: 20px;
  }

  .intro h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.8rem, 5vw, 2.6rem);
    line-height: 1.25;
    margin-bottom: 24px;
    color: var(--marrom);
  }

  .intro p {
    font-size: 1.05rem;
    color: #5a4030;
    margin-bottom: 16px;
  }

  .paraquem {
    background: var(--marrom);
    padding: 80px 48px;
    color: var(--branco);
  }

  .paraquem-inner {
    max-width: 760px;
    margin: 0 auto;
  }

  .paraquem .section-label {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 20px;
  }

  .paraquem h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.8rem, 5vw, 2.4rem);
    margin-bottom: 40px;
    color: var(--branco);
  }

  .cards-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .card {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 16px;
    padding: 28px 24px;
    transition: background 0.2s;
  }

  .card:hover {
    background: rgba(255,255,255,0.1);
  }

  .card-icon {
    font-size: 1.6rem;
    margin-bottom: 12px;
  }

  .card p {
    font-size: 0.95rem;
    color: var(--areia);
    line-height: 1.6;
  }

  .oque {
    padding: 80px 48px;
    max-width: 760px;
    margin: 0 auto;
  }

  .oque .section-label {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--terracota);
    margin-bottom: 20px;
  }

  .oque h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.8rem, 5vw, 2.4rem);
    color: var(--marrom);
    margin-bottom: 40px;
  }

  .steps {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .step {
    display: flex;
    gap: 24px;
    padding: 28px 0;
    border-bottom: 1px solid var(--areia);
  }

  .step:last-child { border-bottom: none; }

  .step-num {
    font-family: 'DM Serif Display', serif;
    font-size: 2rem;
    color: var(--terra);
    opacity: 0.5;
    min-width: 40px;
    line-height: 1;
    padding-top: 4px;
  }

  .step-content h3 {
    font-family: 'DM Sans', sans-serif;
    font-weight: 600;
    font-size: 1rem;
    color: var(--marrom);
    margin-bottom: 6px;
  }

  .step-content p {
    font-size: 0.95rem;
    color: #6b4a35;
  }

  .entregavel {
    background: var(--terracota);
    padding: 60px 48px;
    text-align: center;
    color: var(--branco);
  }

  .entregavel-inner {
    max-width: 580px;
    margin: 0 auto;
  }

  .entregavel .emoji {
    font-size: 2.5rem;
    margin-bottom: 16px;
  }

  .entregavel h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.6rem, 4vw, 2.2rem);
    margin-bottom: 16px;
  }

  .entregavel p {
    font-size: 1rem;
    opacity: 0.9;
    line-height: 1.7;
  }

  .investimento {
    padding: 80px 48px;
    max-width: 760px;
    margin: 0 auto;
  }

  .investimento .section-label {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--terracota);
    margin-bottom: 20px;
  }

  .investimento h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.8rem, 5vw, 2.4rem);
    color: var(--marrom);
    margin-bottom: 40px;
  }

  .preco-box {
    background: var(--branco);
    border: 2px solid var(--areia);
    border-radius: 24px;
    padding: 40px;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .preco-valor {
    font-family: 'DM Serif Display', serif;
    font-size: 3.5rem;
    color: var(--marrom);
    line-height: 1;
  }

  .preco-valor span {
    font-size: 1.4rem;
    color: var(--terra);
    vertical-align: super;
    font-family: 'DM Sans', sans-serif;
    font-weight: 500;
  }

  .preco-desc {
    font-size: 0.9rem;
    color: #7a5540;
  }

  .preco-itens {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 8px;
  }

  .preco-itens li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 0.95rem;
    color: #5a4030;
  }

  .preco-itens li::before {
    content: '✓';
    color: var(--terracota);
    font-weight: 700;
    flex-shrink: 0;
  }

  .preco-cta {
    display: inline-block;
    background: var(--marrom);
    color: var(--branco);
    font-weight: 600;
    font-size: 0.95rem;
    padding: 16px 36px;
    border-radius: 50px;
    text-decoration: none;
    margin-top: 8px;
    transition: background 0.2s, transform 0.2s;
    align-self: flex-start;
  }

  .preco-cta:hover {
    background: var(--terracota);
    transform: translateY(-2px);
  }

  .sobre {
    background: var(--areia);
    padding: 80px 48px;
  }

  .sobre-inner {
    max-width: 760px;
    margin: 0 auto;
  }

  .sobre .section-label {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--terracota);
    margin-bottom: 20px;
  }

  .sobre h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.8rem, 5vw, 2.4rem);
    color: var(--marrom);
    margin-bottom: 24px;
  }

  .sobre p {
    font-size: 1rem;
    color: #5a4030;
    margin-bottom: 14px;
    max-width: 620px;
  }

  .sobre .creci {
    display: inline-block;
    margin-top: 8px;
    background: var(--marrom);
    color: var(--branco);
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 6px 14px;
    border-radius: 20px;
  }

  footer {
    background: var(--escuro);
    color: rgba(255,255,255,0.4);
    text-align: center;
    padding: 32px 48px;
    font-size: 0.85rem;
  }

  footer strong {
    color: rgba(255,255,255,0.7);
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes scrollLine {
    0%   { transform: scaleY(0); transform-origin: top; }
    50%  { transform: scaleY(1); transform-origin: top; }
    51%  { transform: scaleY(1); transform-origin: bottom; }
    100% { transform: scaleY(0); transform-origin: bottom; }
  }

  @media (max-width: 600px) {
    .hero, .intro, .paraquem, .oque, .entregavel, .investimento, .sobre { padding: 60px 24px; }
    .cards-grid { grid-template-columns: 1fr; }
    .preco-box { padding: 28px 24px; }
    .preco-cta { align-self: stretch; text-align: center; }
  }
</style>
</head>
<body>

<section class="hero">
  <div class="hero-tag">Juliana Moura · Corretora & Avaliadora</div>
  <h1>Comprar o primeiro imóvel<br>não precisa ser <em>assustador.</em></h1>
  <p>Uma sessão só sua, onde a gente entende a sua situação e traça um caminho real.</p>
  <a href="#investimento" class="hero-cta">Quero minha consultoria</a>
  <div class="hero-scroll">rolar</div>
</section>

<section class="intro">
  <div class="intro-label">Por que isso existe</div>
  <h2>A maioria das pessoas chega ao mercado imobiliário completamente perdida.</h2>
  <p>Financiamento, FGTS, documentação, proposta, escritura… é muita coisa ao mesmo tempo — e ninguém explica direito.</p>
  <p>Criamos essa consultoria pra que você chegue no processo <strong>sabendo o que está fazendo.</strong> Com clareza, segurança e uma corretora do seu lado desde o começo.</p>
</section>

<section class="paraquem">
  <div class="paraquem-inner">
    <div class="section-label">Para quem é</div>
    <h2>Se você se identificar com algum desses, a consultoria é pra você.</h2>
    <div class="cards-grid">
      <div class="card">
        <div class="card-icon">🤯</div>
        <p>Quer comprar, mas não sabe nem por onde começar</p>
      </div>
      <div class="card">
        <div class="card-icon">💸</div>
        <p>Tem FGTS parado e não sabe se pode (ou como) usar</p>
      </div>
      <div class="card">
        <div class="card-icon">🏦</div>
        <p>Está com medo do financiamento e de se comprometer</p>
      </div>
      <div class="card">
        <div class="card-icon">📋</div>
        <p>Quer entender o processo antes de assinar qualquer coisa</p>
      </div>
    </div>
  </div>
</section>

<section class="oque">
  <div class="section-label">O que acontece na sessão</div>
  <h2>1h30 focada inteiramente em você.</h2>
  <div class="steps">
    <div class="step">
      <div class="step-num">01</div>
      <div class="step-content">
        <h3>Diagnóstico da sua situação</h3>
        <p>Renda, documentação, FGTS, histórico de crédito — entendo onde você está de verdade, sem julgamento.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">02</div>
      <div class="step-content">
        <h3>O processo explicado do começo ao fim</h3>
        <p>Etapas, prazos, o que pode travar, o que é negociável — tudo em linguagem humana.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">03</div>
      <div class="step-content">
        <h3>Financiamento sem mistério</h3>
        <p>MCMV, banco, consórcio — o que faz mais sentido pro seu perfil e o que esperar de cada opção.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">04</div>
      <div class="step-content">
        <h3>Perfil do imóvel ideal x realidade</h3>
        <p>O que você quer comprar x o que o mercado de Niterói (e região) oferece no seu orçamento.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">05</div>
      <div class="step-content">
        <h3>Próximos passos personalizados</h3>
        <p>Você sai com um plano claro do que fazer primeiro — sem achismo, sem ansiedade desnecessária.</p>
      </div>
    </div>
  </div>
</section>

<section class="entregavel">
  <div class="entregavel-inner">
    <div class="emoji">📝</div>
    <h2>Depois da sessão, você recebe um resumo por escrito.</h2>
    <p>Tudo o que discutimos — diagnóstico, orientações e próximos passos — organizado e enviado pra você. Pra consultar quando quiser, no seu tempo.</p>
  </div>
</section>

<section class="investimento" id="investimento">
  <div class="section-label">Investimento</div>
  <h2>Simples, transparente.</h2>
  <div class="preco-box">
    <div class="preco-valor"><span>R$</span> 197</div>
    <div class="preco-desc">Sessão única · 1h30 · Online ou presencial em Niterói</div>
    <ul class="preco-itens">
      <li>Diagnóstico completo da sua situação</li>
      <li>Orientação de financiamento personalizada</li>
      <li>Mapa de próximos passos</li>
      <li>Resumo por escrito pós-sessão</li>
      <li>Atendimento de quem realmente conhece o mercado local</li>
    </ul>
    <a href="https://wa.me/5521964016478?text=Oi%20Ju!%20Quero%20saber%20mais%20sobre%20a%20Consultoria%20Primeiro%20Im%C3%B3vel%20%F0%9F%8F%A0" class="preco-cta" target="_blank">Falar com a Ju no WhatsApp →</a>
  </div>
</section>

<section class="sobre">
  <div class="sobre-inner">
    <div class="section-label">Quem vai te atender</div>
    <h2>Oi, eu sou a Juliana Moura! 😊</h2>
    <p>Sou corretora e avaliadora de imóveis em Niterói, com mais de 8 anos de experiência no mercado imobiliário. Atuo em todas as etapas do processo: compra e venda, locação, avaliação, regularização e consultoria, do começo ao fim, com atenção e cuidado em cada detalhe.</p>
    <p>Seja qual for o seu momento com o imóvel, estou aqui para te orientar com segurança e clareza, encontrando a melhor solução para a sua necessidade.</p>
    <p>Vamos conversar? Será um prazer te ajudar! 🏡</p>
    <div class="creci">CRECI 076457 · RJ</div>
  </div>
</section>

<footer>
  <strong>Juliana Moura</strong> · Corretora & Avaliadora de Imóveis · Niterói, RJ<br>
  CRECI 076457
</footer>

</body>
</html>
