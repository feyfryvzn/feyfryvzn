<!DOCTYPE html>
<html lang="id" data-bs-theme="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feyza Revalina | Creative Developer Portfolio</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.0/font/bootstrap-icons.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --primary-accent: #FF85B3;
            --secondary-accent: #FFC2D1;
            --accent-dark: #D43A78;
            --bg-light: #FFF5F7;
            --text-main: #4A1D33;
            --text-muted: #8E6C7E;
            --navbar-bg: rgba(255, 255, 255, 0.8);
            --mesh-pink: #ffe5ec;
            --mesh-purple: #f3e5f5;
            --mesh-blue: #e3f2fd;
            --mesh-white: #ffffff;
        }

        [data-bs-theme="dark"] {
            --mesh-white: #2D0B1A;
            --mesh-pink: #45162B;
            --mesh-purple: #580a1f;
            --mesh-blue: #2D0B1A;
            --text-main: #FFE5EC;
            --navbar-bg: rgba(45, 11, 26, 0.9);
            --bg-light: #1a0a12;
            --text-muted: #c89fb3;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; transition: background-color 0.3s ease, color 0.3s ease; }
        body { font-family: 'Poppins', sans-serif; overflow-x: hidden; background-color: var(--mesh-white); color: var(--text-main); position: relative; }

        /* --- DESAIN GELOMBANG & GLASSMORPHISM --- */
        .wave-container { position: relative; width: 100%; overflow: hidden; line-height: 0; background: transparent; }
        .wave-container svg { position: relative; display: block; width: calc(100% + 1.3px); height: 80px; }
        
        .skill-card, .project-card, .contact-card {
            background: rgba(255, 255, 255, 0.4) !important;
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 133, 179, 0.2) !important;
            border-radius: 25px !important;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) !important;
        }

        .skill-card:hover, .project-card:hover {
            transform: translateY(-15px) scale(1.02) !important;
            box-shadow: 0 20px 40px rgba(212, 58, 120, 0.2) !important;
            background: rgba(255, 255, 255, 0.8) !important;
        }

        .animated-bg {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -2;
            background: radial-gradient(circle at 20% 30%, var(--mesh-pink) 0%, transparent 45%),
                        radial-gradient(circle at 80% 20%, var(--mesh-purple) 0%, transparent 45%),
                        radial-gradient(circle at 50% 80%, var(--mesh-blue) 0%, transparent 50%),
                        radial-gradient(circle at 10% 90%, var(--secondary-accent) 0%, transparent 35%);
            filter: blur(65px); animation: moveMesh 15s ease-in-out infinite alternate;
        }

        @keyframes moveMesh { 0% { transform: scale(1) translate(0, 0); } 100% { transform: scale(1.1) translate(3%, 3%); } }

        .navbar { background: var(--navbar-bg) !important; backdrop-filter: blur(10px); padding: 20px 0; border-bottom: 1px solid rgba(255, 133, 179, 0.15); }
        .hero-section { min-height: 100vh; display: flex; align-items: center; padding-top: 100px; position: relative; }
        .profile-img { border-radius: 30px; position: relative; z-index: 2; max-width: 90%; box-shadow: 0 20px 60px rgba(255, 133, 179, 0.3); }
        .text-gradient { background: linear-gradient(135deg, var(--primary-accent), var(--accent-dark)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        
        /* Morphing Border Animation */
        .dotted-border {
            position: absolute; top: 0; left: 0; right: 0; bottom: 0;
            border: 3px dashed var(--primary-accent);
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            animation: morphBlob 8s linear infinite;
        }
        @keyframes morphBlob {
            0%, 100% { border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; }
            50% { border-radius: 60% 40% 30% 70% / 50% 60% 40% 60%; }
        }
    </style>
</head>
<body>
    <div class="animated-bg"></div>

    <nav class="navbar navbar-expand-lg fixed-top" id="navbar">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#home">FEYZA<span style="color:var(--primary-accent)">.</span></a>
            <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto align-items-center">
                    <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
                    <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
                    <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                    <li class="nav-item ms-lg-3"><a class="btn btn-primary-custom nav-link text-white px-4" style="background: linear-gradient(135deg, var(--primary-accent), var(--accent-dark)); border-radius:50px;" href="#contact">Hire Me</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <section id="home" class="hero-section">
        <div class="container">
            <div class="row align-items-center gy-5">
                <div class="col-lg-6" data-aos="fade-right">
                    <div class="badge rounded-pill bg-light text-primary px-3 py-2 mb-3 shadow-sm border">🚀 Available for New Projects</div>
                    <h1 class="hero-title fw-bold display-4">Hi, I'm <span class="text-gradient">Feyza</span><br>Creative <span class="typing-text" id="typingText"></span></h1>
                    <p class="lead text-muted mb-4">Saya menggabungkan analisis data mendalam dengan pembangunan sistem pintar untuk solusi industri otomotif.</p>
                    <div class="d-flex flex-wrap gap-3">
                        <a href="#projects" class="btn btn-primary px-4 py-2 shadow-sm" style="background: var(--accent-dark); border:none; border-radius:50px;">View Projects</a>
                        <div class="social-links d-flex gap-2">
                            <a href="https://github.com/feyfryvzn" class="btn btn-outline-secondary rounded-circle"><i class="bi bi-github"></i></a>
                            <a href="https://www.instagram.com/fey_fryvzn" class="btn btn-outline-secondary rounded-circle"><i class="bi bi-instagram"></i></a>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6 text-center" data-aos="zoom-in">
                    <div class="hero-img-wrapper d-inline-block position-relative p-4">
                        <div class="dotted-border"></div>
                        <img src="fotofeyza.jpeg" alt="Feyza" class="profile-img shadow-lg">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="wave-container">
        <svg viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0,64L80,69.3C160,75,320,85,480,80C640,75,800,53,960,48C1120,43,1280,53,1360,58.7L1440,64V120H0V64Z" fill="#ffffff"/>
        </svg>
    </div>

    <section id="about" style="background: #ffffff; padding: 100px 0;">
        <div class="container">
            <div class="row align-items-center gy-5">
                <div class="col-lg-5" data-aos="fade-right">
                    <div class="about-img-container position-relative">
                        <div class="experience-badge shadow" style="position:absolute; bottom:-20px; right:0; background:white; padding:20px; border-radius:50%; border:2px dashed var(--primary-accent); z-index:5;">
                            <h4 class="mb-0 fw-bold text-gradient">HAI</h4>
                            <span class="small">It's Me</span>
                        </div>
                        <img src="1.jpeg" alt="About Feyza" class="w-100 rounded-4 shadow-lg">
                    </div>
                </div>
                <div class="col-lg-7 px-lg-5" data-aos="fade-left">
                    <h5 class="text-gradient fw-bold text-uppercase mb-3">::: I'M A DEVELOPER</h5>
                    <h2 class="display-5 fw-bold mb-4">I Develop Ideas That Help People</h2>
                    <p class="text-muted mb-5">Sebagai mahasiswi tingkat akhir Sistem Informasi Industri Otomotif, saya memiliki dedikasi tinggi dalam mengimplementasikan algoritma Data Mining untuk memecahkan masalah nyata di industri.</p>
                    
                    <ul class="nav nav-tabs border-0 gap-3 mb-4" id="aboutTab" role="tablist">
                        <li class="nav-item"><button class="nav-link active rounded-pill px-4 shadow-sm" data-bs-toggle="tab" data-bs-target="#details" type="button">MY DETAILS</button></li>
                        <li class="nav-item"><button class="nav-link rounded-pill px-4 shadow-sm" data-bs-toggle="tab" data-bs-target="#experience" type="button">EXPERIENCE</button></li>
                    </ul>
                    <div class="tab-content" id="aboutTabContent">
                        <div class="tab-pane fade show active" id="details">
                            <div class="row g-4">
                                <div class="col-sm-6"><label class="small text-muted d-block">My Name:</label><span class="fw-bold">Feyza Revalina</span></div>
                                <div class="col-sm-6"><label class="small text-muted d-block">My Email:</label><span class="fw-bold text-break">feyzarevalina@gmail.com</span></div>
                                <div class="col-sm-6"><label class="small text-muted d-block">Address:</label><span class="fw-bold">Jakarta, Indonesia</span></div>
                            </div>
                        </div>
                        <div class="tab-pane fade" id="experience">
                            <div class="mb-4">
                                <h6 class="fw-bold mb-1">Kepala Sub Divisi PSDM - HIMASIS</h6>
                                <p class="text-gradient small fw-bold">2025 - Present</p>
                            </div>
                            <div>
                                <h6 class="fw-bold mb-1">Staff Divisi Medinkom - HIMASIS</h6>
                                <p class="text-gradient small fw-bold">2024 - 2025</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="wave-container">
        <svg viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0,32L120,42.7C240,53,480,75,720,74.7C960,75,1200,53,1320,42.7L1440,32V0H0V32Z" fill="#ffffff"/>
        </svg>
    </div>

    <section id="skills" style="padding: 100px 0;">
        <div class="container text-center">
            <h2 class="fw-bold mb-5">My <span class="text-gradient">Specialized</span> Skills</h2>
            <div class="row g-4 justify-content-center">
                <div class="col-6 col-md-3" data-aos="zoom-in">
                    <div class="skill-card p-4 h-100">
                        <i class="bi bi-cpu fs-1 text-gradient"></i>
                        <h6 class="mt-3 fw-bold">Python Data Mining</h6>
                    </div>
                </div>
                <div class="col-6 col-md-3" data-aos="zoom-in" data-aos-delay="100">
                    <div class="skill-card p-4 h-100">
                        <i class="bi bi-bar-chart-steps fs-1 text-gradient"></i>
                        <h6 class="mt-3 fw-bold">DSS Analysis</h6>
                    </div>
                </div>
                <div class="col-6 col-md-3" data-aos="zoom-in" data-aos-delay="200">
                    <div class="skill-card p-4 h-100">
                        <i class="bi bi-diagram-3 fs-1 text-gradient"></i>
                        <h6 class="mt-3 fw-bold">Process Modeling</h6>
                    </div>
                </div>
                <div class="col-6 col-md-3" data-aos="zoom-in" data-aos-delay="300">
                    <div class="skill-card p-4 h-100">
                        <i class="bi bi-eye fs-1 text-gradient"></i>
                        <h6 class="mt-3 fw-bold">Object Detection</h6>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="wave-container">
        <svg viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0,64L80,69.3C160,75,320,85,480,80C640,75,800,53,960,48C1120,43,1280,53,1360,58.7L1440,64V120H0V64Z" fill="#ffffff"/>
        </svg>
    </div>

    <section id="projects" style="background: #ffffff; padding: 100px 0;">
        <div class="container">
            <h2 class="fw-bold display-5 mb-5 text-center">Featured Projects</h2>
            <div class="row g-4">
                <div class="col-md-6 col-lg-4" data-aos="fade-up">
                    <div class="project-card overflow-hidden h-100">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=600" class="w-100" alt="Inventory">
                        <div class="p-4">
                            <h5 class="fw-bold">Web Inventory System</h5>
                            <p class="small text-muted">Optimasi akurasi stok bahan menggunakan Laravel.</p>
                            <a href="https://github.com/feyfryvzn/DC_Inventory" class="btn btn-sm btn-outline-primary rounded-pill">View Code</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4" data-aos="fade-up" data-aos-delay="100">
                    <div class="project-card overflow-hidden h-100">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=600" class="w-100" alt="Furniture">
                        <div class="p-4">
                            <h5 class="fw-bold">IKM Furniture System</h5>
                            <p class="small text-muted">Digitalisasi transaksi penjualan dan pembelian IKM Furniture.</p>
                            <a href="https://github.com/feyfryvzn/SI-Penjualan-dan-Pembelian-Furniture" class="btn btn-sm btn-outline-primary rounded-pill">View Code</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="wave-container">
        <svg viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0,64L120,58.7C240,53,480,43,720,48C960,53,1200,75,1320,85.3L1440,96V0H0V64Z" fill="#ffffff"/>
        </svg>
    </div>

    <section id="contact" style="padding: 100px 0;">
        <div class="container">
            <div class="row g-5 align-items-center">
                <div class="col-lg-5" data-aos="fade-right">
                    <h2 class="display-4 fw-bold mb-4">Let's Work <span class="text-gradient">Together!</span></h2>
                    <p class="text-muted">Punya ide proyek menarik? Kirimkan pesan sekarang!</p>
                </div>
                <div class="col-lg-7" data-aos="fade-left">
                    <div class="contact-card p-4 p-md-5">
                        <form action="https://formspree.io/f/xpqdnvrb" method="POST">
                            <div class="row g-3">
                                <div class="col-md-6"><input type="text" name="name" class="form-control bg-light border-0 py-3" placeholder="Full Name" required></div>
                                <div class="col-md-6"><input type="email" name="email" class="form-control bg-light border-0 py-3" placeholder="Email" required></div>
                                <div class="col-12"><textarea name="message" class="form-control bg-light border-0 py-3" rows="4" placeholder="Your Message" required></textarea></div>
                                <div class="col-12 mt-4"><button type="submit" class="btn btn-primary w-100 py-3 shadow" style="background: var(--accent-dark); border:none; border-radius:15px;">Send Message <i class="bi bi-send-fill ms-2"></i></button></div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-5 text-center bg-white border-top">
        <h3 class="fw-bold">FEYZA<span class="text-gradient">.</span></h3>
        <p class="text-muted small mb-0">&copy; 2026 Feyza Revalina. Made with ❤️ in Jakarta</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script src="script.js"></script>
    <script>
        AOS.init({ duration: 1000, once: true });
    </script>
</body>
</html>
