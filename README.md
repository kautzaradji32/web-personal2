<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio kautzar</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
            text-align: center; /* Menambahkan ini untuk rata tengah */
        }

        /* Header */
        header {
            background-color: #fff;
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 1px 5px rgba(0, 0, 0, 0.1);
        }

        .logo {
            font-size: 1.5em;
            font-weight: bold;
            color: #333;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center; /* Menambahkan ini untuk rata tengah */
        }

        nav li {
            margin-left: 20px;
        }

        nav a {
            text-decoration: none;
            color: #555;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #007bff;
        }

        /* Bagian Perkenalan (Halo, It's Me) */
        .intro-section {
            background-color: #222;
            color: #fff;
            padding: 80px 20px;
            display: flex;
            justify-content: space-around;
            align-items: center;
            background-image: url('background-city.jpg'); /* Ganti dengan gambar latar belakang Anda */
            background-size: cover;
            background-position: center;
            position: relative;
            overflow: hidden;
            text-align: center; /* Menambahkan ini untuk rata tengah */
        }

        .intro-text {
            text-align: center; /* Mengubah ini menjadi center */
            max-width: 500px;
            margin: 0 auto; /* Menambahkan ini untuk rata tengah horizontal */
        }

        .intro-text h2 {
            font-size: 2.5em;
            margin-bottom: 10px;
            color: #eee;
        }

        .intro-text h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            color: #eee;
        }

        .intro-text p {
            font-size: 1.1em;
            color: #ccc;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .social-icons {
            text-align: center; /* Menambahkan ini untuk rata tengah */
        }

        .social-icons a {
            display: inline-block;
            margin-right: 15px;
            font-size: 1.5em;
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .social-icons a:hover {
            color: #ffc107; /* Warna aksen */
        }

        .download-cv-button {
            display: inline-block;
            padding: 10px 20px;
            background-color: transparent;
            color: #ffc107;
            border: 2px solid #ffc107;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 20px;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .download-cv-button:hover {
            background-color: #ffc107;
            color: #222;
        }

        .profile-image-container {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            overflow: hidden;
            border: 5px solid #ffc107;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
            margin: 0 auto; /* Menambahkan ini untuk rata tengah horizontal */
        }

        .profile-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        /* Hero Section (Judul dan Deskripsi Proyek) */
        .hero {
            text-align: center;
            padding: 80px 20px;
            max-width: 960px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            color: #333;
        }

        .hero p {
            font-size: 1.1em;
            color: #666;
            line-height: 1.6;
        }

        /* Bagian Proyek */
        .projects-container {
            max-width: 960px;
            margin: 20px auto;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .project-card {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            transition: transform 0.3s ease-in-out;
            margin: 0 auto; /* Menambahkan ini untuk rata tengah horizontal */
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-image {
            width: 100%;
            height: auto;
            display: block;
        }

        .project-info {
            padding: 15px;
            text-align: center;
        }

        .project-title {
            font-size: 1.2em;
            margin-bottom: 5px;
            color: #333;
        }

        /* Bagian Teknologi yang Dikuasai */
        .skills-container {
            max-width: 800px;
            margin: 40px auto;
        }

        .skills-container h2 {
            text-align: center;
            color: #333;
            margin-bottom: 20px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 15px;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .skill-card {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 15px;
            border: 1px solid #eee;
            border-radius: 6px;
            text-align: center;
            transition: transform 0.3s ease-in-out;
            margin: 0 auto; /* Menambahkan ini untuk rata tengah horizontal */
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        .skill-image {
            width: 60px;
            height: 60px;
            margin-bottom: 10px;
        }

        .skill-name {
            font-size: 0.9em;
            color: #555;
        }

        /* Bagian Kontak */
        #contact {
            text-align: center;
            padding: 40px 20px;
        }

        #contact h2 {
            color: #333;
            margin-bottom: 20px;
        }

        #contact p {
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .contact-icons a {
            display: inline-block;
            margin: 0 10px;
            font-size: 1.5em;
            color: #555;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-icons a:hover {
            color: #007bff;
        }

        /* Footer (jika ada) */
        footer {
            text-align: center;
            padding: 20px;
            background-color: #333;
            color: #fff;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">Portofolio</div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#project">Project</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="intro-section" id="home">
        <div class="intro-text">
            <h2>Halo, It's Me</h2>
            <h1>ADJI PRAMUDYA KAUTZAR</h1>
            <p>And I am a <span style="color: #ffc107;">TEACHER</span> | Changing students to be moral, and students to have extensive knowledge about computers.</p>
            <div class="social-icons">
                <a href="#" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" target="_blank" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
                <a href="#" target="_blank" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="#" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a> </div>
            
            </div>
            <a href="c:\Users\kautzar\Documents\web sekolahan\CV Resume Pekerjaan Manajer Sosial Media Modern Krem dan Biru.pdf" class="download-cv-button" download="CV Adji Pramudya Kautzar.pdf">Download CV</a>
        </div>
        <div class="profile-image-container">
            <img src="https://www.pabuvestindo.co.id/wp-content/uploads/2019/06/Mikrotik-Router-indoor-RB4011iGSRM.jpg" alt="Logo Profil Adji Pramudya Kautzar" class="profile-image">
        </div>
    </section>

    <section class="hero" id="project">
        <h1>My Project</h1>
        <p>Kumpulan karya terbaik saya yang menunjukkan keahlian dalam pengembangan jaringan sekolah. Mulai dari desain canva yang menarik hingga microsoft office yang kompleks — semua proyek ini adalah bukti nyata dari semangat dan keahlian saya di dunia teknologi.</p>
    </section>

    <section id="about">
        <h2>Tentang Saya</h2>
        <p>Informasi tentang diri saya bisa ditambahkan di sini.</p>
    <section class="projects-container">
        <div class="project-card">
            <img src="https://i0.wp.com/jogjahost.co.id/blog/wp-content/uploads/2021/06/image-53-1024x506.png" alt="Website Portfolio" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Desiner</h3>
            </div>
        </div>
        <div class="project-card">
            <img src="https://res.cloudinary.com/arkademi-tech/images/c_scale,w_436,h_271/f_auto,q_auto/v1665666049/Screenshot_8/Screenshot_8.jpg?_i=AA" alt="E-commerce App" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Microsoft Office</h3>
            </div>
        </div>
        <div class="project-card">
            <img src="https://winpoin.com/wp-content/uploads/2014/02/memperbaiki-windows-8-tanpa-install-ulang.jpg" alt="Aplikasi Kasir" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Instal Ulang</h3>
            </div>
        </div>
            <div class="project-card">
                <img src="c:\Users\kautzar\Documents\web sekolahan\mikrotik1.jpg" alt="Mikrotik" class="project-image">
                <div class="project-info">
                    <h3 class="project-title">Mikrotik</h3>
        </div>
    </section>

    <section class="skills-container" id="skills">
        <h2>Skill Yang Saya Kuasai</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTp-v37yR9vC3V-J95PgT4H399KOz1xamqTUQ&s"  alt="html" class="projek-image">

                <p class="skill-name">HTML</p>
            </div>
            <div class="skill-card">
                <img src="https://www.webhozz.com/blog/wp-content/uploads/2014/06/css.jpg" alt="CSS" class="skill-image">

                <p class="skill-name">CSS</p>
            </div>
            <div class="skill-card">
                <img src="https://static.wikia.nocookie.net/coding-help/images/6/69/JavaScript.png/revision/latest?cb=20230517123229"   alt="JavaScript" class="skill-image">

                <p class="skill-name">JavaScript</p>
            </div>
            <div class="skill-card">
                <img src="https://assets-us-01.kc-usercontent.com/a7507759-f4f5-0038-8fff-c1db251108c1/8d5f4c29-9265-4cd7-b0ce-1724660899fb/instal-ulang-windows-7-paling-mudah.jpg" alt="React JS" class="skill-image">

                <p class="skill-name">install ulang  </p>

            </div>
            <div class="skill-card">
                <img src="c:\Users\kautzar\Documents\web sekolahan\mikrotik1.jpg" alt="Mikrotik" class="skill-image">

                <p class="skill-name">Mikrotik</p>

        </div>
    </section>

    <section id="contact">
        <h2>Kontak</h2>
        <h1>085776689695</h1>
        <div class="contact-icons">
    
    </section>

    <footer>
    </footer>


</body>
</html>
