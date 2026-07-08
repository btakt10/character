[index.html](https://github.com/user-attachments/files/29792421/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Batamir | Freelancer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --primary-dark: #1e40af;
            --primary-light: #3b82f6;
            --bg-primary: #ffffff;
            --bg-secondary: #f8fafc;
            --bg-tertiary: #f1f5f9;
            --text-primary: #0f172a;
            --text-secondary: #475569;
            --text-muted: #64748b;
            --border-color: #e2e8f0;
            --accent: #2563eb;
            --success: #10b981;
        }

        @media (prefers-color-scheme: dark) {
            :root {
                --bg-primary: #0f172a;
                --bg-secondary: #1e293b;
                --bg-tertiary: #334155;
                --text-primary: #f1f5f9;
                --text-secondary: #cbd5e1;
                --text-muted: #94a3b8;
                --border-color: #475569;
                --accent: #3b82f6;
                --primary-light: #60a5fa;
            }
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.7;
            font-size: 16px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }

        /* Header */
        header {
            text-align: center;
            padding: 3rem 2rem;
            margin: -4rem -2rem 3rem -2rem;
            margin-bottom: 3rem;
            border-bottom: 2px solid var(--border-color);
            animation: fadeInDown 0.8s ease-out;
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.05), rgba(59, 130, 246, 0.05));
            backdrop-filter: blur(10px);
        }

        h1 {
            font-size: 3.2rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -1px;
        }

        .subtitle {
            font-size: 1.3rem;
            color: var(--text-secondary);
            font-weight: 500;
            margin-bottom: 0.75rem;
        }

        .tagline {
            font-size: 1rem;
            color: var(--text-muted);
            font-style: italic;
            letter-spacing: 0.3px;
        }

        /* Sections */
        section {
            margin-bottom: 4rem;
            animation: fadeInUp 0.8s ease-out;
        }

        h2 {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 2rem;
            color: var(--text-primary);
            position: relative;
            padding-bottom: 1rem;
        }

        h2::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--primary-light));
            border-radius: 2px;
        }

        h3 {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
            color: var(--text-primary);
        }

        /* About Section */
        .about-content {
            display: flex;
            flex-direction: column;
            gap: 1.75rem;
        }

        .about-text {
            color: var(--text-primary);
            line-height: 1.9;
            font-size: 1.02rem;
            background: var(--bg-secondary);
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 4px solid var(--primary);
            transition: all 0.3s ease;
        }

        .about-text:hover {
            transform: translateX(4px);
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.1);
        }

        .about-text p {
            margin: 0;
        }

        /* Services Section */
        .services-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2rem;
        }

        .service-item {
            padding: 2rem;
            background: var(--bg-secondary);
            border-radius: 12px;
            border: 1px solid var(--border-color);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .service-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--primary-light));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }

        .service-item:hover {
            transform: translateY(-6px);
            border-color: var(--primary-light);
            box-shadow: 0 12px 24px rgba(37, 99, 235, 0.15);
        }

        .service-item:hover::before {
            transform: scaleX(1);
        }

        .service-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .service-item h3 {
            font-size: 1.1rem;
            margin-bottom: 0.75rem;
        }

        .service-item p {
            font-size: 0.95rem;
            color: var(--text-secondary);
            line-height: 1.7;
        }

        /* Benefits/Why Section */
        .benefits-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .benefit-item {
            padding: 1.75rem;
            background: var(--bg-secondary);
            border-radius: 10px;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
            position: relative;
            display: flex;
            align-items: flex-start;
            gap: 1rem;
        }

        .benefit-item:hover {
            transform: translateX(6px);
            box-shadow: 0 8px 16px rgba(37, 99, 235, 0.12);
            border-color: var(--primary-light);
        }

        .benefit-icon {
            width: 32px;
            height: 32px;
            background: rgba(37, 99, 235, 0.1);
            border-radius: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--success);
            font-size: 1.2rem;
            flex-shrink: 0;
            font-weight: 600;
        }

        .benefit-item p {
            color: var(--text-primary);
            font-size: 0.95rem;
            line-height: 1.7;
            margin: 0;
        }

        .benefit-item strong {
            color: var(--primary);
        }

        /* Contact Section */
        .contact-section {
            background: linear-gradient(135deg, var(--bg-secondary), var(--bg-tertiary));
            padding: 2.5rem;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            position: relative;
            overflow: hidden;
        }

        .contact-section::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(37, 99, 235, 0.08), transparent);
            border-radius: 50%;
            z-index: 0;
        }

        .contact-grid {
            position: relative;
            z-index: 1;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            position: relative;
            z-index: 1;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.3rem;
            flex-shrink: 0;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
        }

        .contact-label {
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 0.8px;
            margin-bottom: 0.4rem;
        }

        .contact-value {
            font-size: 1.05rem;
            font-weight: 500;
            color: var(--text-primary);
        }

        a {
            color: var(--primary);
            text-decoration: none;
            transition: all 0.3s ease;
            border-bottom: 2px solid transparent;
            padding-bottom: 2px;
        }

        a:hover {
            color: var(--primary-light);
            border-bottom: 2px solid var(--primary-light);
        }

        /* Footer */
        footer {
            margin-top: 4rem;
            padding-top: 2.5rem;
            border-top: 2px solid var(--border-color);
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 2.5rem 1.5rem;
            }

            h1 {
                font-size: 2.4rem;
            }

            h2 {
                font-size: 1.5rem;
            }

            .services-list {
                grid-template-columns: 1fr;
            }

            .benefits-list {
                grid-template-columns: 1fr;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            header {
                padding: 2rem 1.5rem;
                margin: -2.5rem -1.5rem 2rem -1.5rem;
                padding-bottom: 2rem;
                margin-bottom: 2rem;
            }

            section {
                margin-bottom: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Batamir</h1>
            <p class="subtitle">Freelancer & AI Solutions Specialist</p>
            <p class="tagline">Reliable, detail-oriented, and committed to excellence</p>
        </header>

        <section id="about">
            <h2>About me</h2>
            <div class="about-content">
                <div class="about-text">
                    I'm a reliable freelancer specializing in AI-assisted solutions, document creation, automation, and research. I combine modern AI tools with careful human review to deliver high-quality results that meet each client's specific requirements.
                </div>
                <div class="about-text">
                    My goal is not just to complete tasks quickly, but to provide accurate, polished, and professional work. I continuously improve my skills and stay up to date with the latest AI technologies, allowing me to complete projects efficiently without compromising quality.
                </div>
                <div class="about-text">
                    If you're looking for someone dependable, detail-oriented, and committed to delivering excellent results, I'd be happy to help. Feel free to send me your project, and let's bring your ideas to life.
                </div>
            </div>
        </section>

        <section id="services">
            <h2>Services I offer</h2>
            <div class="services-list">
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-pen-fancy"></i></div>
                    <h3>Content & Writing</h3>
                    <p>Content writing, editing, translation, and proofreading tailored to your needs.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-file-alt"></i></div>
                    <h3>Document Preparation</h3>
                    <p>Professional formatting and preparation of reports, documents, and proposals.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-presentation"></i></div>
                    <h3>Presentation Design</h3>
                    <p>Custom PowerPoint and Google Slides presentations with clear visual design.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-chart-bar"></i></div>
                    <h3>Data & Research</h3>
                    <p>Comprehensive data research, analysis, and insights for your projects.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-robot"></i></div>
                    <h3>Automation & Scripting</h3>
                    <p>Python scripting and task automation to streamline your workflow.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-table"></i></div>
                    <h3>Excel & Spreadsheets</h3>
                    <p>Document formatting, data organization, and Excel spreadsheet creation.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-image"></i></div>
                    <h3>Image Generation & Editing</h3>
                    <p>AI-generated images and professional image editing services.</p>
                </div>
                <div class="service-item">
                    <div class="service-icon"><i class="fas fa-star"></i></div>
                    <h3>Custom Projects</h3>
                    <p>Tailored solutions based on your unique requirements and objectives.</p>
                </div>
            </div>
        </section>

        <section id="why">
            <h2>Why work with me</h2>
            <div class="benefits-list">
                <div class="benefit-item">
                    <div class="benefit-icon">✓</div>
                    <p><strong>High attention to detail</strong> — Every project receives careful review to ensure quality and accuracy.</p>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">✓</div>
                    <p><strong>Fast response and communication</strong> — I prioritize clear, timely communication throughout our collaboration.</p>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">✓</div>
                    <p><strong>Always meet deadlines</strong> — Reliability is fundamental to how I work with every client.</p>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">✓</div>
                    <p><strong>Unlimited reasonable revisions</strong> — I work with you until you're completely satisfied with the result.</p>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">✓</div>
                    <p><strong>Confidential file handling</strong> — Your privacy and data security are always protected.</p>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">✓</div>
                    <p><strong>Quality assurance</strong> — Every project is reviewed before delivery to guarantee professional results.</p>
                </div>
            </div>
        </section>

        <section id="contact">
            <h2>Get in touch</h2>
            <div class="contact-section">
                <div class="contact-grid">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-info">
                            <div class="contact-label">Email</div>
                            <div class="contact-value">
                                <a href="mailto:batamir000@gmail.com">batamir000@gmail.com</a>
                            </div>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fab fa-telegram"></i>
                        </div>
                        <div class="contact-info">
                            <div class="contact-label">Telegram</div>
                            <div class="contact-value">
                                <a href="https://t.me/StBata" target="_blank">@StBata</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <footer>
            <p>© 2024 Batamir. All rights reserved.</p>
        </footer>
    </div>
</body>
</html>
