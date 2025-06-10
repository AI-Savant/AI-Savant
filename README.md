<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blockchain Developer & AI Automation Specialist</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: #0a0a0a;
            color: #ffffff;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Particle Background */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: radial-gradient(circle at 20% 50%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%),
                        radial-gradient(circle at 40% 80%, rgba(120, 219, 255, 0.3) 0%, transparent 50%);
            animation: particleFloat 20s ease-in-out infinite;
        }

        @keyframes particleFloat {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-20px) rotate(120deg); }
            66% { transform: translateY(10px) rotate(240deg); }
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="a" cx="50%" cy="50%"><stop offset="0%" stop-color="%23ffffff" stop-opacity="0.1"/><stop offset="100%" stop-color="%23ffffff" stop-opacity="0"/></radialGradient></defs><circle cx="200" cy="200" r="100" fill="url(%23a)"><animate attributeName="cx" values="200;800;200" dur="20s" repeatCount="indefinite"/></circle><circle cx="800" cy="300" r="150" fill="url(%23a)"><animate attributeName="cy" values="300;700;300" dur="25s" repeatCount="indefinite"/></circle><circle cx="400" cy="600" r="80" fill="url(%23a)"><animate attributeName="r" values="80;120;80" dur="15s" repeatCount="indefinite"/></circle></svg>');
            opacity: 0.3;
            animation: backgroundShift 30s ease-in-out infinite;
        }

        @keyframes backgroundShift {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.1) rotate(180deg); }
        }

        .hero-content {
            text-align: center;
            z-index: 2;
            max-width: 800px;
            padding: 2rem;
        }

        .hero-title {
            font-size: clamp(2.5rem, 8vw, 6rem);
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4, #ffeaa7);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientShift 4s ease-in-out infinite;
            transform: perspective(1000px) rotateX(15deg);
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 4vw, 2rem);
            margin-bottom: 2rem;
            opacity: 0;
            animation: fadeInUp 1s ease-out 0.5s forwards;
        }

        .typewriter {
            font-size: clamp(1rem, 3vw, 1.5rem);
            color: #64ffda;
            margin-bottom: 3rem;
            min-height: 2em;
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

        /* 3D Floating Elements */
        .floating-element {
            position: absolute;
            width: 100px;
            height: 100px;
            background: linear-gradient(45deg, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.05));
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            animation: float3D 6s ease-in-out infinite;
        }

        .floating-element:nth-child(1) {
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-element:nth-child(2) {
            top: 60%;
            right: 15%;
            animation-delay: 2s;
        }

        .floating-element:nth-child(3) {
            bottom: 20%;
            left: 20%;
            animation-delay: 4s;
        }

        @keyframes float3D {
            0%, 100% {
                transform: translateY(0px) rotateX(0deg) rotateY(0deg);
            }
            33% {
                transform: translateY(-20px) rotateX(15deg) rotateY(15deg);
            }
            66% {
                transform: translateY(10px) rotateX(-10deg) rotateY(-10deg);
            }
        }

        /* About Section */
        .about {
            padding: 8rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }

        .section-title {
            font-size: clamp(2rem, 6vw, 4rem);
            text-align: center;
            margin-bottom: 4rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
            animation: expandLine 2s ease-out;
        }

        @keyframes expandLine {
            from { width: 0; }
            to { width: 100px; }
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.2rem;
            line-height: 1.8;
            opacity: 0;
            transform: translateX(-50px);
            animation: slideInLeft 1s ease-out forwards;
        }

        .about-visual {
            position: relative;
            height: 400px;
            opacity: 0;
            transform: translateX(50px);
            animation: slideInRight 1s ease-out 0.3s forwards;
        }

        @keyframes slideInLeft {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInRight {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .tech-cube {
            position: absolute;
            width: 80px;
            height: 80px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 15px;
            animation: rotateCube 10s linear infinite;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 0.8rem;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }

        .tech-cube:nth-child(1) {
            top: 50px;
            left: 50px;
            animation-delay: 0s;
        }

        .tech-cube:nth-child(2) {
            top: 150px;
            right: 80px;
            animation-delay: 3s;
        }

        .tech-cube:nth-child(3) {
            bottom: 100px;
            left: 100px;
            animation-delay: 6s;
        }

        @keyframes rotateCube {
            0% { transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg); }
            33% { transform: rotateX(120deg) rotateY(120deg) rotateZ(0deg); }
            66% { transform: rotateX(240deg) rotateY(240deg) rotateZ(120deg); }
            100% { transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg); }
        }

        /* Technical Arsenal */
        .skills {
            padding: 8rem 2rem;
            background: linear-gradient(135deg, rgba(10, 10, 10, 0.9), rgba(30, 30, 30, 0.9));
            position: relative;
        }

        .skills-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            margin-top: 4rem;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transform: translateY(50px);
            opacity: 0;
            animation: fadeInUp 1s ease-out forwards;
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.2);
        }

        .skill-category:nth-child(1) { animation-delay: 0.2s; }
        .skill-category:nth-child(2) { animation-delay: 0.4s; }
        .skill-category:nth-child(3) { animation-delay: 0.6s; }

        .skill-category h3 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: #64ffda;
            position: relative;
        }

        .skill-item {
            margin-bottom: 1.5rem;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .skill-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            overflow: hidden;
            position: relative;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1);
            border-radius: 4px;
            width: 0;
            animation: fillBar 2s ease-out forwards;
            position: relative;
        }

        .skill-progress::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: shimmer 2s ease-in-out infinite;
        }

        @keyframes fillBar {
            to { width: var(--width); }
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Interactive 3D Elements */
        .tech-sphere {
            position: absolute;
            top: 20%;
            right: 10%;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: conic-gradient(from 0deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4, #ffeaa7, #ff6b6b);
            animation: rotateSphere 15s linear infinite;
            opacity: 0.7;
        }

        @keyframes rotateSphere {
            from { transform: rotate(0deg) scale(1); }
            50% { transform: rotate(180deg) scale(1.1); }
            to { transform: rotate(360deg) scale(1); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .about-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .skills-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .floating-element {
                display: none;
            }

            .hero-content {
                padding: 1rem;
            }
        }

        /* Scroll Animations */
        .scroll-reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease-out;
        }

        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }

        /* Loading Animation */
        .loading-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0a0a0a;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            animation: fadeOut 2s ease-out 3s forwards;
        }

        .loading-spinner {
            width: 60px;
            height: 60px;
            border: 3px solid rgba(255, 255, 255, 0.1);
            border-top: 3px solid #64ffda;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes fadeOut {
            to {
                opacity: 0;
                visibility: hidden;
            }
        }
    </style>
</head>
<body>
    <!-- Loading Animation -->
    <div class="loading-overlay">
        <div class="loading-spinner"></div>
    </div>

    <!-- Particle Background -->
    <div class="particles"></div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        
        <div class="hero-content">
            <h1 class="hero-title">Blockchain Developer</h1>
            <h2 class="hero-subtitle">Building the Future with Code & Intelligence</h2>
            <div class="typewriter" id="typewriter"></div>
        </div>
    </section>

    <!-- About Me Section -->
    <section class="about scroll-reveal">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div class="about-text">
                <p>I'm a passionate Blockchain Developer with a vision to revolutionize the digital landscape through innovative decentralized solutions. My journey spans across smart contract development, DeFi protocols, and NFT ecosystems, where I craft secure and scalable blockchain applications.</p>
                
                <p>Currently expanding my expertise into AI Agents and Automation workflows, I'm building the bridge between blockchain technology and artificial intelligence. This unique combination allows me to create intelligent, autonomous systems that can interact with blockchain networks, automate complex processes, and deliver unprecedented value.</p>
                
                <p>My mission is to merge cutting-edge blockchain technology with AI-powered automation to create solutions that not only solve today's problems but anticipate tomorrow's challenges.</p>
            </div>
            
            <div class="about-visual">
                <div class="tech-cube">ETH</div>
                <div class="tech-cube">AI</div>
                <div class="tech-cube">WEB3</div>
            </div>
        </div>
    </section>

    <!-- Technical Arsenal -->
    <section class="skills scroll-reveal">
        <div class="tech-sphere"></div>
        <div class="skills-container">
            <h2 class="section-title">Technical Arsenal</h2>
            
            <div class="skills-grid">
                <!-- Blockchain Mastery -->
                <div class="skill-category">
                    <h3>Blockchain Mastery</h3>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Solidity</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 95%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Ethereum & Polygon</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 90%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Web3.js & Ethers.js</span>
                            <span>88%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 88%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Hardhat & Truffle</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 85%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>DeFi & NFTs</span>
                            <span>82%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 82%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>IPFS & MetaMask</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 80%"></div>
                        </div>
                    </div>
                </div>

                <!-- AI & Automation -->
                <div class="skill-category">
                    <h3>AI & Automation</h3>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Python</span>
                            <span>92%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 92%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>TensorFlow</span>
                            <span>78%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 78%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>LangChain & Langflow</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 85%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>OpenAI GPT APIs</span>
                            <span>88%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 88%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>n8n & Zapier</span>
                            <span>82%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 82%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Hugging Face</span>
                            <span>75%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 75%"></div>
                        </div>
                    </div>
                </div>

                <!-- Full-Stack Development -->
                <div class="skill-category">
                    <h3>Full-Stack Development</h3>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>JavaScript & TypeScript</span>
                            <span>93%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 93%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Next.js</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 90%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>HTML5 & CSS3</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 95%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>MongoDB</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="--width: 85%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <script>
        // Typewriter Effect
        const typewriterText = [
            "Crafting Smart Contracts with Precision",
            "Building DeFi Protocols that Scale",
            "Creating AI-Powered Automation",
            "Developing Next-Gen dApps",
            "Merging Blockchain with Intelligence"
        ];
        
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typewriterElement = document.getElementById('typewriter');
        
        function typeWriter() {
            const currentText = typewriterText[textIndex];
            
            if (isDeleting) {
                typewriterElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typewriterElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            let typeSpeed = isDeleting ? 50 : 100;
            
            if (!isDeleting && charIndex === currentText.length) {
                typeSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % typewriterText.length;
                typeSpeed = 500;
            }
            
            setTimeout(typeWriter, typeSpeed);
        }
        
        // Start typewriter effect after loading
        setTimeout(typeWriter, 3500);
        
        // Scroll Reveal Animation
        function revealOnScroll() {
            const reveals = document.querySelectorAll('.scroll-reveal');
            
            reveals.forEach(element => {
                const windowHeight = window.innerHeight;
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < windowHeight - elementVisible) {
                    element.classList.add('revealed');
                }
            });
        }
        
        window.addEventListener('scroll', revealOnScroll);
        
        // Smooth scrolling for better performance
        let ticking = false;
        
        function updateScrollAnimations() {
            revealOnScroll();
            ticking = false;
        }
        
        window.addEventListener('scroll', () => {
            if (!ticking) {
                requestAnimationFrame(updateScrollAnimations);
                ticking = true;
            }
        });
        
        // Initialize animations on load
        window.addEventListener('load', () => {
            revealOnScroll();
        });
        
        // Interactive hover effects for skill categories
        document.querySelectorAll('.skill-category').forEach(category => {
            category.addEventListener('mouseenter', () => {
                category.style.transform = 'translateY(-10px) scale(1.02) rotateX(5deg)';
            });
            
            category.addEventListener('mouseleave', () => {
                category.style.transform = 'translateY(0) scale(1) rotateX(0deg)';
            });
        });
        
        // Parallax effect for floating elements
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallaxElements = document.querySelectorAll('.floating-element');
            
            parallaxElements.forEach((element, index) => {
                const speed = 0.5 + (index * 0.1);
                element.style.transform = `translateY(${scrolled * speed}px) rotateX(${scrolled * 0.1}deg)`;
            });
        });
    </script>
</body>
</html>


