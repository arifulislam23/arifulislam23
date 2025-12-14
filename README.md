<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ariful Islam Akash - CV</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 40px 20px;
            line-height: 1.6;
        }
        
        .cv-container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            border-radius: 8px;
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 50px 40px;
            text-align: center;
            position: relative;
        }
        
        .header::after {
            content: '';
            position: absolute;
            bottom: -20px;
            left: 0;
            right: 0;
            height: 40px;
            background: white;
            clip-path: polygon(0 50%, 100% 0, 100% 100%, 0 100%);
        }
        
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            font-weight: 700;
            letter-spacing: 1px;
        }
        
        .header .title {
            font-size: 1.3em;
            font-weight: 300;
            letter-spacing: 3px;
            text-transform: uppercase;
            opacity: 0.95;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            margin-top: 25px;
            font-size: 0.95em;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .content {
            padding: 60px 40px 40px;
        }
        
        .section {
            margin-bottom: 40px;
        }
        
        .section-title {
            font-size: 1.5em;
            color: #667eea;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #667eea;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .summary {
            font-size: 1.05em;
            color: #444;
            text-align: justify;
            line-height: 1.8;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .skill-item {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 15px 20px;
            border-radius: 8px;
            border-left: 4px solid #667eea;
            transition: transform 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateX(5px);
        }
        
        .skill-label {
            font-weight: 600;
            color: #333;
            margin-bottom: 5px;
        }
        
        .skill-value {
            color: #666;
            font-size: 0.95em;
        }
        
        .experience-item, .project-item {
            margin-bottom: 30px;
            padding: 25px;
            background: #f8f9fa;
            border-radius: 8px;
            border-left: 4px solid #764ba2;
            transition: all 0.3s ease;
        }
        
        .experience-item:hover, .project-item:hover {
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transform: translateY(-2px);
        }
        
        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }
        
        .job-title {
            font-size: 1.2em;
            font-weight: 600;
            color: #333;
        }
        
        .company {
            font-size: 1.1em;
            color: #667eea;
            font-weight: 500;
            margin-top: 5px;
        }
        
        .duration {
            background: #667eea;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: 500;
        }
        
        .project-title {
            font-size: 1.15em;
            font-weight: 600;
            color: #764ba2;
            margin-bottom: 10px;
        }
        
        .achievements {
            list-style: none;
            margin-top: 15px;
        }
        
        .achievements li {
            padding: 8px 0 8px 25px;
            position: relative;
            color: #555;
        }
        
        .achievements li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
            font-size: 1.2em;
        }
        
        .education-box {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        
        .degree {
            font-size: 1.2em;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .university {
            font-size: 1em;
            opacity: 0.95;
            margin-bottom: 8px;
        }
        
        .gpa {
            display: inline-block;
            background: rgba(255,255,255,0.2);
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: 500;
            margin-top: 10px;
        }
        
        .references-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .reference-card {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 8px;
            border-top: 4px solid #667eea;
        }
        
        .ref-name {
            font-weight: 600;
            font-size: 1.1em;
            color: #333;
            margin-bottom: 5px;
        }
        
        .ref-position {
            color: #667eea;
            font-size: 0.95em;
            margin-bottom: 10px;
        }
        
        .ref-contact {
            color: #666;
            font-size: 0.9em;
        }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2em;
            }
            
            .content {
                padding: 40px 20px 20px;
            }
            
            .experience-header {
                flex-direction: column;
            }
            
            .duration {
                margin-top: 10px;
            }
        }
        
        @media print {
            body {
                background: white;
                padding: 0;
            }
            
            .cv-container {
                box-shadow: none;
            }
        }
    </style>
</head>
<body>
    <div class="cv-container">
        <div class="header">
            <h1>ARIFUL ISLAM AKASH</h1>
            <div class="title">Full Stack Software Developer</div>
            <div class="contact-info">
                <div class="contact-item">📞 019-999-97748</div>
                <div class="contact-item">✉️ ariful.akash23@gmail.com</div>
                <div class="contact-item">🔗 github.com/arifulislam23</div>
                <div class="contact-item">📍 Dhaka, Bangladesh</div>
            </div>
        </div>
        
        <div class="content">
            <div class="section">
                <h2 class="section-title">Professional Summary</h2>
                <p class="summary">
                    Results-driven Full Stack Software Developer with 3.2+ years of expertise in designing and delivering enterprise-level applications. Specialized in .NET ecosystem (C#, ASP.NET Core) with proven success in developing scalable solutions for garments payroll systems and POS applications. Recognized for consistently delivering high-quality, budget-conscious solutions while collaborating effectively with cross-functional teams to transform business requirements into innovative technical solutions.
                </p>
            </div>
            
            <div class="section">
                <h2 class="section-title">Technical Skills</h2>
                <div class="skills-grid">
                    <div class="skill-item">
                        <div class="skill-label">Backend Development</div>
                        <div class="skill-value">ASP.NET MVC Core, C#, LINQ, .NET Framework</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-label">Frontend Technologies</div>
                        <div class="skill-value">JavaScript, AJAX, Bootstrap</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-label">Frameworks & ORM</div>
                        <div class="skill-value">.NET Core, Entity Framework</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-label">Database Management</div>
                        <div class="skill-value">SQL Server, MySQL</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-label">Version Control</div>
                        <div class="skill-value">Git, GitHub</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-label">Additional Tools</div>
                        <div class="skill-value">Crystal Reports, WordPress, Linux</div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Work Experience</h2>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Software Developer</div>
                            <div class="company">FiroTech</div>
                        </div>
                        <div class="duration">July 2023 - Present</div>
                    </div>
                    
                    <div class="project-title">Point of Sale (POS) System</div>
                    <ul class="achievements">
                        <li>Architected and deployed a comprehensive POS system with real-time stock tracking and automated low-inventory alerts</li>
                        <li>Implemented advanced sales module with live transaction processing and instant calculation engine</li>
                        <li>Developed customer due tracking system with detailed payment history and reporting capabilities</li>
                        <li>Integrated role-based access control (RBAC) to ensure data security and operational compliance</li>
                        <li>Created dynamic inventory reporting dashboard for actionable insights on stock levels and supplier performance</li>
                    </ul>
                    
                    <div class="project-title" style="margin-top: 20px;">OnePortal - Team Collaboration System</div>
                    <ul class="achievements">
                        <li>Led end-to-end development of a Trello-inspired collaboration platform for task management</li>
                        <li>Designed intuitive interfaces for efficient task assignment, tracking, and team productivity monitoring</li>
                        <li>Collaborated with stakeholders to gather requirements and iteratively enhanced features based on feedback</li>
                    </ul>
                    
                    <div class="project-title" style="margin-top: 20px;">eCommerce Development (nopCommerce)</div>
                    <ul class="achievements">
                        <li>Customized nopCommerce platform to meet specific client business requirements</li>
                        <li>Implemented SSL integration for secure data transmission and enhanced site security</li>
                        <li>Extended plugin functionality to optimize user experience and conversion rates</li>
                    </ul>
                    
                    <div class="project-title" style="margin-top: 20px;">HisabKhata - Madrasha Tuition Management Software</div>
                    <ul class="achievements">
                        <li>Built comprehensive student fee management system with automated payment tracking</li>
                        <li>Developed automated alert system for due payment notifications to students and parents</li>
                        <li>Created financial reporting module with Excel/PDF export capabilities for administrative use</li>
                    </ul>
                </div>
                
                <div class="experience-item">
                    <div class="experience-header">
                        <div>
                            <div class="job-title">Software Developer</div>
                            <div class="company">KS Apparels Limited</div>
                        </div>
                        <div class="duration">May 2022 - June 2023</div>
                    </div>
                    
                    <div class="project-title">Garments Payroll Management System</div>
                    <ul class="achievements">
                        <li>Spearheaded development of enterprise payroll system using .NET Core 3.1 in collaboration with HR department</li>
                        <li>Integrated multiple biometric systems (ZKT, Biostar, RAS, HAMS) for seamless attendance and overtime data collection</li>
                        <li>Automated complex salary calculations based on attendance, overtime, and statutory deductions (income tax, social security)</li>
                        <li>Implemented comprehensive employee benefit modules including leave management and loan tracking</li>
                        <li>Generated automated payslips and management reports, reducing processing time by 60%</li>
                        <li>Successfully deployed application to production with performance optimization and tuning</li>
                    </ul>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Personal Projects</h2>
                
                <div class="project-item">
                    <div class="project-title">Bus Ticket Booking & Management System</div>
                    <ul class="achievements">
                        <li>Full-featured web application for bus scheduling, driver management, and ticket booking</li>
                        <li>Implemented ticket printing functionality and customer information storage</li>
                    </ul>
                </div>
                
                <div class="project-item">
                    <div class="project-title">Store POS Desktop Application</div>
                    <ul class="achievements">
                        <li>Desktop application for inventory management with product tracking and stock updates</li>
                        <li>Automated calculation engine for pricing, tax, and discounts with dual bill printing</li>
                    </ul>
                </div>
                
                <div class="project-item">
                    <div class="project-title">Telegram Chat Bot</div>
                    <ul class="achievements">
                        <li>Developed intelligent auto-reply bot using Telegram API for automated customer engagement</li>
                    </ul>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Education</h2>
                <div class="education-box">
                    <div class="degree">B.Sc. in Computer Science and Engineering</div>
                    <div class="university">IUBAT - International University of Business Agriculture and Technology</div>
                    <div class="gpa">CGPA: 3.27 / 4.00</div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">References</h2>
                <div class="references-grid">
                    <div class="reference-card">
                        <div class="ref-name">Dr. Utpal Kanti Das</div>
                        <div class="ref-position">Professor & Chairman, IUBAT University</div>
                        <div class="ref-contact">📧 ukd@iubat.edu</div>
                        <div class="ref-contact">📞 01819-199419</div>
                    </div>
                    <div class="reference-card">
                        <div class="ref-name">Ataul Haq</div>
                        <div class="ref-position">Sr. Software Engineer, Pisstech Limited</div>
                        <div class="ref-contact">📧 ataul.piistech@gmail.com</div>
                        <div class="ref-contact">📞 01922-277730</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
