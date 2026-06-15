<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แฟ้มสะสมผลงาน | แนะนำตัวเอง</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        /* ตัวแปรสี */
        :root {
            --primary-color: #2196F3;
            --secondary-color: #E3F2FD;
            --white: #FFFFFF;
            --text-dark: #333333;
            --text-light: #666666;
        }

        /* การตั้งค่าพื้นฐาน */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Sarabun', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth; /* Smooth Scroll */
        }

        body {
            background-color: var(--white);
            color: var(--text-dark);
            line-height: 1.6;
        }

        /* Navigation Bar แบบ Sticky */
        nav {
            position: sticky;
            top: 0;
            background-color: var(--primary-color);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            z-index: 1000;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 15px 0;
        }

        nav ul li {
            margin: 0 20px;
        }

        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--secondary-color);
        }

        /* การจัดวาง Section พื้นฐาน */
        section {
            padding: 80px 20px;
            max-width: 900px;
            margin: 0 auto;
        }

        h2 {
            text-align: center;
            color: var(--primary-color);
            margin-bottom: 40px;
            font-size: 2rem;
        }

        /* 1. ส่วนหัว (Hero Section) */
        #hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-top: 40px;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary-color);
            box-shadow: 0 4px 15px rgba(33, 150, 243, 0.2);
            margin-bottom: 20px;
        }

        #hero h1 {
            font-size: 2.5rem;
            color: var(--text-dark);
            margin-bottom: 10px;
        }

        #hero p {
            font-size: 1.2rem;
            color: var(--primary-color);
            font-weight: 600;
        }

        /* 2. ส่วนประวัติย่อ (About Me) */
        #about {
            background-color: var(--secondary-color);
            border-radius: 15px;
            padding: 50px 40px;
            margin-top: 40px;
            margin-bottom: 40px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }

        #about p {
            font-size: 1.1rem;
            color: var(--text-dark);
        }

        /* 3. ส่วนความสามารถพิเศษ (Skills) */
        .skill-item {
            margin-bottom: 25px;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .progress-bar-bg {
            background-color: var(--secondary-color);
            border-radius: 10px;
            height: 20px;
            width: 100%;
            overflow: hidden;
        }

        .progress-bar-fill {
            background-color: var(--primary-color);
            height: 100%;
            width: 0; /* เริ่มต้นที่ 0 เพื่อทำแอนิเมชัน */
            border-radius: 10px;
            transition: width 1.5s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        /* 4. ส่วนช่องทางติดต่อ (Contact) */
        .contact-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: var(--text-dark);
            padding: 20px;
            border-radius: 10px;
            transition: transform 0.3s, background-color 0.3s;
            width: 150px;
        }

        .contact-item:hover {
            transform: translateY(-5px);
            background-color: var(--secondary-color);
        }

        .contact-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        /* Responsive Design (มือถือ) */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
                padding: 10px 0;
            }

            nav ul li {
                margin: 5px 0;
            }

            #hero h1 {
                font-size: 2rem;
            }

            #about {
                padding: 30px 20px;
            }

            .contact-container {
                flex-direction: column;
                align-items: center;
            }

            .contact-item {
                width: 100%;
                max-width: 300px;
                flex-direction: row;
                justify-content: center;
                gap: 15px;
            }

            .contact-icon {
                margin-bottom: 0;
            }
        }
    </style>
</head>
<body>

    <nav>
        <ul>
            <li><a href="#hero">หน้าแรก</a></li>
            <li><a href="#about">เกี่ยวกับฉัน</a></li>
            <li><a href="#skills">ทักษะ</a></li>
            <li><a href="#contact">ติดต่อ</a></li>
        </ul>
    </nav>

    <section id="hero">
        <img src="https://placehold.co/200x200/2196F3/FFFFFF?text=Profile" alt="รูปโปรไฟล์" class="profile-img">
        <h1>สมชาย รักการโค้ด</h1>
        <p>Front-end Developer & UI/UX Enthusiast</p>
    </section>

    <section id="about">
        <h2>เกี่ยวกับฉัน</h2>
        <p>
            สวัสดีครับ ผมคือนักพัฒนาเว็บไซต์ที่หลงใหลในการสร้างสรรค์ประสบการณ์ผู้ใช้ (UX) ที่ดีและหน้าตาเว็บไซต์ (UI) ที่สวยงาม 
            มีความสนใจเป็นพิเศษในเทคโนโลยี Web Modern เช่น React และ Tailwind CSS 
            เป้าหมายของผมคือการนำเทคโนโลยีมาแก้ปัญหาในชีวิตจริงและพัฒนาตนเองอย่างต่อเนื่องเพื่อเป็น Full-stack Developer ในอนาคต
        </p>
    </section>

    <section id="skills">
        <h2>ความสามารถพิเศษ</h2>
        
        <div class="skill-item">
            <div class="skill-info">
                <span>HTML & CSS</span>
                <span>95%</span>
            </div>
            <div class="progress-bar-bg">
                <div class="progress-bar-fill" data-width="95%"></div>
            </div>
        </div>

        <div class="skill-item">
            <div class="skill-info">
                <span>JavaScript</span>
                <span>85%</span>
            </div>
            <div class="progress-bar-bg">
                <div class="progress-bar-fill" data-width="85%"></div>
            </div>
        </div>

        <div class="skill-item">
            <div class="skill-info">
                <span>UI/UX Design</span>
                <span>80%</span>
            </div>
            <div class="progress-bar-bg">
                <div class="progress-bar-fill" data-width="80%"></div>
            </div>
        </div>

        <div class="skill-item">
            <div class="skill-info">
                <span>React.js</span>
                <span>75%</span>
            </div>
            <div class="progress-bar-bg">
                <div class="progress-bar-fill" data-width="75%"></div>
            </div>
        </div>

        <div class="skill-item">
            <div class="skill-info">
                <span>Python</span>
                <span>60%</span>
            </div>
            <div class="progress-bar-bg">
                <div class="progress-bar-fill" data-width="60%"></div>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>ช่องทางติดต่อ</h2>
        <div class="contact-container">
            <a href="mailto:example@email.com" class="contact-item">
                <span class="contact-icon">📧</span>
                <span>อีเมล</span>
            </a>
            <a href="tel:+66812345678" class="contact-item">
                <span class="contact-icon">📱</span>
                <span>เบอร์โทรศัพท์</span>
            </a>
            <a href="https://github.com" target="_blank" class="contact-item">
                <span class="contact-icon">💻</span>
                <span>GitHub</span>
            </a>
            <a href="https://linkedin.com" target="_blank" class="contact-item">
                <span class="contact-icon">🤝</span>
                <span>LinkedIn</span>
            </a>
        </div>
    </section>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // ใช้ Intersection Observer เพื่อให้ Progress bar ทำงานเมื่อเลื่อนมาถึง Section นี้
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    // หากเลื่อนมาเจอ section ของ skills
                    if (entry.isIntersecting) {
                        const progressBars = entry.target.querySelectorAll('.progress-bar-fill');
                        progressBars.forEach(bar => {
                            // ดึงค่า width จาก data-width แล้วกำหนดให้ style
                            const width = bar.getAttribute('data-width');
                            bar.style.width = width;
                        });
                        // ยกเลิกการ observe หลังจากแอนิเมชันทำงานแล้ว (เล่นครั้งเดียว)
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.3 }); // ทำงานเมื่อเห็นหน้าจอ 30% ของ Section

            // เริ่ม observe ส่วน Skills
            const skillsSection = document.getElementById('skills');
            observer.observe(skillsSection);
        });
    </script>
</body>
</html>
