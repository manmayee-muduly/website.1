# website.1
Centralised digital platform for comprehensive student  activity records for HEIs 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Odisha Scholarship Portal - Empowering Education</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        } 

        :root {
            --primary-color: #4a6bdf;
            --secondary-color: #f97316;
            --accent-color: #10b981;
            --text-dark: #1f2937;
            --text-light: #6b7280;
            --bg-light: #f9fafb;
            --white: #ffffff;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary-color), #6366f1);
            color: var(--white);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: var(--shadow);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .logo i {
            margin-right: 10px;
            font-size: 2rem;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            color: var(--white);
            text-decoration: none;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            border-bottom: 2px solid transparent;
        }

        nav ul li a:hover {
            border-bottom: 2px solid var(--white);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--white);
            padding: 4rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://picsum.photos/seed/education/1200/400.jpg') center/cover;
            opacity: 0.2;
            z-index: -1;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            animation: fadeInDown 1s ease;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            animation: fadeInUp 1s ease;
        }

        .search-box {
            max-width: 600px;
            margin: 0 auto;
            position: relative;
            animation: fadeIn 1.5s ease;
        }

        .search-box input {
            width: 100%;
            padding: 1rem 3rem 1rem 1.5rem;
            border-radius: 50px;
            border: none;
            font-size: 1rem;
            box-shadow: var(--shadow-lg);
        }

        .search-box button {
            position: absolute;
            right: 5px;
            top: 50%;
            transform: translateY(-50%);
            background: var(--secondary-color);
            color: var(--white);
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .search-box button:hover {
            background: #ea580c;
        }

        /* Filter Section */
        .filter-section {
            padding: 2rem 0;
            background: var(--white);
            box-shadow: var(--shadow);
            margin-bottom: 2rem;
        }

        .filter-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .filter-btn {
            padding: 0.5rem 1.5rem;
            background: var(--white);
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .filter-btn:hover, .filter-btn.active {
            background: var(--primary-color);
            color: var(--white);
        }

        /* Colleges Section */
        .colleges-section {
            padding: 3rem 0;
            background: var(--white);
            margin-bottom: 2rem;
        }

        .colleges-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .college-card {
            background: var(--white);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
            height: 100%;
        }

        .college-card:hover {
            transform: translateY(-8px);
            box-shadow: var(--shadow-lg);
        }

        .college-image {
            height: 160px;
            background: linear-gradient(135deg, var(--primary-color), #6366f1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 3rem;
        }

        .college-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .college-name {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--text-dark);
        }

        .college-type {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .college-link {
            display: inline-flex;
            align-items: center;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            margin-top: auto;
            transition: all 0.3s ease;
        }

        .college-link:hover {
            color: var(--secondary-color);
        }

        .college-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }

        .college-link:hover i {
            transform: translateX(5px);
        }

        /* Scholarship Cards */
        .scholarships-section {
            padding: 2rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 3rem;
            color: var(--text-dark);
            position: relative;
        }

        .section-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--secondary-color);
            border-radius: 2px;
        }

        .scholarship-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .scholarship-card {
            background: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            animation: fadeInUp 0.8s ease;
        }

        .scholarship-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .card-header {
            background: linear-gradient(135deg, var(--primary-color), #6366f1);
            color: var(--white);
            padding: 1.5rem;
            position: relative;
        }

        .card-header h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .card-header .badge {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: var(--secondary-color);
            color: var(--white);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        .card-body {
            padding: 1.5rem;
        }

        .card-section {
            margin-bottom: 1.5rem;
        }

        .card-section h4 {
            color: var(--primary-color);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
        }

        .card-section h4 i {
            margin-right: 0.5rem;
        }

        .card-section ul {
            list-style-type: none;
            padding-left: 1.5rem;
        }

        .card-section ul li {
            position: relative;
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
        }

        .card-section ul li::before {
            content: "•";
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-weight: bold;
        }

        .card-footer {
            padding: 1rem 1.5rem;
            background: var(--bg-light);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .apply-btn {
            background: var(--accent-color);
            color: var(--white);
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .apply-btn:hover {
            background: #059669;
            transform: scale(1.05);
        }

        .source-links {
            display: flex;
            gap: 0.5rem;
        }

        .source-link {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: var(--primary-color);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .source-link:hover {
            background: var(--secondary-color);
            transform: scale(1.1);
        }

        /* Footer */
        footer {
            background: var(--text-dark);
            color: var(--white);
            padding: 3rem 0 1rem;
            margin-top: 4rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section ul li a {
            color: #d1d5db;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section ul li a:hover {
            color: var(--secondary-color);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #374151;
            color: #9ca3af;
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }

            nav ul {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }

            nav ul li {
                margin: 0.5rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .scholarship-grid {
                grid-template-columns: 1fr;
            }

            .colleges-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-graduation-cap"></i>
                    <span>Odisha Scholarship Portal</span>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#colleges">Colleges</a></li>
                        <li><a href="#scholarships">Scholarships</a></li>
                        <li><a href="omps5.html">How to Apply</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Empowering Education Through Scholarships</h1>
            <p>Discover various scholarship opportunities in Odisha to support your educational journey. Find the right scholarship that matches your needs and eligibility.</p>
            <div class="search-box">
                <input type="text" id="searchInput" placeholder="Search for scholarships...">
                <button type="button" onclick="searchScholarships()"><i class="fas fa-search"></i></button>
            </div>
        </div>
    </section>

    <!-- Colleges Section -->
    <section class="colleges-section" id="colleges">
        <div class="container">
            <h2 class="section-title">Top Colleges in Odisha</h2>
            <div class="colleges-grid">
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">KIIT University</h3>
                        <p class="college-type">Private University</p>
                        <a href="https://kiit.ac.in" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">Rajdhani Engineering College</h3>
                        <p class="college-type">Engineering College</p>
                        <a href="https://www.rec.ac.in/" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">OUTR (CET Bhubaneswar)</h3>
                        <p class="college-type">Government University</p>
                        <a href="https://outr.ac.in" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">ITER (SOA University)</h3>
                        <p class="college-type">Private University</p>
                        <a href="https://soa.ac.in/iter" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">NIT Rourkela</h3>
                        <p class="college-type">Institute of National Importance</p>
                        <a href="https://nitrkl.ac.in" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">VSSUT Burla</h3>
                        <p class="college-type">Government University</p>
                        <a href="https://vssut.ac.in" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">CET Bhubaneswar</h3>
                        <p class="college-type">Government Engineering College</p>
                        <a href="https://cet.edu.in" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
                
                <div class="college-card">
                    <div class="college-image">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="college-content">
                        <h3 class="college-name">Silicon Institute of Technology</h3>
                        <p class="college-type">Engineering College</p>
                        <a href="https://silicon.ac.in" target="_blank" class="college-link">
                            Visit Website <i class="fas fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Filter Section -->
    <section class="filter-section">
        <div class="container">
            <div class="filter-container">
                <button class="filter-btn active" onclick="filterScholarships('all')">All Scholarships</button>
                <button class="filter-btn" onclick="filterScholarships('merit')">Merit Based</button>
                <button class="filter-btn" onclick="filterScholarships('need')">Need Based</button>
                <button class="filter-btn" onclick="filterScholarships('caste')">Caste Based</button>
                <button class="filter-btn" onclick="filterScholarships('language')">Language Based</button>
            </div>
        </div>
    </section>

    <!-- Scholarships Section -->
    <section class="scholarships-section" id="scholarships">
        <div class="container">
            <h2 class="section-title">Available Scholarships</h2>
            <div class="scholarship-grid">
                <!-- e-Medhabruti Scholarship -->
                <div class="scholarship-card" data-category="merit need">
                    <div class="card-header">
                        <h3>e-Medhabruti</h3>
                        <span class="badge">Popular</span>
                    </div>
                    <div class="card-body">
                        <div class="card-section">
                            <h4><i class="fas fa-bullseye"></i> Purpose</h4>
                            <p>Helps meritorious students in Odisha for higher/technical/professional education who need financial support.</p>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-check-circle"></i> Eligibility Criteria</h4>
                            <ul>
                                <li>Must be an Odisha resident</li>
                                <li>Must have achieved minimum 60% marks in previous qualifying exam</li>
                                <li>Parental/family income must be ≤ ₹6,00,000</li>
                                <li>Only in first year of course (for many categories)</li>
                                <li>Professional/technical courses included; distance education excluded</li>
                            </ul>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-rupee-sign"></i> Amount & Updates</h4>
                            <ul>
                                <li>Number of scholarships: ~14,500 each year</li>
                                <li>UG students: ~₹5,000/year</li>
                                <li>PG students: ~₹10,000/year</li>
                                <li>Technical/Professional courses: ~₹10,000/year</li>
                                <li>Recent update (2025-26): Total awarded ~same number, with fixed amounts each year</li>
                            </ul>
                        </div>
                    </div>
                    <div class="card-footer">
                        <a href="https://scholarship.odisha.gov.in" target="_blank" class="apply-btn">Apply Now</a>
                        <div class="source-links">
                            <a href="# " class="source-link" title="Buddy4Study"><i class="fas fa-link"></i></a>
                            <a href="# " class="source-link" title="Govt Schemes"><i class="fas fa-link"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Pre-Matric Scholarship -->
                <div class="scholarship-card" data-category="caste need">
                    <div class="card-header">
                        <h3>Pre-Matric Scholarship (SC/ST)</h3>
                        <span class="badge">Updated</span>
                    </div>
                    <div class="card-body">
                        <div class="card-section">
                            <h4><i class="fas fa-bullseye"></i> Purpose</h4>
                            <p>To help students from Scheduled Castes/Scheduled Tribes in school (upto class X) to continue education without financial hardship. Covers both boarders and day scholars.</p>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-check-circle"></i> Eligibility Criteria</h4>
                            <ul>
                                <li>Must come from SC or ST</li>
                                <li>Annual family income limit varies</li>
                                <li>Parents should not be Income Tax payers</li>
                                <li>Students in certain classes (often classes 9 & 10 for OBC pre-matric)</li>
                                <li>Must enroll in recognized school</li>
                            </ul>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-rupee-sign"></i> Amount & Updates</h4>
                            <ul>
                                <li>Monthly maintenance allowance for SC/ST boarders increased from ₹750 to ₹950 for boys</li>
                                <li>For girls: increased from ₹800 to ₹1,000</li>
                                <li>Additional ad-hoc/annual grant component in some cases</li>
                                <li>Covers about 5 lakh+ boarders under SC/ST pre-matric</li>
                            </ul>
                        </div>
                    </div>
                    <div class="card-footer">
                        <a href="https://scholarship.odisha.gov.in" target="_blank" class="apply-btn">Apply Now</a>
                        <div class="source-links">
                            <a href="# " class="source-link" title="Official Portal"><i class="fas fa-link"></i></a>
                            <a href="#  " class="source-link" title="News Source"><i class="fas fa-link"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Vyasakabi Fakir Mohan Bhasabruti Scholarship -->
                <div class="scholarship-card" data-category="merit language">
                    <div class="card-header">
                        <h3>VFMB Scholarship</h3>
                        <span class="badge">Language</span>
                    </div>
                    <div class="card-body">
                        <div class="card-section">
                            <h4><i class="fas fa-bullseye"></i> Purpose</h4>
                            <p>To promote the Odia language and provide support for students pursuing Odia Honours (UG) or MA in Odia (PG). Merit based.</p>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-check-circle"></i> Eligibility Criteria</h4>
                            <ul>
                                <li>Students must be studying in Odia language (Odia Honours in UG or Odia PG)</li>
                                <li>Need to satisfy merit criteria</li>
                                <li>Application via Odisha State Scholarship Portal</li>
                            </ul>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-rupee-sign"></i> Amount & Updates</h4>
                            <ul>
                                <li>One-time ₹20,000 scholarship per student</li>
                                <li>Around 1,500 scholarships per year</li>
                                <li>Distribution: ~1,200 for UG and ~300 for PG</li>
                            </ul>
                        </div>
                    </div>
                    <div class="card-footer">
                        <a href="https://scholarship.odisha.gov.in" target="_blank" class="apply-btn">Apply Now</a>
                        <div class="source-links">
                            <a href="# " class="source-link" title="Scholarship Portal"><i class="fas fa-link"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Anwesha Scholarship -->
                <div class="scholarship-card" data-category="caste need">
                    <div class="card-header">
                        <h3>Anwesha</h3>
                        <span class="badge">Special</span>
                    </div>
                    <div class="card-body">
                        <div class="card-section">
                            <h4><i class="fas fa-bullseye"></i> Purpose</h4>
                            <p>Special scheme for ST & SC students to improve access to quality education in urban areas — enabling them to attend better private/aided schools.</p>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-check-circle"></i> Eligibility Criteria</h4>
                            <ul>
                                <li>For ST/SC students</li>
                                <li>Admitted in Class I in certain partnered/private/Govt aided schools</li>
                                <li>Located in district headquarters/urban areas</li>
                                <li>Student continues up to Class X under this scheme</li>
                            </ul>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-rupee-sign"></i> Amount & Updates</h4>
                            <ul>
                                <li>Covers educational costs for selected students (tuition, additional support)</li>
                                <li>Usually in English-medium or better schools</li>
                                <li>Number of seats: ~5,000 students each year</li>
                            </ul>
                        </div>
                    </div>
                    <div class="card-footer">
                        <a href="https://scholarship.odisha.gov.in" target="_blank" class="apply-btn">Apply Now</a>
                        <div class="source-links">
                            <a href="# " class="source-link" title="ST/SC Portal"><i class="fas fa-link"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Mukhyamantri Medhabruti -->
                <div class="scholarship-card" data-category="merit need">
                    <div class="card-header">
                        <h3>Mukhyamantri Medhabruti</h3>
                        <span class="badge">Updated</span>
                    </div>
                    <div class="card-body">
                        <div class="card-section">
                            <h4><i class="fas fa-bullseye"></i> Purpose</h4>
                            <p>Odisha government recently increased the amounts awarded in many of the state scholarship programs to reduce financial burden.</p>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-check-circle"></i> Eligibility Criteria</h4>
                            <ul>
                                <li>The hike applies to both boys & girls in relevant categories</li>
                                <li>For post-matric and pre-matric scholarship categories</li>
                                <li>Transition done via official announcements</li>
                            </ul>
                        </div>
                        <div class="card-section">
                            <h4><i class="fas fa-rupee-sign"></i> Amount & Updates</h4>
                            <ul>
                                <li>Recent increases in scholarship amounts across categories</li>
                                <li>Aimed at reducing financial burden on students</li>
                                <li>Applicable for both pre-matric and post-matric scholarships</li>
                            </ul>
                        </div>
                    </div>
                    <div class="card-footer">
                        <a href="https://scholarship.odisha.gov.in" target="_blank" class="apply-btn">Apply Now</a>
                        <div class="source-links">
                            <a href="# " class="source-link" title="Shiksha Portal"><i class="fas fa-link"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About Us</h3>
                    <p>We are dedicated to providing comprehensive information about scholarship opportunities in Odisha to help students achieve their educational goals.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="# ">Home</a></li>
                        <li><a href="# ">All Scholarships</a></li>
                        <li><a href="# ">Application Process</a></li>
                        <li><a href="# ">FAQs</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="https://scholarship.odisha.gov.in" target="_blank">Odisha Scholarship Portal</a></li>
                        <li><a href="# ">Educational Guidelines</a></li>
                        <li><a href="# ">Contact Support</a></li>
                        <li><a href="# ">Terms & Conditions</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Connect With Us</h3>
                    <div style="display: flex; gap: 1rem; margin-top: 1rem;">
                        <a href="# " style="color: white; font-size: 1.5rem;"><i class="fab fa-facebook"></i></a>
                        <a href="# " style="color: white; font-size: 1.5rem;"><i class="fab fa-twitter"></i></a>
                        <a href="# " style="color: white; font-size: 1.5rem;"><i class="fab fa-instagram"></i></a>
                        <a href="# " style="color: white; font-size: 1.5rem;"><i class="fab fa-linkedin"></i></a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy;2023 Odisha Scholarship Portal. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Filter functionality
        function filterScholarships(category) {
            const cards = document.querySelectorAll('.scholarship-card');
            const buttons = document.querySelectorAll('.filter-btn');
            
            // Update active button
            buttons.forEach(btn => {
                btn.classList.remove('active');
                if (btn.textContent.toLowerCase().includes(category) || 
                    (category === 'all' && btn.textContent === 'All Scholarships')) {
                    btn.classList.add('active');
                }
            });
            
            // Show/hide cards based on category
            cards.forEach(card => {
                if (category === 'all' || card.dataset.category.includes(category)) {
                    card.style.display = 'block';
                    setTimeout(() => {
                        card.style.opacity = '1';
                        card.style.transform = 'translateY(0)';
                    }, 10);
                } else {
                    card.style.opacity = '0';
                    card.style.transform = 'translateY(20px)';
                    setTimeout(() => {
                        card.style.display = 'none';
                    }, 300);
                }
            });
        }

        // Search functionality
        function searchScholarships() {
            const searchTerm = document.getElementById('searchInput').value.toLowerCase();
            const cards = document.querySelectorAll('.scholarship-card');
            
            cards.forEach(card => {
                const text = card.textContent.toLowerCase();
                if (text.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Add event listener for Enter key in search box
        document.getElementById('searchInput').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                searchScholarships();
            }
        });

        // Add smooth scrolling to navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all scholarship cards and college cards
        document.querySelectorAll('.scholarship-card, .college-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(card);
        }); 



    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Dashboard | Activity Record System</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: "Segoe UI", sans-serif;
        }
        /* 🌨 Winter Chill Background */
        
        body {
            display: flex;
            min-height: 100vh;
            color: #333;
            background: linear-gradient(135deg, #dbeafe, #e0f2fe, #f0f9ff);
            background-attachment: fixed;
            background-size: cover;
        }
        /* Sidebar */
        
        aside {
            width: 250px;
            background: rgba(30, 58, 138, 0.9);
            color: white;
            height: 100vh;
            padding: 20px;
            position: fixed;
            backdrop-filter: blur(6px);
            box-shadow: 2px 0 10px rgba(0, 0, 0, 0.2);
        }
        
        aside h2 {
            font-size: 20px;
            margin-bottom: 15px;
            text-align: center;
        }
        
        aside ul {
            list-style: none;
        }
        
        aside ul li {
            margin: 10px 0;
        }
        
        aside ul li a {
            color: white;
            text-decoration: none;
            display: block;
            padding: 8px 10px;
            border-radius: 6px;
            transition: background 0.3s;
        }
        
        aside ul li a:hover {
            background: rgba(37, 99, 235, 0.9);
        }
        /* Main Area */
        
        main {
            margin-left: 270px;
            padding: 20px;
            width: calc(100% - 270px);
        }
        /* Frosted Glass Section Styling ❄ */
        
        section {
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.4);
        }
        
        h2 {
            margin-bottom: 10px;
            color: #1e3a8a;
        }
        
        h3 {
            color: #2563eb;
            margin-top: 10px;
        }
        
        .profile-info div {
            margin-bottom: 6px;
        }
        
        input,
        select,
        textarea {
            width: 100%;
            padding: 8px;
            margin: 6px 0 12px;
            border: 1px solid #ccc;
            border-radius: 6px;
        }
        
        button {
            background: #2563eb;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: 0.3s;
        }
        
        button:hover {
            background: #1e40af;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        
        th,
        td {
            border: 1px solid #ccc;
            padding: 8px;
            text-align: left;
        }
        
        th {
            background: #e2e8f0;
        }
        
        .filter-bar {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .progress {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        .progress div {
            flex: 1;
            background: rgba(226, 232, 240, 0.8);
            border-radius: 6px;
            padding: 10px;
        }
        
        .chart {
            height: 150px;
            background: rgba(241, 245, 249, 0.7);
            border-radius: 8px;
            margin-top: 10px;
            backdrop-filter: blur(8px);
        }
        
        .notification {
            background: rgba(254, 249, 195, 0.8);
            padding: 10px;
            border-radius: 8px;
            margin: 6px 0;
        }
        
        .support-links a {
            color: #2563eb;
            text-decoration: none;
        }
        
        footer {
            text-align: center;
            font-size: 13px;
            color: #555;
            margin-top: 20px;
        }
    </style>
</head>

<body>

    <aside>
        <h2>🎓 Student Panel</h2>
        <ul>
            <li><a href="#profile">Profile</a></li>
            <li><a href="#activity-log">Log Activity</a></li>
            <li><a href="#records">My Records</a></li>
            <li><a href="#status">Status Tracking</a></li>
            <li><a href="#progress">Progress Tracker</a></li>
            <li><a href="#analytics">Analytics & Reports</a></li>
            <li><a href="#feedback">Faculty Feedback</a></li>
            <li><a href="#events">Upcoming Events</a></li>
            <li><a href="#notifications">Notifications</a></li>
            <li><a href="#support">Support & Help</a></li>
            <li><a href="#settings">Settings</a></li>
        </ul>
    </aside>

    <main>
        <!-- Profile -->
        <section id="profile">
            <h2>🔐 Login & Profile Section</h2>
            <div class="profile-info">
                <div><strong>Name:</strong> John Doe</div>
                <div><strong>Roll No:</strong> 2025CS001</div>
                <div><strong>Course:</strong> B.Tech Computer Science</div>
                <div><strong>Department:</strong> CSE</div>
                <div><strong>Year:</strong> 3rd Year</div>
                <div><strong>Email:</strong> johndoe@university.edu</div>
                <div><strong>Contact:</strong> +91 9876543210</div>
            </div>
            <button>Edit / Update Profile</button>
            <button style="background:#dc2626;">Logout</button>
        </section>

        <!-- Activity Logging -->
        <section id="activity-log">
            <h2>📝 Activity Logging Module</h2>
            <form>
                <label>Activity Title</label>
                <input type="text" placeholder="Enter activity title">
                <label>Type of Activity</label>
                <select>
        <option>Academic</option><option>Co-Curricular</option><option>Extra-Curricular</option>
        <option>Volunteer</option><option>Research</option><option>Innovation</option>
        <option>Sports</option><option>Cultural</option>
      </select>
                <label>Date & Duration</label>
                <input type="date">
                <input type="text" placeholder="Duration (e.g., 2 hours)">
                <label>Description / Learning Outcome</label>
                <textarea rows="3" placeholder="Write details..."></textarea>
                <label>Upload Evidence</label>
                <input type="file">
                <label>Tags / Skills</label>
                <input type="text" placeholder="Leadership, Communication...">
                <label>Faculty Validator</label>
                <select>
        <option>Prof. A. Sharma</option><option>Prof. R. Nair</option><option>Prof. M. Singh</option>
      </select>
                <button>➕ Add New Activity</button>
                <button type="button" style="background:#9ca3af;">💾 Save as Draft</button>
                <button type="button">📤 Submit for Validation</button>
            </form>
        </section>

        <!-- Records -->
        <section id="records">
            <h2>📊 My Activity Records</h2>
            <div class="filter-bar">
                <select><option>All Types</option></select>
                <select><option>Academic Year</option></select>
                <select><option>Status</option></select>
            </div>
            <table>
                <tr>
                    <th>Activity Name</th>
                    <th>Type</th>
                    <th>Date</th>
                    <th>Status</th>
                    <th>Faculty Remarks</th>
                    <th>Points</th>
                </tr>
                <tr>
                    <td>Hackathon 2025</td>
                    <td>Innovation</td>
                    <td>2025-08-12</td>
                    <td>Approved</td>
                    <td>Excellent work</td>
                    <td>20</td>
                </tr>
                <tr>
                    <td>Tech Seminar</td>
                    <td>Academic</td>
                    <td>2025-06-21</td>
                    <td>Pending</td>
                    <td>–</td>
                    <td>–</td>
                </tr>
            </table>
        </section>

        <!-- Status -->
        <section id="status">
            <h2>🔍 Activity Status Tracking</h2>
            <div class="notification">Hackathon 2025 – ✅ Approved by Prof. Sharma</div>
            <div class="notification">Tech Seminar – ⏳ Under Review by Prof. Nair</div>
        </section>

        <!-- Progress -->
        <section id="progress">
            <h2>🗂 Categories & Progress Tracker</h2>
            <div class="progress">
                <div>Academic: 70%</div>
                <div>Co-Curricular: 60%</div>
                <div>Extra-Curricular: 45%</div>
            </div>
            <p>Badges Earned: 🥇 Innovation Star, 🎯 Consistent Performer</p>
        </section>

        <!-- Analytics -->
        <section id="analytics">
            <h2>🧮 Analytics & Reports</h2>
            <div class="chart">[Chart Placeholder: Activities per Semester]</div>
            <div class="chart">[Chart Placeholder: Engagement by Category]</div>
            <button>⬇ Download PDF Report</button>
            <button>⬇ Export to Excel</button>
        </section>

        <!-- Feedback -->
        <section id="feedback">
            <h2>💬 Faculty Feedback</h2>
            <div class="notification">Prof. Sharma commented on “Hackathon 2025”: Excellent presentation.</div>
            <div class="notification">Prof. Nair requested resubmission for “Tech Seminar”.</div>
        </section>

        <!-- Events -->
        <section id="events">
            <h2>📅 Upcoming Events / Opportunities</h2>
            <ul>
                <li>AI Workshop – 21 Oct 2025 <button>Register Now</button></li>
                <li>Annual Sports Meet – 28 Oct 2025 <button>Register Now</button></li>
                <li>National NSS Camp – Nov 2025 <button>Register Now</button></li>
            </ul>
        </section>

        <!-- Notifications -->
        <section id="notifications">
            <h2>🔔 Notification Center</h2>
            <div class="notification">Your “Hackathon 2025” activity was approved ✅</div>
            <div class="notification">System Update: Platform maintenance scheduled on 25 Oct.</div>
            <div class="notification">Reminder: Submit your Semester Activity Report by 31 Oct.</div>
        </section>

        <!-- Support -->
        <section id="support">
            <h2>🧰 Support & Help</h2>
            <div class="support-links">
                <a href="#">📘 User Manual</a> |
                <a href="#">🔁 Reset Password</a> |
                <a href="#">🐞 Report Issue</a>
            </div>
            <p style="margin-top:10px;">For further assistance, email: <b>support@university.edu</b></p>
        </section>

        <!-- Settings -->
        <section id="settings">
            <h2>⚙ Settings & Account Management</h2>
            <label>Change Password</label>
            <input type="password" placeholder="Enter new password">
            <label>Notification Preferences</label>
            <select><option>Email</option><option>SMS</option><option>Both</option></select>
            <label><input type="checkbox"> I accept the privacy policy and terms.</label>
            <button>Save Settings</button>
        </section>

        <footer>© 2025 Centralized Student Activity Platform | Designed for HEIs</footer>
    </main>
    <li><a href="test3.html">Upcoming Events</a></li>


</body>

</html>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Dashboard | Activity Record System</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: "Segoe UI", sans-serif;
        }
        /* 🌨 Winter Chill Background */
        
        body {
            display: flex;
            min-height: 100vh;
            color: #333;
            background: linear-gradient(135deg, #dbeafe, #e0f2fe, #f0f9ff);
            background-attachment: fixed;
            background-size: cover;
        }
        /* Sidebar */
        
        aside {
            width: 250px;
            background: rgba(30, 58, 138, 0.9);
            color: white;
            height: 100vh;
            padding: 20px;
            position: fixed;
            backdrop-filter: blur(6px);
            box-shadow: 2px 0 10px rgba(0, 0, 0, 0.2);
        }
        
        aside h2 {
            font-size: 20px;
            margin-bottom: 15px;
            text-align: center;
        }
        
        aside ul {
            list-style: none;
        }
        
        aside ul li {
            margin: 10px 0;
        }
        
        aside ul li a {
            color: white;
            text-decoration: none;
            display: block;
            padding: 8px 10px;
            border-radius: 6px;
            transition: background 0.3s;
        }
        
        aside ul li a:hover {
            background: rgba(37, 99, 235, 0.9);
        }
        /* Main Area */
        
        main {
            margin-left: 270px;
            padding: 20px;
            width: calc(100% - 270px);
        }
        /* Frosted Glass Section Styling ❄ */
        
        section {
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.4);
        }
        
        h2 {
            margin-bottom: 10px;
            color: #1e3a8a;
        }
        
        h3 {
            color: #2563eb;
            margin-top: 10px;
        }
        
        .profile-info div {
            margin-bottom: 6px;
        }
        
        input,
        select,
        textarea {
            width: 100%;
            padding: 8px;
            margin: 6px 0 12px;
            border: 1px solid #ccc;
            border-radius: 6px;
        }
        
        button {
            background: #2563eb;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: 0.3s;
        }
        
        button:hover {
            background: #1e40af;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        
        th,
        td {
            border: 1px solid #ccc;
            padding: 8px;
            text-align: left;
        }
        
        th {
            background: #e2e8f0;
        }
        
        .filter-bar {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .progress {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        .progress div {
            flex: 1;
            background: rgba(226, 232, 240, 0.8);
            border-radius: 6px;
            padding: 10px;
        }
        
        .chart {
            height: 150px;
            background: rgba(241, 245, 249, 0.7);
            border-radius: 8px;
            margin-top: 10px;
            backdrop-filter: blur(8px);
        }
        
        .notification {
            background: rgba(254, 249, 195, 0.8);
            padding: 10px;
            border-radius: 8px;
            margin: 6px 0;
        }
        
        .support-links a {
            color: #2563eb;
            text-decoration: none;
        }
        
        footer {
            text-align: center;
            font-size: 13px;
            color: #555;
            margin-top: 20px;
        }
    </style>
</head>

<body>

    <aside>
        <h2>🎓 Student Panel</h2>
        <ul>
            <li><a href="#profile">Profile</a></li>
            <li><a href="#activity-log">Log Activity</a></li>
            <li><a href="#records">My Records</a></li>
            <li><a href="#status">Status Tracking</a></li>
            <li><a href="#progress">Progress Tracker</a></li>
            <li><a href="#analytics">Analytics & Reports</a></li>
            <li><a href="#feedback">Faculty Feedback</a></li>
            <li><a href="#events">Upcoming Events</a></li>
            <li><a href="#notifications">Notifications</a></li>
            <li><a href="#support">Support & Help</a></li>
            <li><a href="#settings">Settings</a></li>
        </ul>
    </aside>

    <main>
        <!-- Profile -->
        <section id="profile">
            <h2>🔐 Login & Profile Section</h2>
            <div class="profile-info">
                <div><strong>Name:</strong> John Doe</div>
                <div><strong>Roll No:</strong> 2025CS001</div>
                <div><strong>Course:</strong> B.Tech Computer Science</div>
                <div><strong>Department:</strong> CSE</div>
                <div><strong>Year:</strong> 3rd Year</div>
                <div><strong>Email:</strong> johndoe@university.edu</div>
                <div><strong>Contact:</strong> +91 9876543210</div>
            </div>
            <button>Edit / Update Profile</button>
            <button style="background:#dc2626;">Logout</button>
        </section>

        <!-- Activity Logging -->
        <section id="activity-log">
            <h2>📝 Activity Logging Module</h2>
            <form>
                <label>Activity Title</label>
                <input type="text" placeholder="Enter activity title">
                <label>Type of Activity</label>
                <select>
        <option>Academic</option><option>Co-Curricular</option><option>Extra-Curricular</option>
        <option>Volunteer</option><option>Research</option><option>Innovation</option>
        <option>Sports</option><option>Cultural</option>
      </select>
                <label>Date & Duration</label>
                <input type="date">
                <input type="text" placeholder="Duration (e.g., 2 hours)">
                <label>Description / Learning Outcome</label>
                <textarea rows="3" placeholder="Write details..."></textarea>
                <label>Upload Evidence</label>
                <input type="file">
                <label>Tags / Skills</label>
                <input type="text" placeholder="Leadership, Communication...">
                <label>Faculty Validator</label>
                <select>
        <option>Prof. A. Sharma</option><option>Prof. R. Nair</option><option>Prof. M. Singh</option>
      </select>
                <button>➕ Add New Activity</button>
                <button type="button" style="background:#9ca3af;">💾 Save as Draft</button>
                <button type="button">📤 Submit for Validation</button>
            </form>
        </section>

        <!-- Records -->
        <section id="records">
            <h2>📊 My Activity Records</h2>
            <div class="filter-bar">
                <select><option>All Types</option></select>
                <select><option>Academic Year</option></select>
                <select><option>Status</option></select>
            </div>
            <table>
                <tr>
                    <th>Activity Name</th>
                    <th>Type</th>
                    <th>Date</th>
                    <th>Status</th>
                    <th>Faculty Remarks</th>
                    <th>Points</th>
                </tr>
                <tr>
                    <td>Hackathon 2025</td>
                    <td>Innovation</td>
                    <td>2025-08-12</td>
                    <td>Approved</td>
                    <td>Excellent work</td>
                    <td>20</td>
                </tr>
                <tr>
                    <td>Tech Seminar</td>
                    <td>Academic</td>
                    <td>2025-06-21</td>
                    <td>Pending</td>
                    <td>–</td>
                    <td>–</td>
                </tr>
            </table>
        </section>

        <!-- Status -->
        <section id="status">
            <h2>🔍 Activity Status Tracking</h2>
            <div class="notification">Hackathon 2025 – ✅ Approved by Prof. Sharma</div>
            <div class="notification">Tech Seminar – ⏳ Under Review by Prof. Nair</div>
        </section>

        <!-- Progress -->
        <section id="progress">
            <h2>🗂 Categories & Progress Tracker</h2>
            <div class="progress">
                <div>Academic: 70%</div>
                <div>Co-Curricular: 60%</div>
                <div>Extra-Curricular: 45%</div>
            </div>
            <p>Badges Earned: 🥇 Innovation Star, 🎯 Consistent Performer</p>
        </section>

        <!-- Analytics -->
        <section id="analytics">
            <h2>🧮 Analytics & Reports</h2>
            <div class="chart">[Chart Placeholder: Activities per Semester]</div>
            <div class="chart">[Chart Placeholder: Engagement by Category]</div>
            <button>⬇ Download PDF Report</button>
            <button>⬇ Export to Excel</button>
        </section>

        <!-- Feedback -->
        <section id="feedback">
            <h2>💬 Faculty Feedback</h2>
            <div class="notification">Prof. Sharma commented on “Hackathon 2025”: Excellent presentation.</div>
            <div class="notification">Prof. Nair requested resubmission for “Tech Seminar”.</div>
        </section>

        <!-- Events -->
        <section id="events">
            <h2>📅 Upcoming Events / Opportunities</h2>
            <ul>
                <li>AI Workshop – 21 Oct 2025 <button>Register Now</button></li>
                <li>Annual Sports Meet – 28 Oct 2025 <button>Register Now</button></li>
                <li>National NSS Camp – Nov 2025 <button>Register Now</button></li>
            </ul>
        </section>

        <!-- Notifications -->
        <section id="notifications">
            <h2>🔔 Notification Center</h2>
            <div class="notification">Your “Hackathon 2025” activity was approved ✅</div>
            <div class="notification">System Update: Platform maintenance scheduled on 25 Oct.</div>
            <div class="notification">Reminder: Submit your Semester Activity Report by 31 Oct.</div>
        </section>

        <!-- Support -->
        <section id="support">
            <h2>🧰 Support & Help</h2>
            <div class="support-links">
                <a href="#">📘 User Manual</a> |
                <a href="#">🔁 Reset Password</a> |
                <a href="#">🐞 Report Issue</a>
            </div>
            <p style="margin-top:10px;">For further assistance, email: <b>support@university.edu</b></p>
        </section>

        <!-- Settings -->
        <section id="settings">
            <h2>⚙ Settings & Account Management</h2>
            <label>Change Password</label>
            <input type="password" placeholder="Enter new password">
            <label>Notification Preferences</label>
            <select><option>Email</option><option>SMS</option><option>Both</option></select>
            <label><input type="checkbox"> I accept the privacy policy and terms.</label>
            <button>Save Settings</button>
        </section>

        <footer>© 2025 Centralized Student Activity Platform | Designed for HEIs</footer>
    </main>
    <li><a href="test3.html">Upcoming Events</a></li>


</body>

</html>


