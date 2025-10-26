<!doctype html>
<html lang="fa" dir="rtl">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GitHub Profile - مبین حسن قاسمی</title>
  <script src="/_sdk/element_sdk.js"></script>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 20px;
            font-family: 'Segoe UI', Tahoma, Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100%;
            color: #333;
        }

        .profile-container {
            max-width: 900px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            backdrop-filter: blur(10px);
        }

        .header-section {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            padding: 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="2" fill="rgba(255,255,255,0.1)"/></svg>') repeat;
            animation: float 20s infinite linear;
        }

        @keyframes float {
            0% { transform: translateX(0) translateY(0); }
            100% { transform: translateX(-50px) translateY(-50px); }
        }

        .profile-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 48px;
            color: white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            position: relative;
            z-index: 2;
        }

        .profile-name {
            font-size: 2.5rem;
            font-weight: 700;
            color: white;
            margin: 0 0 10px 0;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            position: relative;
            z-index: 2;
        }

        .profile-title {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.9);
            margin: 0 0 20px 0;
            position: relative;
            z-index: 2;
        }

        .stats-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            position: relative;
            z-index: 2;
        }

        .stat-item {
            text-align: center;
            color: white;
        }

        .stat-number {
            font-size: 1.8rem;
            font-weight: 700;
            display: block;
        }

        .stat-label {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .content-section {
            padding: 40px;
        }

        .section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-icon {
            width: 24px;
            height: 24px;
            fill: #4facfe;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .info-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 20px;
            border-radius: 15px;
            border-left: 4px solid #4facfe;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .info-label {
            font-weight: 600;
            color: #495057;
            margin-bottom: 5px;
            font-size: 0.9rem;
        }

        .info-value {
            color: #2c3e50;
            font-size: 1.1rem;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: transform 0.3s ease;
        }

        .skill-tag:hover {
            transform: scale(1.05);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            font-size: 1.2rem;
        }

        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(79, 172, 254, 0.3);
        }

        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: white;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            border: 1px solid #e9ecef;
        }

        .activity-indicator {
            display: inline-block;
            width: 8px;
            height: 8px;
            background: #28a745;
            border-radius: 50%;
            margin-left: 8px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { opacity: 1; }
            50% { opacity: 0.5; }
            100% { opacity: 1; }
        }

        @media (max-width: 768px) {
            .profile-container {
                margin: 10px;
                border-radius: 15px;
            }
            
            .header-section {
                padding: 30px 20px;
            }
            
            .content-section {
                padding: 30px 20px;
            }
            
            .stats-container {
                flex-direction: column;
                gap: 15px;
            }
            
            .info-grid {
                grid-template-columns: 1fr;
            }
            
            .profile-name {
                font-size: 2rem;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="profile-container"><!-- Header Section -->
   <div class="header-section">
    <div class="profile-avatar"><span id="avatar-emoji">👨‍💻</span>
    </div>
    <h1 class="profile-name" id="profile-name">سلام 👋، من مبین هستم</h1>
    <p class="profile-title" id="profile-title">من یک توسعه‌دهنده وب از ایران هستم</p>
    <div class="stats-container">
     <div class="stat-item"><span class="stat-number">2.5K+</span> <span class="stat-label">بازدید پروفایل</span>
     </div>
     <div class="stat-item"><span class="stat-number">15+</span> <span class="stat-label">پروژه</span>
     </div>
     <div class="stat-item"><span class="stat-number">Active</span> <span class="stat-label">وضعیت<span class="activity-indicator"></span></span>
     </div>
    </div>
   </div><!-- Content Section -->
   <div class="content-section"><!-- About Me Section -->
    <div class="section">
     <h2 class="section-title">
      <svg class="section-icon" viewbox="0 0 24 24"><path d="M12 2C13.1 2 14 2.9 14 4C14 5.1 13.1 6 12 6C10.9 6 10 5.1 10 4C10 2.9 10.9 2 12 2ZM21 9V7L15 7V9C15 10.1 14.1 11 13 11V22H11V16H9V22H7V11C5.9 11 5 10.1 5 9V7H3V9C3 11.2 4.8 13 7 13V22H17V13C19.2 13 21 11.2 21 9Z" />
      </svg> درباره من</h2>
     <div class="info-grid">
      <div class="info-card">
       <div class="info-label">
        📍 موقعیت مکانی
       </div>
       <div class="info-value" id="location">
        ایران
       </div>
      </div>
      <div class="info-card">
       <div class="info-label">
        📧 ایمیل
       </div>
       <div class="info-value" id="email">
        mobin.hasanghasemi.m@gmail.com
       </div>
      </div>
      <div class="info-card">
       <div class="info-label">
        🌱 در حال یادگیری
       </div>
       <div class="info-value" id="learning">
        cv2, Computer Vision
       </div>
      </div>
      <div class="info-card">
       <div class="info-label">
        💬 تخصص اصلی
       </div>
       <div class="info-value" id="expertise">
        Django, Python Backend
       </div>
      </div>
     </div>
    </div><!-- Skills Section -->
    <div class="section">
     <h2 class="section-title">
      <svg class="section-icon" viewbox="0 0 24 24"><path d="M9.4 16.6L4.8 12L3.4 13.4L9.4 19.4L20.6 8.2L19.2 6.8L9.4 16.6Z" />
      </svg> مهارت‌ها و تکنولوژی‌ها</h2>
     <div class="skills-container"><span class="skill-tag">🐍 Python</span> <span class="skill-tag">🌐 Django</span> <span class="skill-tag">⚡ JavaScript</span> <span class="skill-tag">🎨 HTML/CSS</span> <span class="skill-tag">🎯 Tailwind CSS</span> <span class="skill-tag">📱 Bootstrap</span> <span class="skill-tag">🔍 OpenCV</span> <span class="skill-tag">🗄️ SQL Server</span> <span class="skill-tag">📊 Computer Vision</span> <span class="skill-tag">🚀 Web Development</span>
     </div>
    </div><!-- GitHub Stats Section -->
    <div class="section">
     <h2 class="section-title">
      <svg class="section-icon" viewbox="0 0 24 24"><path d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z" />
      </svg> آمار گیت‌هاب</h2>
     <div class="github-stats">
      <div class="stat-card">
       <h3 style="margin-top: 0; color: #4facfe;">📈 آمار کلی</h3>
       <p>⭐ ستاره‌های دریافتی: <strong>25+</strong></p>
       <p>🔄 Pull Request ها: <strong>12+</strong></p>
       <p>🐛 Issue های حل شده: <strong>8+</strong></p>
       <p>📝 Commit های امسال: <strong>200+</strong></p>
      </div>
      <div class="stat-card">
       <h3 style="margin-top: 0; color: #4facfe;">🏆 دستاورد‌ها</h3>
       <p>🥇 Contributor فعال</p>
       <p>🎯 پروژه‌های متن‌باز</p>
       <p>💡 ایده‌های خلاقانه</p>
       <p>🚀 کد تمیز و بهینه</p>
      </div>
     </div>
    </div><!-- Social Links -->
    <div class="section">
     <h2 class="section-title">
      <svg class="section-icon" viewbox="0 0 24 24"><path d="M16,4C18.2,4 20,5.8 20,8C20,10.2 18.2,12 16,12C13.8,12 12,10.2 12,8C12,5.8 13.8,4 16,4M16,14C20.4,14 24,15.8 24,18V20H8V18C8,15.8 11.6,14 16,14Z" />
      </svg> راه‌های ارتباطی</h2>
     <div class="social-links"><a href="https://linkedin.com/in/mobin-hasanghasemi-067154384" target="_blank" rel="noopener noreferrer" class="social-link" title="LinkedIn"> 💼 </a> <a href="https://instagram.com/devriftlab" target="_blank" rel="noopener noreferrer" class="social-link" title="Instagram"> 📷 </a> <a href="https://www.youtube.com/c/@devriftlab" target="_blank" rel="noopener noreferrer" class="social-link" title="YouTube"> 📺 </a> <a href="mailto:mobin.hasanghasemi.m@gmail.com" class="social-link" title="Email"> 📧 </a>
     </div>
    </div>
   </div>
  </div>
  <script>
        // Configuration object
        const defaultConfig = {
            name: "سلام 👋، من مبین هستم",
            title: "من یک توسعه‌دهنده وب از ایران هستم",
            location: "ایران",
            email: "mobin.hasanghasemi.m@gmail.com",
            learning: "cv2, Computer Vision",
            expertise: "Django, Python Backend",
            background_color: "#667eea",
            surface_color: "#ffffff",
            text_color: "#2c3e50",
            primary_action_color: "#4facfe",
            secondary_action_color: "#764ba2",
            font_family: "Segoe UI",
            font_size: 16
        };

        // Element SDK implementation
        const element = {
            defaultConfig,
            
            onConfigChange: async (config) => {
                // Update text content
                const nameElement = document.getElementById('profile-name');
                const titleElement = document.getElementById('profile-title');
                const locationElement = document.getElementById('location');
                const emailElement = document.getElementById('email');
                const learningElement = document.getElementById('learning');
                const expertiseElement = document.getElementById('expertise');

                if (nameElement) nameElement.textContent = config.name || defaultConfig.name;
                if (titleElement) titleElement.textContent = config.title || defaultConfig.title;
                if (locationElement) locationElement.textContent = config.location || defaultConfig.location;
                if (emailElement) emailElement.textContent = config.email || defaultConfig.email;
                if (learningElement) learningElement.textContent = config.learning || defaultConfig.learning;
                if (expertiseElement) expertiseElement.textContent = config.expertise || defaultConfig.expertise;

                // Update colors
                const backgroundColor = config.background_color || defaultConfig.background_color;
                const surfaceColor = config.surface_color || defaultConfig.surface_color;
                const textColor = config.text_color || defaultConfig.text_color;
                const primaryActionColor = config.primary_action_color || defaultConfig.primary_action_color;
                const secondaryActionColor = config.secondary_action_color || defaultConfig.secondary_action_color;

                document.body.style.background = `linear-gradient(135deg, ${backgroundColor} 0%, ${secondaryActionColor} 100%)`;
                
                const profileContainer = document.querySelector('.profile-container');
                if (profileContainer) {
                    profileContainer.style.background = `rgba(255, 255, 255, 0.95)`;
                }

                const sectionTitles = document.querySelectorAll('.section-title');
                sectionTitles.forEach(title => {
                    title.style.color = textColor;
                });

                const sectionIcons = document.querySelectorAll('.section-icon');
                sectionIcons.forEach(icon => {
                    icon.style.fill = primaryActionColor;
                });

                const socialLinks = document.querySelectorAll('.social-link');
                socialLinks.forEach(link => {
                    link.style.background = `linear-gradient(135deg, ${primaryActionColor} 0%, #00f2fe 100%)`;
                });

                // Update font
                const customFont = config.font_family || defaultConfig.font_family;
                const baseFontStack = 'Tahoma, Arial, sans-serif';
                document.body.style.fontFamily = `${customFont}, ${baseFontStack}`;

                // Update font sizes
                const baseSize = config.font_size || defaultConfig.font_size;
                if (nameElement) nameElement.style.fontSize = `${baseSize * 2.5}px`;
                if (titleElement) titleElement.style.fontSize = `${baseSize * 1.2}px`;
                
                const sectionTitleElements = document.querySelectorAll('.section-title');
                sectionTitleElements.forEach(title => {
                    title.style.fontSize = `${baseSize * 1.5}px`;
                });

                const infoValues = document.querySelectorAll('.info-value');
                infoValues.forEach(value => {
                    value.style.fontSize = `${baseSize * 1.1}px`;
                });
            },

            mapToCapabilities: (config) => ({
                recolorables: [
                    {
                        get: () => config.background_color || defaultConfig.background_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ background_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.surface_color || defaultConfig.surface_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ surface_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.text_color || defaultConfig.text_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ text_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.primary_action_color || defaultConfig.primary_action_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ primary_action_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.secondary_action_color || defaultConfig.secondary_action_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ secondary_action_color: value });
                            }
                        }
                    }
                ],
                borderables: [],
                fontEditable: {
                    get: () => config.font_family || defaultConfig.font_family,
                    set: (value) => {
                        if (window.elementSdk) {
                            window.elementSdk.setConfig({ font_family: value });
                        }
                    }
                },
                fontSizeable: {
                    get: () => config.font_size || defaultConfig.font_size,
                    set: (value) => {
                        if (window.elementSdk) {
                            window.elementSdk.setConfig({ font_size: value });
                        }
                    }
                }
            }),

            mapToEditPanelValues: (config) => new Map([
                ["name", config.name || defaultConfig.name],
                ["title", config.title || defaultConfig.title],
                ["location", config.location || defaultConfig.location],
                ["email", config.email || defaultConfig.email],
                ["learning", config.learning || defaultConfig.learning],
                ["expertise", config.expertise || defaultConfig.expertise]
            ])
        };

        // Initialize Element SDK
        if (window.elementSdk) {
            window.elementSdk.init(element);
        }
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9948292df216dc8d',t:'MTc2MTQ2MjkwOS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
