# pandorastudio
[index.html.html](https://github.com/user-attachments/files/26847948/index.html.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anúncios que Vendem no Mercado Livre | Pandora Studio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800;900&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #070D1A;
    --surface: #0D1628;
    --surface2: #111E35;
    --border: rgba(180,200,255,0.08);
    --border2: rgba(180,200,255,0.18);
    --yellow: #C9A84C;
    --yellow2: #E2C06A;
    --text: #F0F4FF;
    --muted: #7A8BAA;
    --muted2: #B0BEDB;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  /* ─── NAV ─── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    padding: 20px 40px;
    display: flex; align-items: center; justify-content: space-between;
    border-bottom: 1px solid var(--border);
    background: rgba(7,13,26,0.94);
    backdrop-filter: blur(12px);
  }
  .logo {
    font-family: 'Playfair Display', serif;
    font-weight: 800;
    font-size: 18px;
    letter-spacing: -0.5px;
  }
  .logo span { color: var(--yellow); }
  nav a.btn-nav {
    background: var(--yellow);
    color: #1a0e00;
    font-weight: 600;
    font-size: 14px;
    padding: 10px 22px;
    border-radius: 4px;
    text-decoration: none;
    transition: background 0.2s;
  }
  nav a.btn-nav:hover { background: var(--yellow2); }

  /* ─── SECTIONS ─── */
  section { padding: 100px 40px; max-width: 1100px; margin: 0 auto; text-align: center; }

  /* ─── HERO ─── */
  #hero {
    min-height: 100vh;
    display: flex; flex-direction: column; justify-content: center; align-items: center;
    padding-top: 140px;
    max-width: 100%;
    padding-left: 60px;
    padding-right: 60px;
    position: relative;
    overflow: hidden;
    text-align: center;
  }
  #hero::before {
    content: '';
    position: absolute;
    top: -200px; right: -200px;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(245,197,24,0.07) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-inner { max-width: 1100px; margin: 0 auto; width: 100%; text-align: center; display: flex; flex-direction: column; align-items: center; }

  .eyebrow {
    display: inline-flex; align-items: center; gap: 10px;
    background: rgba(245,197,24,0.1);
    border: 1px solid rgba(245,197,24,0.25);
    color: var(--yellow);
    font-size: 13px;
    font-weight: 500;
    padding: 6px 14px;
    border-radius: 100px;
    margin-bottom: 32px;
    letter-spacing: 0.3px;
  }
  .eyebrow::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--yellow);
    border-radius: 50%;
  }

  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(38px, 5vw, 68px);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -2px;
    margin-bottom: 28px;
    max-width: 900px;
    margin-left: auto;
    margin-right: auto;
  }
  h1 em {
    font-style: normal;
    color: var(--yellow);
    position: relative;
  }

  .hero-sub {
    font-size: 18px;
    color: var(--muted2);
    max-width: 600px;
    line-height: 1.7;
    margin-bottom: 44px;
    font-weight: 300;
    text-align: center;
  }

  .hero-cta-group { display: flex; align-items: center; justify-content: center; gap: 20px; flex-wrap: wrap; }

  .btn-primary {
    display: inline-block;
    background: var(--yellow);
    color: #1a0e00;
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 16px;
    padding: 16px 36px;
    border-radius: 4px;
    text-decoration: none;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: var(--yellow2); transform: translateY(-1px); }

  .hero-proof {
    font-size: 14px;
    color: var(--muted);
    display: flex; align-items: center; gap: 8px;
  }
  .stars { color: var(--yellow); font-size: 13px; letter-spacing: 2px; }

  .hero-stats {
    display: grid;
    grid-template-columns: repeat(4, auto);
    gap: 0;
    margin-top: 80px;
    border-top: 1px solid var(--border);
    padding-top: 48px;
    width: fit-content;
    margin-left: auto;
    margin-right: auto;
  }
  .stat-item {
    padding-right: 60px;
    border-right: 1px solid var(--border);
    margin-right: 60px;
  }
  .stat-item:last-child { border-right: none; margin-right: 0; padding-right: 0; }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 42px;
    font-weight: 800;
    color: var(--yellow);
    letter-spacing: -2px;
    display: block;
    line-height: 1;
    margin-bottom: 6px;
  }
  .stat-label { font-size: 13px; color: var(--muted); font-weight: 400; }

  /* ─── PAIN ─── */
  #pain { border-top: 1px solid var(--border); }

  .section-label {
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--yellow);
    margin-bottom: 20px;
  }

  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 3.5vw, 46px);
    font-weight: 800;
    line-height: 1.1;
    letter-spacing: -1.5px;
    margin-bottom: 20px;
  }
  h2 em { font-style: normal; color: var(--yellow); }

  .section-intro {
    font-size: 17px;
    color: var(--muted2);
    max-width: 560px;
    font-weight: 300;
    line-height: 1.7;
    margin-bottom: 56px;
    margin-left: auto;
    margin-right: auto;
  }

  .pain-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
  }
  .pain-card {
    background: var(--surface);
    padding: 36px 32px;
    transition: background 0.2s;
    text-align: left;
  }
  .pain-card:hover { background: var(--surface2); }
  .pain-icon {
    width: 40px; height: 40px;
    background: rgba(245,197,24,0.1);
    border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px;
    margin-bottom: 20px;
  }
  .pain-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 17px;
    font-weight: 700;
    margin-bottom: 10px;
    line-height: 1.3;
  }
  .pain-card p { font-size: 14px; color: var(--muted); line-height: 1.6; }

  /* ─── SOLUTION ─── */
  #solution { border-top: 1px solid var(--border); }

  .solution-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: start;
    text-align: left;
  }
  .solution-steps { display: flex; flex-direction: column; gap: 0; }
  .step {
    display: flex; gap: 24px;
    padding: 28px 0;
    border-bottom: 1px solid var(--border);
    transition: padding-left 0.2s;
  }
  .step:last-child { border-bottom: none; }
  .step:hover { padding-left: 8px; }
  .step-num {
    font-family: 'Playfair Display', serif;
    font-size: 13px;
    font-weight: 700;
    color: var(--yellow);
    opacity: 0.5;
    min-width: 28px;
    padding-top: 3px;
  }
  .step-content h3 {
    font-family: 'Playfair Display', serif;
    font-size: 17px;
    font-weight: 700;
    margin-bottom: 8px;
  }
  .step-content p { font-size: 14px; color: var(--muted); line-height: 1.6; }

  .solution-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 40px;
    position: sticky;
    top: 100px;
  }
  .solution-card-label {
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: var(--muted);
    margin-bottom: 24px;
    font-weight: 600;
  }
  .big-result {
    font-family: 'Playfair Display', serif;
    font-size: 52px;
    font-weight: 800;
    color: var(--yellow);
    letter-spacing: -2px;
    line-height: 1;
    margin-bottom: 8px;
  }
  .big-result-label { font-size: 15px; color: var(--muted2); margin-bottom: 32px; }

  .result-list { list-style: none; display: flex; flex-direction: column; gap: 14px; }
  .result-list li {
    display: flex; align-items: flex-start; gap: 12px;
    font-size: 14px; color: var(--muted2); line-height: 1.5;
  }
  .result-list li::before {
    content: '→';
    color: var(--yellow);
    font-weight: 700;
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* ─── TESTIMONIALS ─── */
  #testimonials { border-top: 1px solid var(--border); }

  .testi-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 16px;
  }
  .testi-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 32px;
    text-align: left;
  }
  .testi-stars { color: var(--yellow); font-size: 14px; letter-spacing: 3px; margin-bottom: 16px; }
  .testi-text {
    font-size: 15px;
    color: var(--muted2);
    line-height: 1.65;
    margin-bottom: 24px;
    font-style: italic;
  }
  .testi-author { display: flex; align-items: center; gap: 12px; }
  .testi-avatar {
    width: 40px; height: 40px;
    background: rgba(245,197,24,0.15);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 14px;
    color: var(--yellow);
  }
  .testi-name { font-size: 14px; font-weight: 600; }
  .testi-role { font-size: 12px; color: var(--muted); }

  /* ─── PARA QUEM ─── */
  #para-quem { border-top: 1px solid var(--border); }

  .who-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
  }
  .who-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 28px;
    transition: border-color 0.2s;
    text-align: left;
  }
  .who-card:hover { border-color: rgba(245,197,24,0.35); }
  .who-check {
    width: 28px; height: 28px;
    background: rgba(245,197,24,0.12);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    color: var(--yellow);
    font-size: 13px;
    font-weight: 700;
    margin-bottom: 16px;
  }
  .who-card h3 { font-family: 'Playfair Display', serif; font-size: 15px; font-weight: 700; margin-bottom: 8px; }
  .who-card p { font-size: 13px; color: var(--muted); line-height: 1.55; }

  /* ─── CTA ─── */
  #cta {
    border-top: 1px solid var(--border);
    text-align: center;
    padding: 120px 40px;
    max-width: 100%;
    position: relative;
    overflow: hidden;
  }
  #cta::before {
    content: '';
    position: absolute;
    bottom: -100px; left: 50%; transform: translateX(-50%);
    width: 700px; height: 400px;
    background: radial-gradient(ellipse, rgba(245,197,24,0.08) 0%, transparent 70%);
    pointer-events: none;
  }
  #cta .inner { max-width: 700px; margin: 0 auto; position: relative; }
  #cta h2 { margin-bottom: 20px; }
  #cta .section-intro { margin: 0 auto 44px; max-width: 520px; }

  /* ─── FORM ─── */
  .form-wrap {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 44px;
    text-align: left;
    max-width: 500px;
    margin: 0 auto;
  }
  .form-title {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 8px;
  }
  .form-sub { font-size: 14px; color: var(--muted); margin-bottom: 28px; }

  .form-group { margin-bottom: 16px; }
  label { display: block; font-size: 13px; font-weight: 500; color: var(--muted2); margin-bottom: 7px; }
  input, select, textarea {
    width: 100%;
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--border2);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    padding: 12px 16px;
    border-radius: 6px;
    outline: none;
    transition: border-color 0.2s;
  }
  input:focus, select:focus, textarea:focus { border-color: rgba(245,197,24,0.6); }
  select option { background: #1A1A1A; }
  textarea { height: 100px; resize: none; }

  .btn-submit {
    width: 100%;
    background: var(--yellow);
    color: #1a0e00;
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 16px;
    padding: 16px;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    margin-top: 8px;
    transition: background 0.2s;
  }
  .btn-submit:hover { background: var(--yellow2); }
  .form-footer { font-size: 12px; color: var(--muted); text-align: center; margin-top: 14px; }

  /* ─── FOOTER ─── */
  footer {
    border-top: 1px solid var(--border);
    padding: 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 100%;
  }
  footer p { font-size: 13px; color: var(--muted); }

  /* ─── ANIMATIONS ─── */
  .fade-in {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-in.visible { opacity: 1; transform: translateY(0); }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 768px) {
    nav { padding: 16px 20px; }
    #hero { padding: 120px 24px 80px; }
    section { padding: 70px 24px; }
    .solution-grid { grid-template-columns: 1fr; }
    .solution-card { position: static; }
    .hero-stats { grid-template-columns: 1fr 1fr; gap: 24px; }
    .stat-item { border-right: none; margin-right: 0; padding-right: 0; border-bottom: 1px solid var(--border); padding-bottom: 24px; }
    .stat-item:last-child { border-bottom: none; }
    .form-wrap { padding: 28px 20px; }
    footer { flex-direction: column; gap: 12px; text-align: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">Pandora <span>Studio</span></div>
  <a href="https://api.whatsapp.com/message/CNX7FWROAMBJP1?autoload=1&app_absent=0" target="_blank" rel="noopener" class="btn-nav">Quero diagnóstico gratuito</a>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-inner">
    <div class="eyebrow fade-in">Especialista em Anúncios para Mercado Livre</div>

    <h1 class="fade-in">Seus anúncios aparecem.<br>Mas <em>ninguém compra.</em><br>Até agora!</h1>

    <p class="hero-sub fade-in">
      Transformo anúncios invisíveis em máquinas de venda. Sem depender de baixar preço, sem pagar mais por clique, sem achismo.
    </p>

    <div class="hero-cta-group fade-in">
      <a href="https://api.whatsapp.com/message/CNX7FWROAMBJP1?autoload=1&app_absent=0" target="_blank" rel="noopener" class="btn-primary">Quero anúncios que vendem →</a>
      <div class="hero-proof">
        <span class="stars">★★★★★</span>
        <span>+1.500 vendedores atendidos</span>
      </div>
    </div>

    <div class="hero-stats fade-in">
      <div class="stat-item">
        <span class="stat-num">3×</span>
        <span class="stat-label">Aumento médio em conversão</span>
      </div>
      <div class="stat-item">
        <span class="stat-num">-40%</span>
        <span class="stat-label">Custo por clique no produto</span>
      </div>
      <div class="stat-item">
        <span class="stat-num">30d</span>
        <span class="stat-label">Para ver os primeiros resultados</span>
      </div>
      <div class="stat-item">
        <span class="stat-num">+98%</span>
        <span class="stat-label">Taxa de satisfação dos clientes</span>
      </div>
    </div>
  </div>
</section>

<!-- PAIN -->
<section id="pain">
  <div class="section-label">O problema</div>
  <h2 class="fade-in">Por que seus anúncios<br><em>não vendem</em> como deveriam</h2>
  <p class="section-intro fade-in">Não é falta de estoque, não é o preço. É a forma como o seu produto está sendo apresentado dentro da plataforma.</p>

  <div class="pain-grid fade-in">
    <div class="pain-card">
      <div class="pain-icon">👁</div>
      <h3>Anúncio que ninguém encontra</h3>
      <p>O algoritmo do Mercado Livre é implacável. Sem as palavras certas, seu produto some na página 3 enquanto o concorrente domina a busca.</p>
    </div>
    <div class="pain-card">
      <div class="pain-icon">📉</div>
      <h3>Visita mas não converte</h3>
      <p>Tráfego existe, venda não acontece. Fotos ruins, título fraco e descrição sem estrutura jogam fora cada clique que você pagou.</p>
    </div>
    <div class="pain-card">
      <div class="pain-icon">⚔️</div>
      <h3>Preso na guerra de preço</h3>
      <p>Quando o anúncio não convence sozinho, a única saída parece ser baixar o preço. E aí a margem vai por água abaixo todo mês.</p>
    </div>
    <div class="pain-card">
      <div class="pain-icon">🔁</div>
      <h3>Sem consistência nas vendas</h3>
      <p>Um dia vende, uma semana some. Sem dados, sem estratégia. As vendas ficam refém do acaso e de promoções pontuais.</p>
    </div>
    <div class="pain-card">
      <div class="pain-icon">💸</div>
      <h3>Verba em Ads sem retorno</h3>
      <p>Produto Patrocinado rodando, mas o custo por venda é maior do que o lucro. Você paga para aparecer e não recebe de volta.</p>
    </div>
    <div class="pain-card">
      <div class="pain-icon">😤</div>
      <h3>Copiado e espremido</h3>
      <p>O concorrente copia seu anúncio, coloca R$ 1 mais barato e fica na frente. Parece que não tem saída. Mas tem.</p>
    </div>
  </div>
</section>

<!-- SOLUTION -->
<section id="solution">
  <div style="text-align:center; margin-bottom: 56px;">
    <div class="section-label">A solução</div>
    <h2 class="fade-in">Como transformo<br>um anúncio parado<br>em <em>venda recorrente</em></h2>
    <p class="section-intro fade-in" style="margin-bottom:0;">Um processo estruturado, sem achismo. Aplicado em mais de 120 anúncios no Mercado Livre.</p>
  </div>
  <div class="solution-grid">
    <div>

      <div class="solution-steps fade-in">
        <div class="step">
          <span class="step-num">01</span>
          <div class="step-content">
            <h3>Diagnóstico completo do anúncio</h3>
            <p>Análise de posicionamento, palavras-chave, taxa de conversão, reputação, concorrência e performance atual dos Ads.</p>
          </div>
        </div>
        <div class="step">
          <span class="step-num">02</span>
          <div class="step-content">
            <h3>Otimização de título e SEO interno</h3>
            <p>Reestruturação do título com as palavras que seu comprador realmente pesquisa. Sem encher de lixo que o algoritmo penaliza.</p>
          </div>
        </div>
        <div class="step">
          <span class="step-num">03</span>
          <div class="step-content">
            <h3>Fotos e descrição que convertem</h3>
            <p>Roteiro de imagens e estrutura de descrição persuasiva que elimina a dúvida e empurra o cliente para o botão de compra.</p>
          </div>
        </div>
        <div class="step">
          <span class="step-num">04</span>
          <div class="step-content">
            <h3>Gestão estratégica de Produto Patrocinado</h3>
            <p>Configuração e otimização de campanhas para pagar menos por clique, aparecer para quem compra e ter ROI real.</p>
          </div>
        </div>
        <div class="step">
          <span class="step-num">05</span>
          <div class="step-content">
            <h3>Monitoramento e ajuste contínuo</h3>
            <p>Acompanhamento semanal de métricas e ajustes rápidos para manter o anúncio competitivo conforme o mercado muda.</p>
          </div>
        </div>
      </div>
    </div>

    <div class="fade-in">
      <div class="solution-card">
        <div class="solution-card-label">Resultado esperado</div>
        <div class="big-result">+3×</div>
        <div class="big-result-label">vendas sem aumentar o orçamento em Ads</div>

        <ul class="result-list">
          <li>Anúncio na primeira página do resultado orgânico</li>
          <li>Taxa de conversão acima da média da categoria</li>
          <li>Preço defendido sem precisar dar desconto</li>
          <li>Custo por venda no Produto Patrocinado reduzido</li>
          <li>Consistência: vendas todos os dias, não só em promoção</li>
          <li>Relatório claro para você saber exatamente o que está funcionando</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="section-label">Quem já passou por aqui</div>
  <h2 class="fade-in">Resultados que <em>falam por si</em></h2>
  <p class="section-intro fade-in">Vendedores reais, no mesmo mercado que você enfrenta todo dia.</p>

  <div class="testi-grid fade-in">
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text">"Estava travado há 6 meses. Em 3 semanas de otimização minhas vendas triplicaram e os resultados superaram tudo que eu esperava."</p>
      <div class="testi-author">
        <div class="testi-avatar">RC</div>
        <div>
          <div class="testi-name">Ricardo C.</div>
          <div class="testi-role">Vendedor de eletrônicos • SP</div>
        </div>
      </div>
    </div>
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text">"Achei que meu problema era preço. Era o anúncio mesmo. Depois que conheci a Pandora Studio parei de brigar por centavo e ainda melhorei a margem."</p>
      <div class="testi-author">
        <div class="testi-avatar">FM</div>
        <div>
          <div class="testi-name">Fernanda M.</div>
          <div class="testi-role">Loja de casa e decoração • MG</div>
        </div>
      </div>
    </div>
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text">"Nunca imaginei que o problema estava na apresentação do produto. A Pandora Studio virou o jogo em menos de um mês. Hoje vendo todos os dias sem precisar fazer promoção."</p>
      <div class="testi-author">
        <div class="testi-avatar">LP</div>
        <div>
          <div class="testi-name">Lucas P.</div>
          <div class="testi-role">Loja de moda • PR</div>
        </div>
      </div>
    </div>
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text">"Produto Patrocinado que eu rodava há meses sem retorno ficou lucrativo em menos de 30 dias. Metodologia clara, resultado de verdade."</p>
      <div class="testi-author">
        <div class="testi-avatar">AT</div>
        <div>
          <div class="testi-name">André T.</div>
          <div class="testi-role">Vendedor de ferramentas • RS</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PARA QUEM -->
<section id="para-quem">
  <div class="section-label">Para quem é isso</div>
  <h2 class="fade-in">Esse serviço foi feito <em>para você</em> se...</h2>

  <div class="who-grid fade-in">
    <div class="who-card">
      <div class="who-check">✓</div>
      <h3>Você já vende no ML</h3>
      <p>Tem produtos ativos mas as vendas estão abaixo do que você sabe que podem ser.</p>
    </div>
    <div class="who-card">
      <div class="who-check">✓</div>
      <h3>Está preso na guerra de preço</h3>
      <p>Sempre tem alguém mais barato e você não aguenta mais baixar margem para competir.</p>
    </div>
    <div class="who-card">
      <div class="who-check">✓</div>
      <h3>Gastou com Ads sem resultado</h3>
      <p>Investiu em Produto Patrocinado, mas o custo por venda não fecha. Quer fazer isso funcionar.</p>
    </div>
    <div class="who-card">
      <div class="who-check">✓</div>
      <h3>Quer crescer sem contratar</h3>
      <p>Não quer montar um time de marketing. Quer delegar e ver resultado sem complicação.</p>
    </div>
  </div>
</section>

<!-- CTA -->
<section id="cta">
  <div class="inner">
    <div class="section-label">Próximo passo</div>
    <h2 class="fade-in">Chega de anúncio<br>que <em>não vende.</em></h2>
    <p class="section-intro fade-in">Preencha abaixo para um diagnóstico gratuito do seu anúncio. Você será redirecionado para o nosso WhatsApp.</p>

    <div class="form-wrap fade-in" id="form">
      <div class="form-title">Diagnóstico gratuito</div>
      <p class="form-sub">Sem compromisso. Vejo seu anúncio e te digo o que pode melhorar.</p>

      <div class="form-group">
        <label>Seu nome</label>
        <input type="text" placeholder="João Silva">
      </div>
      <div class="form-group">
        <label>WhatsApp</label>
        <input type="tel" placeholder="(11) 99999-9999">
      </div>
      <div class="form-group">
        <label>Link do seu anúncio no ML</label>
        <input type="url" placeholder="https://mercadolivre.com.br/...">
      </div>
      <div class="form-group">
        <label>Qual é o seu maior problema hoje?</label>
        <select>
          <option value="">Selecione...</option>
          <option>Pouca visibilidade / ninguém encontra</option>
          <option>Visitas mas sem conversão</option>
          <option>Guerra de preço / perco para mais baratos</option>
          <option>Produto Patrocinado sem retorno</option>
          <option>Vendas inconsistentes / sem previsibilidade</option>
        </select>
      </div>
      <button class="btn-submit">Quero meu diagnóstico gratuito →</button>
      <p class="form-footer">🔒 Seus dados estão seguros. Sem spam, sem enrolação.</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="logo">Pandora <span>Studio</span></div>
  <p>© 2025 Pandora Studio · Especialista em Neurodesign · Todos os direitos reservados</p>
</footer>

<script>
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        obs.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));

  // cole sua URL aqui apos o passo 5 do tutorial
  const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbz7OE08wmNfJ8kl1VWtu6rRzLqu9ARVVUX5eERkRweMJioBqV47UztnPOOayBpY5rm4VA/exec';
  const WA_URL = 'https://api.whatsapp.com/message/CNX7FWROAMBJP1?autoload=1&app_absent=0';

  document.querySelector('.btn-submit').addEventListener('click', async function(e) {
    e.preventDefault();
    const btn = this;
    const nome     = document.querySelector('input[type="text"]').value.trim();
    const whatsapp = document.querySelector('input[type="tel"]').value.trim();
    const link     = document.querySelector('input[type="url"]').value.trim();
    const problema = document.querySelector('select').value;

    if (!nome || !whatsapp) {
      alert('Por favor, preencha seu nome e WhatsApp.');
      return;
    }

    btn.textContent = 'Enviando...';
    btn.disabled = true;

    const body = new FormData();
    body.append('nome', nome);
    body.append('whatsapp', whatsapp);
    body.append('link', link);
    body.append('problema', problema);

    try { await fetch(SCRIPT_URL, { method: 'POST', body }); } catch (_) {}

    btn.textContent = 'Redirecionando para o WhatsApp...';
    btn.style.background = '#1a7a4a';
    btn.style.color = '#fff';
    setTimeout(() => window.open(WA_URL, '_blank'), 800);
  });
</script>
</body>
</html>
