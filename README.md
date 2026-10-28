<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Land - Global Tech Solutions & Consulting</title>
    <style>
        :root {
            --primary-color: #1f4e78;
            --secondary-color: #2e75b6;
            --dark-bg: #0f172a;
            --light-bg: #f8fafc;
            --card-bg: #ffffff;
            --text-color: #334155;
            --accent-color: #0ea5e9;
        }

        * {
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background-color: var(--dark-bg);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-box {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-box img {
            height: 55px;
            width: auto;
            border-radius: 6px;
        }

        .logo-text h1 {
            color: #ffffff;
            font-size: 1.5rem;
            margin: 0;
        }

        .logo-text p {
            color: var(--accent-color);
            font-size: 0.8rem;
            margin: 0;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
            margin: 0;
            padding: 0;
        }

        nav a {
            color: #ffffff;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--accent-color);
        }

        /* Hero / About Section */
        .about-section {
            background: linear-gradient(135deg, var(--dark-bg), var(--primary-color));
            color: #ffffff;
            padding: 80px 0;
            text-align: center;
        }

        .brand-title {
            font-size: 3rem;
            margin-bottom: 10px;
            letter-spacing: 2px;
            font-weight: 800;
        }

        .brand-subtitle {
            font-size: 1.5rem;
            color: var(--accent-color);
            margin-bottom: 15px;
        }

        .brand-tagline {
            font-size: 1.1rem;
            opacity: 0.9;
            margin-bottom: 40px;
        }

        .about-content {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 12px;
            backdrop-filter: blur(10px);
            max-width: 850px;
            margin: 0 auto;
            text-align: right;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .about-content h2 {
            color: #ffffff;
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 10px;
        }

        /* Video Showcase Section */
        .video-section {
            padding: 60px 0;
            background-color: #0b1329;
            color: #ffffff;
            text-align: center;
        }

        .video-container {
            max-width: 900px;
            margin: 30px auto 0 auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0,0,0,0.5);
            border: 2px solid var(--accent-color);
        }

        .video-container video {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Projects Section */
        .projects-section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 50px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-top: 4px solid var(--secondary-color);
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
        }

        .project-img-box {
            width: 100%;
            height: 200px;
            overflow: hidden;
            background-color: #e2e8f0;
        }

        .project-img-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-img-box img {
            transform: scale(1.05);
        }

        .project-info {
            padding: 25px;
            flex-grow: 1;
        }

        .project-name {
            font-size: 1.4rem;
            color: var(--primary-color);
            margin-top: 0;
            margin-bottom: 5px;
        }

        .project-slogan {
            font-size: 0.9rem;
            color: #64748b;
            font-style: italic;
            margin-bottom: 15px;
        }

        .project-desc {
            font-size: 0.95rem;
            color: #475569;
        }

        /* Digital Gallery Section */
        .gallery-section {
            padding: 70px 0;
            background-color: #f1f5f9;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .gallery-item {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            height: 250px;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(15, 23, 42, 0.9));
            color: #ffffff;
            padding: 15px;
            text-align: center;
        }

        /* Contact Section */
        .contact-section {
            padding: 80px 0;
            background-color: var(--dark-bg);
            color: #ffffff;
        }

        .contact-wrapper {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            align-items: center;
        }

        .contact-info h3 {
            color: var(--accent-color);
            font-size: 1.8rem;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-size: 0.9rem;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border-radius: 6px;
            border: 1px solid #334155;
            background-color: #1e293b;
            color: #ffffff;
            font-family: inherit;
        }

        .submit-btn {
            background-color: var(--accent-color);
            color: #ffffff;
            border: none;
            padding: 12px 25px;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: background 0.3s;
        }

        .submit-btn:hover {
            background-color: var(--secondary-color);
        }

        /* Footer Section */
        .footer-section {
            background-color: #070c18;
            color: #ffffff;
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid #1e293b;
        }

        .footer-quote {
            font-size: 1.2rem;
            color: var(--accent-color);
            font-weight: bold;
            margin-bottom: 15px;
        }

        .copyright {
            font-size: 0.9rem;
            opacity: 0.7;
        }
    </style>
</head>
<body>

    <!-- الهيدر وشريط التنقل -->
    <header>
        <div class="container nav-container">
            <div class="logo-box">
                <img src="images/smartland_logo.webp" alt="Smart Land Logo">
                <div class="logo-text">
                    <h1>SMART LAND</h1>
                    <p>Global Tech Solutions & Consulting</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#about">عن الشركة</a></li>
                    <li><a href="#video">الفيديو التعريفي</a></li>
                    <li><a href="#projects">مشاريعنا</a></li>
                    <li><a href="#gallery">معرض الوسائط</a></li>
                    <li><a href="#contact">اتصل بنا</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- قسم التعريف بالشركة (About Section) -->
    <section id="about" class="about-section">
      <div class="container">
        <h1 class="brand-title">SMART LAND</h1>
        <h3 class="brand-subtitle">Innovative Technology Solutions</h3>
        <p class="brand-tagline">Powered by Artificial Intelligence to build a smarter future.</p>
        
        <div class="about-content">
          <h2>Technology with a Vision</h2>
          <p>
            تأسست شركة <strong>Smart Land</strong> في عام 2011 لتكون بيتاً عالمياً للخبرة في مجال الاستشارات والحلول البرمجية المتقدمة. نؤمن بـ <em>"تكنولوجيا ذات رؤية"</em> تعمل على تحويل الأفكار إلى حلول رقمية عملية تربط بين الأفراد، الأعمال، والفرص، وتصنع آفاقاً جديدة للابتكار الشامل.
          </p>
          
          <h3>Ideas into Innovation - Our Approach</h3>
          <p>
            ندمج بين التكنولوجيا المتقدمة والإبداع البصري لتطوير أنظمة وبرمجيات مخصصة تلبي تطلعات الأفراد والمؤسسات بدقة.
          </p>
        </div>
      </div>
    </section>

    <!-- قسم مقطع الفيديو التعريفي الشامل (Video Section) -->
    <section id="video" class="video-section">
        <div class="container">
            <h2 class="section-title" style="color: #ffffff;">العرض التعريفي الشامل للشركة ومشاريعها</h2>
            <p>فيديو ترويجي عالي الدقة يوضح رؤية Smart Land ومحفظة حلولها الذكية</p>
            
            <div class="video-container">
                <video controls poster="images/video_thumbnail.webp">
                    <source src="videos/smartland_intro.mp4" type="video/mp4">
                    متصفحك لا يدعم تشغيل مقطع الفيديو.
                </video>
            </div>
        </div>
    </section>

    <!-- قسم الخدمات والمشاريع (Projects Section) -->
    <section id="projects" class="projects-section">
      <div class="container">
        <h2 class="section-title">Our Services & Solutions</h2>

        <div class="projects-grid">
          
          <!-- المشروع الأول: Smart Signal -->
          <div class="project-card">
            <div class="project-img-box">
                <img src="images/smart_signal.webp" alt="Smart Signal App">
            </div>
            <div class="project-info">
                <h3 class="project-name">Smart Signal</h3>
                <h5 class="project-slogan">Bridging Communication Through Technology</h5>
                <p class="project-desc">
                  تطبيق متطور يعتمد على خوارزميات الرؤية الحاسوبية والتعلم العميق لترجمة لغة الإشارة فورياً إلى نصوص وأصوات مسموعة، مما يبني جسور التواصل الفعّال ويدعم الدمج المجتمعي لجميع الأفراد.
                </p>
            </div>
          </div>

          <!-- المشروع الثاني: MyKey -->
          <div class="project-card">
            <div class="project-img-box">
                <img src="images/mykey.webp" alt="MyKey Platform">
            </div>
            <div class="project-info">
                <h3 class="project-name">MY KEY</h3>
                <h5 class="project-slogan">Your Marketplace, Simplified</h5>
                <p class="project-desc">
                  منصة تفاعلية متكاملة مخصصة لسوق العقارات والمركبات لعمليات البيع والإيجار، تمنح المستخدم تجربة تصفح مبسطة وسريعة بدعم نظام تصفية ذكي.
                </p>
            </div>
          </div>

          <!-- المشروع الثالث: Sada -->
          <div class="project-card">
            <div class="project-img-box">
                <img src="images/sada.webp" alt="Sada E-Learning">
            </div>
            <div class="project-info">
                <h3 class="project-name">SADA</h3>
                <h5 class="project-slogan">Learning Without Limits</h5>
                <p class="project-desc">
                  بيئة تعليمية افتراضية تحت شعار "تعلم بلا حدود"، تدعم إدارة الفصول الذكية ومشاركة المحتوى التفاعلي لضمان استمرارية العملية التعليمية بمرونة عالية.
                </p>
            </div>
          </div>

          <!-- المشروع الرابع: Welcome -->
          <div class="project-card">
            <div class="project-img-box">
                <img src="images/welcome.webp" alt="Welcome E-Commerce">
            </div>
            <div class="project-info">
                <h3 class="project-name">WELCOME</h3>
                <h5 class="project-slogan">A World of Digital Shopping</h5>
                <p class="project-desc">
                  منصة تجارة إلكترونية متعددة المتاجر توفر عالماً كاملاً من التسوق الرقمي عبر واجهات تفاعلية جذابة وسريعة لتصفح العروض والمنتجات.
                </p>
            </div>
          </div>

          <!-- المشروع الخامس: Hospital Management System -->
          <div class="project-card">
            <div class="project-img-box">
                <img src="images/hospital_system.webp" alt="Hospital Management System">
            </div>
            <div class="project-info">
                <h3 class="project-name">Hospital Management System</h3>
                <h5 class="project-slogan">Smarter Healthcare Management</h5>
                <p class="project-desc">
                  أنظمة برمجية متطورة لإدارة الرعاية الصحية والمؤسسات الطبية بكفاءة أعلى، تشمل إدارة المواعيد، السجلات الطبية الذكية، وموارد المستشفيات.
                </p>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- قسم معرض الصور الرقمية الذكية (Digital Gallery Section) -->
    <section id="gallery" class="gallery-section">
        <div class="container">
            <h2 class="section-title">معرض الحلول الرقمية الذكية</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="images/tablet_dashboard.webp" alt="Smart Dashboard Application">
                    <div class="gallery-overlay">
                        <span>تطبيقات الأجهزة اللوحية الذكية</span>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="images/control_room.webp" alt="AI Control & Command Center">
                    <div class="gallery-overlay">
                        <span>مراكز التحكم والبيانات الذكية</span>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="images/contact_interface.webp" alt="Smart Contact Hub">
                    <div class="gallery-overlay">
                        <span>منظومة التواصل الرقمي المتقدمة</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم نموذج التواصل والمعلومات (Contact Section) -->
    <section id="contact" class="contact-section">
        <div class="container">
            <div class="contact-wrapper">
                <div class="contact-info">
                    <h3>تواصل معنا</h3>
                    <p>نحن هنا لمساعدتك في تحويل أفكارك ومؤسستك إلى العصر الرقمي القادم.</p>
                    <p><strong>العنوان:</strong> Smart Land HQ - Global Tech Park</p>
                    <p><strong>البريد الإلكتروني:</strong> info@smartland-tech.com</p>
                    <p><strong>الهاتف:</strong> +963 11 000 0000</p>
                </div>

                <div class="contact-form">
                    <form action="#" method="post">
                        <div class="form-group">
                            <label for="name">الاسم الكامل (Name)</label>
                            <input type="text" id="name" name="name" placeholder="أدخل اسمك الكامل" required>
                        </div>
                        <div class="form-group">
                            <label for="email">البريد الإلكتروني (Email)</label>
                            <input type="email" id="email" name="email" placeholder="example@domain.com" required>
                        </div>
                        <div class="form-group">
                            <label for="message">الرسالة (Message)</label>
                            <textarea id="message" name="message" rows="4" placeholder="اكتب رسالتك هنا..." required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">إرسال الرسالة (Send)</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم الخاتمة (Footer Quote) -->
    <footer class="footer-section">
      <div class="container">
        <p class="footer-quote">"We don't just build technology, WE BUILD THE FUTURE"</p>
        <p class="copyright">&copy; 2026 Smart Land. All Rights Reserved.</p>
      </div>
    </footer>

</body>
</html>
