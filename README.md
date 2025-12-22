<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shubham Kumar Pandey | AI & Cybersecurity</title>
    <style>
        :root {
            --primary-bg: #0a0e1a;
            --secondary-bg: #151922;
            --accent-cyan: #00ffff;
            --accent-blue: #0078ff;
            --accent-purple: #7c3aed;
            --accent-green: #10b981;
            --text-primary: #e5e7eb;
            --text-secondary: #9ca3af;
            --glass-bg: rgba(20, 25, 40, 0.7);
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Courier New', monospace;
        }

        body {
            background-color: var(--primary-bg);
            color: var(--text-primary);
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* बैकग्राउंड एनिमेशन */
        .bg-animation {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
            opacity: 0.1;
            background-image: 
                radial-gradient(circle at 20% 30%, var(--accent-cyan) 0%, transparent 8%),
                radial-gradient(circle at 75% 40%, var(--accent-blue) 0%, transparent 6%),
                radial-gradient(circle at 46% 52%, var(--accent-purple) 0%, transparent 7%),
                radial-gradient(circle at 80% 70%, var(--accent-green) 0%, transparent 6%);
            animation: bgAnimation 20s ease infinite;
        }

        @keyframes bgAnimation {
            0%, 100% { transform: translate(0, 0) scale(1); }
            33% { transform: translate(-20px, -20px) scale(1.05); }
            66% { transform: translate(20px, -10px) scale(0.95); }
        }

        /* हीरो सेक्शन */
        .hero {
            text-align: center;
            padding: 40px 0;
            position: relative;
            border-bottom: 1px solid var(--glass-border);
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, var(--accent-cyan), var(--accent-blue));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 20px rgba(0, 255, 255, 0.3);
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 5px rgba(0, 255, 255, 0.5)); }
            to { filter: drop-shadow(0 0 15px rgba(0, 255, 255, 0.8)); }
        }

        .subtitle {
            font-size: 1.3rem;
            color: var(--text-secondary);
            margin-bottom: 30px;
        }

        .dynamic-tagline {
            font-family: 'Courier New', monospace;
            font-size: 1.1rem;
            color: var(--accent-green);
            margin-bottom: 40px;
            min-height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .cursor {
            display: inline-block;
            width: 3px;
            height: 1.2rem;
            background-color: var(--accent-green);
            margin-left: 5px;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .btn {
            padding: 12px 25px;
            border: 1px solid var(--accent-cyan);
            background: rgba(0, 255, 255, 0.1);
            color: var(--accent-cyan);
            text-decoration: none;
            border-radius: 4px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 500;
        }

        .btn:hover {
            background: rgba(0, 255, 255, 0.2);
            box-shadow: 0 0 15px rgba(0, 255, 255, 0.5);
            transform: translateY(-3px);
        }

        /* सेक्शन कॉमन स्टाइल */
        .section {
            padding: 40px 0;
            position: relative;
        }

        .section-title {
            font-size: 2.2rem;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent-cyan), transparent);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* अबाउट सेक्शन */
        .about-card {
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid var(--glass-border);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            margin: 0 auto;
            max-width: 800px;
        }

        /* स्किल्स सेक्शन */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid var(--glass-border);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }

        .skill-category h3 {
            color: var(--accent-cyan);
            margin-bottom: 15px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 8px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .skill-name {
            color: var(--text-primary);
        }

        .skill-tag {
            font-size: 0.8rem;
            padding: 3px 8px;
            border-radius: 4px;
            background: rgba(0, 255, 255, 0.1);
            color: var(--accent-cyan);
            font-family: 'Courier New', monospace;
        }

        /* प्रोजेक्ट्स सेक्शन */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid var(--glass-border);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, var(--accent-cyan), var(--accent-blue));
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
        }

        .project-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--accent-cyan);
        }

        .project-description {
            color: var(--text-secondary);
            margin-bottom: 20px;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--accent-blue);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            color: var(--accent-cyan);
            transform: translateX(5px);
        }

        /* एजुकेशन सेक्शन */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 2px;
            background: var(--accent-cyan);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1px;
        }

        .timeline-item {
            padding: 20px 40px;
            position: relative;
            width: 50%;
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            right: -7px;
            background: var(--primary-bg);
            border: 2px solid var(--accent-cyan);
            top: 25px;
            border-radius: 50%;
            z-index: 1;
        }

        .left {
            left: 0;
        }

        .right {
            left: 50%;
        }

        .right::after {
            left: -7px;
        }

        .timeline-content {
            padding: 20px;
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border-radius: 10px;
            border: 1px solid var(--glass-border);
        }

        .timeline-date {
            color: var(--accent-cyan);
            font-family: 'Courier New', monospace;
            margin-bottom: 10px;
        }

        /* कॉन्टैक्ट सेक्शन */
        .contact-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-text {
            margin-bottom: 30px;
            color: var(--text-secondary);
        }

        .contact-links {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--text-primary);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .contact-link:hover {
            color: var(--accent-cyan);
            transform: translateY(-3px);
        }

        .contact-link i {
            font-size: 1.5rem;
        }

        /* फुटर */
        footer {
            padding: 30px 0;
            text-align: center;
            background: var(--secondary-bg);
            border-top: 1px solid var(--glass-border);
            margin-top: 40px;
        }

        /* रेस्पॉन्सिव डिजाइन */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item::after {
                left: 23px;
            }
            
            .right {
                left: 0%;
            }
        }
    </style>
</head>
<body>
    <div class="bg-animation"></div>
    
    <div class="container">
        <!-- हीरो सेक्शन -->
        <section id="home" class="hero">
            <h1>Shubham Kumar Pandey</h1>
            <p class="subtitle">AI & Cybersecurity Student @ IIT Patna (BS AICS '29)</p>
            <div class="dynamic-tagline">
                <span id="tagline-text">Designing secure AI systems at the intersection of machine learning and cybersecurity.</span><span class="cursor"></span>
            </div>
            <div class="hero-buttons">
                <a href="https://github.com/AICyberShubham" class="btn">
                    <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://www.linkedin.com/in/shubham-kumar-pandey-iitp/" class="btn">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="https://x.com/AICyberShubham" class="btn">
                    <i class="fab fa-twitter"></i> X (Twitter)
                </a>
            </div>
        </section>
        
        <!-- अबाउट सेक्शन -->
        <section id="about" class="section">
            <h2 class="section-title">About</h2>
            <div class="about-card">
                <p>I am currently pursuing a Bachelor of Science in Artificial Intelligence & Cybersecurity at the Indian Institute of Technology, Patna.</p>
                <br>
                <p>My interests lie in understanding how modern AI systems can be attacked, misused, and ultimately secured — from traditional infrastructure to large language models.</p>
                <br>
                <p>I focus on building strong foundations in Python, machine learning, Linux, and core cybersecurity concepts, with a long-term goal of working in AI security and LLM defense.</p>
            </div>
        </section>
        
        <!-- स्किल्स सेक्शन -->
        <section id="skills" class="section">
            <h2 class="section-title">Skills</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3><i class="fas fa-brain"></i> AI & Machine Learning</h3>
                    <div class="skill-item">
                        <span class="skill-name">Python for AI</span>
                        <span class="skill-tag">[FOUNDATION]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Machine learning fundamentals</span>
                        <span class="skill-tag">[FOUNDATION]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Generative AI basics</span>
                        <span class="skill-tag">[LEARNING]</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-shield-alt"></i> Cybersecurity</h3>
                    <div class="skill-item">
                        <span class="skill-name">Linux systems & CLI</span>
                        <span class="skill-tag">[FOUNDATION]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Networking fundamentals</span>
                        <span class="skill-tag">[FOUNDATION]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Security principles</span>
                        <span class="skill-tag">[FOUNDATION]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Ethical hacking fundamentals</span>
                        <span class="skill-tag">[LEARNING]</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-tools"></i> Tools & Platforms</h3>
                    <div class="skill-item">
                        <span class="skill-name">Git & GitHub</span>
                        <span class="skill-tag">[ACTIVE]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Cloud fundamentals</span>
                        <span class="skill-tag">[LEARNING]</span>
                    </div>
                    <div class="skill-item">
                        <span class="skill-name">Terminal-based workflows</span>
                        <span class="skill-tag">[ACTIVE]</span>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- प्रोजेक्ट्स सेक्शन -->
        <section id="projects" class="section">
            <h2 class="section-title">Projects</h2>
            <div class="projects-container">
                <div class="project-card">
                    <h3 class="project-title">AI Security Engineer Roadmap</h3>
                    <p class="project-description">A publicly available roadmap documenting my learning journey from core programming and machine learning fundamentals to AI security, LLM security, and defensive system design.</p>
                    <a href="https://github.com/AICyberShubham/ai-security-engineer-roadmap" class="project-link">
                        View Project <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">Python Automation Scripts</h3>
                    <p class="project-description">A collection of Python scripts for automating various cybersecurity tasks, including network scanning, vulnerability assessment, and log analysis.</p>
                    <a href="#" class="project-link">
                        In Progress <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">AI + Cybersecurity Mini Labs</h3>
                    <p class="project-description">A series of hands-on mini-labs exploring the intersection of AI and cybersecurity, including adversarial attacks on ML models and AI-powered security tools.</p>
                    <a href="#" class="project-link">
                        Planned <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </section>
        
        <!-- एजुकेशन सेक्शन -->
        <section id="education" class="section">
            <h2 class="section-title">Education & Certifications</h2>
            <div class="timeline">
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <div class="timeline-date">2025 - 2029</div>
                        <h3>Indian Institute of Technology, Patna</h3>
                        <p>Bachelor of Science (BS) – Artificial Intelligence & Cybersecurity</p>
                    </div>
                </div>
                
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <div class="timeline-date">2025</div>
                        <h3>Introduction to Generative AI</h3>
                        <p>IBM Certification</p>
                    </div>
                </div>
                
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <div class="timeline-date">2025</div>
                        <h3>Oracle Cloud Infrastructure 2025 AI Foundations</h3>
                        <p>Oracle Certification</p>
                    </div>
                </div>
                
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <div class="timeline-date">2025</div>
                        <h3>Programming with Generative AI</h3>
                        <p>Certification</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- कॉन्टैक्ट सेक्शन -->
        <section id="contact" class="section">
            <h2 class="section-title">Contact</h2>
            <div class="contact-container">
                <p class="contact-text">Currently building strong foundations in AI Security and Cybersecurity. Open to mentorship, learning opportunities, and foundational internships.</p>
                <div class="contact-links">
                    <a href="mailto:shubhamkpandey009@gmail.com" class="contact-link">
                        <i class="fas fa-envelope"></i> shubhamkpandey009@gmail.com
                    </a>
                    <a href="https://github.com/AICyberShubham" class="contact-link">
                        <i class="fab fa-github"></i> github.com/AICyberShubham
                    </a>
                    <a href="https://www.linkedin.com/in/shubham-kumar-pandey-iitp/" class="contact-link">
                        <i class="fab fa-linkedin"></i> linkedin.com/in/shubham-kumar-pandey-iitp
                    </a>
                </div>
            </div>
        </section>
        
        <!-- फुटर -->
        <footer>
            <p>&copy; 2025 Shubham Kumar Pandey. All Rights Reserved.</p>
        </footer>
    </div>

    <script>
        // डायनामिक टैगलाइन रोटेटर
        const taglines = [
            "Designing secure AI systems at the intersection of machine learning and cybersecurity.",
            "Securing intelligent systems against modern cyber threats.",
            "Where artificial intelligence meets cyber defense.",
            "Building resilient AI systems for a hostile digital world.",
            "Exploring the security boundaries of intelligent machines.",
            "Defending AI models, data, and systems in the age of automation."
        ];
        
        const taglineElement = document.getElementById('tagline-text');
        let taglineIndex = Math.floor(Math.random() * taglines.length);
        let charIndex = 0;
        let isDeleting = false;
        let typingSpeed = 50;
        
        function typeTagline() {
            const currentTagline = taglines[taglineIndex];
            
            if (!isDeleting) {
                taglineElement.textContent = currentTagline.substring(0, charIndex + 1);
                charIndex++;
                
                if (charIndex === currentTagline.length) {
                    isDeleting = true;
                    typingSpeed = 2000; // पूरा टैगलाइन दिखाने के बाद रुकें
                } else {
                    typingSpeed = 50;
                }
            } else {
                taglineElement.textContent = currentTagline.substring(0, charIndex - 1);
                charIndex--;
                
                if (charIndex === 0) {
                    isDeleting = false;
                    taglineIndex = (taglineIndex + 1) % taglines.length;
                    typingSpeed = 500; // अगला टैगलाइन शुरू करने से पहले रुकें
                } else {
                    typingSpeed = 30;
                }
            }
            
            setTimeout(typeTagline, typingSpeed);
        }
        
        // पेज लोड होने पर टाइपिंग इफेक्ट शुरू करें
        window.addEventListener('load', () => {
            setTimeout(typeTagline, 1000);
        });
        
        // स्मूथ स्क्रॉलिंग
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
