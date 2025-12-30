<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="GiantX Algo - Learn Professional Algorithmic Trading">
    <title>GiantX Algo | Master Algorithmic Trading</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: #1a1a1a;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            width: 100%;
            top: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0,0,0,0.05);
            z-index: 1000;
            padding: 1rem 0;
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -1px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            align-items: center;
        }

        .nav-links a {
            color: #4b5563;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #6366f1;
        }

        .nav-cta {
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            color: white;
            padding: 0.7rem 1.8rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .nav-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(99, 102, 241, 0.3);
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            min-height: 90vh;
            background: linear-gradient(135deg, #1e1b4b 0%, #312e81 50%, #4c1d95 100%);
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 150%;
            height: 150%;
            background: radial-gradient(circle, rgba(139, 92, 246, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: gridMove 20s linear infinite;
        }

        @keyframes gridMove {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 4rem 2rem;
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-content h1 {
            font-size: 4rem;
            font-weight: 900;
            color: white;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            letter-spacing: -2px;
        }

        .hero-content h1 span {
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-content p {
            font-size: 1.3rem;
            color: rgba(255, 255, 255, 0.85);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        .hero-stats {
            display: flex;
            gap: 3rem;
            margin-bottom: 2.5rem;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: #60a5fa;
            display: block;
        }

        .stat-label {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }

        .hero-cta {
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            background: white;
            color: #6366f1;
            padding: 1.2rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            transition: all 0.3s;
        }

        .hero-cta:hover {
            transform: translateY(-3px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.4);
        }

        .hero-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 24px;
            padding: 2.5rem;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
        }

        .hero-card h3 {
            color: white;
            font-size: 1.8rem;
            margin-bottom: 2rem;
            font-weight: 700;
        }

        .card-features {
            display: flex;
            flex-direction: column;
            gap: 1.2rem;
            margin-bottom: 2rem;
        }

        .card-feature {
            display: flex;
            align-items: center;
            gap: 1rem;
            color: rgba(255, 255, 255, 0.9);
        }

        .card-feature::before {
            content: "✓";
            width: 24px;
            height: 24px;
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            font-weight: bold;
        }

        .card-cta {
            width: 100%;
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            color: white;
            padding: 1rem;
            border: none;
            border-radius: 12px;
            font-weight: 700;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
        }

        .card-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(96, 165, 250, 0.4);
        }

        /* Features Section */
        .features {
            padding: 6rem 2rem;
            background: #fafafa;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-header .badge {
            display: inline-block;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            color: white;
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .section-header h2 {
            font-size: 3rem;
            font-weight: 800;
            color: #1a1a1a;
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }

        .section-header p {
            font-size: 1.2rem;
            color: #6b7280;
            max-width: 700px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
        }

        .feature-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border-color: #6366f1;
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .feature-card h3 {
            font-size: 1.4rem;
            color: #1a1a1a;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .feature-card p {
            color: #6b7280;
            line-height: 1.7;
        }

        /* Curriculum Section */
        .curriculum {
            padding: 6rem 2rem;
            background: white;
        }

        .curriculum-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .curriculum-item {
            background: #fafafa;
            padding: 1.5rem;
            border-radius: 12px;
            border-left: 4px solid #6366f1;
            display: flex;
            align-items: center;
            gap: 1rem;
            transition: all 0.3s;
        }

        .curriculum-item:hover {
            background: #f3f4f6;
            transform: translateX(10px);
            box-shadow: 0 5px 15px rgba(99, 102, 241, 0.1);
        }

        .curriculum-item::before {
            content: "✓";
            width: 32px;
            height: 32px;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            color: white;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            flex-shrink: 0;
        }

        .curriculum-item span {
            font-weight: 600;
            color: #1a1a1a;
        }

        /* Pricing Section */
        .pricing {
            padding: 6rem 2rem;
            background: #fafafa;
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .pricing-card {
            background: white;
            border-radius: 24px;
            padding: 3rem 2rem;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
            position: relative;
        }

        .pricing-card.featured {
            background: linear-gradient(135deg, #1e1b4b 0%, #4c1d95 100%);
            color: white;
            transform: scale(1.05);
            box-shadow: 0 20px 40px rgba(99, 102, 241, 0.2);
        }

        .pricing-card.featured::before {
            content: "MOST POPULAR";
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            color: white;
            padding: 0.4rem 1.5rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 700;
        }

        .pricing-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .pricing-card.featured:hover {
            transform: scale(1.07) translateY(-5px);
        }

        .pricing-header h3 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
            font-weight: 700;
        }

        .pricing-card.featured .pricing-header h3 {
            color: white;
        }

        .pricing-price {
            font-size: 3rem;
            font-weight: 800;
            margin: 1.5rem 0;
        }

        .pricing-card.featured .pricing-price {
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .pricing-price span {
            font-size: 1rem;
            color: #6b7280;
        }

        .pricing-card.featured .pricing-price span {
            color: rgba(255, 255, 255, 0.7);
        }

        .pricing-features {
            list-style: none;
            margin: 2rem 0;
        }

        .pricing-features li {
            padding: 0.8rem 0;
            border-bottom: 1px solid #f3f4f6;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .pricing-card.featured .pricing-features li {
            border-bottom-color: rgba(255, 255, 255, 0.1);
        }

        .pricing-features li::before {
            content: "✓";
            color: #6366f1;
            font-weight: bold;
        }

        .pricing-card.featured .pricing-features li::before {
            color: #60a5fa;
        }

        .pricing-cta {
            width: 100%;
            padding: 1rem;
            border-radius: 12px;
            font-weight: 700;
            font-size: 1.1rem;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
        }

        .pricing-card:not(.featured) .pricing-cta {
            background: #f3f4f6;
            color: #6366f1;
        }

        .pricing-card.featured .pricing-cta {
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            color: white;
        }

        .pricing-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(99, 102, 241, 0.3);
        }

        /* Testimonials */
        .testimonials {
            padding: 6rem 2rem;
            background: white;
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .testimonial-card {
            background: #fafafa;
            padding: 2rem;
            border-radius: 20px;
            transition: all 0.3s;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .testimonial-text {
            color: #4b5563;
            font-style: italic;
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-size: 1.2rem;
        }

        .author-info strong {
            display: block;
            color: #1a1a1a;
        }

        .author-info span {
            color: #6b7280;
            font-size: 0.9rem;
        }

        /* Registration */
        .registration {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, #1e1b4b 0%, #4c1d95 100%);
        }

        .registration-container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            border-radius: 24px;
            padding: 3rem;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
        }

        .registration-container h2 {
            font-size: 2.5rem;
            font-weight: 800;
            text-align: center;
            margin-bottom: 0.5rem;
            color: #1a1a1a;
        }

        .registration-container p {
            text-align: center;
            color: #6b7280;
            margin-bottom: 2.5rem;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group.full {
            grid-column: 1 / -1;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            color: #1a1a1a;
            margin-bottom: 0.5rem;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.9rem;
            border: 2px solid #e5e7eb;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #6366f1;
            box-shadow: 0 0 0 4px rgba(99, 102, 241, 0.1);
        }

        .submit-btn {
            width: 100%;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            color: white;
            padding: 1.2rem;
            border: none;
            border-radius: 12px;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 35px rgba(99, 102, 241, 0.4);
        }

        /* Footer */
        footer {
            background: #0f172a;
            color: white;
            padding: 4rem 2rem 2rem;
        }

        .footer-container {
            max-width: 1400px;
            margin: 0 auto;
            text-align: center;
        }

        .footer-logo {
            font-size: 2rem;
            font-weight: 800;
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: #94a3b8;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: white;
        }

        .footer-bottom {
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #94a3b8;
        }

        /* Responsive */
        @media (max-width: 1200px) {
            .hero-container {
                grid-template-columns: 1fr;
            }

            .hero-content h1 {
                font-size: 3rem;
            }

            .features-grid,
            .pricing-grid,
            .testimonial-grid {
                grid-template-columns: 1fr;
            }

            .curriculum-grid {
                grid-template-columns: 1fr;
            }

            .form-grid {
                grid-template-columns: 1fr;
            }

            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">GiantX Algo</div>
            <div class="nav-links">
                <a href="#features">Features</a>
                <a href="#curriculum">Curriculum</a>
                <a href="#pricing">Pricing</a>
                <a href="#testimonials">Reviews</a>
                <a href="#register" class="nav-cta">Join Now</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-container">
            <div class="hero-content">
                <h1>Master <span>Algorithmic Trading</span> & Build Automated Systems</h1>
                <p>Learn from industry experts and transform your trading with proven algorithmic strategies. Join 500+ successful traders who've automated their way to consistent profits.</p>
                
                <div class="hero-stats">
                    <div class="stat">
                        <span class="stat-number">500+</span>
                        <span class="stat-label">Students</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">85%</span>
                        <span class="stat-label">Success Rate</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">50+</span>
                        <span class="stat-label">Strategies</span>
                    </div>
                </div>

                <a href="#register" class="hero-cta">
                    Start Learning Today →
                </a>
            </div>

            <div class="hero-card">
                <h3>Why Choose GiantX Algo?</h3>
                <div class="card-features">
                    <div class="card-feature">Live Trading Sessions</div>
                    <div class="card-feature">Build Your Own Bots</div>
                    <div class="card-feature">1-on-1 Mentorship</div>
                    <div class="card-feature">Lifetime Community Access</div>
                    <div class="card-feature">Real-time Market Analysis</div>
                </div>
                <button class="card-cta" onclick="document.getElementById('register').scrollIntoView({behavior: 'smooth'})">
                    Book Free Demo Session
                </button>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <div class="section-header">
                <div class="badge">OUR PROGRAMS</div>
                <h2>What You'll Master</h2>
                <p>Comprehensive training covering everything from basics to advanced algorithmic trading strategies</p>
            </div>

            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">📊</div>
                    <h3>Technical Analysis</h3>
                    <p>Master chart patterns, indicators, and price action strategies used by professional traders.</p>
                </div>

                <div class="feature-card">
                    <div class="feature-icon">💻</div>
                    <h3>Python for Trading</h3>
                    <p>Learn to code trading algorithms from scratch using Python, Pandas, and NumPy.</p>
                </div>

                <div class="feature-card">
                    <div class="feature-icon">🤖</div>
                    <h3>Build Trading Bots</h3>
                    <p>Create automated trading bots that execute trades 24/7 based on your strategies.</p>
                </div>

                <div class="feature-card">
                    <div class="feature-icon">📈</div>
                    <h3>Backtesting & Optimization</h3>
                    <p>Test and optimize your strategies using historical data before risking real capital.</p>
                </div>

                <div class="feature-card">
                    <div class="feature-icon">🛡️</div>
                    <h3>Risk Management</h3>
                    <p>Learn professional risk management techniques to protect your capital.</p>
                </div>

                <div class="feature-card">
                    <div class="feature-icon">🎯</div>
                    <h3>Live Trading Support</h3>
                    <p>Join daily live sessions with expert traders and get real-time market insights.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Curriculum Section -->
    <section class="curriculum" id="curriculum">
        <div class="container">
            <div class="section-header">
                <div class="badge">COURSE CONTENT</div>
                <h2>Complete Curriculum</h2>
                <p>20+ modules covering every aspect of algorithmic trading</p>
            </div>

            <div class="curriculum-grid">
                <div class="curriculum-item"><span>Introduction to Algorithmic Trading</span></div>
                <div class="curriculum-item"><span>Market Structure & Order Types</span></div>
                <div class="curriculum-item"><span>Python Programming Fundamentals</span></div>
                <div class="curriculum-item"><span>Data Analysis with Pandas</span></div>
                <div class="curriculum-item"><span>Technical Indicators & Signals</span></div>
                <div class="curriculum-item"><span>Candlestick Pattern Recognition</span></div>
                <div class="curriculum-item"><span>Trend Following Strategies</span></div>
                <div class="curriculum-item"><span>Mean Reversion Systems</span></div>
                <div class="curriculum-item"><span>Momentum Trading Algorithms</span></div>
                <div class="curriculum-item"><span>Backtesting Frameworks</span></div>
                <div class="curriculum-item"><span>Strategy Optimization Techniques</span></div>
                <div class="curriculum-item"><span>Risk & Money Management</span></div>
                <div class="curriculum-item"><span>Position Sizing Methods</span></div>
                <div class="curriculum-item"><span>Portfolio Management</span></div>
                <div class="curriculum-item"><span>API Integration & Live Trading</span></div>
                <div class="curriculum-item"><span>Real-time Data Processing</span></div>
                <div class="curriculum-item"><span>Building Trading Bots</span></div>
                <div class="curriculum-item"><span>Deployment & Monitoring</span></div>
                <div class="curriculum-item"><span>Options Trading Strategies</span></div>
                <div class="curriculum-item"><span>Machine Learning Applications</span></div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="pricing" id="pricing">
        <div class="container">
            <div class="section-header">
                <div class="badge">PRICING</div>
                <h2>Choose Your Plan</h2>
                <p>Flexible options to start your algorithmic trading journey</p>
            </div>

            <div class="pricing-grid">
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Foundation</h3>
                    </div>
                    <div class="pricing-price">
                        ₹29,999
                        <span>/8 weeks</span>
                    </div>
                    <ul class="pricing-features">
                        <li>Core Trading Concepts</li>
                        <li>Basic Python for Trading</li>
                        <li>Strategy Development</li>
                        <li>Recorded Sessions</li>
                        <li>Community Access</li>
                        <li>Course Materials</li>
                    </ul>
                    <button class="pricing-cta" onclick="document.getElementById('register').scrollIntoView({behavior: 'smooth'})">Get Started</button>
                </div>

                <div class="pricing-card featured">
                    <div class="pricing-header">
                        <h3>Professional</h3>
                    </div>
                    <div class="pricing-price">
                        ₹49,999
                        <span>/12 weeks</span>
                    </div>
                    <ul class="pricing-features">
                        <li>Everything in Foundation</li>
                        <li>Advanced Strategies</li>
                        <li>Live Trading Sessions</li>
                        <li>1-on-1 Mentorship</li>
                        <li>Bot Development</li>
                        <li>Lifetime Community</li>
                        <li>Job Placement Support</li>
                        <li>Certificate</li>
                    </ul>
                    <button class="pricing-cta" onclick="document.getElementById('register').scrollIntoView({behavior: 'smooth'})">Most Popular</button>
                </div>

                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Elite Trader</h3>
                    </div>
                    <div class="pricing-price">
                        ₹79,999
                        <span>/16 weeks</span>
                    </div>
                    <ul class="pricing-features">
                        <li>Everything in Professional</li>
                        <li>Private Trading Room</li>
                        <li>Proprietary Strategies</li>
                        <li>Personal Account Review</li>
                        <li>6 Months Post Support</li>
                        <li>Prop Firm Preparation</li>
                        <li>ML Integration</li>
                        <li>Priority Support</li>
                    </ul>
                    <button class="pricing-cta" onclick="document.getElementById('register').scrollIntoView({behavior: 'smooth'})">Go Elite</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-header">
                <div class="badge">SUCCESS STORIES</div>
                <h2>What Our Students Say</h2>
                <p>Join hundreds of successful traders who've transformed their trading</p>
            </div>

            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"GiantX Algo completely changed my approach to trading. I went from manual trading to running 5 automated strategies. The mentorship is exceptional!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">RS</div>
                        <div class="author-info">
                            <strong>Rahul Sharma</strong>
                            <span>Full-time Algo Trader</span>
                        </div>
                    </div>
                </div>

                <div class="testimonial-card">
                    <p class="testimonial-text">"The curriculum is perfectly structured. Starting from basics and gradually moving to advanced concepts made learning smooth and effective."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">PK</div>
                        <div class="author-info">
                            <strong>Priya Kapoor</strong>
                            <span>Quantitative Analyst</span>
                        </div>
                    </div>
                </div>

                <div class="testimonial-card">
                    <p class="testimonial-text">"Best investment in my trading career! The strategies are practical and profitable. Live sessions give real insights into professional trading."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">AM</div>
                        <div class="author-info">
                            <strong>Arjun Mehta</strong>
                            <span>Software Engineer turned Trader</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Registration -->
    <section class="registration" id="register">
        <div class="registration-container">
            <h2>Start Your Journey Today</h2>
            <p>Fill out the form below and our team will contact you within 24 hours</p>

            <form id="registrationForm">
                <div class="form-grid">
                    <div class="form-group">
                        <label for="name">Full Name *</label>
                        <input type="text" id="name" name="name" placeholder="John Doe" required>
                    </div>

                    <div class="form-group">
                        <label for="email">Email Address *</label>
                        <input type="email" id="email" name="email" placeholder="john@example.com" required>
                    </div>

                    <div class="form-group">
                        <label for="phone">Phone Number *</label>
                        <input type="tel" id="phone" name="phone" placeholder="+91 98765 43210" required>
                    </div>

                    <div class="form-group">
                        <label for="experience">Trading Experience</label>
                        <select id="experience" name="experience">
                            <option value="">Select your level</option>
                            <option value="beginner">Complete Beginner</option>
                            <option value="basic">Basic Knowledge</option>
                            <option value="intermediate">Intermediate</option>
                            <option value="advanced">Advanced</option>
                        </select>
                    </div>

                    <div class="form-group full">
                        <label for="plan">Interested In</label>
                        <select id="plan" name="plan">
                            <option value="">Select a plan</option>
                            <option value="foundation">Foundation - ₹29,999</option>
                            <option value="professional">Professional - ₹49,999</option>
                            <option value="elite">Elite Trader - ₹79,999</option>
                        </select>
                    </div>

                    <div class="form-group full">
                        <label for="message">What are your trading goals?</label>
                        <textarea id="message" name="message" rows="4" placeholder="Tell us about your aspirations..."></textarea>
                    </div>
                </div>

                <button type="submit" class="submit-btn">Enroll Now - Limited Seats Available!</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-logo">GiantX Algo</div>
            <p style="color: #94a3b8; margin-bottom: 2rem;">Empowering traders with professional algorithmic trading education</p>
            
            <div class="footer-links">
                <a href="#features">Features</a>
                <a href="#curriculum">Curriculum</a>
                <a href="#pricing">Pricing</a>
                <a href="#testimonials">Reviews</a>
                <a href="#register">Join Now</a>
            </div>

            <div class="footer-bottom">
                <p>&copy; 2025 GiantX Algo. All rights reserved.</p>
                <p style="margin-top: 0.5rem;">Contact: info@giantxalgo.com | +91 98765 43210</p>
            </div>
        </div>
    </footer>

    <script>
        // Form submission
        document.getElementById('registrationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your interest in GiantX Algo! Our team will contact you within 24 hours to discuss your enrollment.');
            this.reset();
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });
    </script>
</body>
</html>
