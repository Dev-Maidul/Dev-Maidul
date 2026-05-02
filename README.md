<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Md Maidul Islam · Full-Stack Developer</title>
  <!-- Font Awesome 6 for sharp icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #0b0f1c 0%, #1a1f33 100%);
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1.5rem;
      margin: 0;
      color: #e5e9f0;
    }

    /* main glass card with animated border glow */
    .resume-card {
      max-width: 1100px;
      width: 100%;
      background: rgba(18, 22, 40, 0.8);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border-radius: 3.5rem;
      padding: 2.8rem 2.5rem;
      box-shadow: 0 30px 50px rgba(0, 0, 0, 0.7), 0 0 0 1px rgba(74, 144, 226, 0.25);
      position: relative;
      overflow: hidden;
      transition: all 0.3s ease;
      animation: floatCard 6s infinite ease-in-out;
    }

    /* animated gradient border effect */
    .resume-card::before {
      content: "";
      position: absolute;
      top: -3px;
      left: -3px;
      right: -3px;
      bottom: -3px;
      border-radius: 3.7rem;
      background: linear-gradient(45deg, #4f8af7, #b44ff7, #f74f8a, #f7b44f);
      background-size: 300% 300%;
      z-index: -1;
      animation: rotateGlow 8s ease infinite;
      filter: blur(12px);
      opacity: 0.7;
    }

    @keyframes rotateGlow {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes floatCard {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
      100% { transform: translateY(0px); }
    }

    h1 {
      font-size: 2.9rem;
      font-weight: 700;
      background: linear-gradient(to right, #ffffff, #b1d0ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 0.25rem;
      letter-spacing: -0.5px;
      text-align: center;
      animation: fadeInUp 0.8s ease;
    }

    .subtitle {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.7rem 1.5rem;
      font-weight: 500;
      color: #b9c7e0;
      margin: 0.5rem 0 1rem;
      font-size: 1.1rem;
      animation: fadeInUp 0.9s ease;
    }

    .location-tag {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 1.2rem;
      color: #a0b5dd;
      margin-bottom: 1.5rem;
      font-style: italic;
      font-weight: 400;
      animation: fadeInUp 1s ease;
    }

    .contact-links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      gap: 1rem 2rem;
      margin: 1.2rem 0 1.8rem;
      background: rgba(255, 255, 255, 0.05);
      padding: 0.9rem 2rem;
      border-radius: 60px;
      backdrop-filter: blur(10px);
      animation: fadeInUp 1.1s ease;
    }

    .contact-links a {
      color: #c6d9ff;
      text-decoration: none;
      font-weight: 500;
      transition: all 0.25s;
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }

    .contact-links a:hover {
      color: #ffffff;
      text-shadow: 0 0 12px #4f8af7;
      transform: translateY(-2px);
    }

    hr {
      border: 0.5px solid rgba(255, 255, 255, 0.1);
      margin: 1.8rem 0 2rem;
    }

    .banner {
      border-radius: 2rem;
      overflow: hidden;
      margin: 1.2rem 0 2rem;
      box-shadow: 0 18px 30px -8px rgba(0,0,0,0.7);
      transition: transform 0.3s ease;
      animation: fadeInUp 1.2s ease;
    }

    .banner:hover {
      transform: scale(1.01);
    }

    .banner img {
      width: 100%;
      display: block;
      border-radius: 2rem;
    }

    h2 {
      font-size: 1.8rem;
      font-weight: 650;
      margin: 1.8rem 0 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.7rem;
      background: linear-gradient(135deg, #d6e4ff, #ffffff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      border-left: 4px solid #4f8af7;
      padding-left: 1.1rem;
    }

    .summary-text {
      font-size: 1.15rem;
      line-height: 1.7;
      color: #cfdbf5;
      background: rgba(12, 18, 34, 0.55);
      padding: 1.5rem 1.8rem;
      border-radius: 2rem;
      backdrop-filter: blur(12px);
      margin-bottom: 1.5rem;
      transition: 0.3s;
      animation: fadeInUp 1s ease;
    }

    .badge-container {
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
      margin: 1rem 0 1.8rem;
    }

    .badge-container img {
      transition: all 0.25s ease;
      cursor: default;
      filter: drop-shadow(0 4px 6px black);
    }

    .badge-container img:hover {
      transform: translateY(-5px) scale(1.05);
      filter: drop-shadow(0 10px 12px #3b5998);
    }

    .experience-grid, .education-grid {
      display: flex;
      flex-direction: column;
      gap: 1.4rem;
      margin: 1.2rem 0 1.8rem;
    }

    .exp-item, .edu-item {
      background: rgba(20, 26, 45, 0.6);
      backdrop-filter: blur(10px);
      border-radius: 1.8rem;
      padding: 1.5rem 1.8rem;
      border: 1px solid rgba(79, 138, 247, 0.25);
      transition: all 0.3s ease;
      animation: fadeInUp 0.8s ease;
    }

    .exp-item:hover, .edu-item:hover {
      border-color: #4f8af7;
      box-shadow: 0 12px 28px rgba(79, 138, 247, 0.3);
      transform: translateY(-4px);
    }

    .exp-title {
      font-weight: 700;
      font-size: 1.35rem;
      color: white;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }

    .date {
      color: #9bb5f0;
      font-weight: 500;
    }

    .languages {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
      margin-top: 1rem;
    }

    .focus-list {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      gap: 1rem 2rem;
      margin-top: 1rem;
    }

    .focus-list li i {
      color: #4f8af7;
      margin-right: 0.5rem;
    }

    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(25px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .interactive-icon {
      transition: 0.2s;
      cursor: pointer;
    }

    .interactive-icon:hover {
      color: #f7b44f;
    }

    @media (max-width: 650px) {
      .resume-card {
        padding: 2rem 1.5rem;
      }
    }
  </style>
</head>
<body>
  <div class="resume-card">
    
    <!-- Name with interactive animation -->
    <h1>✨ Md Maidul Islam — Full-Stack Developer</h1>
    
    <div class="subtitle">
      <span><i class="fas fa-laptop-code"></i> Computer Science Undergraduate</span>
      <span>⚡ Full-Stack Engineer</span>
      <span>📘 Technical Educator</span>
    </div>

    <div class="location-tag">
      <span><i class="fas fa-map-pin"></i> Beijing, China</span>
      <span><i class="fas fa-globe-asia"></i> Bangladeshi Expatriate</span>
      <span><i class="fas fa-briefcase"></i> Open to Remote & Global</span>
    </div>

    <div class="contact-links">
      <a href="mailto:maidulislammanik8991@gmail.com"><i class="fas fa-envelope"></i> maidulislammanik8991@gmail.com</a>
      <a href="tel:+8613161750176"><i class="fas fa-phone-alt"></i> +86 131 6175 0176</a>
    </div>

    <div class="contact-links" style="margin-top: 0.2rem; background: rgba(79,138,247,0.1);">
      <a href="https://github.com/Dev-Maidul" target="_blank"><i class="fab fa-github"></i> GitHub</a>
      <a href="https://www.linkedin.com/in/maidul-devs/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
      <a href="https://maiduldevs.netlify.app/" target="_blank"><i class="fas fa-external-link-alt"></i> Portfolio</a>
      <a href="https://codeforces.com/profile/Maidul" target="_blank"><i class="fas fa-code"></i> Codeforces</a>
      <a href="https://leetcode.com/u/maidulislammanik8991/" target="_blank"><i class="fas fa-terminal"></i> LeetCode</a>
      <a href="https://www.upwork.com/freelancers/~01a039892954a8969f?mp_source=share" target="_blank"><i class="fab fa-upwork"></i> Upwork</a>
    </div>

    <hr>

    <!-- Banner with hover animation -->
    <div class="banner">
      <img src="https://raw.githubusercontent.com/Dev-Maidul/Dev-Maidul/main/github-banner.png" alt="Md Maidul Islam Full-Stack Developer Banner">
    </div>

    <hr>

    <!-- Professional Summary with animated entrance -->
    <h2><i class="fas fa-bullseye"></i> Professional Summary</h2>
    <div class="summary-text">
      <i class="fas fa-quote-left" style="margin-right: 0.5rem; color: #4f8af7;"></i>
      Computer Science undergraduate at <strong>China University of Petroleum</strong> with strong hands-on experience in <strong>full-stack web development</strong> and technical instruction. Skilled in building scalable, secure web applications using modern JavaScript frameworks. Actively seeking remote roles, internships, or contract opportunities in software engineering.
    </div>

    <!-- Technical Proficiencies with interactive badges -->
    <h2><i class="fas fa-cogs"></i> Technical Proficiencies</h2>
    <p style="color:#b4c4f0; margin-bottom: 0.2rem;"><i class="fas fa-brain"></i> AI & Machine Learning</p>
    <div class="badge-container">
      <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
      <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white">
      <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
      <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white">
    </div>
    
    <p style="color:#b4c4f0;"><i class="fas fa-paint-brush"></i> Frontend</p>
    <div class="badge-container">
      <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
      <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
      <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white">
    </div>

    <p style="color:#b4c4f0;"><i class="fas fa-server"></i> Backend & Databases</p>
    <div class="badge-container">
      <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white">
      <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white">
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white">
      <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white">
    </div>

    <p style="color:#b4c4f0;"><i class="fas fa-shield-alt"></i> Auth & Security</p>
    <div class="badge-container">
      <img src="https://img.shields.io/badge/Auth.js_(NextAuth)-000000?style=for-the-badge&logo=auth0&logoColor=white">
      <img src="https://img.shields.io/badge/OAuth_2.0-3C3C3D?style=for-the-badge&logo=openid&logoColor=white">
      <img src="https://img.shields.io/badge/JWT_Sessions-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">
    </div>

    <p style="color:#b4c4f0;"><i class="fas fa-cloud-upload-alt"></i> DevOps & Tools</p>
    <div class="badge-container">
      <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white">
      <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
      <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black">
      <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">
    </div>

    <!-- Professional Experience with hover effect -->
    <h2><i class="fas fa-briefcase"></i> Professional Experience</h2>
    <div class="experience-grid">
      <div class="exp-item">
        <div class="exp-title">
          <span><i class="fas fa-chalkboard-teacher"></i> Teaching Assistant – C Programming</span>
          <span class="date"><i class="far fa-calendar-alt"></i> Sep 2023 – Present</span>
        </div>
        <p style="margin-top: 0.8rem; color:#cddaf7;"><i class="fas fa-university"></i> China University of Petroleum</p>
        <ul style="margin-left: 1.8rem; margin-top: 0.8rem; list-style-type: none;">
          <li><i class="fas fa-user-graduate"></i> Mentored 150+ undergraduates in programming concepts</li>
          <li><i class="fas fa-bug"></i> Conducted debugging sessions & code reviews</li>
          <li><i class="fas fa-file-alt"></i> Developed lab exercises and learning materials</li>
        </ul>
      </div>
      <div class="exp-item">
        <div class="exp-title">
          <span><i class="fas fa-code"></i> Independent Full-Stack Developer</span>
          <span class="date"><i class="far fa-calendar-alt"></i> 2022 – Present</span>
        </div>
        <ul style="margin-left: 1.8rem; margin-top: 0.8rem; list-style-type: none;">
          <li><i class="fas fa-layer-group"></i> 10+ full-stack apps with MERN & Next.js</li>
          <li><i class="fas fa-key"></i> Auth, RBAC, REST APIs, production deployment</li>
        </ul>
      </div>
    </div>

    <!-- Education -->
    <h2><i class="fas fa-graduation-cap"></i> Education</h2>
    <div class="edu-item">
      <div class="exp-title">
        <span>🎓 B.Sc. Computer Science</span>
        <span class="date">Expected 2027</span>
      </div>
      <p style="margin-top: 0.3rem;">China University of Petroleum, Beijing</p>
      <p style="color:#b6c9f5; margin-top: 0.6rem;"><i class="fas fa-book"></i> Data Structures · DBMS · Software Eng · Web Tech · Networks · OOP</p>
    </div>

    <!-- Languages & Focus -->
    <h2><i class="fas fa-globe"></i> Languages & Focus</h2>
    <div style="display: flex; flex-wrap: wrap; gap: 2.5rem; background: rgba(0,0,0,0.2); border-radius: 2rem; padding: 1.2rem 1.8rem;">
      <div><strong>🗣️ Bengali</strong> Native · <strong>English</strong> Professional · <strong>中文</strong> Basic</div>
    </div>
    <div style="margin-top: 1.3rem;">
      <p><i class="fas fa-rocket"></i> <strong>Current focus:</strong> Advanced TypeScript, Cloud (AWS/Azure), Competitive Programming, Open Source</p>
    </div>

    <!-- Open to opportunities interactive section -->
    <h2><i class="fas fa-handshake"></i> Open to Opportunities</h2>
    <div style="display: flex; flex-wrap: wrap; gap: 1.2rem; justify-content: center; margin: 1rem 0 0.2rem;">
      <span style="background:#4f8af720; padding:0.6rem 1.5rem; border-radius:3rem;"><i class="fas fa-globe"></i> Remote full-stack roles</span>
      <span style="background:#4f8af720; padding:0.6rem 1.5rem; border-radius:3rem;"><i class="fas fa-file-contract"></i> Internships & contracts</span>
      <span style="background:#4f8af720; padding:0.6rem 1.5rem; border-radius:3rem;"><i class="fab fa-osi"></i> Open source collaboration</span>
    </div>

    <!-- subtle footer animation -->
    <p style="text-align: center; margin-top: 2.2rem; opacity:0.8; font-size:0.9rem; animation: fadeInUp 1.5s;">
      <i class="fas fa-sync-alt fa-spin" style="margin-right:0.4rem;"></i> Let's build something impactful together
    </p>
  </div>
</body>
</html>
