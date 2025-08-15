<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Worldwise - Encontre as melhores vagas de intercâmbio e construa seu futuro global">
    <meta name="robots" content="index, follow">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="referrer" content="strict-origin-when-cross-origin">
    <title>Worldwise - Vagas de Intercâmbio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8f9fa;
            color: var(--dark-color);
        }

        .navbar {
            background-color: var(--primary-color) !important;
        }

        .navbar-brand {
            font-weight: 700;
            color: white !important;
        }

        .btn-primary {
            background-color: var(--secondary-color);
            border-color: var(--secondary-color);
        }

        .btn-primary:hover {
            background-color: #2980b9;
            border-color: #2980b9;
        }

        .card {
            border: none;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .job-card {
            border-left: 4px solid var(--secondary-color);
        }

        .feature-icon {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 1rem;
        }

        footer {
            background-color: var(--primary-color);
            color: white;
        }

        .profile-pic {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 50%;
            border: 5px solid white;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .progress {
            height: 10px;
        }

        .progress-bar {
            background-color: var(--secondary-color);
        }

        .required-field::after {
            content: " *";
            color: var(--accent-color);
        }

        /* Security badges */
        .security-badge {
            font-size: 0.8rem;
            background-color: var(--light-color);
            padding: 0.3rem 0.6rem;
            border-radius: 20px;
            display: inline-block;
            margin-right: 0.5rem;
            margin-bottom: 0.5rem;
        }

        /* Custom SSO styles */
        .sso-container {
            max-width: 400px;
            margin: 0 auto;
            padding: 2rem;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .sso-divider {
            display: flex;
            align-items: center;
            margin: 1.5rem 0;
        }

        .sso-divider::before, .sso-divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #e0e0e0;
        }

        .sso-divider span {
            padding: 0 1rem;
            color: #6c757d;
        }

        .sso-provider-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            padding: 0.5rem;
            border-radius: 5px;
            margin-bottom: 0.5rem;
            transition: all 0.3s;
        }

        .sso-provider-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .sso-provider-btn i {
            margin-right: 0.5rem;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .profile-pic {
                width: 100px;
                height: 100px;
            }
            
            .sso-container {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="fas fa-globe-americas me-2"></i>Worldwise
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="#home">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#vagas">Vagas</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#perfil">Meu Perfil</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#sobre">Sobre</a>
                    </li>
                </ul>
                <div class="ms-3">
                    <button class="btn btn-outline-light" id="loginBtn">Login</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="py-5 bg-light">
        <div class="container py-5">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <h1 class="display-4 fw-bold mb-4">Transforme seu futuro com intercâmbio</h1>
                    <p class="lead mb-4">Encontre as melhores oportunidades de estudo e trabalho no exterior com a Worldwise. Conectamos você a vagas que combinam com seu perfil e aspirações.</p>
                    <div class="d-flex gap-3">
                        <a href="#vagas" class="btn btn-primary btn-lg px-4">Explorar Vagas</a>
                        <a href="#perfil" class="btn btn-outline-secondary btn-lg px-4">Criar Perfil</a>
                    </div>
                    <div class="mt-4">
                        <span class="security-badge"><i class="fas fa-lock me-1"></i>Dados Protegidos</span>
                        <span class="security-badge"><i class="fas fa-shield-alt me-1"></i>SSL</span>
                        <span class="security-badge"><i class="fas fa-user-shield me-1"></i>Privacidade</span>
                    </div>
                </div>
                <div class="col-lg-6">
                    <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Estudantes no exterior" class="img-fluid rounded-3 shadow">
                </div>
            </div>
        </div>
    </section>

    <!-- Vagas Section -->
    <section id="vagas" class="py-5">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="fw-bold">Vagas Disponíveis</h2>
                <p class="text-muted">Encontre a oportunidade perfeita para seu intercâmbio</p>
            </div>
            
            <div class="row mb-4">
                <div class="col-md-6 col-lg-4 mb-3">
                    <div class="card h-100 job-card">
                        <div class="card-body">
                            <div class="d-flex justify-content-between align-items-start mb-3">
                                <div>
                                    <span class="badge bg-success mb-2">Disponível</span>
                                    <h5 class="card-title">Au Pair na Alemanha</h5>
                                    <p class="text-muted"><i class="fas fa-map-marker-alt me-2"></i>Berlim, Alemanha</p>
                                </div>
                                <img src="https://flagcdn.com/w40/de.png" alt="Alemanha" style="width: 40px; height: auto;">
                            </div>
                            <p class="card-text">Trabalhe cuidando de crianças em uma família alemã enquanto aprende o idioma e a cultura local.</p>
                            <ul class="list-unstyled">
                                <li><i class="fas fa-euro-sign me-2"></i>Salário: €300-500/mês</li>
                                <li><i class="fas fa-clock me-2"></i>Duração: 12 meses</li>
                                <li><i class="fas fa-graduation-cap me-2"></i>Requisitos: Inglês intermediário</li>
                            </ul>
                        </div>
                        <div class="card-footer bg-transparent border-0">
                            <button class="btn btn-primary w-100" data-bs-toggle="modal" data-bs-target="#applyModal" data-job="Au Pair na Alemanha">Aplicar</button>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-3">
                    <div class="card h-100 job-card">
                        <div class="card-body">
                            <div class="d-flex justify-content-between align-items-start mb-3">
                                <div>
                                    <span class="badge bg-success mb-2">Disponível</span>
                                    <h5 class="card-title">Estágio em TI no Canadá</h5>
                                    <p class="text-muted"><i class="fas fa-map-marker-alt me-2"></i>Toronto, Canadá</p>
                                </div>
                                <img src="https://flagcdn.com/w40/ca.png" alt="Canadá" style="width: 40px; height: auto;">
                            </div>
                            <p class="card-text">Estágio remunerado em empresas de tecnologia com possibilidade de efetivação após o término.</p>
                            <ul class="list-unstyled">
                                <li><i class="fas fa-dollar-sign me-2"></i>Salário: CAD$2000-2500/mês</li>
                                <li><i class="fas fa-clock me-2"></i>Duração: 6-12 meses</li>
                                <li><i class="fas fa-graduation-cap me-2"></i>Requisitos: Inglês avançado, conhecimento em programação</li>
                            </ul>
                        </div>
                        <div class="card-footer bg-transparent border-0">
                            <button class="btn btn-primary w-100" data-bs-toggle="modal" data-bs-target="#applyModal" data-job="Estágio em TI no Canadá">Aplicar</button>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-3">
                    <div class="card h-100 job-card">
                        <div class="card-body">
                            <div class="d-flex justify-content-between align-items-start mb-3">
                                <div>
                                    <span class="badge bg-warning text-dark mb-2">Últimas vagas</span>
                                    <h5 class="card-title">Trabalho em Resort na Austrália</h5>
                                    <p class="text-muted"><i class="fas fa-map-marker-alt me-2"></i>Gold Coast, Austrália</p>
                                </div>
                                <img src="https://flagcdn.com/w40/au.png" alt="Austrália" style="width: 40px; height: auto;">
                            </div>
                            <p class="card-text">Vagas em resort para recepção, restaurante e entretenimento com acomodação inclusa.</p>
                            <ul class="list-unstyled">
                                <li><i class="fas fa-dollar-sign me-2"></i>Salário: AUD$20-25/hora</li>
                                <li><i class="fas fa-clock me-2"></i>Duração: 6-24 meses</li>
                                <li><i class="fas fa-graduation-cap me-2"></i>Requisitos: Inglês intermediário</li>
                            </ul>
                        </div>
                        <div class="card-footer bg-transparent border-0">
                            <button class="btn btn-primary w-100" data-bs-toggle="modal" data-bs-target="#applyModal" data-job="Trabalho em Resort na Austrália">Aplicar</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-4">
                <a href="#" class="btn btn-outline-primary">Ver todas as vagas</a>
            </div>
        </div>
    </section>

    <!-- Perfil Section -->
    <section id="perfil" class="py-5 bg-light">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="fw-bold">Meu Perfil</h2>
                <p class="text-muted">Complete seu perfil para aumentar suas chances nas vagas</p>
            </div>
            
            <div class="row">
                <div class="col-lg-4 mb-4">
                    <div class="card">
                        <div class="card-body text-center">
                            <img src="https://ui-avatars.com/api/?name=John+Doe&background=3498db&color=fff&size=150" alt="Foto do perfil" class="profile-pic mb-3">
                            <h4>John Doe</h4>
                            <p class="text-muted">Candidato a Intercâmbio</p>
                            <div class="d-flex justify-content-center gap-2 mb-3">
                                <span class="badge bg-primary">Inglês Avançado</span>
                                <span class="badge bg-secondary">TI</span>
                                <span class="badge bg-success">Disponível</span>
                            </div>
                            
                            <div class="mb-4">
                                <h6>Perfil Completo</h6>
                                <div class="progress">
                                    <div class="progress-bar" role="progressbar" style="width: 65%;" aria-valuenow="65" aria-valuemin="0" aria-valuemax="100">65%</div>
                                </div>
                            </div>
                            
                            <button class="btn btn-outline-primary btn-sm w-100 mb-2">
                                <i class="fas fa-edit me-1"></i>Editar Perfil
                            </button>
                            <button class="btn btn-outline-secondary btn-sm w-100">
                                <i class="fas fa-file-pdf me-1"></i>Baixar CV
                            </button>
                        </div>
                    </div>
                    
                    <div class="card mt-4">
                        <div class="card-body">
                            <h5 class="card-title">Minhas Candidaturas</h5>
                            <ul class="list-group list-group-flush">
                                <li class="list-group-item d-flex justify-content-between align-items-center">
                                    Estágio em TI no Canadá
                                    <span class="badge bg-info">Em análise</span>
                                </li>
                                <li class="list-group-item d-flex justify-content-between align-items-center">
                                    Au Pair na França
                                    <span class="badge bg-secondary">Arquivada</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-8">
                    <div class="card">
                        <div class="card-body">
                            <ul class="nav nav-tabs" id="profileTabs" role="tablist">
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link active" id="info-tab" data-bs-toggle="tab" data-bs-target="#info" type="button">Informações Pessoais</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link" id="education-tab" data-bs-toggle="tab" data-bs-target="#education" type="button">Formação</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link" id="experience-tab" data-bs-toggle="tab" data-bs-target="#experience" type="button">Experiência</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link" id="documents-tab" data-bs-toggle="tab" data-bs-target="#documents" type="button">Documentos</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link" id="preferences-tab" data-bs-toggle="tab" data-bs-target="#preferences" type="button">Preferências</button>
                                </li>
                            </ul>
                            
                            <div class="tab-content p-3" id="profileTabsContent">
                                <div class="tab-pane fade show active" id="info" role="tabpanel">
                                    <form id="personalInfoForm">
                                        <div class="row mb-3">
                                            <div class="col-md-6">
                                                <label for="firstName" class="form-label required-field">Nome</label>
                                                <input type="text" class="form-control" id="firstName" value="John" required>
                                            </div>
                                            <div class="col-md-6">
                                                <label for="lastName" class="form-label required-field">Sobrenome</label>
                                                <input type="text" class="form-control" id="lastName" value="Doe" required>
                                            </div>
                                        </div>
                                        
                                        <div class="row mb-3">
                                            <div class="col-md-6">
                                                <label for="email" class="form-label required-field">Email</label>
                                                <input type="email" class="form-control" id="email" value="john.doe@example.com" required>
                                            </div>
                                            <div class="col-md-6">
                                                <label for="phone" class="form-label">Telefone</label>
                                                <input type="tel" class="form-control" id="phone" value="+55 11 99999-9999">
                                            </div>
                                        </div>
                                        
                                        <div class="row mb-3">
                                            <div class="col-md-6">
                                                <label for="birthDate" class="form-label required-field">Data de Nascimento</label>
                                                <input type="date" class="form-control" id="birthDate" value="1995-05-15" required>
                                            </div>
                                            <div class="col-md-6">
                                                <label for="nationality" class="form-label required-field">Nacionalidade</label>
                                                <select class="form-select" id="nationality" required>
                                                    <option value="BR" selected>Brasileiro</option>
                                                    <option value="PT">Português</option>
                                                    <option value="OTHER">Outra</option>
                                                </select>
                                            </div>
                                        </div>
                                        
                                        <div class="mb-3">
                                            <label for="address" class="form-label">Endereço</label>
                                            <textarea class="form-control" id="address" rows="2">Rua Exemplo, 123 - São Paulo/SP</textarea>
                                        </div>
                                        
                                        <div class="text-end">
                                            <button type="submit" class="btn btn-primary">Salvar Alterações</button>
                                        </div>
                                    </form>
                                </div>
                                
                                <div class="tab-pane fade" id="education" role="tabpanel">
                                    <h6>Formação Acadêmica</h6>
                                    <div class="table-responsive">
                                        <table class="table">
                                            <thead>
                                                <tr>
                                                    <th>Curso</th>
                                                    <th>Instituição</th>
                                                    <th>Ano</th>
                                                    <th>Ações</th>
                                                </tr>
                                            </thead>
                                            <tbody>
                                                <tr>
                                                    <td>Ciência da Computação</td>
                                                    <td>Universidade de São Paulo</td>
                                                    <td>2018-2022</td>
                                                    <td>
                                                        <button class="btn btn-sm btn-outline-primary"><i class="fas fa-edit"></i></button>
                                                        <button class="btn btn-sm btn-outline-danger"><i class="fas fa-trash"></i></button>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <td>Ensino Médio</td>
                                                    <td>Colégio Estadual</td>
                                                    <td>2015-2017</td>
                                                    <td>
                                                        <button class="btn btn-sm btn-outline-primary"><i class="fas fa-edit"></i></button>
                                                        <button class="btn btn-sm btn-outline-danger"><i class="fas fa-trash"></i></button>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                    
                                    <button class="btn btn-primary mt-3" data-bs-toggle="modal" data-bs-target="#educationModal">
                                        <i class="fas fa-plus me-1"></i>Adicionar Formação
                                    </button>
                                </div>
                                
                                <div class="tab-pane fade" id="experience" role="tabpanel">
                                    <h6>Experiência Profissional</h6>
                                    <div class="table-responsive">
                                        <table class="table">
                                            <thead>
                                                <tr>
                                                    <th>Cargo</th>
                                                    <th>Empresa</th>
                                                    <th>Período</th>
                                                    <th>Ações</th>
                                                </tr>
                                            </thead>
                                            <tbody>
                                                <tr>
                                                    <td>Desenvolvedor Júnior</td>
                                                    <td>Tech Solutions Ltda</td>
                                                    <td>2021-Presente</td>
                                                    <td>
                                                        <button class="btn btn-sm btn-outline-primary"><i class="fas fa-edit"></i></button>
                                                        <button class="btn btn-sm btn-outline-danger"><i class="fas fa-trash"></i></button>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <td>Estagiário em TI</td>
                                                    <td>Digital Systems</td>
                                                    <td>2019-2021</td>
                                                    <td>
                                                        <button class="btn btn-sm btn-outline-primary"><i class="fas fa-edit"></i></button>
                                                        <button class="btn btn-sm btn-outline-danger"><i class="fas fa-trash"></i></button>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                    
                                    <button class="btn btn-primary mt-3" data-bs-toggle="modal" data-bs-target="#experienceModal">
                                        <i class="fas fa-plus me-1"></i>Adicionar Experiência
                                    </button>
                                </div>
                                
                                <div class="tab-pane fade" id="documents" role="tabpanel">
                                    <div class="alert alert-info">
                                        <i class="fas fa-info-circle me-2"></i>Envie seus documentos para completar seu perfil e aumentar suas chances nas vagas.
                                    </div>
                                    
                                    <div class="row">
                                        <div class="col-md-6 mb-3">
                                            <div class="card">
                                                <div class="card-body">
                                                    <div class="d-flex justify-content-between align-items-center">
                                                        <div>
                                                            <h6 class="card-title mb-1">Currículo (CV)</h6>
                                                            <p class="text-muted small mb-0">Envie seu currículo atualizado</p>
                                                        </div>
                                                        <span class="badge bg-success">Enviado</span>
                                                    </div>
                                                    <div class="mt-3">
                                                        <button class="btn btn-sm btn-outline-primary me-2">
                                                            <i class="fas fa-download me-1"></i>Baixar
                                                        </button>
                                                        <button class="btn btn-sm btn-outline-secondary">
                                                            <i class="fas fa-upload me-1"></i>Substituir
                                                        </button>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        
                                        <div class="col-md-6 mb-3">
                                            <div class="card">
                                                <div class="card-body">
                                                    <div class="d-flex justify-content-between align-items-center">
                                                        <div>
                                                            <h6 class="card-title mb-1">Documento de Identidade</h6>
                                                            <p class="text-muted small mb-0">RG ou Passaporte</p>
                                                        </div>
                                                        <span class="badge bg-warning text-dark">Pendente</span>
                                                    </div>
                                                    <div class="mt-3">
                                                        <button class="btn btn-sm btn-outline-primary">
                                                            <i class="fas fa-upload me-1"></i>Enviar
                                                        </button>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        
                                        <div class="col-md-6 mb-3">
                                            <div class="card">
                                                <div class="card-body">
                                                    <div class="d-flex justify-content-between align-items-center">
                                                        <div>
                                                            <h6 class="card-title mb-1">Comprovante de Escolaridade</h6>
                                                            <p class="text-muted small mb-0">Diploma ou Histórico</p>
                                                        </div>
                                                        <span class="badge bg-warning text-dark">Pendente</span>
                                                    </div>
                                                    <div class="mt-3">
                                                        <button class="btn btn-sm btn-outline-primary">
                                                            <i class="fas fa-upload me-1"></i>Enviar
                                                        </button>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        
                                        <div class="col-md-6 mb-3">
                                            <div class="card">
                                                <div class="card-body">
                                                    <div class="d-flex justify-content-between align-items-center">
                                                        <div>
                                                            <h6 class="card-title mb-1">Certificado de Proficiência</h6>
                                                            <p class="text-muted small mb-0">Inglês ou outro idioma</p>
                                                        </div>
                                                        <span class="badge bg-danger">Não Enviado</span>
                                                    </div>
                                                    <div class="mt-3">
                                                        <button class="btn btn-sm btn-outline-primary">
                                                            <i class="fas fa-upload me-1"></i>Enviar
                                                        </button>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                
                                <div class="tab-pane fade" id="preferences" role="tabpanel">
                                    <form id="preferencesForm">
                                        <div class="row mb-3">
                                            <div class="col-md-6">
                                                <label for="preferredCountries" class="form-label required-field">Países de Interesse</label>
                                                <select class="form-select" id="preferredCountries" multiple required>
                                                    <option value="CA" selected>Canadá</option>
                                                    <option value="AU" selected>Austrália</option>
                                                    <option value="NZ">Nova Zelândia</option>
                                                    <option value="US">Estados Unidos</option>
                                                    <option value="UK">Reino Unido</option>
                                                    <option value="DE">Alemanha</option>
                                                    <option value="FR">França</option>
                                                    <option value="PT">Portugal</option>
                                                </select>
                                                <small class="text-muted">Segure Ctrl para selecionar múltiplos países</small>
                                            </div>
                                            <div class="col-md-6">
                                                <label for="programType" class="form-label required-field">Tipo de Programa</label>
                                                <select class="form-select" id="programType" required>
                                                    <option value="" disabled selected>Selecione...</option>
                                                    <option value="WORK">Trabalho</option>
                                                    <option value="STUDY" selected>Estudo</option>
                                                    <option value="WORK_STUDY">Trabalho e Estudo</option>
                                                    <option value="AU_PAIR">Au Pair</option>
                                                    <option value="INTERNSHIP">Estágio</option>
                                                </select>
                                            </div>
                                        </div>
                                        
                                        <div class="row mb-3">
                                            <div class="col-md-6">
                                                <label for="startDate" class="form-label">Data Prevista para Início</label>
                                                <input type="date" class="form-control" id="startDate" value="2024-01-15">
                                            </div>
                                            <div class="col-md-6">
                                                <label for="duration" class="form-label">Duração Pretendida</label>
                                                <select class="form-select" id="duration">
                                                    <option value="3">3 meses</option>
                                                    <option value="6">6 meses</option>
                                                    <option value="12" selected>1 ano</option>
                                                    <option value="24">2 anos</option>
                                                    <option value="36">3 anos ou mais</option>
                                                </select>
                                            </div>
                                        </div>
                                        
                                        <div class="mb-3">
                                            <label for="additionalInfo" class="form-label">Informações Adicionais</label>
                                            <textarea class="form-control" id="additionalInfo" rows="3">Gostaria de ter a oportunidade de trabalhar na área de tecnologia enquanto estudo inglês no exterior.</textarea>
                                        </div>
                                        
                                        <div class="text-end">
                                            <button type="submit" class="btn btn-primary">Salvar Preferências</button>
                                        </div>
                                    </form>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sobre Section -->
    <section id="sobre" class="py-5">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <h2 class="fw-bold mb-4">Sobre a Worldwise</h2>
                    <p class="lead">Conectamos talentos globais a oportunidades de intercâmbio que transformam vidas.</p>
                    <p>Fundada em 2025, a Worldwise já ajudou milhares de estudantes e profissionais a realizarem o sonho de viver uma experiência internacional. Nossa equipe de especialistas está comprometida em oferecer as melhores oportunidades personalizadas para cada perfil.</p>
                    <p>Nossa missão é promover o desenvolvimento pessoal e profissional através de experiências interculturais que enriquecem vidas e carreiras.</p>
                    
                    <div class="mt-4">
                        <div class="d-flex align-items-center mb-3">
                            <div class="feature-icon me-4">
                                <i class="fas fa-globe"></i>
                            </div>
                            <div>
                                <h5 class="mb-1">Presença Global</h5>
                                <p class="mb-0 text-muted">Parcerias em mais de 20 países</p>
                            </div>
                        </div>
                        
                        <div class="d-flex align-items-center mb-3">
                            <div class="feature-icon me-4">
                                <i class="fas fa-user-tie"></i>
                            </div>
                            <div>
                                <h5 class="mb-1">Suporte Personalizado</h5>
                                <p class="mb-0 text-muted">Consultores especializados para cada caso</p>
                            </div>
                        </div>
                        
                        <div class="d-flex align-items-center">
                            <div class="feature-icon me-4">
                                <i class="fas fa-shield-alt"></i>
                            </div>
                            <div>
                                <h5 class="mb-1">Segurança Garantida</h5>
                                <p class="mb-0 text-muted">Processos seguros e transparentes</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <img src="https://images.unsplash.com/photo-1521791055366-0d553872125f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1469&q=80" alt="Equipe Worldwise" class="img-fluid rounded-3 shadow">
                </div>
            </div>
        </div>
    </section>

    <!-- Modal de Aplicação -->
    <div class="modal fade" id="applyModal" tabindex="-1" aria-labelledby="applyModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="applyModalLabel">Aplicar para Vaga</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="applicationForm">
                        <div class="mb-4">
                            <h6 id="jobTitle">Au Pair na Alemanha</h6>
                            <p class="text-muted" id="jobLocation"><i class="fas fa-map-marker-alt me-2"></i>Berlim, Alemanha</p>
                        </div>
                        
                        <div class="alert alert-info">
                            <i class="fas fa-info-circle me-2"></i>Verifique se seu perfil está completo antes de aplicar. Vagas com perfil incompleto têm menor chance de aprovação.
                        </div>
                        
                        <div class="mb-3">
                            <label for="applicationMessage" class="form-label required-field">Mensagem de Candidatura</label>
                            <textarea class="form-control" id="applicationMessage" rows="5" required>Prezados, 

Meu nome é John Doe e estou muito interessado na vaga de Au Pair na Alemanha. Tenho experiência cuidando de crianças e estou ansioso para aprender mais sobre a cultura alemã enquanto ajudo uma família local.

Sou organizado, responsável e adoro trabalhar com crianças. Tenho inglês intermediário e estou começando a aprender alemão.

Agradeço pela consideração e estou à disposição para qualquer informação adicional.

Atenciosamente,
John Doe</textarea>
                            <small class="text-muted">Explique por que você é o candidato ideal para esta vaga (mínimo 200 caracteres)</small>
                        </div>
                        
                        <div class="mb-3">
                            <label class="form-label required-field">Documentos para Aplicação</label>
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox" id="attachCV" checked>
                                <label class="form-check-label" for="attachCV">Currículo (enviado no perfil)</label>
                            </div>
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox" id="attachLetter">
                                <label class="form-check-label" for="attachLetter">Carta de Recomendação (opcional)</label>
                            </div>
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox" id="attachCertificates">
                                <label class="form-check-label" for="attachCertificates">Certificados (opcional)</label>
                            </div>
                        </div>
                        
                        <div class="mb-3">
                            <label for="additionalDocuments" class="form-label">Outros Documentos</label>
                            <input class="form-control" type="file" id="additionalDocuments" multiple>
                            <small class="text-muted">Você pode enviar até 3 arquivos adicionais (PDF, DOC ou JPEG)</small>
                        </div>
                        
                        <div class="form-check mb-4">
                            <input class="form-check-input" type="checkbox" id="agreeTerms" required>
                            <label class="form-check-label" for="agreeTerms">Li e concordo com os <a href="#" data-bs-toggle="modal" data-bs-target="#termsModal">Termos de Serviço</a> e <a href="#" data-bs-toggle="modal" data-bs-target="#privacyModal">Política de Privacidade</a> da Worldwise</label>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancelar</button>
                    <button type="submit" form="applicationForm" class="btn btn-primary">Enviar Aplicação</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal de Termos -->
    <div class="modal fade" id="termsModal" tabindex="-1" aria-labelledby="termsModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="termsModalLabel">Termos de Serviço</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <h6>1. Aceitação dos Termos</h6>
                    <p>Ao utilizar os serviços da Worldwise, você concorda com estes Termos de Serviço. Se não concordar, não utilize nossos serviços.</p>
                    
                    <h6 class="mt-4">2. Serviços Oferecidos</h6>
                    <p>A Worldwise atua como intermediária entre candidatos a intercâmbio e oportunidades no exterior. Não somos empregadores diretos nem instituições de ensino.</p>
                    
                    <h6 class="mt-4">3. Responsabilidades do Usuário</h6>
                    <p>Você é responsável por fornecer informações verdadeiras e manter seus dados atualizados. Informações falsas podem resultar no cancelamento de sua candidatura.</p>
                    
                    <h6 class="mt-4">4. Processo de Seleção</h6>
                    <p>A Worldwise não garante a aprovação em nenhum programa. A seleção final é sempre feita pela instituição/empresa no país de destino.</p>
                    
                    <h6 class="mt-4">5. Taxas e Pagamentos</h6>
                    <p>Alguns programas podem têm taxas associadas, que serão claramente comunicadas antes do compromisso.</p>
                    
                    <h6 class="mt-4">6. Cancelamento e Reembolsos</h6>
                    <p>Políticas de cancelamento e reembolso variam conforme o programa e serão informadas no contrato específico.</p>
                    
                    <h6 class="mt-4">7. Limitação de Responsabilidade</h6>
                    <p>A Worldwise não se responsabiliza por decisões de vistos, alterações em programas ou questões decorrentes da estadia no exterior.</p>
                    
                    <h6 class="mt-4">8. Alterações nos Termos</h6>
                    <p>Podemos alterar estes termos a qualquer momento. O uso continuado dos serviços após alterações constitui aceitação dos novos termos.</p>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-primary" data-bs-dismiss="modal">Entendi</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal de Privacidade -->
    <div class="modal fade" id="privacyModal" tabindex="-1" aria-labelledby="privacyModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="privacyModalLabel">Política de Privacidade</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <h6>1. Informações Coletadas</h6>
                    <p>Coletamos informações pessoais como nome, contato, dados acadêmicos e profissionais necessários para o processo de intercâmbio.</p>
                    
                    <h6 class="mt-4">2. Uso das Informações</h6>
                    <p>Suas informações são usadas para: (a) processar sua candidatura; (b) comunicar sobre oportunidades; (c) melhorar nossos serviços.</p>
                    
                    <h6 class="mt-4">3. Compartilhamento de Dados</h6>
                    <p>Seus dados podem ser compartilhados apenas com: (a) instituições/empresas parceiras para as quais você se candidatar; (b) autoridades quando exigido por lei.</p>
                    
                    <h6 class="mt-4">4. Segurança de Dados</h6>
                    <p>Implementamos medidas técnicas e organizacionais para proteger seus dados contra acesso não autorizado ou perda.</p>
                    
                    <h6 class="mt-4">5. Seus Direitos</h6>
                    <p>Você tem direito a: (a) acessar seus dados; (b) corrigir informações incorretas; (c) solicitar a exclusão de dados, quando aplicável.</p>
                    
                    <h6 class="mt-4">6. Cookies e Tecnologias Similares</h6>
                    <p>Utilizamos cookies para melhorar a experiência no site. Você pode gerenciar as preferências de cookies no seu navegador.</p>
                    
                    <h6 class="mt-4">7. Alterações na Política</h6>
                    <p>Esta política pode ser atualizada periodicamente. Alterações significativas serão comunicadas aos usuários.</p>
                    
                    <h6 class="mt-4">8. Contato</h6>
                    <p>Para questões sobre privacidade, entre em contato com nosso Encarregado de Dados em privacidade@worldwise.com.</p>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-primary" data-bs-dismiss="modal">Entendi</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal de Educação -->
    <div class="modal fade" id="educationModal" tabindex="-1" aria-labelledby="educationModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="educationModalLabel">Adicionar Formação Acadêmica</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="educationForm">
                        <div class="mb-3">
                            <label for="educationLevel" class="form-label required-field">Nível de Formação</label>
                            <select class="form-select" id="educationLevel" required>
                                <option value="" selected disabled>Selecione...</option>
                                <option value="HIGH_SCHOOL">Ensino Médio</option>
                                <option value="TECHNICAL">Técnico</option>
                                <option value="BACHELOR">Graduação</option>
                                <option value="MASTER">Mestrado</option>
                                <option value="PHD">Doutorado</option>
                                <option value="OTHER">Outro</option>
                            </select>
                        </div>
                        
                        <div class="mb-3">
                            <label for="educationCourse" class="form-label required-field">Curso/Área</label>
                            <input type="text" class="form-control" id="educationCourse" required>
                        </div>
                        
                        <div class="mb-3">
                            <label for="educationInstitution" class="form-label required-field">Instituição</label>
                            <input type="text" class="form-control" id="educationInstitution" required>
                        </div>
                        
                        <div class="row mb-3">
                            <div class="col-md-6">
                                <label for="educationStart" class="form-label required-field">Ano de Início</label>
                                <input type="number" class="form-control" id="educationStart" min="1900" max="2099" required>
                            </div>
                            <div class="col-md-6">
                                <label for="educationEnd" class="form-label">Ano de Conclusão</label>
                                <input type="number" class="form-control" id="educationEnd" min="1900" max="2099">
                                <div class="form-check mt-2">
                                    <input class="form-check-input" type="checkbox" id="educationCurrent">
                                    <label class="form-check-label" for="educationCurrent">Cursando atualmente</label>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mb-3">
                            <label for="educationDescription" class="form-label">Descrição (opcional)</label>
                            <textarea class="form-control" id="educationDescription" rows="3"></textarea>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancelar</button>
                    <button type="submit" form="educationForm" class="btn btn-primary">Salvar Formação</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal de Experiência -->
    <div class="modal fade" id="experienceModal" tabindex="-1" aria-labelledby="experienceModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="experienceModalLabel">Adicionar Experiência Profissional</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="experienceForm">
                        <div class="mb-3">
                            <label for="experiencePosition" class="form-label required-field">Cargo/Função</label>
                            <input type="text" class="form-control" id="experiencePosition" required>
                        </div>
                        
                        <div class="mb-3">
                            <label for="experienceCompany" class="form-label required-field">Empresa/Organização</label>
                            <input type="text" class="form-control" id="experienceCompany" required>
                        </div>
                        
                        <div class="row mb-3">
                            <div class="col-md-6">
                                <label for="experienceStart" class="form-label required-field">Data de Início</label>
                                <input type="date" class="form-control" id="experienceStart" required>
                            </div>
                            <div class="col-md-6">
                                <label for="experienceEnd" class="form-label">Data de Término</label>
                                <input type="date" class="form-control" id="experienceEnd">
                                <div class="form-check mt-2">
                                    <input class="form-check-input" type="checkbox" id="experienceCurrent">
                                    <label class="form-check-label" for="experienceCurrent">Emprego atual</label>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mb-3">
                            <label for="experienceDescription" class="form-label required-field">Descrição das Atividades</label>
                            <textarea class="form-control" id="experienceDescription" rows="4" required></textarea>
                        </div>
                        
                        <div class="mb-3">
                            <label for="experienceSkills" class="form-label">Habilidades Desenvolvidas</label>
                            <input type="text" class="form-control" id="experienceSkills" placeholder="Separe por vírgulas (ex: trabalho em equipe, liderança, etc)">
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancelar</button>
                    <button type="submit" form="experienceForm" class="btn btn-primary">Salvar Experiência</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Login Modal -->
    <div class="modal fade" id="loginModal" tabindex="-1" aria-labelledby="loginModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="loginModalLabel">Acesse sua conta Worldwise</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="sso-container">
                        <h4 class="text-center mb-4">Autenticação Única</h4>
                        <p class="text-center mb-4">Escolha um método para acessar sua conta:</p>
                        
                        <div class="d-grid gap-2">
                            <button class="btn btn-primary" id="emailLoginBtn">
                                <i class="fas fa-envelope me-2"></i>Entrar com Email
                            </button>
                            
                            <div class="sso-divider">
                                <span>OU</span>
                            </div>
                            
                            <button class="sso-provider-btn" style="background-color: #4285F4; color: white;">
                                <i class="fab fa-google me-2"></i>Continuar com Google
                            </button>
                            
                            <button class="sso-provider-btn" style="background-color: #3B5998; color: white;">
                                <i class="fab fa-facebook-f me-2"></i>Continuar com Facebook
                            </button>
                            
                            <button class="sso-provider-btn" style="background-color: #1DA1F2; color: white;">
                                <i class="fab fa-twitter me-2"></i>Continuar com Twitter
                            </button>
                            
                            <button class="sso-provider-btn" style="background-color: #000000; color: white;">
                                <i class="fab fa-apple me-2"></i>Continuar com Apple
                            </button>
                        </div>
                        
                        <div class="text-center mt-4">
                            <p class="small">Ao continuar, você concorda com nossos <a href="#" data-bs-toggle="modal" data-bs-target="#termsModal">Termos</a> e <a href="#" data-bs-toggle="modal" data-bs-target="#privacyModal">Política de Privacidade</a>.</p>
                        </div>
                    </div>
                    
                    <!-- Email Login Form (hidden by default) -->
                    <form id="emailLoginForm" style="display: none;">
                        <div class="mb-3">
                            <label for="loginEmail" class="form-label required-field">Email</label>
                            <input type="email" class="form-control" id="loginEmail" required>
                        </div>
                        
                        <div class="mb-3">
                            <label for="loginPassword" class="form-label required-field">Senha</label>
                            <input type="password" class="form-control" id="loginPassword" required>
                            <div class="form-text text-end">
                                <a href="#" id="forgotPassword">Esqueceu a senha?</a>
                            </div>
                        </div>
                        
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="rememberMe">
                            <label class="form-check-label" for="rememberMe">Lembrar de mim</label>
                        </div>
                        
                        <div class="d-grid gap-2">
                            <button type="submit" class="btn btn-primary">Entrar</button>
                        </div>
                        
                        <div class="text-center mt-3">
                            <p>Não tem uma conta? <a href="#" id="registerLink">Cadastre-se</a></p>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-lg-3 mb-4">
                    <h5 class="text-white mb-4">
                        <i class="fas fa-globe-americas me-2"></i>Worldwise
                    </h5>
                    <p class="text-muted">Transformando vidas através de experiências interculturais desde 2025.</p>
                    <div class="d-flex gap-3">
                        <a href="#" class="text-white"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-white"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-white"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="text-white"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="col-lg-3 mb-4">
                    <h5 class="text-white mb-4">Links Rápidos</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#home" class="text-muted">Home</a></li>
                        <li class="mb-2"><a href="#vagas" class="text-muted">Vagas</a></li>
                        <li class="mb-2"><a href="#perfil" class="text-muted">Meu Perfil</a></li>
                        <li class="mb-2"><a href="#sobre" class="text-muted">Sobre Nós</a></li>
                        <li class="mb-2"><a href="#" class="text-muted">Blog</a></li>
                    </ul>
                </div>
                
                <div class="col-lg-3 mb-4">
                    <h5 class="text-white mb-4">Suporte</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#" class="text-muted">FAQ</a></li>
                        <li class="mb-2"><a href="#" class="text-muted">Contato</a></li>
                        <li class="mb-2"><a href="#" data-bs-toggle="modal" data-bs-target="#privacyModal" class="text-muted">Privacidade</a></li>
                        <li class="mb-2"><a href="#" data-bs-toggle="modal" data-bs-target="#termsModal" class="text-muted">Termos de Serviço</a></li>
                    </ul>
                </div>
                
                <div class="col-lg-3 mb-4">
                    <h5 class="text-white mb-4">Contato</h5>
                    <ul class="list-unstyled text-muted">
                        <li class="mb-2"><i class="fas fa-map-marker-alt me-2"></i>Av. Paulista, 1000 - São Paulo/SP</li>
                        <li class="mb-2"><i class="fas fa-phone me-2"></i>(11) 9999-9999</li>
                        <li class="mb-2"><i class="fas fa-envelope me-2"></i>contato@worldwise.com</li>
                    </ul>
                </div>
            </div>
            
            <div class="border-top pt-4 mt-4 text-center">
                <p class="text-muted mb-0">&copy; 2025 Worldwise. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Atualiza o título da vaga no modal de aplicação
        document.addEventListener('DOMContentLoaded', function() {
            var applyModal = document.getElementById('applyModal');
            if (applyModal) {
                applyModal.addEventListener('show.bs.modal', function(event) {
                    var button = event.relatedTarget;
                    var jobTitle = button.getAttribute('data-job');
                    var modalTitle = applyModal.querySelector('.modal-title');
                    var jobTitleElement = applyModal.querySelector('#jobTitle');
                    
                    modalTitle.textContent = 'Aplicar para: ' + jobTitle;
                    jobTitleElement.textContent = jobTitle;
                });
            }
            
            // Mostra o modal de login quando o botão de login é clicado
            var loginBtn = document.getElementById('loginBtn');
            if (loginBtn) {
                loginBtn.addEventListener('click', function() {
                    var loginModal = new bootstrap.Modal(document.getElementById('loginModal'));
                    loginModal.show();
                });
            }
            
            // Toggle between SSO and email login
            var emailLoginBtn = document.getElementById('emailLoginBtn');
            var emailLoginForm = document.getElementById('emailLoginForm');
            var ssoContainer = document.querySelector('.sso-container');
            
            if (emailLoginBtn && emailLoginForm && ssoContainer) {
                emailLoginBtn.addEventListener('click', function() {
                    ssoContainer.style.display = 'none';
                    emailLoginForm.style.display = 'block';
                });
            }
            
            // Validação do formulário de perfil
            var personalInfoForm = document.getElementById('personalInfoForm');
            if (personalInfoForm) {
                personalInfoForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    alert('Informações pessoais salvas com sucesso!');
                    // Aqui você adicionaria o código para enviar os dados para o servidor
                });
            }
            
            // Validação do formulário de preferências
            var preferencesForm = document.getElementById('preferencesForm');
            if (preferencesForm) {
                preferencesForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    alert('Preferências salvas com sucesso!');
                    // Aqui você adicionaria o código para enviar os dados para o servidor
                });
            }
            
            // Validação do formulário de aplicação
            var applicationForm = document.getElementById('applicationForm');
            if (applicationForm) {
                applicationForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    var jobTitle = document.getElementById('jobTitle').textContent;
                    alert('Aplicação para "' + jobTitle + '" enviada com sucesso!');
                    var applyModalInstance = bootstrap.Modal.getInstance(applyModal);
                    applyModalInstance.hide();
                    // Aqui você adicionaria o código para enviar os dados para o servidor
                });
            }
            
            // Validação do formulário de educação
            var educationForm = document.getElementById('educationForm');
            if (educationForm) {
                educationForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    alert('Formação acadêmica adicionada com sucesso!');
                    var educationModalInstance = bootstrap.Modal.getInstance(document.getElementById('educationModal'));
                    educationModalInstance.hide();
                    // Aqui você adicionaria o código para enviar os dados para o servidor
                });
            }
            
            // Validação do formulário de experiência
            var experienceForm = document.getElementById('experienceForm');
            if (experienceForm) {
                experienceForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    alert('Experiência profissional adicionada com sucesso!');
                    var experienceModalInstance = bootstrap.Modal.getInstance(document.getElementById('experienceModal'));
                    experienceModalInstance.hide();
                    // Aqui você adicionaria o código para enviar os dados para o servidor
                });
            }
            
            // Validação do formulário de login
            var loginForm = document.getElementById('loginForm');
            if (loginForm) {
                loginForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    // Aqui você adicionaria o código para autenticar o usuário
                    // Por enquanto, apenas fechamos o modal e mudamos o botão de login para logout
                    var loginModalInstance = bootstrap.Modal.getInstance(document.getElementById('loginModal'));
                    loginModalInstance.hide();
                    
                    var loginBtn = document.getElementById('loginBtn');
                    loginBtn.textContent = 'Logout';
                    loginBtn.className = 'btn btn-outline-light';
                    loginBtn.onclick = function() {
                        if (confirm('Deseja realmente sair?')) {
                            loginBtn.textContent = 'Login';
                            loginBtn.className = 'btn btn-outline-light';
                            loginBtn.onclick = function() {
                                loginModalInstance.show();
                            };
                        }
                    };
                });
            }
            
            // Link para registro
            var registerLink = document.getElementById('registerLink');
            if (registerLink) {
                registerLink.addEventListener('click', function(e) {
                    e.preventDefault();
                    alert('Página de registro será implementada na versão completa.');
                });
            }
            
            // Link para esqueceu a senha
            var forgotPassword = document.getElementById('forgotPassword');
            if (forgotPassword) {
                forgotPassword.addEventListener('click', function(e) {
                    e.preventDefault();
                    alert('Recuperação de senha será implementada na versão completa.');
                });
            }
            
            // Handle SSO provider buttons
            var ssoProviderBtns = document.querySelectorAll('.sso-provider-btn');
            ssoProviderBtns.forEach(function(btn) {
                btn.addEventListener('click', function(e) {
                    e.preventDefault();
                    var provider = this.querySelector('i').className.split(' ')[1].replace('fa-', '');
                    alert('Autenticação com ' + provider.charAt(0).toUpperCase() + provider.slice(1) + ' será implementada na versão completa.');
                    
                    // Simulate successful login
                    var loginModalInstance = bootstrap.Modal.getInstance(document.getElementById('loginModal'));
                    loginModalInstance.hide();
                    
                    var loginBtn = document.getElementById('loginBtn');
                    loginBtn.textContent = 'Logout';
                    loginBtn.className = 'btn btn-outline-light';
                    loginBtn.onclick = function() {
                        if (confirm('Deseja realmente sair?')) {
                            loginBtn.textContent = 'Login';
                            loginBtn.className = 'btn btn-outline-light';
                            loginBtn.onclick = function() {
                                loginModalInstance.show();
                            };
                        }
                    };
                });
            });
        });
    </script>
</body>
</html>
