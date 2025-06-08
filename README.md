<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="Free online image compressor that shrinks your images while maintaining quality. Process images locally in your browser - no uploads required.">
    <meta name="keywords" content="image compressor, reduce image size, free image optimizer, privacy-focused image tool, online image shrinker, compress jpeg, compress png, webp converter">
    <meta name="author" content="Krita Compress">
    <meta name="robots" content="index, follow">
    <meta property="og:title" content="Krita Compress - Shrink Your Images Like Magic">
    <meta property="og:description" content="Free online image compressor that processes files locally in your browser - no uploads required.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://kritacompress.com">
    <meta property="og:image" content="https://kritacompress.com/images/og-image.jpg">
    <meta property="og:site_name" content="Krita Compress">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Krita Compress - Free Online Image Compressor">
    <meta name="twitter:description" content="Shrink your images while maintaining quality. 100% private - no server uploads needed.">
    <link rel="canonical" href="https://kritacompress.com">
    
    <title>Krita Compress - Free Online Image Compressor | Shrink Images Locally</title>
    
    <!-- Favicon -->
    <link rel="icon" href="/favicon.ico" type="image/x-icon">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
    <link rel="manifest" href="/site.webmanifest">
    
    <!-- Preload critical resources -->
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" as="style" onload="this.onload=null;this.rel='stylesheet'">
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" as="style" onload="this.onload=null;this.rel='stylesheet'">
    <noscript>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    </noscript>
    
    <style>
        :root {
            --primary: #4361ee;
            --primary-dark: #3a56d4;
            --secondary: #3f37c9;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --success: #4cc9f0;
            --warning: #f8961e;
            --danger: #f72585;
            --gray: #6c757d;
            --gray-light: #e9ecef;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7ff;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            width: 100%;
        }

        header {
            text-align: center;
            margin-bottom: 20px;
            animation: fadeInDown 0.8s ease-out;
        }

        .logo {
            font-family: 'Arial', sans-serif;
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            perspective: 1000px;
        }

        .logo-line1 {
            font-size: 1em;
            line-height: 0.9;
            transform-style: preserve-3d;
            animation: float 6s ease-in-out infinite;
        }

        .logo-line2 {
            font-size: 0.7em;
            line-height: 1;
            margin-top: -5px;
            transform-style: preserve-3d;
            animation: float 6s ease-in-out infinite reverse;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotateY(0deg); }
            50% { transform: translateY(-5px) rotateY(5deg); }
        }

        .tagline {
            font-size: 1.2rem;
            color: var(--dark);
            margin-bottom: 20px;
            min-height: 40px;
            position: relative;
            display: inline-block;
        }

        .typewriter {
            border-right: 3px solid var(--primary);
            animation: blink-caret 0.75s step-end infinite;
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--primary); }
        }

        /* Ad container styles */
        .ad-container {
            width: 100%;
            margin: 15px 0;
            text-align: center;
            background-color: white;
            padding: 10px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            animation: fadeIn 0.8s ease-out;
        }

        .ad-label {
            font-size: 0.7rem;
            color: var(--gray);
            margin-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .upload-area {
            border: 2px dashed var(--gray-light);
            border-radius: 10px;
            padding: 30px 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            margin-bottom: 20px;
            background-color: white;
            transform: translateY(0);
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            touch-action: manipulation;
            animation: fadeInUp 0.8s ease-out;
            min-height: 120px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .upload-area:hover, .upload-area:active {
            border-color: var(--primary);
            background-color: rgba(67, 97, 238, 0.05);
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .upload-area.active {
            animation: pulse 1.5s infinite;
            border-color: var(--success);
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(67, 97, 238, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(67, 97, 238, 0); }
            100% { box-shadow: 0 0 0 0 rgba(67, 97, 238, 0); }
        }

        .upload-area i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 10px;
            transition: all 0.3s;
        }

        .upload-area:hover i, .upload-area:active i {
            transform: scale(1.1);
            color: var(--secondary);
        }

        .upload-text {
            margin-bottom: 10px;
            font-size: 0.9rem;
        }

        .upload-button {
            display: inline-block;
            padding: 8px 16px;
            background-color: var(--primary);
            color: white;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 0.9rem;
            position: relative;
            overflow: hidden;
            min-height: 48px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .upload-button:hover, .upload-button:active {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(67, 97, 238, 0.3);
        }

        .upload-button:after {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: all 0.5s;
        }

        .upload-button:hover:after, .upload-button:active:after {
            left: 100%;
        }

        .file-types {
            color: var(--gray);
            font-size: 0.8rem;
            margin-top: 10px;
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .privacy-guarantee {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
            padding: 12px;
            background-color: white;
            border-radius: 10px;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            animation: fadeInUp 0.8s ease-out 0.2s both;
        }

        .privacy-guarantee:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .privacy-guarantee i {
            color: var(--success);
            margin-right: 12px;
            font-size: 1.3rem;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-8px); }
            60% { transform: translateY(-4px); }
        }

        .privacy-text h3 {
            font-size: 1rem;
        }

        .privacy-text p {
            font-size: 0.85rem;
        }

        .target-size-section {
            background-color: white;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            animation: fadeInUp 0.8s ease-out 0.4s both;
        }

        .target-size-section:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .target-size-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .target-size-header i {
            color: var(--primary);
            margin-right: 8px;
            font-size: 1.3rem;
            animation: spin 4s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .target-size-header h3 {
            font-size: 1rem;
        }

        .size-controls {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }

        .size-input {
            flex: 1;
            padding: 10px;
            border: 1px solid var(--gray-light);
            border-radius: 6px;
            font-size: 0.9rem;
            transition: all 0.3s;
            font-size: 16px;
        }

        .size-input:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.2);
            outline: none;
        }

        .unit-select, .format-select {
            padding: 10px;
            border: 1px solid var(--gray-light);
            border-radius: 6px;
            background-color: white;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 0.9rem;
            font-size: 16px;
        }

        .unit-select:hover, .format-select:hover {
            border-color: var(--primary);
        }

        .format-select {
            width: 100%;
            margin-bottom: 12px;
        }

        .compress-btn {
            display: block;
            width: 100%;
            padding: 12px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            animation: fadeInUp 0.8s ease-out 0.6s both;
            min-height: 48px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .compress-btn:hover, .compress-btn:active {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(67, 97, 238, 0.3);
        }

        .compress-btn:disabled {
            background-color: var(--gray-light);
            color: var(--gray);
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .compress-btn:after {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: all 0.5s;
        }

        .compress-btn:not(:disabled):hover:after, .compress-btn:not(:disabled):active:after {
            left: 100%;
        }

        .success-message {
            background-color: #d4edda;
            color: #155724;
            padding: 12px;
            border-radius: 6px;
            margin-bottom: 15px;
            text-align: center;
            font-weight: 500;
            display: none;
            animation: slideInDown 0.5s ease-out;
        }

        .image-results {
            display: none;
            background-color: white;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
            animation: fadeInUp 0.5s ease-out;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .image-comparison {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 15px;
        }

        .image-box {
            flex: 1;
            transition: all 0.3s;
        }

        .image-box:hover {
            transform: translateY(-5px);
        }

        .image-box img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            margin-bottom: 8px;
            max-height: 250px;
            object-fit: contain;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .image-box img:hover {
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .image-label {
            font-weight: 600;
            margin-bottom: 8px;
            position: relative;
            display: inline-block;
            font-size: 0.95rem;
        }

        .image-label:after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s;
        }

        .image-box:hover .image-label:after {
            width: 100%;
        }

        .image-info {
            font-size: 0.8rem;
            color: var(--gray);
        }

        .download-btn {
            display: block;
            width: 100%;
            padding: 12px;
            background-color: var(--success);
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-align: center;
            text-decoration: none;
            margin-top: 15px;
            position: relative;
            overflow: hidden;
            min-height: 48px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .download-btn:hover, .download-btn:active {
            background-color: #3aa8d8;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(76, 201, 240, 0.3);
        }

        .download-btn:after {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: all 0.5s;
        }

        .download-btn:hover:after, .download-btn:active:after {
            left: 100%;
        }

        .download-btn.bounce {
            animation: bounce 2s infinite;
        }

        .features {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
            margin: 30px 0;
        }

        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
            transform: translateY(0);
            animation: fadeInUp 0.8s ease-out;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-icon {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 10px;
            display: inline-block;
            transition: all 0.3s;
        }

        .feature-card:hover .feature-icon {
            transform: scale(1.2);
            color: var(--secondary);
        }

        .feature-card h3 {
            font-size: 1rem;
            margin-bottom: 8px;
        }

        .feature-card p {
            font-size: 0.85rem;
        }

        footer {
            text-align: center;
            padding: 15px;
            color: var(--gray);
            font-size: 0.8rem;
            background-color: white;
            border-radius: 10px;
            margin-top: 20px;
            box-shadow: 0 -4px 15px rgba(0,0,0,0.05);
            animation: fadeInUp 0.8s ease-out;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 12px;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: var(--gray);
            text-decoration: none;
            font-size: 0.8rem;
            transition: all 0.3s;
            position: relative;
        }

        .footer-links a:after {
            content: "";
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 1px;
            background-color: var(--primary);
            transition: width 0.3s;
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .footer-links a:hover:after {
            width: 100%;
        }

        .made-with {
            margin-top: 8px;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            font-size: 0.8rem;
        }

        .heart {
            color: var(--danger);
            animation: heartbeat 1.5s infinite;
        }

        @keyframes heartbeat {
            0% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1); }
            75% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        #file-input {
            display: none;
        }

        /* Loading spinner */
        .spinner {
            display: inline-block;
            width: 18px;
            height: 18px;
            border: 2px solid rgba(255,255,255,.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s ease-in-out infinite;
        }

        /* Modal styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
            z-index: 1000;
            overflow-y: auto;
            padding: 10px;
            box-sizing: border-box;
            animation: fadeIn 0.3s;
        }

        .modal-content {
            background-color: white;
            margin: 20px auto;
            padding: 20px;
            border-radius: 10px;
            max-width: 600px;
            width: 100%;
            box-shadow: 0 5px 30px rgba(0,0,0,0.3);
            position: relative;
            animation: slideInDown 0.4s;
        }

        .close-modal {
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 1.5rem;
            color: var(--gray);
            cursor: pointer;
            transition: all 0.3s;
        }

        .close-modal:hover {
            color: var(--danger);
            transform: rotate(90deg);
        }

        .modal h2 {
            color: var(--primary);
            margin-bottom: 15px;
            font-size: 1.3rem;
            border-bottom: 2px solid var(--gray-light);
            padding-bottom: 10px;
        }

        .modal h3 {
            margin: 15px 0 8px;
            font-size: 1.1rem;
            color: var(--dark);
        }

        .modal p, .modal ul {
            margin-bottom: 12px;
            line-height: 1.5;
            font-size: 0.9rem;
        }

        .modal ul {
            padding-left: 20px;
        }

        /* Contact form styles */
        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .form-group label {
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--dark);
        }

        .form-group input, .form-group textarea {
            padding: 10px;
            border: 1px solid var(--gray-light);
            border-radius: 6px;
            font-size: 0.9rem;
            transition: all 0.3s;
            font-size: 16px;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.2);
            outline: none;
        }

        .form-group textarea {
            min-height: 100px;
            resize: vertical;
        }

        .send-btn {
            padding: 10px 15px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 0.9rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            align-self: flex-start;
            min-height: 48px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .send-btn:hover, .send-btn:active {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(67, 97, 238, 0.3);
        }

        /* Schema.org structured data */
        .sr-only {
            position: absolute;
            width: 1px;
            height: 1px;
            padding: 0;
            margin: -1px;
            overflow: hidden;
            clip: rect(0, 0, 0, 0);
            white-space: nowrap;
            border-width: 0;
        }

        /* Animations */
        @keyframes slideInDown {
            from {
                transform: translateY(-50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes fadeInUp {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes fadeInDown {
            from {
                transform: translateY(-20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        /* Responsive adjustments for larger screens */
        @media (min-width: 768px) {
            .logo {
                font-size: 3rem;
            }
            
            .logo-line1 {
                font-size: 1em;
            }
            
            .logo-line2 {
                font-size: 0.7em;
            }
            
            .tagline {
                font-size: 1.5rem;
                min-height: 60px;
            }
            
            .upload-area {
                padding: 40px 20px;
            }
            
            .upload-area i {
                font-size: 3rem;
            }
            
            .upload-text {
                font-size: 1rem;
            }
            
            .upload-button {
                padding: 10px 20px;
                font-size: 1rem;
            }
            
            .file-types {
                font-size: 0.9rem;
            }
            
            .privacy-guarantee {
                padding: 15px;
            }
            
            .privacy-text h3 {
                font-size: 1.1rem;
            }
            
            .privacy-text p {
                font-size: 0.9rem;
            }
            
            .target-size-section {
                padding: 20px;
            }
            
            .target-size-header h3 {
                font-size: 1.1rem;
            }
            
            .size-input, .unit-select, .format-select {
                font-size: 1rem;
                padding: 12px;
            }
            
            .compress-btn {
                padding: 15px;
                font-size: 1.1rem;
            }
            
            .success-message {
                padding: 15px;
                font-size: 1rem;
            }
            
            .image-results {
                padding: 20px;
            }
            
            .image-comparison {
                flex-direction: row;
                gap: 20px;
            }
            
            .image-label {
                font-size: 1rem;
            }
            
            .image-info {
                font-size: 0.9rem;
            }
            
            .download-btn {
                padding: 15px;
                font-size: 1.1rem;
            }
            
            .features {
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
                gap: 30px;
                margin: 50px 0;
            }
            
            .feature-card {
                padding: 30px;
            }
            
            .feature-icon {
                font-size: 2.5rem;
            }
            
            .feature-card h3 {
                font-size: 1.1rem;
            }
            
            .feature-card p {
                font-size: 0.9rem;
            }
            
            footer {
                padding: 20px;
                font-size: 0.9rem;
            }
            
            .footer-links a {
                font-size: 0.9rem;
            }
            
            .modal-content {
                padding: 30px;
                margin: 5% auto;
            }
            
            .modal h2 {
                font-size: 1.5rem;
            }
            
            .modal h3 {
                font-size: 1.2rem;
            }
            
            .modal p, .modal ul {
                font-size: 1rem;
            }
            
            .contact-form {
                gap: 15px;
            }
            
            .form-group input, .form-group textarea {
                padding: 12px;
                font-size: 1rem;
            }
            
            .form-group textarea {
                min-height: 120px;
            }
            
            .send-btn {
                padding: 12px 20px;
                font-size: 1rem;
            }
        }

        /* Mobile-specific adjustments */
        @media (max-width: 767px) {
            .container {
                padding: 15px;
                max-width: 100%;
                overflow-x: hidden;
            }

            .upload-area {
                padding: 25px 10px;
            }

            .target-size-section {
                padding: 15px;
            }

            .size-controls {
                flex-direction: column;
            }

            .size-input, .unit-select {
                width: 100%;
            }

            .image-comparison {
                flex-direction: column;
            }

            .image-box {
                margin-bottom: 15px;
            }

            .features {
                grid-template-columns: 1fr;
                gap: 15px;
            }

            .feature-card {
                padding: 15px;
            }

            .modal-content {
                margin: 10px auto;
                padding: 15px;
                width: 95%;
            }

            .close-modal {
                top: 5px;
                right: 5px;
                font-size: 1.2rem;
            }

            .tagline {
                font-size: 1.1rem;
                min-height: 40px;
            }

            .logo {
                font-size: 2rem;
            }
        }

        /* Very small screens (e.g., iPhone 5/SE) */
        @media (max-width: 320px) {
            .logo {
                font-size: 1.8rem;
            }
            
            .tagline {
                font-size: 1rem;
            }
            
            .upload-button {
                padding: 8px 12px;
            }
            
            .compress-btn {
                padding: 10px;
            }
        }

        /* Prevent layout shift when scrollbar appears */
        html {
            overflow-x: hidden;
            margin-right: calc(-1 * (100vw - 100%));
        }
    </style>
    
    <!-- Schema.org markup for Google -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebApplication",
      "name": "Krita Compress",
      "url": "https://kritacompress.com",
      "description": "Free online image compressor that processes files locally in your browser - no uploads required.",
      "applicationCategory": "ImageCompression",
      "operatingSystem": "Any",
      "offers": {
        "@type": "Offer",
        "price": "0",
        "priceCurrency": "USD"
      },
      "creator": {
        "@type": "Organization",
        "name": "Krita Compress"
      }
    }
    </script>
    
    <!-- Google AdSense -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-app-pub-8439221564602264" crossorigin="anonymous"></script>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <div class="logo-line1">Krita</div>
                <div class="logo-line2">Compress</div>
            </div>
            <div class="tagline" id="typewriter"></div>
            <p>Upload an image, set your target size, and let us do the magic!</p>
        </header>

        <!-- Top Ad Banner -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Google AdSense Ad Unit -->
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client=""ca-pub-8439221564602264"
                 data-ad-slot="1548065511"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <div class="upload-area" id="uploadArea">
            <i class="fas fa-cloud-upload-alt"></i>
            <h3>Upload Image</h3>
            <p class="upload-text">Drop your images here or</p>
            <div class="upload-button" id="uploadButton">Upload Files</div>
            <p class="file-types">JPEG, PNG, WEBP (Max 20MB)</p>
            <input type="file" id="file-input" accept="image/jpeg,image/png,image/webp">
        </div>

        <div class="privacy-guarantee">
            <i class="fas fa-check-circle"></i>
            <div class="privacy-text">
                <h3>Privacy Guaranteed</h3>
                <p>All image processing happens directly in your browser. Your files are never uploaded to any server.</p>
            </div>
        </div>

        <div class="target-size-section">
            <div class="target-size-header">
                <i class="fas fa-bullseye"></i>
                <h3>Set Target Size</h3>
            </div>
            <select id="output-format" class="format-select">
                <option value="jpeg">JPEG</option>
                <option value="png">PNG</option>
                <option value="webp">WebP</option>
            </select>
            <div class="size-controls">
                <input type="number" id="target-size" class="size-input" value="100" min="1">
                <select id="size-unit" class="unit-select">
                    <option value="kb">KB</option>
                    <option value="mb">MB</option>
                </select>
            </div>
            <button id="compress-btn" class="compress-btn" disabled>
                <i class="fas fa-compress-alt"></i> Compress Image
            </button>
        </div>

        <!-- Middle Ad Banner -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Google AdSense Ad Unit -->
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_ADSENSE_ID"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <div class="success-message" id="success-message">
            <i class="fas fa-check-circle"></i> <span id="success-text">Image compressed successfully to 211.25 KB. (Quality: 100%)</span>
        </div>

        <div class="image-results" id="image-results">
            <div class="image-comparison">
                <div class="image-box">
                    <div class="image-label">Original Image</div>
                    <img id="original-image" src="" alt="Original Image" style="display: none;">
                    <div class="image-info" id="original-info">-</div>
                </div>
                <div class="image-box">
                    <div class="image-label">Compressed Image</div>
                    <img id="compressed-image" src="" alt="Compressed Image" style="display: none;">
                    <div class="image-info" id="compressed-info">-</div>
                </div>
            </div>
            <a href="#" class="download-btn" id="download-btn" style="display: none;">
                <i class="fas fa-download"></i> Download Compressed Image
            </a>
        </div>

        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-bullseye"></i>
                </div>
                <h3>Target Size Compression</h3>
                <p>Specify your desired file size in KB or MB, and Krita Compress will optimize your image to meet that target precisely.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-lock"></i>
                </div>
                <h3>Privacy First</h3>
                <p>Images are processed locally in your browser. Nothing is uploaded to our servers, ensuring your data remains private.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-gift"></i>
                </div>
                <h3>Free & Easy to Use</h3>
                <p>A simple, intuitive interface makes image compression accessible to everyone, completely free of charge.</p>
            </div>
        </div>

        <!-- Bottom Ad Banner -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Google AdSense Ad Unit -->
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_ADSENSE_ID"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <footer>
            <div class="footer-links">
                <a href="#" id="privacy-link">Privacy Policy</a>
                <a href="#" id="terms-link">Terms & Conditions</a>
                <a href="#" id="about-link">About Us</a>
                <a href="#" id="contact-link">Contact Us</a>
            </div>
            <p>Images are processed in your browser and never uploaded to our servers.</p>
            <p class="made-with">Made with <span class="heart">♥</span> by Krita Compress</p>
            <p>© 2025 Krita Compress. All rights reserved.</p>
        </footer>
    </div>

    <!-- Privacy Policy Modal -->
    <div id="privacy-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal" id="close-privacy">&times;</span>
            <h2>Privacy Policy</h2>
            <p><strong>Last updated: 5/14/2025</strong></p>
            
            <h3>1. Introduction</h3>
            <p>Welcome to Krita Compress ("we", "us", or "our"). We are committed to protecting your privacy. This Privacy Policy explains how we handle information when you use our image compression tool (the "Service").</p>
            <p>Our core principle regarding your images and data is simple: All image processing is done locally in your browser. Your images are never uploaded to our servers.</p>
            
            <h3>2. Information We Do Not Collect</h3>
            <p>Since all image processing occurs on your device (client-side), we do not collect, store, or have access to:</p>
            <ul>
                <li>The images you upload for compression.</li>
                <li>The compressed images you download.</li>
                <li>Any personal data embedded within your images (e.g., EXIF data that is not stripped by your browser before processing).</li>
            </ul>
            
            <h3>3. Information We May Collect (Non-Personal)</h3>
            <p>We may collect anonymous usage data to improve our Service. This data is aggregated and does not personally identify you. This may include:</p>
            <ul>
                <li>Browser type and version.</li>
                <li>Operating system.</li>
                <li>Date and time of access.</li>
                <li>Features used within the Service (e.g., compression settings chosen, errors encountered).</li>
                <li>Referring URLs (if you came to our site from another website).</li>
            </ul>
            <p>This information is collected through standard web analytics tools and helps us understand how users interact with Krita Compress so we can enhance its functionality and user experience.</p>
            
            <h3>4. Cookies and Tracking Technologies</h3>
            <p>We may use cookies or similar tracking technologies for purposes such as:</p>
            <ul>
                <li>Remembering your preferences (e.g., theme settings if applicable).</li>
                <li>Analytics to understand service usage.</li>
                <li>Serving advertisements through third-party networks like Google AdSense.</li>
            </ul>
            <p>Google AdSense may use cookies (like the DoubleClick DART cookie) to serve ads based on your visit to our site and other sites on the Internet. You may opt out of the use of the DART cookie by visiting the Google Ad and Content Network privacy policy. Your browser settings can also be configured to manage or block cookies.</p>
            
            <h3>5. Third-Party Services (Advertising)</h3>
            <p>Krita Compress may display advertisements, potentially through third-party ad networks like Google AdSense. These ad networks may use cookies and web beacons to collect non-personal information about your visits to this and other websites to provide advertisements about goods and services of interest to you.</p>
            <p>We do not provide any personal information to these third-party advertisers. Please consult their respective privacy policies for more information on their data collection practices.</p>
            
            <h3>6. Security</h3>
            <p>While your images are processed client-side, we take reasonable measures to protect any anonymous data we collect. However, no internet transmission is 100% secure.</p>
            
            <h3>7. Children's Privacy</h3>
            <p>Our Service is not intended for children under the age of 13. We do not knowingly collect personal information from children under 13.</p>
            
            <h3>8. Changes to This Privacy Policy</h3>
            <p>We may update this Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page. You are advised to review this Privacy Policy periodically for any changes.</p>
            
            <h3>9. Contact Us</h3>
            <p>If you have any questions about this Privacy Policy, please contact us at kritacompresscontact@gmail.com or through the information provided on our Contact Us page.</p>
        </div>
    </div>

    <!-- Terms & Conditions Modal -->
    <div id="terms-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal" id="close-terms">&times;</span>
            <h2>Terms & Conditions</h2>
            <p><strong>Last updated: 5/14/2025</strong></p>
            
            <h3>1. Acceptance of Terms</h3>
            <p>By accessing and using Krita Compress (the "Service"), you agree to be bound by these Terms & Conditions ("Terms"). If you do not agree to all of these Terms, do not use this Service.</p>
            
            <h3>2. Service Description</h3>
            <p>Krita Compress provides an online tool for compressing image files. All image processing is performed locally within your web browser; no image data is transmitted to our servers.</p>
            
            <h3>3. User Responsibilities</h3>
            <p>You are solely responsible for the images you choose to process using Krita Compress. You agree not to use the Service to compress images that:</p>
            <ul>
                <li>Infringe upon any third party's copyright, patent, trademark, trade secret, or other proprietary rights or rights of publicity or privacy.</li>
                <li>Are illegal, defamatory, abusive, harassing, obscene, or otherwise objectionable.</li>
            </ul>
            <p>You acknowledge that Krita Compress does not review or pre-screen content, but we reserve the right (though not the obligation) to refuse or remove any content processed through the service if it violates these terms.</p>
            
            <h3>4. Intellectual Property</h3>
            <p>The Service and its original content (excluding content provided by users), features, and functionality are and will remain the exclusive property of Krita Compress and its licensors. The Service is protected by copyright, trademark, and other laws of both domestic and foreign countries.</p>
            
            <h3>5. Advertisements</h3>
            <p>The Service may display advertisements. Your interactions with advertisers found on or through the Service are solely between you and such advertisers. You agree that we shall not be responsible or liable for any loss or damage of any sort incurred as the result of any such dealings or as the result of the presence of such advertisers on the Service.</p>
            
            <h3>6. Disclaimer of Warranties</h3>
            <p>The Service is provided on an "AS IS" and "AS AVAILABLE" basis. Your use of the Service is at your sole risk. Krita Compress expressly disclaims all warranties of any kind, whether express or implied, including, but not limited to, the implied warranties of merchantability, fitness for a particular purpose, and non-infringement.</p>
            <p>Krita Compress makes no warranty that the Service will be uninterrupted, timely, secure, or error-free, or that the results obtained from the use of the Service will be accurate or reliable.</p>
            
            <h3>7. Limitation of Liability</h3>
            <p>In no event shall Krita Compress, nor its directors, employees, partners, agents, suppliers, or affiliates, be liable for any indirect, incidental, special, consequential or punitive damages, including without limitation, loss of profits, data, use, goodwill, or other intangible losses, resulting from (i) your access to or use of or inability to access or use the Service; (ii) any conduct or content of any third party on the Service; (iii) any content obtained from the Service; and (iv) unauthorized access, use or alteration of your transmissions or content, whether based on warranty, contract, tort (including negligence) or any other legal theory, whether or not we have been informed of the possibility of such damage.</p>
            
            <h3>8. Changes to Terms</h3>
            <p>We reserve the right, at our sole discretion, to modify or replace these Terms at any time. If a revision is material, we will try to provide at least 30 days' notice prior to any new terms taking effect. What constitutes a material change will be determined at our sole discretion.</p>
            <p>By continuing to access or use our Service after those revisions become effective, you agree to be bound by the revised terms.</p>
            
            <h3>9. Governing Law</h3>
            <p>These Terms shall be governed and construed in accordance with the laws of [Your Jurisdiction - e.g., State of California, USA], without regard to its conflict of law provisions.</p>
            
            <h3>10. Contact Us</h3>
            <p>If you have any questions about these Terms, please contact us via the information on our Contact Us page.</p>
        </div>
    </div>

    <!-- About Us Modal -->
    <div id="about-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal" id="close-about">&times;</span>
            <h2>About Krita Compress</h2>
            <h3>Your Privacy-Focused Image Compression Solution</h3>
            
            <p>Krita Compress was born from a simple idea: image compression should be easy, effective, and above all, private. In a digital world where data privacy is paramount, we believe you shouldn't have to upload your sensitive images to a server just to reduce their file size.</p>
            
            <h3>Our Mission</h3>
            <p>To provide a powerful, user-friendly image compression tool that respects your privacy by processing everything directly in your web browser. We aim to help individuals and businesses optimize their images for the web without compromising on security or quality.</p>
            
            <div style="display: flex; flex-direction: column; gap: 15px; margin: 20px 0;">
                <div>
                    <h4><i class="fas fa-bullseye" style="color: var(--primary);"></i> Precision</h4>
                    <p>Compress images to your exact target size in KB or MB.</p>
                </div>
                <div>
                    <h4><i class="fas fa-bolt" style="color: var(--primary);"></i> Speed & Efficiency</h4>
                    <p>Fast client-side processing means quick results without waiting for uploads.</p>
                </div>
                <div>
                    <h4><i class="fas fa-lock" style="color: var(--primary);"></i> Privacy First</h4>
                    <p>Your images stay on your device. We never see or store them.</p>
                </div>
            </div>
            
            <h3>Why Krita Compress?</h3>
            <p>We understand the need for smaller image files - for faster websites, easier sharing, and saving storage space. Existing tools often require uploads or compromise on control. Krita Compress puts you in charge, offering a transparent process that happens entirely on your computer.</p>
            
            <p>Whether you're a web developer, blogger, photographer, or just someone looking to shrink an image, Krita Compress is designed for you. We are constantly working to improve our tool and add new features, always keeping our core values of privacy, usability, and performance in mind.</p>
            
            <h3>Get in Touch</h3>
            <p>We value your feedback! If you have any questions, suggestions, or just want to say hello, please visit our Contact Us page.</p>
        </div>
    </div>

    <!-- Contact Us Modal -->
    <div id="contact-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal" id="close-contact">&times;</span>
            <h2>Contact Us</h2>
            <p>We'd love to hear from you! Send us your questions, feedback, or suggestions.</p>
            
            <form class="contact-form" id="contact-form">
                <div class="form-group">
                    <label for="contact-name">Your Name</label>
                    <input type="text" id="contact-name" placeholder="John Doe" required>
                </div>
                
                <div class="form-group">
                    <label for="contact-email">Your Email</label>
                    <input type="email" id="contact-email" placeholder="you@example.com" required>
                </div>
                
                <div class="form-group">
                    <label for="contact-message">Your Message</label>
                    <textarea id="contact-message" placeholder="How can we help you?" required></textarea>
                </div>
                
                <button type="submit" class="send-btn">Send Message</button>
            </form>
            
            <p style="margin-top: 20px;">Alternatively, you can reach us at <a href="mailto:kritacompresscontact@gmail.com">kritacompresscontact@gmail.com</a>.</p>
        </div>
    </div>

    <script>
        // Typewriter Effect
        const typewriterText = "Shrink your images like magic.";
        const typewriterElement = document.getElementById('typewriter');
        let i = 0;
        let isDeleting = false;
        let speed = 100;
        
        function typeWriter() {
            const currentText = typewriterText.substring(0, i);
            typewriterElement.innerHTML = currentText + '<span class="typewriter"></span>';
            
            if (!isDeleting && i === typewriterText.length) {
                isDeleting = true;
                speed = 50;
                setTimeout(typeWriter, 2000); // Pause at end
            } else if (isDeleting && i === 0) {
                isDeleting = false;
                speed = 100;
                setTimeout(typeWriter, 500); // Pause at start
            } else {
                i = isDeleting ? i - 1 : i + 1;
                setTimeout(typeWriter, speed);
            }
        }
        
        // Start the typewriter effect
        setTimeout(typeWriter, 1000);

        // Image Compression Functionality
        const uploadArea = document.getElementById('uploadArea');
        const uploadButton = document.getElementById('uploadButton');
        const fileInput = document.getElementById('file-input');
        const compressBtn = document.getElementById('compress-btn');
        const successMessage = document.getElementById('success-message');
        const successText = document.getElementById('success-text');
        const imageResults = document.getElementById('image-results');
        const downloadBtn = document.getElementById('download-btn');
        const originalImageEl = document.getElementById('original-image');
        const compressedImageEl = document.getElementById('compressed-image');
        const originalInfoEl = document.getElementById('original-info');
        const compressedInfoEl = document.getElementById('compressed-info');
        const outputFormat = document.getElementById('output-format');
        
        let originalImage = null;
        let compressedImageBlob = null;
        let originalSize = 0;
        let fileName = '';
        let isProcessing = false;
        
        uploadButton.addEventListener('click', (e) => {
            e.stopPropagation();
            fileInput.click();
        });
        
        uploadArea.addEventListener('click', () => {
            if (!isProcessing) {
                fileInput.click();
            }
        });
        
        uploadArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadArea.style.borderColor = 'var(--primary)';
            uploadArea.style.backgroundColor = 'rgba(67, 97, 238, 0.05)';
            uploadArea.classList.add('active');
        });
        
        uploadArea.addEventListener('dragleave', () => {
            uploadArea.style.borderColor = 'var(--gray-light)';
            uploadArea.style.backgroundColor = 'white';
            uploadArea.classList.remove('active');
        });
        
        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.style.borderColor = 'var(--gray-light)';
            uploadArea.style.backgroundColor = 'white';
            uploadArea.classList.remove('active');
            
            if (e.dataTransfer.files.length && !isProcessing) {
                handleFileSelect(e.dataTransfer.files[0]);
            }
        });
        
        fileInput.addEventListener('change', () => {
            if (fileInput.files.length && !isProcessing) {
                handleFileSelect(fileInput.files[0]);
            }
        });
        
        function handleFileSelect(file) {
            if (isProcessing) return;
            isProcessing = true;
            
            // Check if file is an image
            if (!file.type.match('image.*')) {
                alert('Please select an image file (JPEG, PNG, or WebP)');
                isProcessing = false;
                return;
            }
            
            // Check file size (limit to 20MB)
            if (file.size > 20 * 1024 * 1024) {
                alert('Image size should be less than 20MB');
                isProcessing = false;
                return;
            }
            
            fileName = file.name;
            originalSize = file.size;
            
            // Create a preview of the original image
            const reader = new FileReader();
            reader.onload = function(e) {
                originalImage = new Image();
                originalImage.onload = function() {
                    // Enable compress button
                    compressBtn.disabled = false;
                    
                    // Show original image
                    originalImageEl.src = e.target.result;
                    originalImageEl.style.display = 'block';
                    
                    // Show original file info
                    originalInfoEl.textContent = formatFileSize(originalSize);
                    
                    // Hide previous results
                    successMessage.style.display = 'none';
                    imageResults.style.display = 'none';
                    compressedImageEl.style.display = 'none';
                    downloadBtn.style.display = 'none';
                    
                    isProcessing = false;
                };
                originalImage.onerror = function() {
                    alert('Error loading image. Please try another file.');
                    isProcessing = false;
                };
                originalImage.src = e.target.result;
            };
            reader.onerror = function() {
                alert('Error reading file. Please try again.');
                isProcessing = false;
            };
            reader.readAsDataURL(file);
        }
        
        function compressImage() {
            if (!originalImage || isProcessing) return;
            isProcessing = true;
            
            // Show loading state
            compressBtn.disabled = true;
            compressBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Compressing...';
            
            // Get user settings
            const targetSize = parseFloat(document.getElementById('target-size').value);
            const sizeUnit = document.getElementById('size-unit').value;
            const format = outputFormat.value;
            
            // Convert target size to bytes
            let targetSizeBytes;
            if (sizeUnit === 'kb') {
                targetSizeBytes = targetSize * 1024;
            } else {
                targetSizeBytes = targetSize * 1024 * 1024;
            }
            
            // Calculate quality based on target size
            let quality = Math.min(1, targetSizeBytes / originalSize);
            quality = Math.max(0.1, quality); // Minimum quality 10%
            
            // Create a canvas to compress the image
            const canvas = document.createElement('canvas');
            const ctx = canvas.getContext('2d');
            
            // Set canvas dimensions
            canvas.width = originalImage.width;
            canvas.height = originalImage.height;
            ctx.drawImage(originalImage, 0, 0);
            
            // Get the compressed image as JPEG
            canvas.toBlob((blob) => {
                compressedImageBlob = blob;
                const compressedSize = blob.size;
                const reduction = ((originalSize - compressedSize) / originalSize * 100).toFixed(1);
                
                // Display results
                compressedImageEl.src = URL.createObjectURL(blob);
                compressedImageEl.style.display = 'block';
                compressedInfoEl.textContent = `${formatFileSize(compressedSize)} (${reduction}% reduction) (Quality: ${Math.round(quality * 100)}%)`;
                
                // Update success message
                successText.textContent = `Image compressed successfully to ${formatFileSize(compressedSize)}. (Quality: ${Math.round(quality * 100)}%)`;
                successMessage.style.display = 'block';
                imageResults.style.display = 'block';
                downloadBtn.style.display = 'block';
                downloadBtn.classList.add('bounce');
                
                // Reset button
                compressBtn.disabled = false;
                compressBtn.innerHTML = '<i class="fas fa-compress-alt"></i> Compress Image';
                
                // Scroll to results
                imageResults.scrollIntoView({ behavior: 'smooth' });
                
                isProcessing = false;
            }, 'image/jpeg', quality);
        }
        
        function downloadImage(e) {
            e.preventDefault();
            if (!compressedImageBlob || isProcessing) return;
            
            const a = document.createElement('a');
            const url = URL.createObjectURL(compressedImageBlob);
            
            // Create download filename
            const newFileName = fileName.replace(/\.[^/.]+$/, '') + '-compressed.jpg';
            
            a.href = url;
            a.download = newFileName;
            document.body.appendChild(a);
            a.click();
            
            setTimeout(() => {
                document.body.removeChild(a);
                URL.revokeObjectURL(url);
            }, 100);
        }
        
        function formatFileSize(bytes) {
            if (bytes < 1024) return bytes + ' bytes';
            else if (bytes < 1048576) return (bytes / 1024).toFixed(2) + ' KB';
            else return (bytes / 1048576).toFixed(2) + ' MB';
        }

        // Modal functionality
        const privacyModal = document.getElementById('privacy-modal');
        const termsModal = document.getElementById('terms-modal');
        const aboutModal = document.getElementById('about-modal');
        const contactModal = document.getElementById('contact-modal');
        
        const privacyLink = document.getElementById('privacy-link');
        const termsLink = document.getElementById('terms-link');
        const aboutLink = document.getElementById('about-link');
        const contactLink = document.getElementById('contact-link');
        
        const closePrivacy = document.getElementById('close-privacy');
        const closeTerms = document.getElementById('close-terms');
        const closeAbout = document.getElementById('close-about');
        const closeContact = document.getElementById('close-contact');
        
        privacyLink.addEventListener('click', (e) => {
            e.preventDefault();
            privacyModal.style.display = 'block';
            document.body.style.overflow = 'hidden';
        });
        
        termsLink.addEventListener('click', (e) => {
            e.preventDefault();
            termsModal.style.display = 'block';
            document.body.style.overflow = 'hidden';
        });
        
        aboutLink.addEventListener('click', (e) => {
            e.preventDefault();
            aboutModal.style.display = 'block';
            document.body.style.overflow = 'hidden';
        });
        
        contactLink.addEventListener('click', (e) => {
            e.preventDefault();
            contactModal.style.display = 'block';
            document.body.style.overflow = 'hidden';
        });
        
        closePrivacy.addEventListener('click', () => {
            privacyModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        closeTerms.addEventListener('click', () => {
            termsModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        closeAbout.addEventListener('click', () => {
            aboutModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        closeContact.addEventListener('click', () => {
            contactModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        window.addEventListener('click', (e) => {
            if (e.target === privacyModal) {
                privacyModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
            if (e.target === termsModal) {
                termsModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
            if (e.target === aboutModal) {
                aboutModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
            if (e.target === contactModal) {
                contactModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });

        // Contact form submission
        const contactForm = document.getElementById('contact-form');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const name = document.getElementById('contact-name').value;
            const email = document.getElementById('contact-email').value;
            const message = document.getElementById('contact-message').value;
            
            // In a real implementation, you would send this data to your server
            alert(`Thank you for your message, ${name}! We'll get back to you soon.`);
            
            // Reset form
            contactForm.reset();
            
            // Close modal
            contactModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });

        // Event listeners
        compressBtn.addEventListener('click', compressImage);
        downloadBtn.addEventListener('click', downloadImage);

        // Load Google AdSense ads
        window.addEventListener('load', function() {
            if (typeof adsbygoogle !== 'undefined') {
                adsbygoogle = window.adsbygoogle || [];
                adsbygoogle.push({});
            }
        });
    </script>
</body>
</html>
