    <title>PDF to Word Converter | Free Online Tool</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #4a6cf7;
            --secondary-color: #6b82fb;
            --dark-color: #1d2143;
            --light-color: #f8f9ff;
            --success-color: #28a745;
            --warning-color: #ffc107;
            --error-color: #dc3545;
            --border-radius: 8px;
            --box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fb;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 20px 0;
            box-shadow: var(--box-shadow);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            font-size: 28px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--light-color);
        }
        
        .hero {
            text-align: center;
            padding: 60px 0;
            background-color: white;
            margin: 30px 0;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
        }
        
        .hero h1 {
            font-size: 2.5rem;
            color: var(--dark-color);
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.1rem;
            color: #666;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .converter-container {
            background-color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            margin-bottom: 40px;
        }
        
        .upload-area {
            border: 2px dashed #ccc;
            border-radius: var(--border-radius);
            padding: 40px 20px;
            text-align: center;
            margin-bottom: 20px;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
        }
        
        .upload-area:hover {
            border-color: var(--primary-color);
            background-color: var(--light-color);
        }
        
        .upload-area.active {
            border-color: var(--primary-color);
            background-color: var(--light-color);
        }
        
        .upload-area i {
            font-size: 48px;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .upload-area h3 {
            margin-bottom: 10px;
            color: var(--dark-color);
        }
        
        .upload-area p {
            color: #777;
            margin-bottom: 15px;
        }
        
        .file-info {
            margin-top: 15px;
            padding: 10px;
            background-color: #f8f9fa;
            border-radius: var(--border-radius);
            display: none;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .btn:disabled {
            background: #ccc;
            cursor: not-allowed;
        }
        
        .btn-large {
            padding: 15px 35px;
            font-size: 1.1rem;
        }
        
        .progress-bar {
            height: 6px;
            background-color: #e9ecef;
            border-radius: 3px;
            margin: 20px 0;
            overflow: hidden;
            display: none;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            width: 0%;
            transition: width 0.3s ease;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }
        
        .feature-card {
            background-color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .feature-card i {
            font-size: 40px;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            margin-bottom: 15px;
            color: var(--dark-color);
        }
        
        .how-it-works {
            background-color: white;
            padding: 50px 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            margin: 50px 0;
        }
        
        .how-it-works h2 {
            text-align: center;
            margin-bottom: 40px;
            color: var(--dark-color);
        }
        
        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .step {
            text-align: center;
            padding: 20px;
        }
        
        .step-number {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border-radius: 50%;
            font-size: 24px;
            font-weight: 700;
            margin: 0 auto 20px;
        }
        
        .testimonials {
            margin: 50px 0;
        }
        
        .testimonials h2 {
            text-align: center;
            margin-bottom: 40px;
            color: var(--dark-color);
        }
        
        .testimonial-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
        }
        
        .testimonial-card p {
            font-style: italic;
            margin-bottom: 20px;
            color: #555;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .testimonial-author img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-section p, .footer-section a {
            color: #ccc;
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-section a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #ccc;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-file-word"></i>
                <span>PDF to Word Converter</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#how-it-works">How It Works</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container">
        <section class="hero">
            <h1>Convert PDF to Editable Word Documents</h1>
            <p>Free online tool to convert your PDF files to fully editable Word documents. Perfect for USA students, professionals, and businesses.</p>
            <a href="#converter" class="btn btn-large">Start Converting Now</a>
        </section>

        <section id="converter" class="converter-container">
            <div class="upload-area" id="dropArea">
                <i class="fas fa-file-upload"></i>
                <h3>Upload Your PDF File</h3>
                <p>Drag & drop your file here or click to browse</p>
                <p>Max file size: 50MB</p>
                <input type="file" id="fileInput" accept=".pdf" style="display: none;">
                <button class="btn" onclick="document.getElementById('fileInput').click()">Select PDF File</button>
                <div class="file-info" id="fileInfo"></div>
            </div>
            
            <div class="progress-bar" id="progressBar">
                <div class="progress" id="progress"></div>
            </div>
            
            <div style="text-align: center; margin-top: 30px;">
                <button class="btn btn-large" id="convertBtn" disabled>Convert to Word</button>
            </div>
            
            <div id="resultArea" style="display: none; text-align: center; margin-top: 30px; padding: 20px; background-color: #f0f7ff; border-radius: 8px;">
                <i class="fas fa-check-circle" style="font-size: 48px; color: var(--success-color); margin-bottom: 15px;"></i>
                <h3>Conversion Complete!</h3>
                <p>Your Word document is ready to download</p>
                <button class="btn" style="margin-top: 15px;" id="downloadBtn">Download Word File</button>
            </div>
        </section>

        <section id="features" class="features">
            <div class="feature-card">
                <i class="fas fa-shield-alt"></i>
                <h3>100% Secure</h3>
                <p>Your files are encrypted and automatically deleted after 2 hours. We prioritize your privacy.</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-bolt"></i>
                <h3>Fast Conversion</h3>
                <p>Advanced algorithms ensure your PDF to Word conversion takes just seconds.</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-highlighter"></i>
                <h3>High Accuracy</h3>
                <p>Maintain original formatting, images, and layouts with our precision conversion technology.</p>
            </div>
        </section>

        <section id="how-it-works" class="how-it-works">
            <h2>How to Convert PDF to Word</h2>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Upload PDF File</h3>
                    <p>Drag and drop your PDF file or click to browse your device</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Convert</h3>
                    <p>Click the convert button and let our tool process your file</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Download</h3>
                    <p>Download your editable Word document instantly</p>
                </div>
            </div>
        </section>

        <section id="testimonials" class="testimonials">
            <h2>What Our Users Say</h2>
            <div class="testimonial-cards">
                <div class="testimonial-card">
                    <p>"This is the best PDF to Word converter I've used. It preserved all the formatting perfectly!"</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/65.jpg" alt="Sarah Johnson">
                        <div>
                            <h4>Sarah Johnson</h4>
                            <p>New York, USA</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p>"As a student, this tool has been a lifesaver for converting research papers. Fast and accurate!"</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Michael Chen">
                        <div>
                            <h4>Michael Chen</h4>
                            <p>California, USA</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p>"The conversion quality is exceptional. I use it regularly for my business documents."</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Emily Rodriguez">
                        <div>
                            <h4>Emily Rodriguez</h4>
                            <p>Texas, USA</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>PDF to Word Converter</h3>
                    <p>The fastest and most reliable tool to convert your PDF files to editable Word documents online.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <a href="#">Home</a>
                    <a href="#how-it-works">How It Works</a>
                    <a href="#features">Features</a>
                    <a href="#testimonials">Testimonials</a>
                </div>
                <div class="footer-section">
                    <h3>Legal</h3>
                    <a href="#">Privacy Policy</a>
                    <a href="#">Terms of Service</a>
                    <a href="#">Cookie Policy</a>
                </div>
                <div class="footer-section">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-envelope"></i> support@pdftoword.com</p>
                    <div style="margin-top: 15px;">
                        <a href="#" style="display: inline-block; margin-right: 15px;"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" style="display: inline-block; margin-right: 15px;"><i class="fab fa-twitter"></i></a>
                        <a href="#" style="display: inline-block;"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 PDF to Word Converter. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // DOM elements
        const dropArea = document.getElementById('dropArea');
        const fileInput = document.getElementById('fileInput');
        const fileInfo = document.getElementById('fileInfo');
        const convertBtn = document.getElementById('convertBtn');
        const progressBar = document.getElementById('progressBar');
        const progress = document.getElementById('progress');
        const resultArea = document.getElementById('resultArea');
        const downloadBtn = document.getElementById('downloadBtn');
        
        let selectedFile = null;
        
        // Event listeners
        fileInput.addEventListener('change', handleFileSelect);
        convertBtn.addEventListener('click', convertFile);
        downloadBtn.addEventListener('click', downloadFile);
        
        // Drag and drop functionality
        ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(eventName => {
            dropArea.addEventListener(eventName, preventDefaults, false);
        });
        
        function preventDefaults(e) {
            e.preventDefault();
            e.stopPropagation();
        }
        
        ['dragenter', 'dragover'].forEach(eventName => {
            dropArea.addEventListener(eventName, highlight, false);
        });
        
        ['dragleave', 'drop'].forEach(eventName => {
            dropArea.addEventListener(eventName, unhighlight, false);
        });
        
        function highlight() {
            dropArea.classList.add('active');
        }
        
        function unhighlight() {
            dropArea.classList.remove('active');
        }
        
        dropArea.addEventListener('drop', handleDrop, false);
        
        function handleDrop(e) {
            const dt = e.dataTransfer;
            const files = dt.files;
            
            if (files.length > 0) {
                handleFiles(files);
            }
        }
        
        function handleFileSelect(e) {
            const files = e.target.files;
            
            if (files.length > 0) {
                handleFiles(files);
            }
        }
        
        function handleFiles(files) {
            const file = files[0];
            
            // Check if file is PDF
            if (file.type !== 'application/pdf') {
                alert('Please select a PDF file.');
                return;
            }
            
            // Check file size (max 50MB)
            if (file.size > 50 * 1024 * 1024) {
                alert('File size exceeds 50MB limit.');
                return;
            }
            
            selectedFile = file;
            
            // Display file info
            fileInfo.style.display = 'block';
            fileInfo.innerHTML = `
                <strong>Selected file:</strong> ${file.name} <br>
                <strong>Size:</strong> ${formatFileSize(file.size)}
            `;
            
            // Enable convert button
            convertBtn.disabled = false;
        }
        
        function formatFileSize(bytes) {
            if (bytes === 0) return '0 Bytes';
            
            const k = 1024;
            const sizes = ['Bytes', 'KB', 'MB', 'GB'];
            const i = Math.floor(Math.log(bytes) / Math.log(k));
            
            return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
        }
        
        function convertFile() {
            if (!selectedFile) return;
            
            // Show progress bar
            progressBar.style.display = 'block';
            convertBtn.disabled = true;
            convertBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Converting...';
            
            // Simulate conversion process
            let width = 0;
            const interval = setInterval(() => {
                width += 5;
                progress.style.width = width + '%';
                
                if (width >= 100) {
                    clearInterval(interval);
                    conversionComplete();
                }
            }, 100);
        }
        
        function conversionComplete() {
            // Show result area
            resultArea.style.display = 'block';
            
            // Reset convert button
            convertBtn.innerHTML = 'Convert to Word';
            convertBtn.disabled = false;
            
            // Scroll to results
            resultArea.scrollIntoView({ behavior: 'smooth' });
        }
        
        function downloadFile() {
            // In a real application, this would download the converted file
            // For demo purposes, we'll show an alert
            alert('In a real application, this would download the converted Word document. Since this is a frontend demo, actual file conversion would require server-side processing.');
        }
    </script>
</body>
</html>
