ai-resume-website/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
└── assets/
    └── (images go here)
    <!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alex Morgan | AI-Powered Resume</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Particle Background -->
    <canvas id="particleCanvas"></canvas>

    <!-- AI Assistant Chat Bot -->
    <div id="ai-chat" class="ai-chat">
        <div class="ai-chat-toggle" id="chatToggle">
            <i class="fas fa-robot"></i>
            <span class="pulse-dot"></span>
        </div>
        <div class="ai-chat-window" id="chatWindow">
            <div class="ai-chat-header">
                <div class="ai-avatar">
                    <i class="fas fa-robot"></i>
                </div>
                <div>
                    <h4>AI Resume Assistant</h4>
                    <span class="status-online">● Online</span>
                </div>
                <button class="chat-close" id="chatClose"><i class="fas fa-times"></i></button>
            </div>
            <div class="ai-chat-messages" id="chatMessages">
                <div class="message bot">
                    <p>👋 Hi! I'm the AI assistant for Alex Morgan. Ask me anything about skills, experience, or projects!</p>
                </div>
            </div>
            <div class="ai-chat-input">
                <input type="text" id="chatInput" placeholder="Ask about skills, experience..." autocomplete="off">
                <button id="chatSend"><i class="fas fa-paper-plane"></i></button>
            </div>
            <div class="quick-questions">
                <button class="quick-btn" data-question="What are your top skills?">🛠 Skills</button>
                <button class="quick-btn" data-question="Tell me about your experience">💼 Experience</button>
                <button class="quick-btn" data-question="What projects have you built?">🚀 Projects</button>
                <button class="quick-btn" data-question="How can I contact you?">📧 Contact</button>
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <a href="#" class="nav-logo">
                <span class="logo-bracket">&lt;</span>AM<span class="logo-bracket">/&gt;</span>
            </a>
            <ul class="nav-menu" id="navMenu">
                <li><a href="#home" class="nav-link active">Home</a></li>
                <li><a href="#about" class="nav-link">About</a></li>
                <li><a href="#skills" class="nav-link">Skills</a></li>
                <li><a href="#experience" class="nav-link">Experience</a></li>
                <li><a href="#projects" class="nav-link">Projects</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
            <div class="nav-actions">
                <button class="theme-toggle" id="themeToggle" title="Toggle Theme">
                    <i class="fas fa-moon"></i>
                </button>
                <a href="#" class="btn-download" id="downloadResume">
                    <i class="fas fa-download"></i> Resume
                </a>
                <div class="hamburger" id="hamburger">
                    <span></span><span></span><span></span>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <div class="hero-text">
                <div class="hero-greeting">
                    <span class="greeting-line"></span>
                    <span class="greeting-text" id="greetingText">Hello, World!</span>
                </div>
                <h1 class="hero-name">
                    I'm <span class="highlight">Alex Morgan</span>
                </h1>
                <div class="typewriter-container">
                    <span class="typewriter-prefix">I build </span>
                    <span class="typewriter" id="typewriter"></span>
                    <span class="cursor">|</span>
                </div>
                <p class="hero-description">
                    Full-Stack Developer & AI Enthusiast crafting intelligent digital 
                    experiences with modern technologies. Passionate about turning complex 
                    problems into elegant solutions.
                </p>
                <div class="hero-stats">
                    <div class="stat" data-count="5">
                        <span class="stat-number">0</span>
                        <span class="stat-label">Years Experience</span>
                    </div>
                    <div class="stat" data-count="50">
                        <span class="stat-number">0</span>
                        <span class="stat-label">Projects Done</span>
                    </div>
                    <div class="stat" data-count="30">
                        <span class="stat-number">0</span>
                        <span class="stat-label">Happy Clients</span>
                    </div>
                </div>
                <div class="hero-buttons">
                    <a href="#projects" class="btn btn-primary">
                        <i class="fas fa-rocket"></i> View My Work
                    </a>
                    <a href="#contact" class="btn btn-outline">
                        <i class="fas fa-envelope"></i> Get In Touch
                    </a>
                </div>
                <div class="social-links">
                    <a href="#" class="social-link" title="GitHub"><i class="fab fa-github"></i></a>
                    <a href="#" class="social-link" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#" class="social-link" title="Twitter"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-link" title="Dev.to"><i class="fab fa-dev"></i></a>
                </div>
            </div>
            <div class="hero-visual">
                <div class="code-window">
                    <div class="code-header">
                        <div class="code-dots">
                            <span class="dot red"></span>
                            <span class="dot yellow"></span>
                            <span class="dot green"></span>
                        </div>
                        <span class="code-title">developer.js</span>
                    </div>
                    <pre class="code-body"><code><span class="code-keyword">const</span> <span class="code-variable">developer</span> = {
  <span class="code-property">name</span>: <span class="code-string">"Alex Morgan"</span>,
  <span class="code-property">role</span>: <span class="code-string">"Full-Stack Developer"</span>,
  <span class="code-property">skills</span>: [
    <span class="code-string">"JavaScript"</span>, <span class="code-string">"Python"</span>,
    <span class="code-string">"React"</span>, <span class="code-string">"Node.js"</span>,
    <span class="code-string">"AI/ML"</span>, <span class="code-string">"Cloud"</span>
  ],
  <span class="code-property">passion</span>: <span class="code-string">"Building the future"</span>,
  <span class="code-method">createMagic</span>() {
    <span class="code-keyword">return</span> <span class="code-string">"✨ Amazing Apps"</span>;
  }
};</code></pre>
                </div>
            </div>
        </div>
        <div class="scroll-indicator">
            <div class="mouse">
                <div class="wheel"></div>
            </div>
            <span>Scroll Down</span>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section about">
        <div class="container">
            <div class="section-header">
                <span class="section-tag"><i class="fas fa-user"></i> Get To Know Me</span>
                <h2 class="section-title">About <span class="highlight">Me</span></h2>
                <div class="section-line"></div>
            </div>
            <div class="about-content">
                <div class="about-image">
                    <div class="image-wrapper">
                        <div class="image-placeholder">
                            <i class="fas fa-user-astronaut"></i>
                        </div>
                        <div class="image-border"></div>
                        <div class="image-dots"></div>
                    </div>
                    <div class="experience-badge">
                        <span class="badge-number">5+</span>
                        <span class="badge-text">Years of<br>Experience</span>
                    </div>
                </div>
                <div class="about-text">
                    <h3>A Passionate Developer Who Loves to Create</h3>
                    <p>
                        I'm a full-stack developer based in San Francisco with 5+ years of experience 
                        building web applications and AI-powered solutions. I specialize in creating 
                        scalable, user-friendly applications that solve real-world problems.
                    </p>
                    <p>
                        My journey in tech started with a curiosity about how things work on the internet. 
                        Today, I combine my skills in frontend development, backend engineering, and 
                        artificial intelligence to build products that make a difference.
                    </p>
                    <div class="about-details">
                        <div class="detail-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>San Francisco, CA</span>
                        </div>
                        <div class="detail-item">
                            <i class="fas fa-envelope"></i>
                            <span>alex@example.com</span>
                        </div>
                        <div class="detail-item">
                            <i class="fas fa-graduation-cap"></i>
                            <span>M.S. Computer Science</span>
                        </div>
                        <div class="detail-item">
                            <i class="fas fa-briefcase"></i>
                            <span>Open to Opportunities</span>
                        </div>
                    </div>
                    <div class="about-interests">
                        <span class="interest-tag">🤖 AI/ML</span>
                        <span class="interest-tag">🌐 Web Dev</span>
                        <span class="interest-tag">☁️ Cloud</span>
                        <span class="interest-tag">📱 Mobile</span>
                        <span class="interest-tag">🎨 UI/UX</span>
                        <span class="interest-tag">🔐 Security</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section skills">
        <div class="container">
            <div class="section-header">
                <span class="section-tag"><i class="fas fa-code"></i> What I Know</span>
                <h2 class="section-title">Skills & <span class="highlight">Technologies</span></h2>
                <div class="section-line"></div>
            </div>

            <div class="skills-filter">
                <button class="filter-btn active" data-filter="all">All</button>
                <button class="filter-btn" data-filter="frontend">Frontend</button>
                <button class="filter-btn" data-filter="backend">Backend</button>
                <button class="filter-btn" data-filter="ai">AI/ML</button>
                <button class="filter-btn" data-filter="tools">Tools</button>
            </div>

            <div class="skills-grid" id="skillsGrid">
                <!-- Frontend Skills -->
                <div class="skill-card" data-category="frontend" data-level="95">
                    <div class="skill-icon"><i class="fab fa-react"></i></div>
                    <h4>React</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 95%"></div></div>
                    <span class="skill-percent">95%</span>
                </div>
                <div class="skill-card" data-category="frontend" data-level="90">
                    <div class="skill-icon"><i class="fab fa-js-square"></i></div>
                    <h4>JavaScript</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 90%"></div></div>
                    <span class="skill-percent">90%</span>
                </div>
                <div class="skill-card" data-category="frontend" data-level="85">
                    <div class="skill-icon"><i class="fab fa-html5"></i></div>
                    <h4>HTML/CSS</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 85%"></div></div>
                    <span class="skill-percent">85%</span>
                </div>
                <div class="skill-card" data-category="frontend" data-level="80">
                    <div class="skill-icon"><i class="fab fa-vuejs"></i></div>
                    <h4>Vue.js</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 80%"></div></div>
                    <span class="skill-percent">80%</span>
                </div>
                <div class="skill-card" data-category="frontend" data-level="88">
                    <div class="skill-icon"><i class="fab fa-css3-alt"></i></div>
                    <h4>Tailwind CSS</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 88%"></div></div>
                    <span class="skill-percent">88%</span>
                </div>

                <!-- Backend Skills -->
                <div class="skill-card" data-category="backend" data-level="92">
                    <div class="skill-icon"><i class="fab fa-node-js"></i></div>
                    <h4>Node.js</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 92%"></div></div>
                    <span class="skill-percent">92%</span>
                </div>
                <div class="skill-card" data-category="backend" data-level="88">
                    <div class="skill-icon"><i class="fab fa-python"></i></div>
                    <h4>Python</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 88%"></div></div>
                    <span class="skill-percent">88%</span>
                </div>
                <div class="skill-card" data-category="backend" data-level="82">
                    <div class="skill-icon"><i class="fas fa-database"></i></div>
                    <h4>MongoDB</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 82%"></div></div>
                    <span class="skill-percent">82%</span>
                </div>
                <div class="skill-card" data-category="backend" data-level="78">
                    <div class="skill-icon"><i class="fas fa-server"></i></div>
                    <h4>PostgreSQL</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 78%"></div></div>
                    <span class="skill-percent">78%</span>
                </div>

                <!-- AI/ML Skills -->
                <div class="skill-card" data-category="ai" data-level="85">
                    <div class="skill-icon"><i class="fas fa-brain"></i></div>
                    <h4>TensorFlow</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 85%"></div></div>
                    <span class="skill-percent">85%</span>
                </div>
                <div class="skill-card" data-category="ai" data-level="80">
                    <div class="skill-icon"><i class="fas fa-robot"></i></div>
                    <h4>PyTorch</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 80%"></div></div>
                    <span class="skill-percent">80%</span>
                </div>
                <div class="skill-card" data-category="ai" data-level="75">
                    <div class="skill-icon"><i class="fas fa-language"></i></div>
                    <h4>NLP</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 75%"></div></div>
                    <span class="skill-percent">75%</span>
                </div>

                <!-- Tools -->
                <div class="skill-card" data-category="tools" data-level="90">
                    <div class="skill-icon"><i class="fab fa-git-alt"></i></div>
                    <h4>Git</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 90%"></div></div>
                    <span class="skill-percent">90%</span>
                </div>
                <div class="skill-card" data-category="tools" data-level="85">
                    <div class="skill-icon"><i class="fab fa-docker"></i></div>
                    <h4>Docker</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 85%"></div></div>
                    <span class="skill-percent">85%</span>
                </div>
                <div class="skill-card" data-category="tools" data-level="80">
                    <div class="skill-icon"><i class="fab fa-aws"></i></div>
                    <h4>AWS</h4>
                    <div class="skill-bar"><div class="skill-progress" style="--progress: 80%"></div></div>
                    <span class="skill-percent">80%</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="section experience">
        <div class="container">
            <div class="section-header">
                <span class="section-tag"><i class="fas fa-briefcase"></i> Where I've Worked</span>
                <h2 class="section-title">Work <span class="highlight">Experience</span></h2>
                <div class="section-line"></div>
            </div>
            <div class="timeline">
                <div class="timeline-item" data-aos="fade-right">
                    <div class="timeline-dot">
                        <i class="fas fa-building"></i>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-header">
                            <h3>Senior Full-Stack Developer</h3>
                            <span class="company">TechCorp AI</span>
                        </div>
                        <span class="timeline-date"><i class="fas fa-calendar"></i> 2022 – Present</span>
                        <p>Led development of AI-powered web applications serving 100K+ users. 
                        Implemented microservices architecture reducing response time by 40%.</p>
                        <div class="timeline-tags">
                            <span>React</span><span>Node.js</span><span>Python</span><span>AWS</span>
                        </div>
                    </div>
                </div>
                <div class="timeline-item" data-aos="fade-left">
                    <div class="timeline-dot">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-header">
                            <h3>Full-Stack Developer</h3>
                            <span class="company">InnovateTech Solutions</span>
                        </div>
                        <span class="timeline-date"><i class="fas fa-calendar"></i> 2020 – 2022</span>
                        <p>Built and maintained 15+ client projects including e-commerce platforms 
                        and SaaS applications. Mentored junior developers.</p>
                        <div class="timeline-tags">
                            <span>Vue.js</span><span>Django</span><span>PostgreSQL</span><span>Docker</span>
                        </div>
                    </div>
                </div>
                <div class="timeline-item" data-aos="fade-right">
                    <div class="timeline-dot">
                        <i class="fas fa-code"></i>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-header">
                            <h3>Junior Developer</h3>
                            <span class="company">StartupHub</span>
                        </div>
                        <span class="timeline-date"><i class="fas fa-calendar"></i> 2019 – 2020</span>
                        <p>Developed responsive web applications and RESTful APIs. 
                        Collaborated with design team to implement pixel-perfect UIs.</p>
                        <div class="timeline-tags">
                            <span>JavaScript</span><span>React</span><span>Express</span><span>MongoDB</span>
                        </div>
                    </div>
                </div>
                <div class="timeline-item" data-aos="fade-left">
                    <div class="timeline-dot">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="timeline-content">
                        <div class="timeline-header">
                            <h3>M.S. Computer Science</h3>
                            <span class="company">Stanford University</span>
                        </div>
                        <span class="timeline-date"><i class="fas fa-calendar"></i> 2017 – 2019</span>
                        <p>Specialized in Artificial Intelligence and Machine Learning. 
                        Published research on natural language processing.</p>
                        <div class="timeline-tags">
                            <span>AI/ML</span><span>NLP</span><span>Research</span><span>Python</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section projects">
        <div class="container">
            <div class="section-header">
                <span class="section-tag"><i class="fas fa-rocket"></i> My Work</span>
                <h2 class="section-title">Featured <span class="highlight">Projects</span></h2>
                <div class="section-line"></div>
            </div>
            <div class="projects-grid">
                <div class="project-card featured">
                    <div class="project-image">
                        <div class="project-placeholder">
                            <i class="fas fa-brain"></i>
                        </div>
                        <div class="project-overlay">
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                        </div>
                    </div>
                    <div class="project-info">
                        <span class="project-category">AI / Machine Learning</span>
                        <h3>AI Content Generator</h3>
                        <p>An AI-powered platform that generates blog posts, social media content, 
                        and marketing copy using GPT-4 and custom fine-tuned models.</p>
                        <div class="project-tech">
                            <span>Python</span><span>React</span><span>OpenAI</span><span>FastAPI</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">
                        <div class="project-placeholder">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <div class="project-overlay">
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                        </div>
                    </div>
                    <div class="project-info">
                        <span class="project-category">SaaS Platform</span>
                        <h3>Analytics Dashboard</h3>
                        <p>Real-time analytics dashboard with customizable widgets, 
                        data visualization, and automated reporting features.</p>
                        <div class="project-tech">
                            <span>Next.js</span><span>D3.js</span><span>Node.js</span><span>Redis</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">
                        <div class="project-placeholder">
                            <i class="fas fa-shopping-cart"></i>
                        </div>
                        <div class="project-overlay">
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                        </div>
                    </div>
                    <div class="project-info">
                        <span class="project-category">E-Commerce</span>
                        <h3>Smart Shop Platform</h3>
                        <p>Full-featured e-commerce platform with AI-powered product 
                        recommendations and personalized shopping experience.</p>
                        <div class="project-tech">
                            <span>React</span><span>Node.js</span><span>MongoDB</span><span>Stripe</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">
                        <div class="project-placeholder">
                            <i class="fas fa-comments"></i>
                        </div>
                        <div class="project-overlay">
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i></a>
                            <a href="#" class="project-link"><i class="fab fa-github"></i></a>
                        </div>
                    </div>
                    <div class="project-info">
                        <span class="project-category">Real-time App</span>
                        <h3>CollabSpace</h3>
                        <p>Real-time collaboration tool with video conferencing, 
                        shared whiteboard, and project management features.</p>
                        <div class="project-tech">
                            <span>Vue.js</span><span>WebRTC</span><span>Socket.io</span><span>PostgreSQL</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <div class="container">
            <div class="section-header">
                <span class="section-tag"><i class="fas fa-envelope"></i> Reach Out</span>
                <h2 class="section-title">Get In <span class="highlight">Touch</span></h2>
                <div class="section-line"></div>
                <p class="section-subtitle">Have a project in mind or want to collaborate? Let's talk!</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-card">
                        <div class="contact-icon"><i class="fas fa-envelope"></i></div>
                        <div>
                            <h4>Email</h4>
                            <p>alex@example.com</p>
                        </div>
                    </div>
                    <div class="contact-card">
                        <div class="contact-icon"><i class="fas fa-map-marker-alt"></i></div>
                        <div>
                            <h4>Location</h4>
                            <p>San Francisco, CA</p>
                        </div>
                    </div>
                    <div class="contact-card">
                        <div class="contact-icon"><i class="fas fa-phone"></i></div>
                        <div>
                            <h4>Phone</h4>
                            <p>+1 (555) 123-4567</p>
                        </div>
                    </div>
                    <div class="contact-social">
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-dribbble"></i></a>
                    </div>
                </div>
                <form class="contact-form" id="contactForm">
                    <div class="form-group">
                        <div class="form-field">
                            <input type="text" id="name" required>
                            <label for="name"><i class="fas fa-user"></i> Your Name</label>
                        </div>
                        <div class="form-field">
                            <input type="email" id="email" required>
                            <label for="email"><i class="fas fa-envelope"></i> Your Email</label>
                        </div>
                    </div>
                    <div class="form-field">
                        <input type="text" id="subject" required>
                        <label for="subject"><i class="fas fa-tag"></i> Subject</label>
                    </div>
                    <div class="form-field">
                        <textarea id="message" rows="5" required></textarea>
                        <label for="message"><i class="fas fa-comment"></i> Your Message</label>
                    </div>
                    <button type="submit" class="btn btn-primary btn-full">
                        <i class="fas fa-paper-plane"></i> Send Message
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <span class="logo-bracket">&lt;</span>AM<span class="logo-bracket">/&gt;</span>
                    <p>Building the future, one line of code at a time.</p>
                </div>
                <div class="footer-links">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#skills">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#contact">Contact</a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Alex Morgan. All rights reserved. Built with ❤️ and ☕</p>
            </div>
        </div>
    </footer>

    <script src="js/main.js"></script>
</body>
</html>
/* ===== CSS VARIABLES ===== */
:root {
    --font-main: 'Inter', sans-serif;
    --font-code: 'Fira Code', monospace;
}

[data-theme="dark"] {
    --bg-primary: #0a0a0f;
    --bg-secondary: #12121a;
    --bg-card: #1a1a2e;
    --bg-card-hover: #1f1f35;
    --text-primary: #e4e4e7;
    --text-secondary: #a1a1aa;
    --text-muted: #71717a;
    --accent: #6c63ff;
    --accent-light: #8b83ff;
    --accent-dark: #5a52e0;
    --accent-glow: rgba(108, 99, 255, 0.3);
    --gradient: linear-gradient(135deg, #6c63ff, #e040fb);
    --border: #2a2a3e;
    --shadow: 0 10px 40px rgba(0, 0, 0, 0.4);
    --nav-bg: rgba(10, 10, 15, 0.9);
    --code-bg: #1e1e2e;
    --success: #22c55e;
    --warning: #f59e0b;
    --error: #ef4444;
}

[data-theme="light"] {
    --bg-primary: #fafafa;
    --bg-secondary: #f4f4f5;
    --bg-card: #ffffff;
    --bg-card-hover: #f8f8ff;
    --text-primary: #18181b;
    --text-secondary: #52525b;
    --text-muted: #a1a1aa;
    --accent: #6c63ff;
    --accent-light: #8b83ff;
    --accent-dark: #5a52e0;
    --accent-glow: rgba(108, 99, 255, 0.15);
    --gradient: linear-gradient(135deg, #6c63ff, #e040fb);
    --border: #e4e4e7;
    --shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
    --nav-bg: rgba(250, 250, 250, 0.9);
    --code-bg: #282a36;
    --success: #22c55e;
    --warning: #f59e0b;
    --error: #ef4444;
}

/* ===== RESET & BASE ===== */
*, *::before, *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 80px;
}

body {
    font-family: var(--font-main);
    background: var(--bg-primary);
    color: var(--text-primary);
    line-height: 1.7;
    overflow-x: hidden;
    transition: background 0.3s ease, color 0.3s ease;
}

a {
    text-decoration: none;
    color: inherit;
}

ul { list-style: none; }

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.highlight {
    background: var(--gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

/* ===== PARTICLE CANVAS ===== */
#particleCanvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 0;
    pointer-events: none;
}

/* ===== NAVBAR ===== */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    background: var(--nav-bg);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
    transition: all 0.3s ease;
}

.navbar.scrolled {
    box-shadow: var(--shadow);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 70px;
}

.nav-logo {
    font-size: 1.5rem;
    font-weight: 800;
    color: var(--text-primary);
}

.logo-bracket {
    color: var(--accent);
}

.nav-menu {
    display: flex;
    gap: 8px;
}

.nav-link {
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--text-secondary);
    transition: all 0.3s ease;
    position: relative;
}

.nav-link:hover,
.nav-link.active {
    color: var(--accent);
    background: var(--accent-glow);
}

.nav-actions {
    display: flex;
    align-items: center;
    gap: 12px;
}

.theme-toggle {
    width: 40px;
    height: 40px;
    border: 1px solid var(--border);
    border-radius: 10px;
    background: var(--bg-card);
    color: var(--text-primary);
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1rem;
    transition: all 0.3s ease;
}

.theme-toggle:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: rotate(180deg);
}

.btn-download {
    padding: 8px 20px;
    background: var(--gradient);
    color: white;
    border-radius: 8px;
    font-size: 0.85rem;
    font-weight: 600;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: all 0.3s ease;
}

.btn-download:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 20px var(--accent-glow);
}

.hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
    padding: 5px;
}

.hamburger span {
    width: 25px;
    height: 2px;
    background: var(--text-primary);
    border-radius: 2px;
    transition: all 0.3s ease;
}

.hamburger.active span:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
}

.hamburger.active span:nth-child(2) {
    opacity: 0;
}

.hamburger.active span:nth-child(3) {
    transform: rotate(-45deg) translate(5px, -5px);
}

/* ===== HERO ===== */
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 120px 20px 60px;
    position: relative;
    z-index: 1;
}

.hero-content {
    max-width: 1200px;
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
}

.hero-greeting {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 16px;
}

.greeting-line {
    width: 40px;
    height: 2px;
    background: var(--accent);
}

.greeting-text {
    color: var(--accent);
    font-weight: 500;
    font-size: 1rem;
    letter-spacing: 1px;
}

.hero-name {
    font-size: 3.5rem;
    font-weight: 900;
    line-height: 1.1;
    margin-bottom: 16px;
}

.typewriter-container {
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 20px;
    min-height: 40px;
}

.typewriter-prefix {
    color: var(--text-secondary);
}

.typewriter {
    color: var(--accent);
}

.cursor {
    color: var(--accent);
    animation: blink 0.8s infinite;
}

@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}

.hero-description {
    color: var(--text-secondary);
    font-size: 1.05rem;
    max-width: 520px;
    margin-bottom: 30px;
}

.hero-stats {
    display: flex;
    gap: 40px;
    margin-bottom: 32px;
}

.stat {
    text-align: center;
}

.stat-number {
    display: block;
    font-size: 2rem;
    font-weight: 800;
    background: var(--gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.stat-label {
    font-size: 0.8rem;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 1px;
}

.hero-buttons {
    display: flex;
    gap: 16px;
    margin-bottom: 32px;
}

.btn {
    padding: 14px 28px;
    border-radius: 12px;
    font-size: 0.95rem;
    font-weight: 600;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    transition: all 0.3s ease;
    cursor: pointer;
    border: none;
}

.btn-primary {
    background: var(--gradient);
    color: white;
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 30px var(--accent-glow);
}

.btn-outline {
    border: 2px solid var(--border);
    color: var(--text-primary);
    background: transparent;
}

.btn-outline:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-3px);
}

.btn-full {
    width: 100%;
    justify-content: center;
}

.social-links {
    display: flex;
    gap: 12px;
}

.social-link {
    width: 44px;
    height: 44px;
    border: 1px solid var(--border);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
    color: var(--text-secondary);
    transition: all 0.3s ease;
}

.social-link:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-3px);
    box-shadow: 0 5px 15px var(--accent-glow);
}

/* Code Window */
.code-window {
    background: var(--code-bg);
    border-radius: 16px;
    overflow: hidden;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
    animation: float 6s ease-in-out infinite;
}

@keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-15px); }
}

.code-header {
    background: rgba(255, 255, 255, 0.05);
    padding: 12px 16px;
    display: flex;
    align-items: center;
    gap: 12px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.code-dots {
    display: flex;
    gap: 6px;
}

.dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
}

.dot.red { background: #ff5f57; }
.dot.yellow { background: #ffbd2e; }
.dot.green { background: #28c840; }

.code-title {
    font-size: 0.8rem;
    color: #888;
    font-family: var(--font-code);
}

.code-body {
    padding: 24px;
    font-family: var(--font-code);
    font-size: 0.85rem;
    line-height: 1.8;
    overflow-x: auto;
}

.code-body code {
    color: #e4e4e7;
}

.code-keyword { color: #c678dd; }
.code-variable { color: #61afef; }
.code-property { color: #e06c75; }
.code-string { color: #98c379; }
.code-method { color: #61afef; }

/* Scroll Indicator */
.scroll-indicator {
    position: absolute;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    color: var(--text-muted);
    font-size: 0.8rem;
    animation: bounce 2s infinite;
}

@keyframes bounce {
    0%, 100% { transform: translateX(-50%) translateY(0); }
    50% { transform: translateX(-50%) translateY(-10px); }
}

.mouse {
    width: 24px;
    height: 38px;
    border: 2px solid var(--text-muted);
    border-radius: 12px;
    position: relative;
}

.wheel {
    width: 3px;
    height: 8px;
    background: var(--accent);
    border-radius: 2px;
    position: absolute;
    top: 8px;
    left: 50%;
    transform: translateX(-50%);
    animation: scroll 1.5s infinite;
}

@keyframes scroll {
    0% { opacity: 1; top: 8px; }
    100% { opacity: 0; top: 22px; }
}

/* ===== SECTIONS ===== */
.section {
    padding: 100px 0;
    position: relative;
    z-index: 1;
}

.section-header {
    text-align: center;
    margin-bottom: 60px;
}

.section-tag {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 6px 16px;
    background: var(--accent-glow);
    color: var(--accent);
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
    margin-bottom: 16px;
}

.section-title {
    font-size: 2.5rem;
    font-weight: 800;
    margin-bottom: 12px;
}

.section-line {
    width: 60px;
    height: 4px;
    background: var(--gradient);
    border-radius: 2px;
    margin: 0 auto;
}

.section-subtitle {
    color: var(--text-secondary);
    margin-top: 16px;
    font-size: 1.05rem;
}

/* ===== ABOUT ===== */
.about-content {
    display: grid;
    grid-template-columns: 400px 1fr;
    gap: 60px;
    align-items: center;
}

.image-wrapper {
    position: relative;
    width: 300px;
    height: 350px;
    margin: 0 auto;
}

.image-placeholder {
    width: 100%;
    height: 100%;
    background: var(--bg-card);
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 6rem;
    color: var(--accent);
    border: 2px solid var(--border);
    position: relative;
    z-index: 2;
    overflow: hidden;
}

.image-placeholder::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--gradient);
    opacity: 0.1;
}

.image-border {
    position: absolute;
    top: 20px;
    left: 20px;
    width: 100%;
    height: 100%;
    border: 3px solid var(--accent);
    border-radius: 20px;
    z-index: 1;
}

.image-dots {
    position: absolute;
    bottom: -20px;
    right: -20px;
    width: 80px;
    height: 80px;
    background-image: radial-gradient(var(--accent) 2px, transparent 2px);
    background-size: 12px 12px;
    z-index: 0;
}

.experience-badge {
    position: absolute;
    bottom: -10px;
    left: -10px;
    background: var(--gradient);
    color: white;
    padding: 16px 20px;
    border-radius: 16px;
    text-align: center;
    z-index: 3;
    box-shadow: 0 10px 30px var(--accent-glow);
}

.badge-number {
    display: block;
    font-size: 2rem;
    font-weight: 900;
    line-height: 1;
}

.badge-text {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    opacity: 0.9;
}

.about-text h3 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 16px;
}

.about-text p {
    color: var(--text-secondary);
    margin-bottom: 16px;
}

.about-details {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin: 24px 0;
}

.detail-item {
    display: flex;
    align-items: center;
    gap: 10px;
    color: var(--text-secondary);
    font-size: 0.9rem;
}

.detail-item i {
    color: var(--accent);
    width: 20px;
}

.about-interests {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 20px;
}

.interest-tag {
    padding: 6px 14px;
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 20px;
    font-size: 0.85rem;
    color: var(--text-secondary);
    transition: all 0.3s ease;
}

.interest-tag:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-2px);
}

/* ===== SKILLS ===== */
.skills-filter {
    display: flex;
    justify-content: center;
    gap: 8px;
    margin-bottom: 40px;
    flex-wrap: wrap;
}

.filter-btn {
    padding: 8px 24px;
    border: 1px solid var(--border);
    border-radius: 20px;
    background: var(--bg-card);
    color: var(--text-secondary);
    font-size: 0.9rem;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.3s ease;
    font-family: var(--font-main);
}

.filter-btn:hover,
.filter-btn.active {
    background: var(--gradient);
    color: white;
    border-color: transparent;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
}

.skill-card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    text-align: center;
    transition: all 0.4s ease;
    position: relative;
    overflow: hidden;
}

.skill-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 3px;
    background: var(--gradient);
    transform: scaleX(0);
    transition: transform 0.3s ease;
}

.skill-card:hover {
    transform: translateY(-5px);
    border-color: var(--accent);
    box-shadow: 0 10px 30px var(--accent-glow);
}

.skill-card:hover::before {
    transform: scaleX(1);
}

.skill-card.hidden {
    display: none;
}

.skill-icon {
    width: 50px;
    height: 50px;
    background: var(--accent-glow);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    color: var(--accent);
    margin: 0 auto 12px;
}

.skill-card h4 {
    font-size: 0.95rem;
    font-weight: 600;
    margin-bottom: 12px;
}

.skill-bar {
    width: 100%;
    height: 6px;
    background: var(--bg-secondary);
    border-radius: 3px;
    overflow: hidden;
    margin-bottom: 8px;
}

.skill-progress {
    height: 100%;
    background: var(--gradient);
    border-radius: 3px;
    width: 0;
    transition: width 1.5s ease;
}

.skill-card.animate .skill-progress {
    width: var(--progress);
}

.skill-percent {
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--accent);
}

/* ===== EXPERIENCE TIMELINE ===== */
.timeline {
    position: relative;
    max-width: 800px;
    margin: 0 auto;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 50px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: var(--border);
}

.timeline-item {
    position: relative;
    padding-left: 100px;
    padding-bottom: 40px;
    opacity: 0;
    transform: translateX(-20px);
    transition: all 0.6s ease;
}

.timeline-item.visible {
    opacity: 1;
    transform: translateX(0);
}

.timeline-dot {
    position: absolute;
    left: 36px;
    top: 0;
    width: 30px;
    height: 30px;
    background: var(--gradient);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.7rem;
    color: white;
    z-index: 2;
    box-shadow: 0 0 0 5px var(--bg-primary), 0 0 20px var(--accent-glow);
}

.timeline-content {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    transition: all 0.3s ease;
}

.timeline-content:hover {
    border-color: var(--accent);
    box-shadow: 0 5px 20px var(--accent-glow);
}

.timeline-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 12px;
    margin-bottom: 8px;
    flex-wrap: wrap;
}

.timeline-header h3 {
    font-size: 1.1rem;
    font-weight: 700;
}

.company {
    color: var(--accent);
    font-weight: 600;
    font-size: 0.9rem;
}

.timeline-date {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    color: var(--text-muted);
    font-size: 0.85rem;
    margin-bottom: 12px;
}

.timeline-content p {
    color: var(--text-secondary);
    font-size: 0.9rem;
    margin-bottom: 12px;
}

.timeline-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}

.timeline-tags span {
    padding: 4px 12px;
    background: var(--accent-glow);
    color: var(--accent);
    border-radius: 12px;
    font-size: 0.75rem;
    font-weight: 500;
}

/* ===== PROJECTS ===== */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
}

.project-card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    transition: all 0.4s ease;
}

.project-card:hover {
    transform: translateY(-5px);
    border-color: var(--accent);
    box-shadow: 0 15px 40px var(--accent-glow);
}

.project-card.featured {
    grid-column: span 2;
    display: grid;
    grid-template-columns: 1fr 1fr;
}

.project-image {
    position: relative;
    overflow: hidden;
    min-height: 220px;
}

.project-placeholder {
    width: 100%;
    height: 100%;
    min-height: 220px;
    background: var(--bg-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 4rem;
    color: var(--accent);
    position: relative;
}

.project-placeholder::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--gradient);
    opacity: 0.1;
}

.project-overlay {
    position: absolute;
    inset: 0;
    background: rgba(108, 99, 255, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    opacity: 0;
    transition: all 0.3s ease;
}

.project-card:hover .project-overlay {
    opacity: 1;
}

.project-link {
    width: 48px;
    height: 48px;
    background: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    font-size: 1.1rem;
    transform: translateY(20px);
    transition: all 0.3s ease;
}

.project-card:hover .project-link {
    transform: translateY(0);
}

.project-link:hover {
    transform: translateY(0) scale(1.1);
}

.project-info {
    padding: 24px;
}

.project-category {
    color: var(--accent);
    font-size: 0.8rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
}

.project-info h3 {
    font-size: 1.2rem;
    font-weight: 700;
    margin: 8px 0;
}

.project-info p {
    color: var(--text-secondary);
    font-size: 0.9rem;
    margin-bottom: 16px;
}

.project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}

.project-tech span {
    padding: 4px 12px;
    background: var(--accent-glow);
    color: var(--accent);
    border-radius: 12px;
    font-size: 0.75rem;
    font-weight: 500;
}

/* ===== CONTACT ===== */
.contact-content {
    display: grid;
    grid-template-columns: 1fr 1.5fr;
    gap: 40px;
}

.contact-card {
    display: flex;
    gap: 16px;
    padding: 20px;
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 16px;
    margin-bottom: 16px;
    transition: all 0.3s ease;
}

.contact-card:hover {
    border-color: var(--accent);
    transform: translateX(5px);
}

.contact-icon {
    width: 50px;
    height: 50px;
    min-width: 50px;
    background: var(--accent-glow);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2rem;
    color: var(--accent);
}

.contact-card h4 {
    font-size: 0.9rem;
    font-weight: 600;
    margin-bottom: 4px;
}

.contact-card p {
    color: var(--text-secondary);
    font-size: 0.9rem;
}

.contact-social {
    display: flex;
    gap: 12px;
    margin-top: 16px;
}

.contact-social a {
    width: 44px;
    height: 44px;
    border: 1px solid var(--border);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
    color: var(--text-secondary);
    transition: all 0.3s ease;
}

.contact-social a:hover {
    background: var(--gradient);
    color: white;
    border-color: transparent;
    transform: translateY(-3px);
}

/* Contact Form */
.contact-form {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 32px;
}

.form-group {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
}

.form-field {
    position: relative;
    margin-bottom: 20px;
}

.form-field input,
.form-field textarea {
    width: 100%;
    padding: 16px;
    padding-top: 24px;
    background: var(--bg-secondary);
    border: 2px solid var(--border);
    border-radius: 12px;
    color: var(--text-primary);
    font-size: 0.95rem;
    font-family: var(--font-main);
    outline: none;
    transition: all 0.3s ease;
    resize: vertical;
}

.form-field input:focus,
.form-field textarea:focus {
    border-color: var(--accent);
    box-shadow: 0 0 0 4px var(--accent-glow);
}

.form-field label {
    position: absolute;
    top: 50%;
    left: 16px;
    transform: translateY(-50%);
    color: var(--text-muted);
    font-size: 0.9rem;
    pointer-events: none;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 6px;
}

.form-field textarea ~ label {
    top: 20px;
    transform: none;
}

.form-field input:focus ~ label,
.form-field input:valid ~ label,
.form-field textarea:focus ~ label,
.form-field textarea:valid ~ label {
    top: 8px;
    transform: none;
    font-size: 0.7rem;
    color: var(--accent);
}

/* ===== AI CHAT ===== */
.ai-chat {
    position: fixed;
    bottom: 24px;
    right: 24px;
    z-index: 999;
}

.ai-chat-toggle {
    width: 60px;
    height: 60px;
    background: var(--gradient);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    color: white;
    cursor: pointer;
    box-shadow: 0 5px 25px var(--accent-glow);
    transition: all 0.3s ease;
    position: relative;
}

.ai-chat-toggle:hover {
    transform: scale(1.1);
}

.pulse-dot {
    position: absolute;
    top: 0;
    right: 0;
    width: 16px;
    height: 16px;
    background: var(--success);
    border-radius: 50%;
    border: 3px solid var(--bg-primary);
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0% { box-shadow: 0 0 0 0 rgba(34, 197, 94, 0.4); }
    100% { box-shadow: 0 0 0 10px rgba(34, 197, 94, 0); }
}

.ai-chat-window {
    position: absolute;
    bottom: 70px;
    right: 0;
    width: 380px;
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: var(--shadow);
    display: none;
    flex-direction: column;
    animation: slideUp 0.3s ease;
}

.ai-chat-window.active {
    display: flex;
}

@keyframes slideUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.ai-chat-header {
    background: var(--gradient);
    padding: 16px 20px;
    display: flex;
    align-items: center;
    gap: 12px;
    color: white;
}

.ai-avatar {
    width: 40px;
    height: 40px;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2rem;
}

.ai-chat-header h4 {
    font-size: 0.95rem;
    font-weight: 600;
}

.status-online {
    font-size: 0.75rem;
    opacity: 0.9;
    color: #bbf7d0;
}

.chat-close {
    margin-left: auto;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
    font-size: 1rem;
    opacity: 0.8;
    transition: opacity 0.3s;
}

.chat-close:hover {
    opacity: 1;
}

.ai-chat-messages {
    padding: 16px;
    max-height: 300px;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.message {
    max-width: 85%;
    padding: 12px 16px;
    border-radius: 16px;
    font-size: 0.9rem;
    line-height: 1.5;
    animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

.message.bot {
    background: var(--bg-secondary);
    color: var(--text-primary);
    align-self: flex-start;
    border-bottom-left-radius: 4px;
}

.message.user {
    background: var(--gradient);
    color: white;
    align-self: flex-end;
    border-bottom-right-radius: 4px;
}

.ai-chat-input {
    padding: 12px 16px;
    display: flex;
    gap: 8px;
    border-top: 1px solid var(--border);
}

.ai-chat-input input {
    flex: 1;
    padding: 10px 16px;
    background: var(--bg-secondary);
    border: 1px solid var(--border);
    border-radius: 12px;
    color: var(--text-primary);
    font-size: 0.9rem;
    font-family: var(--font-main);
    outline: none;
}

.ai-chat-input input:focus {
    border-color: var(--accent);
}

.ai-chat-input button {
    width: 42px;
    height: 42px;
    background: var(--gradient);
    border: none;
    border-radius: 12px;
    color: white;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.9rem;
    transition: transform 0.3s;
}

.ai-chat-input button:hover {
    transform: scale(1.05);
}

.quick-questions {
    padding: 8px 16px 16px;
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}

.quick-btn {
    padding: 6px 12px;
    background: var(--bg-secondary);
    border: 1px solid var(--border);
    border-radius: 16px;
    color: var(--text-secondary);
    font-size: 0.75rem;
    cursor: pointer;
    font-family: var(--font-main);
    transition: all 0.3s ease;
}

.quick-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
}

/* ===== FOOTER ===== */
.footer {
    background: var(--bg-secondary);
    border-top: 1px solid var(--border);
    padding: 40px 0 20px;
    position: relative;
    z-index: 1;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 24px;
    flex-wrap: wrap;
    gap: 20px;
}

.footer-logo {
    font-size: 1.5rem;
    font-weight: 800;
}

.footer-logo p {
    font-size: 0.85rem;
    color: var(--text-muted);
    font-weight: 400;
    margin-top: 4px;
}

.footer-links {
    display: flex;
    gap: 24px;
    flex-wrap: wrap;
}

.footer-links a {
    color: var(--text-secondary);
    font-size: 0.9rem;
    transition: color 0.3s;
}

.footer-links a:hover {
    color: var(--accent);
}

.footer-bottom {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    color: var(--text-muted);
    font-size: 0.85rem;
}

/* ===== RESPONSIVE ===== */
@media (max-width: 1024px) {
    .hero-content {
        grid-template-columns: 1fr;
        text-align: center;
        gap: 40px;
    }

    .hero-description {
        margin-left: auto;
        margin-right: auto;
    }

    .hero-stats {
        justify-content: center;
    }

    .hero-buttons {
        justify-content: center;
    }

    .social-links {
        justify-content: center;
    }

    .hero-greeting {
        justify-content: center;
    }

    .code-window {
        max-width: 500px;
        margin: 0 auto;
    }

    .about-content {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .about-image {
        margin-bottom: 20px;
    }

    .projects-grid {
        grid-template-columns: 1fr;
    }

    .project-card.featured {
        grid-column: span 1;
        grid-template-columns: 1fr;
    }

    .contact-content {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 768px) {
    .nav-menu {
        position: fixed;
        top: 70px;
        left: 0;
        width: 100%;
        background: var(--nav-bg);
        backdrop-filter: blur(20px);
        flex-direction: column;
        padding: 20px;
        border-bottom: 1px solid var(--border);
        transform: translateY(-100%);
        opacity: 0;
        pointer-events: none;
        transition: all 0.3s ease;
    }

    .nav-menu.active {
        transform: translateY(0);
        opacity: 1;
        pointer-events: all;
    }

    .hamburger {
        display: flex;
    }

    .hero-name {
        font-size: 2.5rem;
    }

    .typewriter-container {
        font-size: 1.2rem;
    }

    .section-title {
        font-size: 2rem;
    }

    .hero-stats {
        gap: 20px;
    }

    .stat-number {
        font-size: 1.5rem;
    }

    .form-group {
        grid-template-columns: 1fr;
    }

    .about-details {
        grid-template-columns: 1fr;
    }

    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .timeline::before {
        left: 20px;
    }

    .timeline-item {
        padding-left: 60px;
    }

    .timeline-dot {
        left: 6px;
    }

    .ai-chat-window {
        width: calc(100vw - 48px);
        right: -12px;
    }
}

@media (max-width: 480px) {
    .hero-name {
        font-size: 2rem;
    }

    .hero-buttons {
        flex-direction: column;
        align-items: center;
    }

    .skills-grid {
        grid-template-columns: 1fr;
    }

    .btn-download span {
        display: none;
    }
}

/* ===== SCROLLBAR ===== */
::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: var(--bg-primary);
}

::-webkit-scrollbar-thumb {
    background: var(--accent);
    border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
    background: var(--accent-light);
}

/* ===== SELECTION ===== */
::selection {
    background: var(--accent);
    color: white;
}

/* ===== LOADING ANIMATION FOR SKILL CARDS ===== */
.skill-card {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.5s ease, transform 0.5s ease;
}

.skill-card.visible {
    opacity: 1;
    transform: translateY(0);
    // ===== PARTICLE BACKGROUND =====
class ParticleBackground {
    constructor() {
        this.canvas = document.getElementById('particleCanvas');
        this.ctx = this.canvas.getContext('2d');
        this.particles = [];
        this.mouse = { x: null, y: null, radius: 150 };
        this.init();
        this.animate();

        window.addEventListener('resize', () => this.init());
        window.addEventListener('mousemove', (e) => {
            this.mouse.x = e.x;
            this.mouse.y = e.y;
        });
    }

    init() {
        this.canvas.width = window.innerWidth;
        this.canvas.height = window.innerHeight;
        this.particles = [];

        const numberOfParticles = Math.floor((this.canvas.width * this.canvas.height) / 15000);
        for (let i = 0; i < numberOfParticles; i++) {
            this.particles.push({
                x: Math.random() * this.canvas.width,
                y: Math.random() * this.canvas.height,
                size: Math.random() * 2 + 0.5,
                speedX: (Math.random() - 0.5) * 0.5,
                speedY: (Math.random() - 0.5) * 0.5,
                opacity: Math.random() * 0.5 + 0.1
            });
        }
    }

    animate() {
        this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
        const isDark = document.documentElement.getAttribute('data-theme') === 'dark';
        const particleColor = isDark ? '108, 99, 255' : '108, 99, 255';

        for (let i = 0; i < this.particles.length; i++) {
            const p = this.particles[i];

            // Move particles
            p.x += p.speedX;
            p.y += p.speedY;

            // Wrap around
            if (p.x > this.canvas.width) p.x = 0;
            if (p.x < 0) p.x = this.canvas.width;
            if (p.y > this.canvas.height) p.y = 0;
            if (p.y < 0) p.y = this.canvas.height;

            // Mouse interaction
            if (this.mouse.x) {
                const dx = p.x - this.mouse.x;
                const dy = p.y - this.mouse.y;
                const dist = Math.sqrt(dx * dx + dy * dy);
                if (dist < this.mouse.radius) {
                    const force = (this.mouse.radius - dist) / this.mouse.radius;
                    p.x += dx * force * 0.02;
                    p.y += dy * force * 0.02;
                }
            }

            // Draw particle
            this.ctx.beginPath();
            this.ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
            this.ctx.fillStyle = `rgba(${particleColor}, ${p.opacity})`;
            this.ctx.fill();

            // Connect nearby particles
            for (let j = i + 1; j < this.particles.length; j++) {
                const p2 = this.particles[j];
                const dx = p.x - p2.x;
                const dy = p.y - p2.y;
                const dist = Math.sqrt(dx * dx + dy * dy);

                if (dist < 120) {
                    this.ctx.beginPath();
                    this.ctx.moveTo(p.x, p.y);
                    this.ctx.lineTo(p2.x, p2.y);
                    this.ctx.strokeStyle = `rgba(${particleColor}, ${0.1 * (1 - dist / 120)})`;
                    this.ctx.lineWidth = 0.5;
                    this.ctx.stroke();
                }
            }
        }

        requestAnimationFrame(() => this.animate());
    }
}

// ===== TYPEWRITER EFFECT =====
class Typewriter {
    constructor(element, words, speed = 100) {
        this.element = element;
        this.words = words;
        this.speed = speed;
        this.wordIndex = 0;
        this.charIndex = 0;
        this.isDeleting = false;
        this.type();
    }

    type() {
        const currentWord = this.words[this.wordIndex];
        let delay = this.speed;

        if (this.isDeleting) {
            this.charIndex--;
            delay = 50;
        } else {
            this.charIndex++;
        }

        this.element.textContent = currentWord.substring(0, this.charIndex);

        if (!this.isDeleting && this.charIndex === currentWord.length) {
            delay = 2000;
            this.isDeleting = true;
        } else if (this.isDeleting && this.charIndex === 0) {
            this.isDeleting = false;
            this.wordIndex = (this.wordIndex + 1) % this.words.length;
            delay = 500;
        }

        setTimeout(() => this.type(), delay);
    }
}

// ===== AI CHATBOT =====
class AIChatbot {
    constructor() {
        this.resumeData = {
            name: "Alex Morgan",
            role: "Full-Stack Developer & AI Enthusiast",
            email: "alex@example.com",
            phone: "+1 (555) 123-4567",
            location: "San Francisco, CA",
            experience: "5+ years",
            education: "M.S. Computer Science from Stanford University",
            skills: {
                frontend: ["React", "JavaScript", "HTML/CSS", "Vue.js", "Tailwind CSS"],
                backend: ["Node.js", "Python", "MongoDB", "PostgreSQL"],
                ai: ["TensorFlow", "PyTorch", "NLP"],
                tools: ["Git", "Docker", "AWS"]
            },
            jobs: [
                { title: "Senior Full-Stack Developer", company: "TechCorp AI", period: "2022-Present" },
                { title: "Full-Stack Developer", company: "InnovateTech Solutions", period: "2020-2022" },
                { title: "Junior Developer", company: "StartupHub", period: "2019-2020" }
            ],
            projects: [
                "AI Content Generator - AI-powered platform using GPT-4",
                "Analytics Dashboard - Real-time analytics with custom widgets",
                "Smart Shop Platform - E-commerce with AI recommendations",
                "CollabSpace - Real-time collaboration tool with video"
            ]
        };

        this.init();
    }

    init() {
        const toggle = document.getElementById('chatToggle');
        const close = document.getElementById('chatClose');
        const send = document.getElementById('chatSend');
        const input = document.getElementById('chatInput');
        const window = document.getElementById('chatWindow');
        const quickBtns = document.querySelectorAll('.quick-btn');

        toggle.addEventListener('click', () => {
            window.classList.toggle('active');
            toggle.style.display = window.classList.contains('active') ? 'none' : 'flex';
        });

        close.addEventListener('click', () => {
            window.classList.remove('active');
            toggle.style.display = 'flex';
        });

        send.addEventListener('click', () => this.sendMessage());
        input.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') this.sendMessage();
        });

        quickBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                input.value = btn.dataset.question;
                this.sendMessage();
            });
        });
    }

    sendMessage() {
        const input = document.getElementById('chatInput');
        const message = input.value.trim();
        if (!message) return;

        this.addMessage(message, 'user');
        input.value = '';

        // Simulate typing delay
        setTimeout(() => {
            const response = this.generateResponse(message);
            this.addMessage(response, 'bot');
        }, 600 + Math.random() * 800);
    }

    addMessage(text, type) {
        const container = document.getElementById('chatMessages');
        const msg = document.createElement('div');
        msg.className = `message ${type}`;
        msg.innerHTML = `<p>${text}</p>`;
        container.appendChild(msg);
        container.scrollTop = container.scrollHeight;
    }

    generateResponse(query) {
        const q = query.toLowerCase();
        const d = this.resumeData;

        // Greeting patterns
        if (q.match(/^(hi|hello|hey|howdy|greetings|sup|yo)/)) {
            return `👋 Hello! I'm ${d.name}'s AI assistant. I can tell you about skills, experience, projects, education, or contact info. What would you like to know?`;
        }

        // Skills
        if (q.match(/skill|tech|stack|know|language|framework|what.*use/)) {
            const all = Object.values(d.skills).flat();
            return `🛠 <strong>Technical Skills:</strong><br><br>
                <strong>Frontend:</strong> ${d.skills.frontend.join(', ')}<br>
                <strong>Backend:</strong> ${d.skills.backend.join(', ')}<br>
                <strong>AI/ML:</strong> ${d.skills.ai.join(', ')}<br>
                <strong>Tools:</strong> ${d.skills.tools.join(', ')}<br><br>
                That's ${all.length} technologies in total! 🚀`;
        }

        // Experience
        if (q.match(/experience|work|job|career|employ|company|where.*work/)) {
            let jobs = d.jobs.map(j => `• <strong>${j.title}</strong> at ${j.company} (${j.period})`).join('<br>');
            return `💼 <strong>Work Experience (${d.experience}):</strong><br><br>${jobs}<br><br>Currently working at TechCorp AI building AI-powered applications!`;
        }

        // Projects
        if (q.match(/project|portfolio|built|build|create|made|work.*on/)) {
            let projects = d.projects.map(p => `• ${p}`).join('<br>');
            return `🚀 <strong>Featured Projects:</strong><br><br>${projects}<br><br>Check out the Projects section for more details!`;
        }

        // Education
        if (q.match(/edu|school|university|degree|study|learn|college|stanford/)) {
            return `🎓 <strong>Education:</strong><br><br>${d.education}<br><br>Specialized in Artificial Intelligence and Machine Learning with published research in NLP.`;
        }

        // Contact
        if (q.match(/contact|email|phone|reach|hire|connect|message|call/)) {
            return `📧 <strong>Contact Information:</strong><br><br>
                📩 Email: ${d.email}<br>
                📱 Phone: ${d.phone}<br>
                📍 Location: ${d.location}<br><br>
                You can also use the contact form on the website! Currently open to new opportunities. 💼`;
        }

        // Location
        if (q.match(/where|location|based|live|city|from/)) {
            return `📍 ${d.name} is based in <strong>${d.location}</strong>. Open to both on-site and remote opportunities!`;
        }

        // Name/Who
        if (q.match(/who|name|about|tell.*about/)) {
            return `👨‍💻 <strong>${d.name}</strong> is a ${d.role} with ${d.experience} of experience, based in ${d.location}. Passionate about building innovative solutions with modern tech! Check the About section for more.`;
        }

        // Resume/Download
        if (q.match(/resume|cv|download|pdf/)) {
            return `📄 You can download the resume by clicking the <strong>"Resume"</strong> button in the navigation bar at the top! It's available in PDF format.`;
        }

        // Thank you
        if (q.match(/thank|thanks|thx|appreciate/)) {
            return `😊 You're welcome! Feel free to ask anything else about ${d.name}'s profile. Happy to help!`;
        }

        // Fallback
        return `🤔 Interesting question! I can help you with:<br><br>
            • <strong>Skills</strong> - Technical abilities<br>
            • <strong>Experience</strong> - Work history<br>
            • <strong>Projects</strong> - Portfolio work<br>
            • <strong>Education</strong> - Academic background<br>
            • <strong>Contact</strong> - How to reach out<br><br>
            Try asking about any of these topics! 💡`;
    }
}

// ===== COUNTER ANIMATION =====
function animateCounters() {
    const stats = document.querySelectorAll('.stat');
    stats.forEach(stat => {
        const target = parseInt(stat.dataset.count);
        const numberEl = stat.querySelector('.stat-number');
        const duration = 2000;
        const step = target / (duration / 16);
        let current = 0;

        const timer = setInterval(() => {
            current += step;
            if (current >= target) {
                current = target;
                clearInterval(timer);
            }
            numberEl.textContent = Math.floor(current) + '+';
        }, 16);
    });
}

// ===== SKILLS FILTER =====
function initSkillsFilter() {
    const filterBtns = document.querySelectorAll('.filter-btn');
    const skillCards = document.querySelectorAll('.skill-card');

    filterBtns.forEach(btn => {
        btn.addEventListener('click', () => {
            filterBtns.forEach(b => b.classList.remove('active'));
            btn.classList.add('active');

            const filter = btn.dataset.filter;

            skillCards.forEach(card => {
                if (filter === 'all' || card.dataset.category === filter) {
                    card.classList.remove('hidden');
                    card.style.display = '';
                } else {
                    card.classList.add('hidden');
                }
            });
        });
    });
}

// ===== INTERSECTION OBSERVER =====
function initScrollAnimations() {
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('visible');

                // Animate skill bars
                if (entry.target.classList.contains('skill-card')) {
                    entry.target.classList.add('animate');
                }
            }
        });
    }, { threshold: 0.2 });

    // Observe skill cards
    document.querySelectorAll('.skill-card').forEach(card => observer.observe(card));

    // Observe timeline items
    document.querySelectorAll('.timeline-item').forEach(item => observer.observe(item));

    // Counter animation
    const heroSection = document.getElementById('home');
    const counterObserver = new IntersectionObserver((entries) => {
        if (entries[0].isIntersecting) {
            animateCounters();
            counterObserver.unobserve(heroSection);
        }
    }, { threshold: 0.5 });
    counterObserver.observe(heroSection);
}

// ===== ACTIVE NAV LINK =====
function initActiveNav() {
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('.nav-link');

    window.addEventListener('scroll', () => {
        let current = '';
        sections.forEach(section => {
            const sectionTop = section.offsetTop - 100;
            if (window.scrollY >= sectionTop) {
                current = section.getAttribute('id');
            }
        });

        navLinks.forEach(link => {
            link.classList.remove('active');
            if (link.getAttribute('href') === `#${current}`) {
                link.classList.add('active');
            }
        });
    });
}

// ===== NAVBAR SCROLL =====
function initNavbarScroll() {
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
        navbar.classList.toggle('scrolled', window.scrollY > 50);
    });
}

// ===== MOBILE MENU =====
function initMobileMenu() {
    const hamburger = document.getElementById('hamburger');
    const navMenu = document.getElementById('navMenu');
    const navLinks = document.querySelectorAll('.nav-link');

    hamburger.addEventListener('click', () => {
        hamburger.classList.toggle('active');
        navMenu.classList.toggle('active');
    });

    navLinks.forEach(link => {
        link.addEventListener('click', () => {
            hamburger.classList.remove('active');
            navMenu.classList.remove('active');
        });
    });
}

// ===== THEME TOGGLE =====
function initThemeToggle() {
    const toggle = document.getElementById('themeToggle');
    const icon = toggle.querySelector('i');

    // Load saved theme
    const savedTheme = localStorage.getItem('theme') || 'dark';
    document.documentElement.setAttribute('data-theme', savedTheme);
    updateIcon(savedTheme);

    toggle.addEventListener('click', () => {
        const current = document.documentElement.getAttribute('data-theme');
        const next = current === 'dark' ? 'light' : 'dark';
        document.documentElement.setAttribute('data-theme', next);
        localStorage.setItem('theme', next);
        updateIcon(next);
    });

    function updateIcon(theme) {
        icon.className = theme === 'dark' ? 'fas fa-moon' : 'fas fa-sun';
    }
}

// ===== GREETING BASED ON TIME =====
function initGreeting() {
    const el = document.getElementById('greetingText');
    const hour = new Date().getHours();
    let greeting;

    if (hour < 12) greeting = 'Good Morning! ☀️';
    else if (hour < 17) greeting = 'Good Afternoon! 🌤️';
    else if (hour < 21) greeting = 'Good Evening! 🌆';
    else greeting = 'Hello, Night Owl! 🌙';

    el.textContent = greeting;
}

// ===== CONTACT FORM =====
function initContactForm() {
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', (e) => {
        e.preventDefault();

        const btn = form.querySelector('button[type="submit"]');
        const originalText = btn.innerHTML;

        btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Sending...';
        btn.disabled = true;

        setTimeout(() => {
            btn.innerHTML = '<i class="fas fa-check"></i> Message Sent!';
            btn.style.background = 'linear-gradient(135deg, #22c55e, #16a34a)';

            setTimeout(() => {
                btn.innerHTML = originalText;
                btn.style.background = '';
                btn.disabled = false;
                form.reset();
            }, 3000);
        }, 1500);
    });
}

// ===== DOWNLOAD RESUME =====
function initDownloadResume() {
    document.getElementById('downloadResume').addEventListener('click', (e) => {
        e.preventDefault();
        // In production, link to actual PDF
        alert('📄 Resume download would start here!\n\nReplace this with an actual PDF link in production.');
    });
}

// ===== SMOOTH REVEAL ON SCROLL =====
function initSmoothReveal() {
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    }, { threshold: 0.1 });

    document.querySelectorAll('.section-header, .about-content, .contact-content, .projects-grid').forEach(el => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(30px)';
        el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
        observer.observe(el);
    });
}

// ===== INITIALIZE EVERYTHING =====
document.addEventListener('DOMContentLoaded', () => {
    // Particle Background
    new ParticleBackground();

    // Typewriter
    new Typewriter(
        document.getElementById('typewriter'),
        [
            'intelligent web apps.',
            'AI-powered solutions.',
            'beautiful interfaces.',
            'scalable backends.',
            'the future of tech.'
        ],
        80
    );

    // AI Chatbot
    new AIChatbot();

    // Init all features
    initThemeToggle();
    initGreeting();
    initNavbarScroll();
    initMobileMenu();
    initActiveNav();
    initScrollAnimations();
    initSkillsFilter();
    initContactForm();
    initDownloadResume();
    initSmoothReveal();
});
    
}
