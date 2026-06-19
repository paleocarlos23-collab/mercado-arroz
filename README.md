<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mercado Arroz - Conectando Produtores e Indústrias</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/purchases.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
</head>
<body>
    <!-- ============================================ -->
    <!-- LANDING PAGE -->
    <!-- ============================================ -->
    <div id="page-landing" class="page active">
        <!-- Navbar Landing -->
        <nav class="navbar-landing">
            <div class="container navbar-content">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <div class="nav-links">
                    <a href="#beneficios">Benefícios</a>
                    <a href="#como-funciona">Como Funciona</a>
                    <a href="#contato">Contato</a>
                    <button class="btn-secondary" onclick="app.navigateTo('login')">Entrar</button>
                    <button class="btn-primary" onclick="app.navigateTo('register')">Cadastrar</button>
                </div>
                <button class="mobile-menu-toggle" onclick="toggleMobileMenu()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </nav>

        <!-- Mobile Menu -->
        <div class="mobile-menu" id="mobileMenu">
            <div class="mobile-menu-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="close-mobile-menu" onclick="toggleMobileMenu()">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            <div class="mobile-menu-links">
                <a href="#beneficios" onclick="toggleMobileMenu()">Benefícios</a>
                <a href="#como-funciona" onclick="toggleMobileMenu()">Como Funciona</a>
                <a href="#contato" onclick="toggleMobileMenu()">Contato</a>
                <button class="btn-secondary btn-block" onclick="app.navigateTo('login')">Entrar</button>
                <button class="btn-primary btn-block" onclick="app.navigateTo('register')">Cadastrar</button>
            </div>
        </div>

        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h1 class="hero-title">Conectando <span class="highlight">produtores</span> e <span class="highlight">indústrias</span> de arroz</h1>
                    <p class="hero-subtitle">A plataforma que facilita a negociação de arroz em casca direto da lavoura para a indústria. Transparência, segurança e agilidade em um só lugar.</p>
                    <div class="hero-buttons">
                        <button class="btn-primary btn-lg" onclick="app.navigateTo('register')">
                            <i class="fas fa-rocket"></i> Comece Agora
                        </button>
                        <button class="btn-secondary btn-lg" onclick="scrollToSection('como-funciona')">
                            <i class="fas fa-play-circle"></i> Como Funciona
                        </button>
                    </div>
                    <div class="hero-stats">
                        <div class="stat">
                            <div class="stat-number">500+</div>
                            <div class="stat-label">Produtores Cadastrados</div>
                        </div>
                        <div class="stat">
                            <div class="stat-number">150+</div>
                            <div class="stat-label">Indústrias Ativas</div>
                        </div>
                        <div class="stat">
                            <div class="stat-number">25.000</div>
                            <div class="stat-label">Toneladas Negociadas</div>
                        </div>
                    </div>
                    <div class="hero-cards">
                        <div class="hero-card floating">
                            <i class="fas fa-chart-line"></i>
                            <div>
                                <div class="card-title">Preço Médio</div>
                                <div class="card-value">R$ 85,50/saca</div>
                            </div>
                        </div>
                        <div class="hero-card floating" style="animation-delay: 0.5s;">
                            <i class="fas fa-handshake"></i>
                            <div>
                                <div class="card-title">Negócios Hoje</div>
                                <div class="card-value">47 fechados</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Benefits Section -->
        <section id="beneficios" class="section-benefits">
            <div class="container">
                <div class="section-header">
                    <h2 class="section-title">Por que usar o Mercado Arroz?</h2>
                    <p class="section-subtitle">A solução completa para compra e venda de arroz em casca</p>
                </div>
                <div class="benefits-grid">
                    <div class="benefit-card">
                        <div class="benefit-icon">
                            <i class="fas fa-search-dollar"></i>
                        </div>
                        <h3>Transparência de Preços</h3>
                        <p>Acompanhe o índice de preços em tempo real e tome decisões com base em dados de mercado</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>Segurança nas Transações</h3>
                        <p>Sistema de avaliações e perfis verificados garantem confiança nas negociações</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-icon">
                            <i class="fas fa-map-marked-alt"></i>
                        </div>
                        <h3>Localização Geográfica</h3>
                        <p>Visualize ofertas no mapa e calcule distâncias para otimizar a logística</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-icon">
                            <i class="fas fa-comments"></i>
                        </div>
                        <h3>Negociação Direta</h3>
                        <p>Chat integrado para negociar valores, prazos e condições de entrega</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <h3>Agilidade</h3>
                        <p>Encontre compradores ou ofertas em minutos, sem intermediários</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-icon">
                            <i class="fas fa-chart-bar"></i>
                        </div>
                        <h3>Relatórios Completos</h3>
                        <p>Dashboard com métricas de vendas, compras e histórico de negociações</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- How it Works -->
        <section id="como-funciona" class="section-how-it-works">
            <div class="container">
                <div class="section-header">
                    <h2 class="section-title">Como Funciona</h2>
                    <p class="section-subtitle">Processo simples em 4 passos</p>
                </div>
                
                <!-- For Producers -->
                <div class="process-wrapper">
                    <h3 class="process-type"><i class="fas fa-tractor"></i> Para Produtores</h3>
                    <div class="process-steps">
                        <div class="step">
                            <div class="step-number">1</div>
                            <div class="step-content">
                                <h4>Cadastre-se</h4>
                                <p>Crie sua conta gratuita com CPF/CNPJ e informações da propriedade</p>
                            </div>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <div class="step-content">
                                <h4>Publique sua Oferta</h4>
                                <p>Informe quantidade, qualidade, umidade, preço e localização do arroz</p>
                            </div>
                        </div>
                        <div class="step">
                            <div class="step-number">3</div>
                            <div class="step-content">
                                <h4>Receba Propostas</h4>
                                <p>Indústrias interessadas entram em contato e fazem propostas</p>
                            </div>
                        </div>
                        <div class="step">
                            <div class="step-number">4</div>
                            <div class="step-content">
                                <h4>Feche o Negócio</h4>
                                <p>Negocie valores, prazos e confirme a venda direto na plataforma</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- For Industries -->
                <div class="process-wrapper">
                    <h3 class="process-type"><i class="fas fa-industry"></i> Para Indústrias</h3>
                    <div class="process-steps">
                        <div class="step">
                            <div class="step-number">1</div>
                            <div class="step-content">
                                <h4>Cadastre-se</h4>
                                <p>Registre sua empresa com CNPJ e informações da unidade industrial</p>
                            </div>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <div class="step-content">
                                <h4>Busque Ofertas</h4>
                                <p>Use filtros avançados por região, preço, qualidade e quantidade</p>
                            </div>
                        </div>
                        <div class="step">
                            <div class="step-number">3</div>
                            <div class="step-content">
                                <h4>Entre em Contato</h4>
                                <p>Converse diretamente com o produtor via chat integrado</p>
                            </div>
                        </div>
                        <div class="step">
                            <div class="step-number">4</div>
                            <div class="step-content">
                                <h4>Confirme a Compra</h4>
                                <p>Acerte detalhes e finalize a negociação com segurança</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <section class="section-cta">
            <div class="container">
                <div class="cta-content">
                    <h2>Pronto para começar?</h2>
                    <p>Cadastre-se gratuitamente e faça parte da maior plataforma de negociação de arroz do Brasil</p>
                    <button class="btn-primary btn-lg" onclick="app.navigateTo('register')">
                        <i class="fas fa-user-plus"></i> Criar Conta Grátis
                    </button>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="footer">
            <div class="container">
                <div class="footer-content">
                    <div class="footer-section">
                        <div class="logo">
                            <div class="logo-icon">
                                <i class="fas fa-seedling"></i>
                            </div>
                            <div class="logo-text">
                                <span class="logo-name">mercado</span>
                                <span class="logo-name">arroz</span>
                            </div>
                        </div>
                        <p>Conectando o campo à indústria com tecnologia e transparência</p>
                    </div>
                    <div class="footer-section">
                        <h4>Plataforma</h4>
                        <ul>
                            <li><a href="#beneficios">Benefícios</a></li>
                            <li><a href="#como-funciona">Como Funciona</a></li>
                            <li><a href="#" onclick="app.navigateTo('register')">Cadastre-se</a></li>
                        </ul>
                    </div>
                    <div class="footer-section">
                        <h4>Suporte</h4>
                        <ul>
                            <li><a href="#">Central de Ajuda</a></li>
                            <li><a href="#">Termos de Uso</a></li>
                            <li><a href="#">Política de Privacidade</a></li>
                        </ul>
                    </div>
                    <div class="footer-section">
                        <h4 id="contato">Contato</h4>
                        <ul>
                            <li><i class="fas fa-envelope"></i> contato@mercadoarroz.com.br</li>
                            <li><i class="fas fa-phone"></i> (51) 3000-0000</li>
                            <li><i class="fas fa-map-marker-alt"></i> Porto Alegre, RS</li>
                        </ul>
                    </div>
                </div>
                <div class="footer-bottom">
                    <p>&copy; 2026 Mercado Arroz. Todos os direitos reservados.</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- ============================================ -->
    <!-- LOGIN PAGE -->
    <!-- ============================================ -->
    <div id="page-login" class="page page-auth">
        <div class="auth-container">
            <div class="auth-left">
                <div class="auth-branding">
                    <div class="logo large">
                        <div class="logo-icon">
                            <i class="fas fa-seedling"></i>
                        </div>
                        <div class="logo-text">
                            <span class="logo-name">mercado</span>
                            <span class="logo-name">arroz</span>
                        </div>
                    </div>
                    <h2>Bem-vindo de volta!</h2>
                    <p>Conectando produtores e indústrias de arroz com tecnologia e transparência</p>
                </div>
            </div>
            <div class="auth-right">
                <div class="auth-form-container">
                    <button class="back-button" onclick="navigateTo('landing')">
                        <i class="fas fa-arrow-left"></i> Voltar
                    </button>
                    <h2>Entrar na sua conta</h2>
                    <p class="auth-subtitle">Acesse seu painel e gerencie suas negociações</p>
                    
                    <form id="loginForm" onsubmit="handleLogin(event)" class="auth-form">
                        <div class="form-group">
                            <label for="loginEmail">E-mail ou CPF/CNPJ</label>
                            <input type="text" id="loginEmail" required placeholder="Digite seu e-mail ou documento">
                        </div>
                        <div class="form-group">
                            <label for="loginPassword">Senha</label>
                            <input type="password" id="loginPassword" required placeholder="Digite sua senha">
                        </div>
                        <div class="form-row space-between">
                            <label class="checkbox-label">
                                <input type="checkbox" id="rememberMe">
                                <span>Lembrar de mim</span>
                            </label>
                            <a href="#" class="link-primary">Esqueci minha senha</a>
                        </div>
                        <button type="submit" class="btn-primary btn-block btn-lg">
                            <i class="fas fa-sign-in-alt"></i> Entrar
                        </button>
                    </form>

                    <div class="auth-divider">
                        <span>ou</span>
                    </div>

                    <div class="social-login">
                        <button class="btn-social">
                            <i class="fab fa-google"></i> Continuar com Google
                        </button>
                    </div>

                    <p class="auth-switch">
                        Não tem uma conta? <a href="#" onclick="navigateTo('register')" class="link-primary">Cadastre-se</a>
                    </p>
                </div>
            </div>
        </div>
    </div>

    <!-- ============================================ -->
    <!-- REGISTER PAGE -->
    <!-- ============================================ -->
    <div id="page-register" class="page page-auth">
        <div class="auth-container">
            <div class="auth-left">
                <div class="auth-branding">
                    <div class="logo large">
                        <div class="logo-icon">
                            <i class="fas fa-seedling"></i>
                        </div>
                        <div class="logo-text">
                            <span class="logo-name">mercado</span>
                            <span class="logo-name">arroz</span>
                        </div>
                    </div>
                    <h2>Junte-se ao Mercado Arroz</h2>
                    <p>Crie sua conta gratuitamente e comece a negociar arroz em casca com segurança e transparência</p>
                </div>
            </div>
            <div class="auth-right">
                <div class="auth-form-container">
                    <button class="back-button" onclick="navigateTo('landing')">
                        <i class="fas fa-arrow-left"></i> Voltar
                    </button>
                    <h2>Criar nova conta</h2>
                    <p class="auth-subtitle">Preencha os dados abaixo para começar</p>
                    
                    <form id="registerForm" onsubmit="handleRegister(event)" class="auth-form">
                        <div class="form-group">
                            <label>Tipo de Usuário</label>
                            <div class="user-type-selector">
                                <label class="user-type-option">
                                    <input type="radio" name="userType" value="producer" required checked>
                                    <div class="user-type-card">
                                        <i class="fas fa-tractor"></i>
                                        <span>Produtor</span>
                                    </div>
                                </label>
                                <label class="user-type-option">
                                    <input type="radio" name="userType" value="industry" required>
                                    <div class="user-type-card">
                                        <i class="fas fa-industry"></i>
                                        <span>Indústria</span>
                                    </div>
                                </label>
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="registerName">Nome Completo / Razão Social</label>
                            <input type="text" id="registerName" required placeholder="Digite seu nome">
                        </div>
                        <div class="form-group">
                            <label for="registerDocument">CPF / CNPJ</label>
                            <input type="text" id="registerDocument" required placeholder="000.000.000-00">
                        </div>
                        <div class="form-group">
                            <label for="registerEmail">E-mail</label>
                            <input type="email" id="registerEmail" required placeholder="seuemail@exemplo.com">
                        </div>
                        <div class="form-group">
                            <label for="registerPhone">Telefone</label>
                            <input type="tel" id="registerPhone" required placeholder="(00) 00000-0000">
                        </div>
                        <div class="form-group">
                            <label for="registerPassword">Senha</label>
                            <input type="password" id="registerPassword" required placeholder="Mínimo 8 caracteres">
                        </div>
                        <div class="form-group">
                            <label class="checkbox-label">
                                <input type="checkbox" id="acceptTerms" required>
                                <span>Concordo com os <a href="#" class="link-primary">Termos de Uso</a> e <a href="#" class="link-primary">Política de Privacidade</a></span>
                            </label>
                        </div>
                        <button type="submit" class="btn-primary btn-block btn-lg">
                            <i class="fas fa-user-plus"></i> Criar Conta
                        </button>
                    </form>

                    <p class="auth-switch">
                        Já tem uma conta? <a href="#" onclick="navigateTo('login')" class="link-primary">Entrar</a>
                    </p>
                </div>
            </div>
        </div>
    </div>

    <!-- ============================================ -->
    <!-- DASHBOARD PRODUCER -->
    <!-- ============================================ -->
    <div id="page-dashboard-producer" class="page page-dashboard">
        <!-- Sidebar -->
        <aside class="sidebar" id="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item active" data-page="dashboard-producer">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item" data-page="active-industries">
                    <i class="fas fa-industry"></i>
                    <span>Indústrias Ativas</span>
                </a>
                <a href="#" class="nav-item" data-page="my-offers">
                    <i class="fas fa-box"></i>
                    <span>Minhas Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="create-offer">
                    <i class="fas fa-plus-circle"></i>
                    <span>Nova Oferta</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">5</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="main-content">
            <!-- Topbar -->
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Dashboard</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button" onclick="toggleNotifications()">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name" id="currentUserName">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <!-- Dashboard Content -->
            <div class="content-wrapper">
                <!-- Stats Cards -->
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-icon green">
                            <i class="fas fa-box"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Ofertas Ativas</span>
                            <span class="stat-value">8</span>
                            <span class="stat-change positive">
                                <i class="fas fa-arrow-up"></i> 2 esta semana
                            </span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon yellow">
                            <i class="fas fa-handshake"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Negociações</span>
                            <span class="stat-value">15</span>
                            <span class="stat-change positive">
                                <i class="fas fa-arrow-up"></i> 3 novas
                            </span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon blue">
                            <i class="fas fa-check-circle"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Vendas Concluídas</span>
                            <span class="stat-value">47</span>
                            <span class="stat-change neutral">Este ano</span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon gold">
                            <i class="fas fa-dollar-sign"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Receita Total</span>
                            <span class="stat-value">R$ 825.400</span>
                            <span class="stat-change positive">
                                <i class="fas fa-arrow-up"></i> 12% vs mês anterior
                            </span>
                        </div>
                    </div>
                </div>

                <!-- Indicators and Chart Row -->
<div class="charts-row">
                    <!-- Economic Indicators -->
                    <div class="chart-card">
                        <div class="card-header">
                            <h3><i class="fas fa-chart-line"></i> Indicadores de Mercado</h3>
                        </div>
                        <div style="padding: 1.5rem; display: flex; flex-direction: column; gap: 1rem;">
                            <!-- Cotação do Dólar -->
                            <div style="background: linear-gradient(135deg, #2196F3 0%, #42A5F5 100%); border-radius: var(--radius-lg); padding: 1.25rem; color: white; box-shadow: 0 4px 12px rgba(33, 150, 243, 0.3);">
                                <div style="display: flex; align-items: center; justify-content: space-between; margin-bottom: 0.75rem;">
                                    <div style="display: flex; align-items: center; gap: 0.5rem;">
                                        <i class="fas fa-dollar-sign" style="font-size: 1.5rem; opacity: 0.9;"></i>
                                        <div>
                                            <div style="font-size: 0.813rem; opacity: 0.9;">Cotação do Dólar</div>
                                            <div style="font-size: 0.688rem; opacity: 0.8;">USD / BRL</div>
                                        </div>
                                    </div>
                                    <div style="text-align: right;">
                                        <div style="font-size: 1.75rem; font-weight: 700; line-height: 1;" id="usdPrice">R$ 5,89</div>
                                        <div style="font-size: 0.75rem; margin-top: 0.25rem; opacity: 0.9;" id="usdChange">
                                            <i class="fas fa-arrow-down"></i> -0,8% hoje
                                        </div>
                                    </div>
                                </div>
                                <div style="font-size: 0.688rem; opacity: 0.8; border-top: 1px solid rgba(255,255,255,0.2); padding-top: 0.5rem;">
                                    <i class="fas fa-clock"></i> <span id="usdTime">Atualizado às 15:30</span>
                                </div>
                            </div>

                            <!-- Clima -->
                            <div style="background: linear-gradient(135deg, #FF9800 0%, #FFB74D 100%); border-radius: var(--radius-lg); padding: 1.25rem; color: white; box-shadow: 0 4px 12px rgba(255, 152, 0, 0.3);">
                                <div style="display: flex; align-items: center; justify-content: space-between; margin-bottom: 0.75rem;">
                                    <div style="display: flex; align-items: center; gap: 0.5rem;">
                                        <i class="fas fa-cloud-sun" style="font-size: 1.5rem; opacity: 0.9;"></i>
                                        <div>
                                            <div style="font-size: 0.813rem; opacity: 0.9;">Clima Pelotas/RS</div>
                                            <div style="font-size: 0.688rem; opacity: 0.8;">Previsão 7 dias</div>
                                        </div>
                                    </div>
                                    <div style="text-align: right;">
                                        <div style="font-size: 1.75rem; font-weight: 700; line-height: 1;" id="weatherTemp">24°C</div>
                                        <div style="font-size: 0.75rem; margin-top: 0.25rem; opacity: 0.9;" id="weatherRain">
                                            <i class="fas fa-tint"></i> 60% chuva
                                        </div>
                                    </div>
                                </div>
                                <div style="font-size: 0.688rem; opacity: 0.8; border-top: 1px solid rgba(255,255,255,0.2); padding-top: 0.5rem;">
                                    <i class="fas fa-info-circle"></i> <span id="weatherCondition">Condições favoráveis para colheita</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Recent Activities -->
                <div class="card">
                    <div class="card-header">
                        <h3>Atividades Recentes</h3>
                        <a href="#" class="link-primary">Ver todas</a>
                    </div>
                    <div class="activity-list">
                        <div class="activity-item">
                            <div class="activity-icon green">
                                <i class="fas fa-plus"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Nova oferta publicada</strong></p>
                                <p class="activity-detail">IRGA 424 - 500 sacas - R$ 88,00/saca</p>
                                <span class="activity-time">Há 2 horas</span>
                            </div>
                        </div>
                        <div class="activity-item">
                            <div class="activity-icon yellow">
                                <i class="fas fa-comment"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Nova mensagem</strong></p>
                                <p class="activity-detail">Indústria Riz S.A. enviou uma mensagem sobre sua oferta</p>
                                <span class="activity-time">Há 4 horas</span>
                            </div>
                        </div>
                        <div class="activity-item">
                            <div class="activity-icon blue">
                                <i class="fas fa-file-alt"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Proposta recebida</strong></p>
                                <p class="activity-detail">Indústria Arroz Nobre propôs R$ 86,50/saca para 300 sacas</p>
                                <span class="activity-time">Ontem às 15:30</span>
                            </div>
                        </div>
                        <div class="activity-item">
                            <div class="activity-icon green">
                                <i class="fas fa-check-circle"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Venda concluída</strong></p>
                                <p class="activity-detail">Negociação #4521 finalizada - 400 sacas vendidas</p>
                                <span class="activity-time">2 dias atrás</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- ACTIVE INDUSTRIES PAGE -->
    <!-- ============================================ -->
    <div id="page-active-industries" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item" data-page="dashboard-producer">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item active" data-page="active-industries">
                    <i class="fas fa-industry"></i>
                    <span>Indústrias Ativas</span>
                </a>
                <a href="#" class="nav-item" data-page="my-offers">
                    <i class="fas fa-box"></i>
                    <span>Minhas Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="create-offer">
                    <i class="fas fa-plus-circle"></i>
                    <span>Nova Oferta</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">5</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Indústrias Ativas no Mercado</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button" onclick="toggleNotifications()">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Info Card -->
                <div style="background: linear-gradient(135deg, var(--color-primary), var(--color-secondary)); color: white; padding: 2rem; border-radius: var(--radius-lg); margin-bottom: 2rem; box-shadow: var(--shadow-md);">
                    <h2 style="font-size: 1.5rem; margin-bottom: 0.5rem;">
                        <i class="fas fa-info-circle"></i> Encontre Compradores
                    </h2>
                    <p style="margin: 0; opacity: 0.95;">
                        Veja quais indústrias estão ativas no mercado e prontas para negociar. 
                        Clique em "Enviar Mensagem" para iniciar uma conversa direta!
                    </p>
                </div>

                <!-- Filter and View Options -->
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 2rem; flex-wrap: wrap; gap: 1rem;">
                    <!-- Filter Tabs -->
                    <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                        <button class="btn-primary" onclick="app.filterIndustries('all')">
                            <i class="fas fa-list"></i> Todas
                        </button>
                        <button class="btn-secondary" onclick="app.filterIndustries('active')">
                            <i class="fas fa-check-circle"></i> Ativas
                        </button>
                        <button class="btn-secondary" onclick="app.filterIndustries('inactive')">
                            <i class="fas fa-times-circle"></i> Inativas
                        </button>
                    </div>
                    
                    <!-- View Toggle -->
                    <div style="display: flex; gap: 0.5rem; background: var(--color-gray-100); padding: 0.25rem; border-radius: var(--radius-md);">
                        <button class="view-toggle-btn active" onclick="toggleIndustriesView('grid')" data-view="grid" title="Visualização em Grade">
                            <i class="fas fa-th"></i>
                        </button>
                        <button class="view-toggle-btn" onclick="toggleIndustriesView('list')" data-view="list" title="Visualização em Lista">
                            <i class="fas fa-list"></i>
                        </button>
                    </div>
                </div>

                <!-- Industries Grid -->
                <div class="industries-grid" id="industriesGrid">
                    <!-- Industry 1 - ATIVA -->
                    <div class="industry-card active">
                        <div class="industry-logo">
                            <i class="fas fa-industry"></i>
                        </div>
                        <div class="industry-info">
                            <h3>Indústria Riz S.A.</h3>
                            <p class="industry-location">
                                <i class="fas fa-map-marker-alt"></i> Porto Alegre, RS
                            </p>
                            <p class="industry-capacity">
                                <i class="fas fa-box"></i> Capacidade: 5.000 ton/mês
                            </p>
                            <div class="industry-varieties">
                                <span class="variety-tag">IRGA 424</span>
                                <span class="variety-tag">IRGA 424 RI</span>
                                <span class="variety-tag">GURI INTA CL</span>
                            </div>
                            <div class="industry-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span>4.9 (156 avaliações)</span>
                            </div>
                        </div>
                        <div class="industry-status active-status">
                            <i class="fas fa-circle"></i> Ativa no Mercado
                        </div>
                        <div class="industry-actions">
                            <button class="btn-primary btn-block" onclick="app.sendMessageToIndustry('user_2')">
                                <i class="fas fa-paper-plane"></i> Enviar Mensagem
                            </button>
                            <button class="btn-secondary btn-block" onclick="app.viewIndustryProfile('user_2')">
                                <i class="fas fa-info-circle"></i> Ver Perfil
                            </button>
                        </div>
                    </div>

                    <!-- Industry 2 - ATIVA -->
                    <div class="industry-card active">
                        <div class="industry-logo">
                            <i class="fas fa-building"></i>
                        </div>
                        <div class="industry-info">
                            <h3>Arroz Nobre Ltda.</h3>
                            <p class="industry-location">
                                <i class="fas fa-map-marker-alt"></i> Pelotas, RS
                            </p>
                            <p class="industry-capacity">
                                <i class="fas fa-box"></i> Capacidade: 3.500 ton/mês
                            </p>
                            <div class="industry-varieties">
                                <span class="variety-tag">IRGA 424</span>
                                <span class="variety-tag">BR-IRGA 409</span>
                            </div>
                            <div class="industry-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                                <span>4.7 (89 avaliações)</span>
                            </div>
                        </div>
                        <div class="industry-status active-status">
                            <i class="fas fa-circle"></i> Ativa no Mercado
                        </div>
                        <div class="industry-actions">
                            <button class="btn-primary btn-block" onclick="app.sendMessageToIndustry('user_4')">
                                <i class="fas fa-paper-plane"></i> Enviar Mensagem
                            </button>
                            <button class="btn-secondary btn-block" onclick="app.viewIndustryProfile('user_4')">
                                <i class="fas fa-info-circle"></i> Ver Perfil
                            </button>
                        </div>
                    </div>

                    <!-- Industry 3 - INATIVA -->
                    <div class="industry-card inactive">
                        <div class="industry-logo inactive">
                            <i class="fas fa-warehouse"></i>
                        </div>
                        <div class="industry-info">
                            <h3>Beneficiadora Sul</h3>
                            <p class="industry-location">
                                <i class="fas fa-map-marker-alt"></i> Santa Maria, RS
                            </p>
                            <p class="industry-capacity">
                                <i class="fas fa-box"></i> Capacidade: 2.000 ton/mês
                            </p>
                            <div class="industry-varieties">
                                <span class="variety-tag">IRGA 424</span>
                                <span class="variety-tag">IRGA 424 RI</span>
                            </div>
                            <div class="industry-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="far fa-star"></i>
                                <span>4.2 (45 avaliações)</span>
                            </div>
                        </div>
                        <div class="industry-status inactive-status">
                            <i class="fas fa-circle"></i> Inativa no Momento
                        </div>
                        <div class="industry-actions">
                            <button class="btn-secondary btn-block" disabled style="opacity: 0.5; cursor: not-allowed;">
                                <i class="fas fa-ban"></i> Indisponível para Contato
                            </button>
                            <button class="btn-secondary btn-block" onclick="app.viewIndustryProfile('user_5')">
                                <i class="fas fa-info-circle"></i> Ver Perfil
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- CREATE OFFER PAGE -->
    <!-- ============================================ -->
    <div id="page-create-offer" class="page page-dashboard">
        <aside class="sidebar" id="sidebar-create-offer">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item" data-page="dashboard-producer">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item" data-page="active-industries">
                    <i class="fas fa-industry"></i>
                    <span>Indústrias Ativas</span>
                </a>
                <a href="#" class="nav-item" data-page="my-offers">
                    <i class="fas fa-box"></i>
                    <span>Minhas Ofertas</span>
                </a>
                <a href="#" class="nav-item active" data-page="create-offer">
                    <i class="fas fa-plus-circle"></i>
                    <span>Nova Oferta</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">5</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Nova Oferta</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <div class="form-container">
                    <div class="form-header">
                        <h2>Publicar Nova Oferta de Arroz</h2>
                        <p>Preencha as informações abaixo para disponibilizar sua oferta no mercado</p>
                    </div>

                    <form id="createOfferForm" onsubmit="handleCreateOffer(event)" class="offer-form">
                        <!-- Step 1: Product Info -->
                        <div class="form-section">
                            <h3><i class="fas fa-info-circle"></i> Informações do Produto</h3>
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="offerVariety">Variedade do Arroz *</label>
                                    <select id="offerVariety" required>
                                        <option value="">Selecione...</option>
                                        <option value="IRGA 424">IRGA 424</option>
                                        <option value="IRGA 424 RI">IRGA 424 RI</option>
                                        <option value="GURI INTA CL">GURI INTA CL</option>
                                        <option value="BR-IRGA 409">BR-IRGA 409</option>
                                        <option value="BRS Pampeira">BRS Pampeira</option>
                                        <option value="MISTURA VARIETAL">MISTURA VARIETAL</option>
                                        <option value="PAMPA">PAMPA</option>
                                        <option value="HIBRIDO">HIBRIDO</option>
                                        <option value="Outros">Outros</option>
                                    </select>
                                </div>
                                <div class="form-group">
                                    <label for="offerType">Classificação *</label>
                                    <select id="offerType" required>
                                        <option value="">Selecione...</option>
                                        <option value="62X10 - BRANCO RENDA ALTA">62X10 - BRANCO RENDA ALTA</option>
                                        <option value="60X8 - BRANCO">60X8 - BRANCO</option>
                                        <option value="55X15 - PARBOLIZADO">55X15 - PARBOLIZADO</option>
                                        <option value="50X18 PARBO FRACO">50X18 PARBO FRACO</option>
                                    </select>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="offerQuantity">Quantidade Disponível *</label>
                                    <select id="offerQuantity" required>
                                        <option value="">Selecione...</option>
                                        <option value="5000-10000">5 a 10 mil sacos</option>
                                        <option value="10000-20000">10 a 20 mil sacos</option>
                                        <option value="20000-30000">20 a 30 mil sacos</option>
                                        <option value="30000+">+ 30 mil sacos</option>
                                    </select>
                                </div>
                                <div class="form-group">
                                    <label for="offerUnit">Unidade *</label>
                                    <input type="text" id="offerUnit" value="Sacas (50kg)" readonly style="background-color: var(--color-gray-100); cursor: not-allowed;">
                                </div>
                                <div class="form-group">
                                    <label for="offerHumidity">Umidade *</label>
                                    <select id="offerHumidity" required>
                                        <option value="">Selecione...</option>
                                        <option value="SECO">SECO</option>
                                        <option value="PRÉ-SECO">PRÉ-SECO</option>
                                        <option value="VERDE">VERDE</option>
                                    </select>
                                </div>
                            </div>
                        </div>

                        <!-- Step 2: Pricing -->
                        <div class="form-section">
                            <h3><i class="fas fa-dollar-sign"></i> Precificação</h3>
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="offerPrice">Preço por Saca (R$) *</label>
                                    <input type="text" id="offerPrice" required placeholder="Ex: 85,50" oninput="formatPriceInput(this)">
                                    <small class="form-help">Preço médio no mercado: R$ 82,00 - R$ 90,00</small>
                                </div>
                                <div class="form-group">
                                    <label for="offerNegotiable">Negociável?</label>
                                    <select id="offerNegotiable">
                                        <option value="sim">Sim, aceito propostas</option>
                                        <option value="nao">Não, preço fixo</option>
                                    </select>
                                </div>
                            </div>
                            <div class="form-group">
                                <label>
                                    <input type="checkbox" id="offerPartialSale">
                                    Aceito venda parcial (quantidade menor que o total)
                                </label>
                            </div>
                        </div>

                        <!-- Step 3: Location -->
                        <div class="form-section">
                            <h3><i class="fas fa-map-marker-alt"></i> Localização e Logística</h3>
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="offerCity">Cidade *</label>
                                    <input type="text" id="offerCity" required placeholder="Ex: Cachoeira do Sul">
                                </div>
                                <div class="form-group">
                                    <label for="offerState">Estado *</label>
                                    <select id="offerState" required>
                                        <option value="RS">Rio Grande do Sul</option>
                                        <option value="SC">Santa Catarina</option>
                                        <option value="PR">Paraná</option>
                                    </select>
                                </div>
                            </div>
                            <div class="form-group">
                                <label for="offerFreight">Frete *</label>
                                <select id="offerFreight" required>
                                    <option value="FOB">FOB - Comprador retira na propriedade</option>
                                    <option value="CIF">CIF - Vendedor entrega no destino</option>
                                    <option value="Negociavel">Negociável</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label>
                                    <input type="checkbox" id="offerHasTransport">
                                    Possuo transporte próprio disponível
                                </label>
                            </div>
                        </div>

                        <!-- Step 4: Additional Info -->
                        <div class="form-section">
                            <h3><i class="fas fa-file-alt"></i> Informações Adicionais</h3>
                            <div class="form-group">
                                <label for="offerDescription">Observações</label>
                                <textarea id="offerDescription" rows="4" placeholder="Adicione informações relevantes sobre a oferta (presença de avarias, lote específico, disponibilidade para visita, etc.)"></textarea>
                            </div>
                            <div class="form-group">
                                <label for="offerExpiration">Validade da Oferta *</label>
                                <select id="offerExpiration" required>
                                    <option value="">Selecione...</option>
                                    <option value="3">3 dias</option>
                                    <option value="7">7 dias</option>
                                    <option value="15">15 dias</option>
                                    <option value="30">30 dias</option>
                                </select>
                                <small class="form-help">Você receberá um lembrete 1 dia antes da oferta expirar</small>
                            </div>
                        </div>

                        <!-- Actions -->
                        <div class="form-actions">
                            <button type="button" class="btn-secondary" onclick="navigateToDashboard()">
                                <i class="fas fa-times"></i> Cancelar
                            </button>
                            <button type="submit" class="btn-primary">
                                <i class="fas fa-check"></i> Publicar Oferta
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- MY OFFERS PAGE -->
    <!-- ============================================ -->
    <div id="page-my-offers" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item" data-page="dashboard-producer">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item" data-page="active-industries">
                    <i class="fas fa-industry"></i>
                    <span>Indústrias Ativas</span>
                </a>
                <a href="#" class="nav-item active" data-page="my-offers">
                    <i class="fas fa-box"></i>
                    <span>Minhas Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="create-offer">
                    <i class="fas fa-plus-circle"></i>
                    <span>Nova Oferta</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">5</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Minhas Ofertas</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button" onclick="toggleNotifications()">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Stats Cards -->
                <div class="stats-grid" style="grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); margin-bottom: 2rem;">
                    <div class="stat-card">
                        <div class="stat-icon green">
                            <i class="fas fa-box"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Ofertas Ativas</span>
                            <span class="stat-value" id="myOffersActiveCount">0</span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon gold">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Expirando em breve</span>
                            <span class="stat-value" id="myOffersExpiringCount">0</span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon yellow">
                            <i class="fas fa-eye"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Total de Visualizações</span>
                            <span class="stat-value" id="myOffersTotalViews">0</span>
                        </div>
                    </div>
                </div>

                <!-- Alerts for expiring offers -->
                <div id="expiringOffersAlert" style="display: none; background-color: #FFF3CD; border: 1px solid #FFD05E; border-radius: 12px; padding: 1.5rem; margin-bottom: 2rem; display: flex; align-items: start; gap: 1rem;">
                    <i class="fas fa-exclamation-triangle" style="color: #FF9800; font-size: 1.5rem; margin-top: 0.25rem;"></i>
                    <div style="flex: 1;">
                        <h4 style="font-size: 1rem; font-weight: 600; color: #273617; margin-bottom: 0.5rem;">
                            <i class="fas fa-clock"></i> Ofertas Expirando
                        </h4>
                        <div id="expiringOffersContent"></div>
                    </div>
                </div>

                <!-- Actions Bar -->
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 1.5rem; gap: 1rem; flex-wrap: wrap;">
                    <div style="display: flex; gap: 0.5rem; flex-wrap: wrap;">
                        <button class="btn-secondary" onclick="app.filterMyOffers('all')" id="filterAll">
                            <i class="fas fa-list"></i> Todas
                        </button>
                        <button class="btn-secondary" onclick="app.filterMyOffers('active')" id="filterActive">
                            <i class="fas fa-check-circle"></i> Ativas
                        </button>
                        <button class="btn-secondary" onclick="app.filterMyOffers('expiring')" id="filterExpiring">
                            <i class="fas fa-clock"></i> Expirando
                        </button>
                        <button class="btn-secondary" onclick="app.filterMyOffers('expired')" id="filterExpired">
                            <i class="fas fa-times-circle"></i> Expiradas
                        </button>
                    </div>
                    <div style="display: flex; gap: 0.5rem; align-items: center;">
                        <!-- View Toggle Buttons -->
                        <div class="view-toggle">
                            <button class="view-toggle-btn active" onclick="toggleMyOffersView('grid')" id="myOffersViewGrid" title="Visualização em Grade">
                                <i class="fas fa-th"></i> Grade
                            </button>
                            <button class="view-toggle-btn" onclick="toggleMyOffersView('list')" id="myOffersViewList" title="Visualização em Lista">
                                <i class="fas fa-list"></i> Lista
                            </button>
                        </div>
                        <button class="btn-primary" onclick="navigateTo('create-offer')">
                            <i class="fas fa-plus"></i> Nova Oferta
                        </button>
                    </div>
                </div>

                <!-- My Offers Grid -->
                <div class="offers-grid" id="myOffersGrid">
                    <!-- Offers will be loaded here by JS -->
                </div>

                <!-- Empty State -->
                <div id="myOffersEmptyState" style="display: none; text-align: center; padding: 4rem 2rem; background-color: white; border-radius: 12px; box-shadow: 0 1px 2px 0 rgba(0,0,0,0.05);">
                    <i class="fas fa-box-open" style="font-size: 4rem; color: #BDBDBD; margin-bottom: 1.5rem;"></i>
                    <h3 style="font-size: 1.5rem; color: #273617; margin-bottom: 1rem;">Nenhuma oferta encontrada</h3>
                    <p style="color: #757575; margin-bottom: 2rem;">Você ainda não criou nenhuma oferta. Comece agora!</p>
                    <button class="btn-primary btn-lg" onclick="navigateTo('create-offer')">
                        <i class="fas fa-plus-circle"></i> Criar Primeira Oferta
                    </button>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- NEGOTIATIONS PAGE -->
    <!-- ============================================ -->
    <div id="page-negotiations" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav" id="negotiationsSidebarNav">
                <!-- Menu será renderizado dinamicamente baseado no tipo de usuário -->
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Negociações</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button" onclick="toggleNotifications()">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info" id="negotiationsUserInfo">
                            <span class="user-name">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Tabs de Filtro -->
                <div style="display: flex; gap: 1rem; margin-bottom: 2rem; flex-wrap: wrap;">
                    <button class="btn-primary" id="filterAllBtn" onclick="app.filterNegotiations('all')">
                        <i class="fas fa-list"></i> Todas (<span id="countAll">0</span>)
                    </button>
                    <button class="btn-secondary" id="filterPendingBtn" onclick="app.filterNegotiations('pending')">
                        <i class="fas fa-clock"></i> Pendentes (<span id="countPending">0</span>)
                    </button>
                    <button class="btn-secondary" id="filterAcceptedBtn" onclick="app.filterNegotiations('accepted')">
                        <i class="fas fa-check"></i> Aceitas (<span id="countAccepted">0</span>)
                    </button>
                    <button class="btn-secondary" id="filterRejectedBtn" onclick="app.filterNegotiations('rejected')">
                        <i class="fas fa-times"></i> Recusadas (<span id="countRejected">0</span>)
                    </button>
                </div>

                <!-- Lista de Negociações -->
                <div class="card">
                    <div class="card-header">
                        <h3 id="negotiationsTitle">Propostas Recebidas</h3>
                    </div>
                    <div id="negotiationsContainer" style="padding: 1.5rem;">
                        <!-- Negociação 1 - PENDENTE -->
                        <div class="negotiation-card pending" style="border: 1px solid var(--color-gray-200); border-radius: var(--radius-lg); padding: 1.5rem; margin-bottom: 1rem; background-color: var(--color-white);">
                            <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 1rem;">
                                <div>
                                    <h4 style="font-size: 1.125rem; font-weight: 600; color: var(--color-primary); margin-bottom: 0.5rem;">
                                        <i class="fas fa-building"></i> Indústria Riz S.A.
                                    </h4>
                                    <p style="color: var(--color-gray-600); font-size: 0.875rem;">
                                        <i class="fas fa-clock"></i> Há 2 horas
                                    </p>
                                </div>
                                <span class="badge" style="background-color: #FFF3CD; color: #FF9800; padding: 0.5rem 1rem; border-radius: var(--radius-md);">
                                    <i class="fas fa-clock"></i> Pendente
                                </span>
                            </div>
                            <div style="background-color: var(--color-gray-50); padding: 1rem; border-radius: var(--radius-md); margin-bottom: 1rem;">
                                <p style="margin-bottom: 0.5rem;"><strong>Oferta:</strong> IRGA 424 - Tipo 1</p>
                                <p style="margin-bottom: 0.5rem;"><strong>Seu preço:</strong> R$ 88,00/saca</p>
                                <p style="margin-bottom: 0.5rem;"><strong>Proposta:</strong> <span style="color: var(--color-success); font-weight: 600;">R$ 86,50/saca</span></p>
                                <p style="margin-bottom: 0;"><strong>Quantidade:</strong> 300 sacas</p>
                            </div>
                            <div style="background-color: #F8F9FA; padding: 1rem; border-radius: var(--radius-md); margin-bottom: 1rem; border-left: 3px solid var(--color-info);">
                                <p style="font-size: 0.875rem; color: var(--color-gray-700); margin: 0;">
                                    <i class="fas fa-comment"></i> "Interessado em fechar negócio. Possuo transporte próprio. Pode fazer contraoferta?"
                                </p>
                            </div>
                            <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                                <button class="btn-primary" onclick="app.acceptProposal('prop_1')">
                                    <i class="fas fa-check"></i> Aceitar Proposta
                                </button>
                                <button class="btn-secondary" onclick="app.counterProposal('prop_1')">
                                    <i class="fas fa-exchange-alt"></i> Fazer Contraoferta
                                </button>
                                <button class="btn-secondary" onclick="app.rejectProposal('prop_1')" style="background-color: #F44336; color: white;">
                                    <i class="fas fa-times"></i> Recusar
                                </button>
                                <button class="btn-secondary" onclick="navigateTo('chat')">
                                    <i class="fas fa-comments"></i> Conversar
                                </button>
                            </div>
                        </div>

                        <!-- Negociação 2 - ACEITA -->
                        <div class="negotiation-card accepted" style="border: 1px solid var(--color-gray-200); border-radius: var(--radius-lg); padding: 1.5rem; margin-bottom: 1rem; background-color: var(--color-white);">
                            <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 1rem;">
                                <div>
                                    <h4 style="font-size: 1.125rem; font-weight: 600; color: var(--color-primary); margin-bottom: 0.5rem;">
                                        <i class="fas fa-building"></i> Arroz Nobre Ltda.
                                    </h4>
                                    <p style="color: var(--color-gray-600); font-size: 0.875rem;">
                                        <i class="fas fa-clock"></i> Ontem às 15:30
                                    </p>
                                </div>
                                <span class="badge" style="background-color: #E8F5E9; color: #4CAF50; padding: 0.5rem 1rem; border-radius: var(--radius-md);">
                                    <i class="fas fa-check"></i> Aceita
                                </span>
                            </div>
                            <div style="background-color: var(--color-gray-50); padding: 1rem; border-radius: var(--radius-md); margin-bottom: 1rem;">
                                <p style="margin-bottom: 0.5rem;"><strong>Oferta:</strong> BR-IRGA 409 - Tipo 1</p>
                                <p style="margin-bottom: 0.5rem;"><strong>Seu preço:</strong> R$ 85,00/saca</p>
                                <p style="margin-bottom: 0.5rem;"><strong>Proposta aceita:</strong> <span style="color: var(--color-success); font-weight: 600;">R$ 85,00/saca</span></p>
                                <p style="margin-bottom: 0;"><strong>Quantidade:</strong> 200 sacas</p>
                            </div>
                            <div style="background-color: #E8F5E9; padding: 1rem; border-radius: var(--radius-md); margin-bottom: 1rem; border-left: 3px solid var(--color-success);">
                                <p style="font-size: 0.875rem; color: var(--color-gray-700); margin: 0;">
                                    <i class="fas fa-check-circle"></i> Negociação aceita! Aguardando confirmação de entrega.
                                </p>
                            </div>
                            <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                                <button class="btn-primary" onclick="app.confirmDelivery('prop_2')">
                                    <i class="fas fa-truck"></i> Confirmar Entrega
                                </button>
                                <button class="btn-secondary" onclick="navigateTo('chat')">
                                    <i class="fas fa-comments"></i> Conversar
                                </button>
                            </div>
                        </div>

                        <!-- Negociação 3 - PENDENTE -->
                        <div class="negotiation-card pending" style="border: 1px solid var(--color-gray-200); border-radius: var(--radius-lg); padding: 1.5rem; margin-bottom: 1rem; background-color: var(--color-white);">
                            <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 1rem;">
                                <div>
                                    <h4 style="font-size: 1.125rem; font-weight: 600; color: var(--color-primary); margin-bottom: 0.5rem;">
                                        <i class="fas fa-building"></i> Beneficiadora Sul
                                    </h4>
                                    <p style="color: var(--color-gray-600); font-size: 0.875rem;">
                                        <i class="fas fa-clock"></i> 2 dias atrás
                                    </p>
                                </div>
                                <span class="badge" style="background-color: #FFF3CD; color: #FF9800; padding: 0.5rem 1rem; border-radius: var(--radius-md);">
                                    <i class="fas fa-clock"></i> Pendente
                                </span>
                            </div>
                            <div style="background-color: var(--color-gray-50); padding: 1rem; border-radius: var(--radius-md); margin-bottom: 1rem;">
                                <p style="margin-bottom: 0.5rem;"><strong>Oferta:</strong> IRGA 424 - Tipo 1</p>
                                <p style="margin-bottom: 0.5rem;"><strong>Seu preço:</strong> R$ 88,00/saca</p>
                                <p style="margin-bottom: 0.5rem;"><strong>Proposta:</strong> <span style="color: var(--color-success); font-weight: 600;">R$ 87,00/saca</span></p>
                                <p style="margin-bottom: 0;"><strong>Quantidade:</strong> 500 sacas (lote completo)</p>
                            </div>
                            <div style="background-color: #F8F9FA; padding: 1rem; border-radius: var(--radius-md); margin-bottom: 1rem; border-left: 3px solid var(--color-info);">
                                <p style="font-size: 0.875rem; color: var(--color-gray-700); margin: 0;">
                                    <i class="fas fa-comment"></i> "Proposta para o lote completo. Pagamento à vista. Posso buscar na semana que vem."
                                </p>
                            </div>
                            <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                                <button class="btn-primary" onclick="app.acceptProposal('prop_3')">
                                    <i class="fas fa-check"></i> Aceitar Proposta
                                </button>
                                <button class="btn-secondary" onclick="app.counterProposal('prop_3')">
                                    <i class="fas fa-exchange-alt"></i> Fazer Contraoferta
                                </button>
                                <button class="btn-secondary" onclick="app.rejectProposal('prop_3')" style="background-color: #F44336; color: white;">
                                    <i class="fas fa-times"></i> Recusar
                                </button>
                                <button class="btn-secondary" onclick="navigateTo('chat')">
                                    <i class="fas fa-comments"></i> Conversar
                                </button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Empty State (quando não houver negociações) -->
                <div id="negotiationsEmptyState" style="display: none; text-align: center; padding: 4rem 2rem; background-color: white; border-radius: 12px; box-shadow: 0 1px 2px 0 rgba(0,0,0,0.05);">
                    <i class="fas fa-handshake" style="font-size: 4rem; color: #BDBDBD; margin-bottom: 1.5rem;"></i>
                    <h3 style="font-size: 1.5rem; color: #273617; margin-bottom: 1rem;">Nenhuma negociação ativa</h3>
                    <p style="color: #757575; margin-bottom: 2rem;">Você ainda não recebeu propostas para suas ofertas.</p>
                    <button class="btn-primary btn-lg" onclick="navigateTo('my-offers')">
                        <i class="fas fa-box"></i> Ver Minhas Ofertas
                    </button>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- DASHBOARD INDUSTRY -->
    <!-- ============================================ -->
    <div id="page-dashboard-industry" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item active" data-page="dashboard-industry">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item" data-page="search-offers">
                    <i class="fas fa-search"></i>
                    <span>Buscar Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="map-offers">
                    <i class="fas fa-map"></i>
                    <span>Mapa de Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="my-purchases">
                    <i class="fas fa-shopping-cart"></i>
                    <span>Minhas Compras</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">2</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Dashboard</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-building"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">Indústria Riz S.A.</span>
                            <span class="user-role">Indústria</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Stats Cards -->
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-icon blue">
                            <i class="fas fa-shopping-cart"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Compras Realizadas</span>
                            <span class="stat-value">34</span>
                            <span class="stat-change neutral">Este mês</span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon yellow">
                            <i class="fas fa-handshake"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Negociações Ativas</span>
                            <span class="stat-value">8</span>
                            <span class="stat-change positive">
                                <i class="fas fa-arrow-up"></i> 2 novas hoje
                            </span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon green">
                            <i class="fas fa-box"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Volume Comprado</span>
                            <span class="stat-value">1.250 t</span>
                            <span class="stat-change neutral">Este ano</span>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon gold">
                            <i class="fas fa-dollar-sign"></i>
                        </div>
                        <div class="stat-info">
                            <span class="stat-label">Investimento Total</span>
                            <span class="stat-value">R$ 2.1M</span>
                            <span class="stat-change positive">
                                <i class="fas fa-arrow-up"></i> 8% vs mês anterior
                            </span>
                        </div>
                    </div>
                </div>

                <!-- Market Index -->
                <div class="card market-index">
                    <div class="card-header">
                        <h3><i class="fas fa-chart-line"></i> Índice de Preços - Mercado Arroz</h3>
                        <span class="badge badge-info">Atualizado há 2 horas</span>
                    </div>
                    <div class="market-stats">
                        <div class="market-stat">
                            <span class="label">Média de Preços Ofertados</span>
                            <span class="value" id="averageOfferPrice">R$ 85,50/saca</span>
                            <span id="averageOfferPriceChange" class="change positive"><i class="fas fa-arrow-up"></i> 2,3%</span>
                        </div>
                        <div class="market-stat">
                            <span class="label">Ofertas Disponíveis</span>
                            <span class="value" id="totalOffersCount">247</span>
                            <span id="totalOffersChange" class="change positive"><i class="fas fa-arrow-up"></i> 12 novas</span>
                        </div>
                    </div>
                </div>

                <!-- Top 5 Cities with Most Offers -->
                <div class="card">
                    <div class="card-header">
                        <h3><i class="fas fa-map-marker-alt"></i> Top 5 Cidades com Mais Ofertas</h3>
                        <span class="badge badge-info">Atualizado agora</span>
                    </div>
                    <div style="padding: 1.5rem;">
                        <div id="topCitiesList" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); gap: 0.75rem;">
                            <!-- Cities will be dynamically rendered here -->
                        </div>
                    </div>
                </div>

                <!-- Recent Activity -->
                <div class="card">
                    <div class="card-header">
                        <h3>Atividades Recentes</h3>
                    </div>
                    <div class="activity-list">
                        <div class="activity-item">
                            <div class="activity-icon blue">
                                <i class="fas fa-file-alt"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Proposta enviada</strong></p>
                                <p class="activity-detail">Você enviou proposta de R$ 86,00/saca para 500 sacas</p>
                                <span class="activity-time">Há 1 hora</span>
                            </div>
                        </div>
                        <div class="activity-item">
                            <div class="activity-icon green">
                                <i class="fas fa-check-circle"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Compra confirmada</strong></p>
                                <p class="activity-detail">Negociação #8841 finalizada - 300 sacas compradas</p>
                                <span class="activity-time">Há 3 horas</span>
                            </div>
                        </div>
                        <div class="activity-item">
                            <div class="activity-icon yellow">
                                <i class="fas fa-comment"></i>
                            </div>
                            <div class="activity-content">
                                <p><strong>Nova mensagem</strong></p>
                                <p class="activity-detail">João Silva respondeu sua proposta</p>
                                <span class="activity-time">Ontem às 16:45</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- SEARCH OFFERS PAGE -->
    <!-- ============================================ -->
    <div id="page-search-offers" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item" data-page="dashboard-industry">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item active" data-page="search-offers">
                    <i class="fas fa-search"></i>
                    <span>Buscar Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="map-offers">
                    <i class="fas fa-map"></i>
                    <span>Mapa de Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="my-purchases">
                    <i class="fas fa-shopping-cart"></i>
                    <span>Minhas Compras</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">2</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Buscar Ofertas</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-building"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">Indústria Riz S.A.</span>
                            <span class="user-role">Indústria</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Search and Filters -->
                <div class="search-section">
                    <div class="search-bar">
                        <i class="fas fa-search"></i>
                        <input type="text" id="searchInput" placeholder="Buscar por variedade, cidade, produtor...">
                    </div>
                    <button class="btn-secondary" onclick="toggleFilters()">
                        <i class="fas fa-filter"></i> Filtros
                    </button>
                    <button class="btn-primary" onclick="navigateTo('map-offers')">
                        <i class="fas fa-map"></i> Ver no Mapa
                    </button>
                    
                    <!-- View Toggle -->
                    <div style="display: flex; gap: 0.5rem; background: var(--color-gray-100); padding: 0.25rem; border-radius: var(--radius-md); margin-left: auto;">
                        <button class="view-toggle-btn active" onclick="toggleOffersView('grid')" data-view="grid" title="Visualização em Grade">
                            <i class="fas fa-th"></i>
                        </button>
                        <button class="view-toggle-btn" onclick="toggleOffersView('list')" data-view="list" title="Visualização em Lista">
                            <i class="fas fa-list"></i>
                        </button>
                    </div>
                </div>

                <!-- Filters Panel -->
                <div class="filters-panel" id="filtersPanel">
                    <div class="filters-content">
                        <div class="filter-group">
                            <label>Localização</label>
                            <select id="filterState">
                                <option value="">Todos os estados</option>
                                <option value="RS">Rio Grande do Sul</option>
                                <option value="SC">Santa Catarina</option>
                                <option value="PR">Paraná</option>
                            </select>
                        </div>
                        <div class="filter-group">
                            <label>Variedade</label>
                            <select id="filterVariety">
                                <option value="">Todas</option>
                                <option value="IRGA 424">IRGA 424</option>
                                <option value="IRGA 424 RI">IRGA 424 RI</option>
                                <option value="GURI INTA CL">GURI INTA CL</option>
                                <option value="BR-IRGA 409">BR-IRGA 409</option>
                            </select>
                        </div>
                        <div class="filter-group">
                            <label>Tipo</label>
                            <select id="filterType">
                                <option value="">Todos</option>
                                <option value="Tipo 1">Tipo 1</option>
                                <option value="Tipo 2">Tipo 2</option>
                                <option value="Tipo 3">Tipo 3</option>
                            </select>
                        </div>
                        <div class="filter-group">
                            <label>Preço (R$/saca)</label>
                            <div class="range-inputs">
                                <input type="number" id="filterPriceMin" placeholder="Mín">
                                <span>até</span>
                                <input type="number" id="filterPriceMax" placeholder="Máx">
                            </div>
                        </div>
                        <div class="filter-group">
                            <label>Quantidade Mínima (sacas)</label>
                            <input type="number" id="filterQuantityMin" placeholder="Ex: 100">
                        </div>
                        <div class="filter-group">
                            <label>Umidade Máxima (%)</label>
                            <input type="number" id="filterHumidity" placeholder="Ex: 20">
                        </div>
                        <div class="filter-actions">
                            <button class="btn-secondary" onclick="clearFilters()">Limpar</button>
                            <button class="btn-primary" onclick="applyFilters()">Aplicar</button>
                        </div>
                    </div>
                </div>

                <!-- Results Header -->
                <div class="results-header">
                    <div class="results-info">
                        <span id="resultsCount">247 ofertas encontradas</span>
                    </div>
                    <div class="results-sort">
                        <label>Ordenar por:</label>
                        <select id="sortBy">
                            <option value="recent">Mais recentes</option>
                            <option value="price-low">Menor preço</option>
                            <option value="price-high">Maior preço</option>
                            <option value="quantity-high">Maior quantidade</option>
                        </select>
                    </div>
                </div>

                <!-- Offers Grid -->
                <div class="offers-grid" id="offersGrid">
                    <!-- Offers will be loaded here by JS -->
                </div>

                <!-- Pagination -->
                <div class="pagination">
                    <button class="pagination-btn" disabled>
                        <i class="fas fa-chevron-left"></i>
                    </button>
                    <button class="pagination-btn active">1</button>
                    <button class="pagination-btn">2</button>
                    <button class="pagination-btn">3</button>
                    <button class="pagination-btn">4</button>
                    <button class="pagination-btn">5</button>
                    <button class="pagination-btn">
                        <i class="fas fa-chevron-right"></i>
                    </button>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- MY PURCHASES PAGE -->
    <!-- ============================================ -->
    <div id="page-my-purchases" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item" data-page="dashboard-industry">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item" data-page="search-offers">
                    <i class="fas fa-search"></i>
                    <span>Buscar Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="map-offers">
                    <i class="fas fa-map"></i>
                    <span>Mapa de Ofertas</span>
                </a>
                <a href="#" class="nav-item active" data-page="my-purchases">
                    <i class="fas fa-shopping-cart"></i>
                    <span>Minhas Compras</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">2</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Minhas Compras</h1>
                    <!-- View Toggle Buttons -->
                    <div class="view-toggle" style="display: flex; gap: 0.5rem; margin-left: auto;">
                        <button class="btn-icon active" id="purchasesGridViewBtn" onclick="app.togglePurchasesView('grid')" title="Visualização em Grade">
                            <i class="fas fa-th"></i>
                        </button>
                        <button class="btn-icon" id="purchasesListViewBtn" onclick="app.togglePurchasesView('list')" title="Visualização em Lista">
                            <i class="fas fa-list"></i>
                        </button>
                    </div>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-building"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">Indústria Riz S.A.</span>
                            <span class="user-role">Indústria</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Filter Tabs -->
                <div class="filter-tabs">
                    <button class="tab-button active" onclick="filterPurchases('all')">
                        Todas <span class="tab-count">8</span>
                    </button>
                    <button class="tab-button" onclick="filterPurchases('pending')">
                        Pendentes <span class="tab-count">2</span>
                    </button>
                    <button class="tab-button" onclick="filterPurchases('confirmed')">
                        Confirmadas <span class="tab-count">4</span>
                    </button>
                    <button class="tab-button" onclick="filterPurchases('delivered')">
                        Entregues <span class="tab-count">2</span>
                    </button>
                </div>

                <!-- Purchases List -->
                <div class="purchases-list" id="purchasesList">
                    <!-- Purchase Card 1 - Confirmed -->
                    <div class="purchase-card" data-status="confirmed">
                        <div class="purchase-header">
                            <div class="purchase-info">
                                <h3>IRGA 424 - Tipo 1</h3>
                                <span class="purchase-id">#COMP-2026-001</span>
                            </div>
                            <span class="status-badge status-confirmed">
                                <i class="fas fa-check-circle"></i> Confirmada
                            </span>
                        </div>
                        <div class="purchase-body">
                            <div class="purchase-details">
                                <div class="detail-row">
                                    <span class="detail-label">Produtor:</span>
                                    <span class="detail-value">João Silva</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Quantidade:</span>
                                    <span class="detail-value">500 sacas (50 kg)</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Preço unitário:</span>
                                    <span class="detail-value">R$ 88,00/saca</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Valor total:</span>
                                    <span class="detail-value total-value">R$ 44.000,00</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Data da compra:</span>
                                    <span class="detail-value">05/03/2026</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Previsão de entrega:</span>
                                    <span class="detail-value">15/03/2026</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Localização:</span>
                                    <span class="detail-value">Cachoeira do Sul, RS</span>
                                </div>
                            </div>
                        </div>
                        <div class="purchase-footer">
                            <button class="btn-secondary" onclick="viewPurchaseDetails('001')">
                                <i class="fas fa-eye"></i> Ver Detalhes
                            </button>
                            <button class="btn-secondary" onclick="contactProducer('user_1')">
                                <i class="fas fa-comments"></i> Mensagem
                            </button>
                            <button class="btn-primary" onclick="confirmDelivery('001')">
                                <i class="fas fa-check"></i> Confirmar Recebimento
                            </button>
                        </div>
                    </div>

                    <!-- Purchase Card 2 - Pending -->
                    <div class="purchase-card" data-status="pending">
                        <div class="purchase-header">
                            <div class="purchase-info">
                                <h3>GURI INTA CL - Tipo 1</h3>
                                <span class="purchase-id">#COMP-2026-002</span>
                            </div>
                            <span class="status-badge status-pending">
                                <i class="fas fa-clock"></i> Aguardando Confirmação
                            </span>
                        </div>
                        <div class="purchase-body">
                            <div class="purchase-details">
                                <div class="detail-row">
                                    <span class="detail-label">Produtor:</span>
                                    <span class="detail-value">Maria Oliveira</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Quantidade:</span>
                                    <span class="detail-value">300 sacas (50 kg)</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Preço unitário:</span>
                                    <span class="detail-value">R$ 86,50/saca</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Valor total:</span>
                                    <span class="detail-value total-value">R$ 25.950,00</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Data da proposta:</span>
                                    <span class="detail-value">08/03/2026</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Localização:</span>
                                    <span class="detail-value">Santa Maria, RS</span>
                                </div>
                            </div>
                        </div>
                        <div class="purchase-footer">
                            <button class="btn-secondary" onclick="viewPurchaseDetails('002')">
                                <i class="fas fa-eye"></i> Ver Detalhes
                            </button>
                            <button class="btn-secondary" onclick="contactProducer('user_3')">
                                <i class="fas fa-comments"></i> Mensagem
                            </button>
                            <button class="btn-danger" onclick="cancelPurchase('002')">
                                <i class="fas fa-times"></i> Cancelar
                            </button>
                        </div>
                    </div>

                    <!-- Purchase Card 3 - Delivered -->
                    <div class="purchase-card" data-status="delivered">
                        <div class="purchase-header">
                            <div class="purchase-info">
                                <h3>BR-IRGA 409 - Tipo 2</h3>
                                <span class="purchase-id">#COMP-2026-003</span>
                            </div>
                            <span class="status-badge status-delivered">
                                <i class="fas fa-truck"></i> Entregue
                            </span>
                        </div>
                        <div class="purchase-body">
                            <div class="purchase-details">
                                <div class="detail-row">
                                    <span class="detail-label">Produtor:</span>
                                    <span class="detail-value">João Silva</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Quantidade:</span>
                                    <span class="detail-value">800 sacas (50 kg)</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Preço unitário:</span>
                                    <span class="detail-value">R$ 82,00/saca</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Valor total:</span>
                                    <span class="detail-value total-value">R$ 65.600,00</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Data da entrega:</span>
                                    <span class="detail-value">28/02/2026</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Localização:</span>
                                    <span class="detail-value">Cachoeira do Sul, RS</span>
                                </div>
                            </div>
                        </div>
                        <div class="purchase-footer">
                            <button class="btn-secondary" onclick="viewPurchaseDetails('003')">
                                <i class="fas fa-eye"></i> Ver Detalhes
                            </button>
                            <button class="btn-secondary" onclick="downloadInvoice('003')">
                                <i class="fas fa-download"></i> Baixar Nota
                            </button>
                            <button class="btn-primary" onclick="ratePurchase('003')">
                                <i class="fas fa-star"></i> Avaliar Produtor
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- MAP OFFERS PAGE -->
    <!-- ============================================ -->
    <div id="page-map-offers" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav">
                <a href="#" class="nav-item" data-page="dashboard-industry">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="nav-item" data-page="search-offers">
                    <i class="fas fa-search"></i>
                    <span>Buscar Ofertas</span>
                </a>
                <a href="#" class="nav-item active" data-page="map-offers">
                    <i class="fas fa-map"></i>
                    <span>Mapa de Ofertas</span>
                </a>
                <a href="#" class="nav-item" data-page="my-purchases">
                    <i class="fas fa-shopping-cart"></i>
                    <span>Minhas Compras</span>
                </a>
                <a href="#" class="nav-item" data-page="negotiations">
                    <i class="fas fa-handshake"></i>
                    <span>Negociações</span>
                    <span class="badge">2</span>
                </a>
                <a href="#" class="nav-item" data-page="chat">
                    <i class="fas fa-comments"></i>
                    <span>Mensagens</span>
                    <span class="badge">3</span>
                </a>
                <a href="#" class="nav-item" data-page="profile">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Mapa de Ofertas</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-building"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">Indústria Riz S.A.</span>
                            <span class="user-role">Indústria</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper no-padding">
                <div class="map-container">
                    <div id="map" class="map-view"></div>
                    <div class="map-controls">
                        <button class="btn-primary" onclick="navigateTo('search-offers')">
                            <i class="fas fa-list"></i> Ver como Lista
                        </button>
                    </div>
                    <div class="map-legend">
                        <h4>Legenda</h4>
                        <div class="legend-item">
                            <div class="legend-marker green"></div>
                            <span>Tipo 1 (até R$ 85/saca)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-marker yellow"></div>
                            <span>Tipo 1 (R$ 85-90/saca)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-marker blue"></div>
                            <span>Tipo 2</span>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- CHAT PAGE -->
    <!-- ============================================ -->
    <div id="page-chat" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav" id="chatSidebarNav">
                <!-- Menu será renderizado dinamicamente baseado no tipo de usuário -->
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Mensagens</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info" id="chatUserInfo">
                            <span class="user-name">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper no-padding">
                <div class="chat-container">
                    <!-- Chat List -->
                    <div class="chat-list">
                        <div class="chat-list-header">
                            <h3>Conversas</h3>
                            <input type="text" placeholder="Buscar..." class="search-chat">
                        </div>
                        <div class="chat-list-items" id="chatList">
                            <!-- Chat items will be loaded here -->
                        </div>
                    </div>

                    <!-- Chat Messages -->
                    <div class="chat-messages">
                        <div class="chat-header">
                            <div class="chat-user-info">
                                <div class="user-avatar">
                                    <i class="fas fa-building"></i>
                                </div>
                                <div>
                                    <h4>Indústria Riz S.A.</h4>
                                    <span class="status online">Online</span>
                                </div>
                            </div>
                            <div class="chat-actions">
                                <button class="icon-button info-toggle" title="Informações da Oferta" onclick="toggleChatInfo()">
                                    <i class="fas fa-info-circle"></i>
                                    <span>Sobre a Oferta</span>
                                </button>
                            </div>
                        </div>
                        <div class="chat-body" id="chatMessages">
                            <!-- Messages will be loaded here -->
                        </div>
                        <div class="chat-footer">
                            <div class="chat-input-container">
                                <button class="icon-button" title="Anexar arquivo">
                                    <i class="fas fa-paperclip"></i>
                                </button>
                                <input type="text" id="messageInput" placeholder="Digite sua mensagem..." onkeypress="handleMessageKeypress(event)">
                                <button class="btn-primary" onclick="sendMessage()">
                                    <i class="fas fa-paper-plane"></i> Enviar
                                </button>
                            </div>
                        </div>
                    </div>

                    <!-- Chat Info Panel (Expands Below) -->
                    <div class="chat-info" id="chatInfoPanel">
                        <div class="chat-info-header">
                            <h3>Sobre a Oferta</h3>
                            <button class="icon-button" onclick="toggleChatInfo()" title="Fechar">
                                <i class="fas fa-times"></i>
                            </button>
                        </div>
                        <div class="chat-info-content">
                            <div class="offer-summary">
                                <img src="https://via.placeholder.com/300x200/5F6C37/FEFADF?text=IRGA+424" alt="Oferta">
                                <h4>IRGA 424 - Tipo 1</h4>
                                <p class="offer-price">R$ 88,00/saca</p>
                                <p class="offer-detail"><i class="fas fa-box"></i> 500 sacas disponíveis</p>
                                <p class="offer-detail"><i class="fas fa-tint"></i> Umidade: 18%</p>
                                <p class="offer-detail"><i class="fas fa-map-marker-alt"></i> Cachoeira do Sul, RS</p>
                                <button class="btn-primary btn-block">
                                    <i class="fas fa-file-alt"></i> Fazer Proposta
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- PROFILE PAGE -->
    <!-- ============================================ -->
    <div id="page-profile" class="page page-dashboard">
        <aside class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <div class="logo-text">
                        <span class="logo-name">mercado</span>
                        <span class="logo-name">arroz</span>
                    </div>
                </div>
                <button class="sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav class="sidebar-nav" id="profileSidebarNav">
                <!-- Menu será renderizado dinamicamente baseado no tipo de usuário -->
            </nav>
            <div class="sidebar-footer">
                <button class="btn-secondary btn-block" onclick="handleLogout()">
                    <i class="fas fa-sign-out-alt"></i>
                    <span>Sair</span>
                </button>
            </div>
        </aside>

        <main class="main-content">
            <header class="topbar">
                <button class="mobile-sidebar-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="topbar-left">
                    <h1 class="page-title">Meu Perfil</h1>
                </div>
                <div class="topbar-right">
                    <button class="icon-button">
                        <i class="fas fa-bell"></i>
                        <span class="notification-dot"></span>
                    </button>
                    <div class="user-menu" onclick="toggleUserMenu()">
                        <div class="user-avatar">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="user-info">
                            <span class="user-name">João Silva</span>
                            <span class="user-role">Produtor</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                </div>
            </header>

            <div class="content-wrapper">
                <!-- Profile Header -->
                <div class="profile-header">
                    <div class="profile-avatar-section">
                        <div class="profile-avatar large">
                            <i class="fas fa-user"></i>
                        </div>
                        <button class="btn-secondary">
                            <i class="fas fa-camera"></i> Alterar Foto
                        </button>
                    </div>
                    <div class="profile-info-section">
                        <h2>João Silva</h2>
                        <p class="profile-subtitle">Produtor de Arroz - Cachoeira do Sul, RS</p>
                        <div class="profile-rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                            <span>4.8 (32 avaliações)</span>
                        </div>
                        <div class="profile-stats-inline">
                            <div class="stat-inline">
                                <i class="fas fa-check-circle"></i>
                                <span>47 vendas realizadas</span>
                            </div>
                            <div class="stat-inline">
                                <i class="fas fa-calendar"></i>
                                <span>Membro desde Jan/2024</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Profile Tabs -->
                <div class="tabs-container">
                    <div class="tabs">
                        <button class="tab active" data-tab="info">Informações</button>
                        <button class="tab" data-tab="reviews">Avaliações</button>
                        <button class="tab" data-tab="settings">Configurações</button>
                    </div>

                    <!-- Tab: Info -->
                    <div class="tab-content active" id="tab-info">
                        <div class="card">
                            <div class="card-header">
                                <h3>Dados Pessoais</h3>
                                <button class="btn-secondary btn-sm">
                                    <i class="fas fa-edit"></i> Editar
                                </button>
                            </div>
                            <div class="profile-details">
                                <div class="detail-row">
                                    <span class="detail-label">Nome Completo</span>
                                    <span class="detail-value">João Silva</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">CPF</span>
                                    <span class="detail-value">123.456.789-00</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">E-mail</span>
                                    <span class="detail-value">joao.silva@email.com</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Telefone</span>
                                    <span class="detail-value">(51) 99999-9999</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Cidade</span>
                                    <span class="detail-value">Cachoeira do Sul - RS</span>
                                </div>
                            </div>
                        </div>

                        <div class="card">
                            <div class="card-header">
                                <h3>Informações da Propriedade</h3>
                                <button class="btn-secondary btn-sm">
                                    <i class="fas fa-edit"></i> Editar
                                </button>
                            </div>
                            <div class="profile-details">
                                <div class="detail-row">
                                    <span class="detail-label">Área Plantada</span>
                                    <span class="detail-value">250 hectares</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Produção Média Anual</span>
                                    <span class="detail-value">1.200 toneladas</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Variedades Cultivadas</span>
                                    <span class="detail-value">IRGA 424, GURI INTA CL, BR-IRGA 409</span>
                                </div>
                                <div class="detail-row">
                                    <span class="detail-label">Certificações</span>
                                    <span class="detail-value">
                                        <span class="badge badge-success">Orgânico</span>
                                        <span class="badge badge-success">GlobalGAP</span>
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Tab: Reviews -->
                    <div class="tab-content" id="tab-reviews">
                        <div class="card">
                            <div class="card-header">
                                <h3>Avaliações Recebidas</h3>
                                <div class="rating-summary">
                                    <span class="rating-score">4.8</span>
                                    <div class="rating-stars">
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star-half-alt"></i>
                                    </div>
                                    <span class="rating-count">32 avaliações</span>
                                </div>
                            </div>
                            <div class="reviews-list">
                                <div class="review-item">
                                    <div class="review-header">
                                        <div class="reviewer-info">
                                            <div class="user-avatar small">
                                                <i class="fas fa-building"></i>
                                            </div>
                                            <div>
                                                <h4>Indústria Riz S.A.</h4>
                                                <div class="rating-stars small">
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                </div>
                                            </div>
                                        </div>
                                        <span class="review-date">15/02/2026</span>
                                    </div>
                                    <p class="review-text">Excelente produtor! Arroz de qualidade superior, entrega pontual e comunicação transparente. Recomendo!</p>
                                </div>
                                <div class="review-item">
                                    <div class="review-header">
                                        <div class="reviewer-info">
                                            <div class="user-avatar small">
                                                <i class="fas fa-building"></i>
                                            </div>
                                            <div>
                                                <h4>Arroz Nobre Indústria</h4>
                                                <div class="rating-stars small">
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                    <i class="fas fa-star"></i>
                                                    <i class="far fa-star"></i>
                                                </div>
                                            </div>
                                        </div>
                                        <span class="review-date">08/02/2026</span>
                                    </div>
                                    <p class="review-text">Ótima negociação, produto conforme anunciado. Apenas a logística teve um pequeno atraso.</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Tab: Settings -->
                    <div class="tab-content" id="tab-settings">
                        <div class="card">
                            <div class="card-header">
                                <h3>Notificações</h3>
                            </div>
                            <div class="settings-list">
                                <div class="setting-item">
                                    <div class="setting-info">
                                        <h4>E-mail de novas propostas</h4>
                                        <p>Receba e-mail quando uma indústria enviar proposta</p>
                                    </div>
                                    <label class="switch">
                                        <input type="checkbox" checked>
                                        <span class="slider"></span>
                                    </label>
                                </div>
                                <div class="setting-item">
                                    <div class="setting-info">
                                        <h4>Notificações push</h4>
                                        <p>Receba notificações no navegador</p>
                                    </div>
                                    <label class="switch">
                                        <input type="checkbox" checked>
                                        <span class="slider"></span>
                                    </label>
                                </div>
                                <div class="setting-item">
                                    <div class="setting-info">
                                        <h4>Newsletter semanal</h4>
                                        <p>Resumo das suas atividades e índice de preços</p>
                                    </div>
                                    <label class="switch">
                                        <input type="checkbox">
                                        <span class="slider"></span>
                                    </label>
                                </div>
                            </div>
                        </div>

                        <div class="card">
                            <div class="card-header">
                                <h3>Segurança</h3>
                            </div>
                            <div class="settings-list">
                                <div class="setting-item clickable" onclick="alert('Funcionalidade em desenvolvimento')">
                                    <div class="setting-info">
                                        <h4>Alterar senha</h4>
                                        <p>Última alteração há 3 meses</p>
                                    </div>
                                    <i class="fas fa-chevron-right"></i>
                                </div>
                                <div class="setting-item">
                                    <div class="setting-info">
                                        <h4>Autenticação em dois fatores</h4>
                                        <p>Adicione uma camada extra de segurança</p>
                                    </div>
                                    <label class="switch">
                                        <input type="checkbox">
                                        <span class="slider"></span>
                                    </label>
                                </div>
                            </div>
                        </div>

                        <!-- Market Availability Card (for industries only) -->
                        <div class="card" id="marketAvailabilityCard" style="display: none;">
                            <div class="card-header">
                                <h3><i class="fas fa-store"></i> Disponibilidade no Mercado</h3>
                            </div>
                            <div class="settings-list">
                                <div class="setting-item">
                                    <div class="setting-info">
                                        <h4>Status no Mercado</h4>
                                        <p id="marketStatusDescription">Sua indústria está <strong>ATIVA</strong> no mercado. Produtores podem ver seu perfil e entrar em contato.</p>
                                    </div>
                                    <label class="switch">
                                        <input type="checkbox" id="marketStatusToggle" checked onchange="toggleMarketStatus()">
                                        <span class="slider"></span>
                                    </label>
                                </div>
                            </div>
                            <div style="padding: 1.5rem; background-color: #E8F5E9; border-radius: 0 0 var(--radius-lg) var(--radius-lg); border-top: 1px solid var(--color-gray-200);">
                                <p style="font-size: 0.875rem; color: var(--color-gray-700); margin: 0;">
                                    <i class="fas fa-info-circle"></i> 
                                    <strong>Dica:</strong> Quando estiver ativa, sua indústria aparecerá com logo colorido para os produtores. 
                                    Quando inativa, aparecerá em cinza e produtores não poderão enviar mensagens.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <!-- ============================================ -->
    <!-- MODALS -->
    <!-- ============================================ -->

    <!-- Indicators Edit Modal -->
    <div id="indicatorsModal" class="modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal('indicatorsModal')">
                <i class="fas fa-times"></i>
            </button>
            <div class="modal-header">
                <h3><i class="fas fa-edit"></i> Atualizar Indicadores de Mercado</h3>
            </div>
            <div class="modal-body">
                <form id="indicatorsForm" onsubmit="handleUpdateIndicators(event)">
                    <!-- Dólar -->
                    <div style="background-color: var(--color-gray-50); padding: 1.5rem; border-radius: var(--radius-md); margin-bottom: 1.5rem;">
                        <h4 style="color: var(--color-primary); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem;">
                            <i class="fas fa-dollar-sign"></i> Cotação do Dólar (USD/BRL)
                        </h4>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="usdPriceInput">Cotação (R$)</label>
                                <input type="number" id="usdPriceInput" step="0.01" required placeholder="5.89">
                            </div>
                            <div class="form-group">
                                <label for="usdChangeInput">Variação (%)</label>
                                <input type="number" id="usdChangeInput" step="0.01" required placeholder="-0.8">
                            </div>
                        </div>
                    </div>

                    <!-- Clima -->
                    <div style="background-color: var(--color-gray-50); padding: 1.5rem; border-radius: var(--radius-md); margin-bottom: 1.5rem;">
                        <h4 style="color: var(--color-primary); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem;">
                            <i class="fas fa-cloud-sun"></i> Clima Pelotas/RS
                        </h4>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="weatherTempInput">Temperatura (°C)</label>
                                <input type="number" id="weatherTempInput" required placeholder="24">
                            </div>
                            <div class="form-group">
                                <label for="weatherRainInput">Chuva (%)</label>
                                <input type="number" id="weatherRainInput" min="0" max="100" required placeholder="60">
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="weatherConditionInput">Condição</label>
                            <select id="weatherConditionInput" required>
                                <option value="Condições favoráveis para colheita">Condições favoráveis para colheita</option>
                                <option value="Condições ideais para plantio">Condições ideais para plantio</option>
                                <option value="Chuvas podem atrasar colheita">Chuvas podem atrasar colheita</option>
                                <option value="Tempo seco, atenção à irrigação">Tempo seco, atenção à irrigação</option>
                                <option value="Condições normais">Condições normais</option>
                            </select>
                        </div>
                    </div>

                    <div class="form-actions">
                        <button type="button" class="btn-secondary" onclick="closeModal('indicatorsModal')">
                            <i class="fas fa-times"></i> Cancelar
                        </button>
                        <button type="submit" class="btn-primary">
                            <i class="fas fa-save"></i> Salvar Alterações
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Offer Detail Modal -->
    <div id="offerDetailModal" class="modal">
        <div class="modal-content large">
            <button class="modal-close" onclick="closeModal('offerDetailModal')">
                <i class="fas fa-times"></i>
            </button>
            <div class="modal-body">
                <div class="offer-detail-content" id="offerDetailContent">
                    <!-- Content will be loaded dynamically -->
                </div>
            </div>
        </div>
    </div>

    <!-- Proposal Modal -->
    <div id="proposalModal" class="modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal('proposalModal')">
                <i class="fas fa-times"></i>
            </button>
            <div class="modal-header">
                <h3><i class="fas fa-file-alt"></i> Enviar Proposta</h3>
            </div>
            <div class="modal-body">
                <form id="proposalForm" onsubmit="handleSendProposal(event)">
                    <div class="form-group">
                        <label for="proposalPrice">Preço Proposto (R$/saca)</label>
                        <input type="number" id="proposalPrice" step="0.01" required placeholder="Ex: 85.00">
                    </div>
                    <div class="form-group">
                        <label for="proposalQuantity">Quantidade Desejada (sacas)</label>
                        <input type="number" id="proposalQuantity" required placeholder="Ex: 300">
                    </div>
                    <div class="form-group">
                        <label for="proposalMessage">Mensagem (opcional)</label>
                        <textarea id="proposalMessage" rows="3" placeholder="Adicione informações sobre sua proposta..."></textarea>
                    </div>
                    <div class="modal-actions">
                        <button type="button" class="btn-secondary" onclick="closeModal('proposalModal')">Cancelar</button>
                        <button type="submit" class="btn-primary">
                            <i class="fas fa-paper-plane"></i> Enviar Proposta
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Manage Offer Modal -->
    <div id="manageOfferModal" class="modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal('manageOfferModal')">
                <i class="fas fa-times"></i>
            </button>
            <div class="modal-header">
                <h3><i class="fas fa-cog"></i> Gerenciar Oferta</h3>
            </div>
            <div class="modal-body">
                <div id="manageOfferContent">
                    <!-- Content will be loaded dynamically -->
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="toast">
        <div class="toast-content">
            <i class="fas fa-check-circle"></i>
            <span id="toastMessage">Ação realizada com sucesso!</span>
        </div>
    </div>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
    <script src="js/script.js"></script>
</body>
</html>
