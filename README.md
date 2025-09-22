# sidra-friends-portal<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bushra'25 - Elegance Personified</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            color: #fff;
            line-height: 1.6;
            overflow-x: hidden;
            background: #1e4193;
        }
        
        /* Video background */
        .video-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .video-background video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            transform: translateX(-50%) translateY(-50%);
            object-fit: cover;
        }
        
        /* Overlay for better readability */
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.4) 100%);
            z-index: 1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 1;
        }
        
        header {
            text-align: center;
            padding: 60px 0;
            background: linear-gradient(135deg, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.4) 100%);
            backdrop-filter: blur(5px);
            border-bottom: 1px solid rgba(144, 23, 23, 0.1);
        }
        
        .logo-container {
            margin-bottom: 30px;
        }
        
        .logo {
            width: 200px;
            height: 200px;
            margin: 0 auto;
            border-radius: 50%;
            box-shadow: 0 0 30px rgba(209, 77, 114, 0.8);
            overflow: hidden;
            border: 3px solid rgba(255, 255, 255, 0.3);
            animation: pulse 3s infinite alternate;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 20px rgba(209, 77, 114, 0.6); }
            100% { box-shadow: 0 0 40px rgba(209, 77, 114, 1); }
        }
        
        .logo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            color: #fff;
            margin-bottom: 15px;
            font-weight: 700;
            text-shadow: 0 0 15px rgba(209, 77, 114, 0.8);
        }
        
        .content {
            padding: 80px 0;
        }
        
        .section {
            margin-bottom: 60px;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            color: #fff;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .section-title:after {
            content: "";
            display: block;
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #d14d72, transparent);
            margin: 15px auto 0;
        }
        
        .top-feature {
            display: flex;
            justify-content: center;
            margin-bottom: 50px;
        }
        
        .feature {
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(10px);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            width: 300px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .feature:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(209, 77, 114, 0.4);
        }
        
        .feature-image {
            width: 200px;
            height: 200px;
            overflow: hidden;
            border-radius: 50%;
            margin: 0 auto 20px;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
            border: 2px solid rgba(255, 255, 255, 0.2);
        }
        
        .feature-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .feature:hover .feature-image img {
            transform: scale(1.05);
        }
        
        .feature h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #fff;
            cursor: pointer;
            transition: color 0.3s ease, text-shadow 0.3s ease;
        }
        
        .feature h3:hover {
            color: #d14d72;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .feature p {
            color: rgba(255, 255, 255, 0.8);
        }
        
        .features-row {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }
        
        .won-message {
            font-size: 2rem;
            color: #fff;
            font-weight: bold;
            margin-top: 10px;
            opacity: 0;
            transition: opacity 0.5s ease;
            text-shadow: 0 0 15px rgba(209, 77, 114, 0.8);
        }
        
        .won-message.show {
            opacity: 1;
        }
        
        .login-btn {
            background: linear-gradient(135deg, #d14d72 0%, #9c2b4e 100%);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s ease;
            margin-top: 15px;
            box-shadow: 0 5px 15px rgba(209, 77, 114, 0.4);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .login-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(209, 77, 114, 0.6);
        }
        
        .login-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(5px);
        }
        
        .login-form-container {
            background: linear-gradient(135deg, rgba(0,0,0,0.9) 0%, rgba(20,20,20,0.9) 100%);
            border-radius: 15px;
            width: 90%;
            max-width: 400px;
            padding: 30px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.7);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .login-form-header {
            text-align: center;
            margin-bottom: 20px;
        }
        
        .login-form-header h2 {
            font-family: 'Playfair Display', serif;
            color: #d14d72;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 8px;
            font-size: 16px;
            color: #fff;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: #d14d72;
            outline: none;
            box-shadow: 0 0 0 2px rgba(209, 77, 114, 0.5);
            background: rgba(255, 255, 255, 0.15);
        }
        
        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(135deg, #d14d72 0%, #9c2b4e 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            box-shadow: 0 5px 15px rgba(209, 77, 114, 0.4);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(209, 77, 114, 0.6);
        }
        
        .btn-block {
            display: block;
            width: 100%;
        }
        
        .btn-secondary {
            background: linear-gradient(135deg, #6c757d 0%, #495057 100%);
        }
        
        .btn-secondary:hover {
            background: linear-gradient(135deg, #5a6268 0%, #3d4142 100%);
        }
        
        .form-actions {
            display: flex;
            gap: 10px;
            justify-content: flex-end;
            margin-top: 20px;
        }
        
        .alert {
            padding: 15px;
            margin-bottom: 20px;
            border-radius: 8px;
            display: none;
        }
        
        .alert-danger {
            background-color: rgba(248, 215, 218, 0.2);
            color: #f8d7da;
            border: 1px solid rgba(245, 198, 203, 0.5);
        }
        
        .dashboard {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(5px);
        }
        
        .dashboard-container {
            background: linear-gradient(135deg, rgba(0,0,0,0.9) 0%, rgba(20,20,20,0.9) 100%);
            border-radius: 15px;
            width: 90%;
            max-width: 600px;
            padding: 30px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.7);
            max-height: 90vh;
            overflow-y: auto;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .dashboard-header {
            text-align: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .dashboard-header h2 {
            font-family: 'Playfair Display', serif;
            color: #d14d72;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .dashboard-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            margin-bottom: 30px;
        }
        
        .dashboard-btn {
            flex: 1;
            min-width: 200px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .dashboard-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(209, 77, 114, 0.3);
            background: rgba(209, 77, 114, 0.2);
        }
        
        .dashboard-btn i {
            font-size: 2rem;
            color: #d14d72;
            margin-bottom: 15px;
        }
        
        .dashboard-btn h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: #fff;
        }
        
        .dashboard-btn p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        .form-section {
            display: none;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .form-section h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: #d14d72;
            margin-bottom: 20px;
            text-align: center;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .success-message {
            background-color: rgba(212, 237, 218, 0.2);
            color: #d4edda;
            border: 1px solid rgba(195, 230, 203, 0.5);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: none;
        }
        
        .close-dashboard {
            position: absolute;
            top: 15px;
            right: 15px;
            background: none;
            border: none;
            font-size: 24px;
            color: rgba(255, 255, 255, 0.7);
            cursor: pointer;
            transition: color 0.3s ease;
        }
        
        .close-dashboard:hover {
            color: #d14d72;
        }
        
        .student-list {
            margin-top: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .student-list h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.2rem;
            color: #d14d72;
            margin-bottom: 15px;
            text-align: center;
        }
        
        .student-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 15px;
            margin-bottom: 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .student-item:last-child {
            margin-bottom: 0;
        }
        
        .student-name {
            font-weight: 500;
        }
        
        .student-program {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        .assign-program-btn {
            background: linear-gradient(135deg, #d14d72 0%, #9c2b4e 100%);
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 12px;
            transition: all 0.3s ease;
            margin-left: 10px;
        }
        
        .assign-program-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 10px rgba(209, 77, 114, 0.4);
        }
        
        .remove-btn {
            background: linear-gradient(135deg, #dc3545 0%, #c82333 100%);
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 12px;
            transition: all 0.3s ease;
        }
        
        .remove-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 10px rgba(220, 53, 69, 0.4);
        }
        
        .data-list {
            margin-top: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .data-list h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.2rem;
            color: #d14d72;
            margin-bottom: 15px;
            text-align: center;
        }
        
        .data-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 15px;
            margin-bottom: 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .data-item:last-child {
            margin-bottom: 0;
        }
        
        .data-name {
            font-weight: 500;
        }
        
        .data-details {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        .student-dashboard {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(5px);
        }
        
        .student-dashboard-container {
            background: linear-gradient(135deg, rgba(0,0,0,0.9) 0%, rgba(20,20,20,0.9) 100%);
            border-radius: 15px;
            width: 90%;
            max-width: 600px;
            padding: 30px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.7);
            max-height: 90vh;
            overflow-y: auto;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .student-dashboard-header {
            text-align: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .student-dashboard-header h2 {
            font-family: 'Playfair Display', serif;
            color: #d14d72;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .student-info {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .student-info h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: #d14d72;
            margin-bottom: 15px;
            text-align: center;
            text-shadow: 0 0 10px rgba(209, 77, 114, 0.8);
        }
        
        .student-details {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .student-detail-item {
            display: flex;
            justify-content: space-between;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .student-detail-label {
            font-weight: 500;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .student-detail-value {
            color: #fff;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .features-row {
                flex-direction: column;
                align-items: center;
            }
            
            .feature {
                width: 100%;
                max-width: 300px;
            }
            
            .dashboard-container {
                width: 95%;
                padding: 20px;
            }
            
            .dashboard-btn {
                min-width: 150px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Video Background -->
    <div class="video-background">
        <video autoplay muted loop playsinline>
            <source src="https://v.ftcdn.net/14/66/63/08/700_F_1466630853_Of1f7jK0TKGn8Bla5QKoloAq3s088T1h_ST.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
        <div class="overlay"></div>
    </div>

    <div class="container">
        <header>
            <div class="logo-container">
                <div class="logo">
                    <img src="https://z-cdn-media.chatglm.cn/files/e0feec1c-be64-446a-89cc-9f84e3d0f3a9_pasted_image_1757908131752.png?auth_key=1789444180-cf4cd4602fd24439908fcae9d1250fe4-0-fbef78a250b4bc6cb41572aff710d83c" alt="Bushra Logo">
                </div>
            </div>
            <h1>Bushra'25</h1>
        </header>
        
        <section class="content">
            <div class="section">
                <h2 class="section-title">Team</h2>
                
                <!-- Irfan Khan alone at the top -->
                <div class="top-feature">
                    <div class="feature">
                        <div class="feature-image">
                            <img src="https://z-cdn-media.chatglm.cn/files/b9503c02-6b82-4be6-8e9e-0d2ec6568035_pasted_image_1757911477782.png?auth_key=1789447682-c9e40713c3ea4c179af603ec62f416ba-0-a000c0f4529dc518149db192027ee758" alt="Irfan Khan">
                        </div>
                        <h3 id="irfan-name" onclick="showWonMessage()">Irfan Khan</h3>
                        <button class="login-btn" onclick="showLoginModal()">Hebron Login</button>
                        <div id="won-message" class="won-message">won!</div>
                    </div>
                </div>
                
                <!-- Other three in one row -->
                <div class="features-row">
                    <div class="feature">
                        <div class="feature-image">
                            <img src="https://z-cdn-media.chatglm.cn/files/951ab9be-d864-42fd-b148-34c1df0177ed_pasted_image_1757913507041.png?auth_key=1789449548-6a086b2b553c48f7b4c890645767dc95-0-3f42ce493ccf5fbbd97b06ce8249c9b9" alt="Abu khozaima">
                        </div>
                        <h3>Abu khozaima</h3>
                        <p>Fustat</p>
                    </div>
                    
                    <div class="feature">
                        <div class="feature-image">
                            <img src="https://z-cdn-media.chatglm.cn/files/63bc6a1f-e181-4fb0-aa90-1e6e12cca6fd_pasted_image_1757914271160.png?auth_key=1789450281-624136f470ef46d5bde15f88bc819f7a-0-ea5755e3804767ff4a1c7a6f323e7e55" alt="Gulam Mobassir">
                        </div>
                        <h3>Gulam Mobassir</h3>
                        <p>kufa</p>
                        <button class="login-btn" onclick="showStudentLoginModal()">Students Login</button>
                        <div id="kufa-success-message" class="won-message">Login Successful!</div>
                    </div>
                    
                    <div class="feature">
                        <div class="feature-image">
                            <img src="https://z-cdn-media.chatglm.cn/files/418eb63b-1506-4d62-a3d7-e73cdff356ec_pasted_image_1757914679666.png?auth_key=1789450700-9bfb9d4b52ae4ebcb216be7f93b6b6eb-0-cc8328439fd81f4dde691ffef63adad2" alt="Sameer ansari">
                        </div>
                        <h3>Sameer ansari</h3>
                        <p>Yathrib</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Main Login Modal -->
    <div id="login-modal" class="login-modal">
        <div class="login-form-container">
            <div class="login-form-header">
                <h2>Hebron Login</h2>
                <p>Please enter your credentials</p>
            </div>
            <div id="login-alert" class="alert alert-danger"></div>
            <form id="login-form">
                <div class="form-group">
                    <label for="username">Username</label>
                    <input type="text" id="username" class="form-control" placeholder="Enter your username" required>
                </div>
                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" class="form-control" placeholder="Enter your password" required>
                </div>
                <div class="form-actions">
                    <button type="button" id="cancel-login-btn" class="btn btn-secondary">Cancel</button>
                    <button type="submit" class="btn">Login</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Students Login Modal -->
    <div id="students-login-modal" class="login-modal">
        <div class="login-form-container">
            <div class="login-form-header">
                <h2>Students Login</h2>
                <p>Please enter your credentials</p>
            </div>
            <div id="students-login-alert" class="alert alert-danger"></div>
            <form id="students-login-form">
                <div class="form-group">
                    <label for="students-username">Username</label>
                    <input type="text" id="students-username" class="form-control" placeholder="Enter your username" required>
                </div>
                <div class="form-group">
                    <label for="students-password">Password</label>
                    <input type="password" id="students-password" class="form-control" placeholder="Enter your password" required>
                </div>
                <div class="form-actions">
                    <button type="button" id="cancel-students-login-btn" class="btn btn-secondary">Cancel</button>
                    <button type="submit" class="btn">Login</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Dashboard Modal -->
    <div id="dashboard" class="dashboard">
        <div class="dashboard-container">
            <button class="close-dashboard" onclick="closeDashboard()">&times;</button>
            <div class="dashboard-header">
                <h2>Hebron Dashboard</h2>
                <p>Welcome to the administration panel</p>
            </div>
            
            <div class="dashboard-buttons">
                <div id="add-program-btn" class="dashboard-btn">
                    <i class="fas fa-book"></i>
                    <h3>Add Program</h3>
                    <p>Create a new academic program</p>
                </div>
                <div id="add-student-btn" class="dashboard-btn">
                    <i class="fas fa-user-plus"></i>
                    <h3>Add Student</h3>
                    <p>Register a new student</p>
                </div>
                <div id="assign-program-btn" class="dashboard-btn">
                    <i class="fas fa-user-graduate"></i>
                    <h3>Assign Program</h3>
                    <p>Assign program to student</p>
                </div>
                <div id="change-password-btn" class="dashboard-btn">
                    <i class="fas fa-key"></i>
                    <h3>Change Password</h3>
                    <p>Update your account password</p>
                </div>
            </div>
            
            <!-- Add Program Form -->
            <div id="add-program-form" class="form-section">
                <h3>Add New Program</h3>
                <div id="program-success" class="success-message"></div>
                <form id="program-form">
                    <div class="form-group">
                        <label for="program-name">Program Name</label>
                        <input type="text" id="program-name" class="form-control" placeholder="Enter program name" required>
                    </div>
                    <div class="form-group">
                        <label for="program-code">Program Code</label>
                        <input type="text" id="program-code" class="form-control" placeholder="Enter program code" required>
                    </div>
                    <div class="form-group">
                        <label for="program-duration">Duration (in years)</label>
                        <input type="number" id="program-duration" class="form-control" placeholder="Enter duration" required>
                    </div>
                    <div class="form-actions">
                        <button type="button" class="btn btn-secondary" onclick="hideForm('add-program-form')">Cancel</button>
                        <button type="submit" class="btn">Add Program</button>
                    </div>
                </form>
                
                <!-- Program List -->
                <div class="data-list">
                    <h4>Existing Programs</h4>
                    <div id="program-list-container">
                        <p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No programs added yet</p>
                    </div>
                </div>
            </div>
            
            <!-- Add Student Form -->
            <div id="add-student-form" class="form-section">
                <h3>Add New Student</h3>
                <div id="student-success" class="success-message"></div>
                <form id="student-form">
                    <div class="form-group">
                        <label for="student-name">Student Name</label>
                        <input type="text" id="student-name" class="form-control" placeholder="Enter student name" required>
                    </div>
                    <div class="form-group">
                        <label for="student-password">Password</label>
                        <input type="password" id="student-password" class="form-control" placeholder="Enter password" required>
                    </div>
                    <div class="form-actions">
                        <button type="button" class="btn btn-secondary" onclick="hideForm('add-student-form')">Cancel</button>
                        <button type="submit" class="btn">Add Student</button>
                    </div>
                </form>
                
                <!-- Student List -->
                <div class="data-list">
                    <h4>Existing Students</h4>
                    <div id="student-list-container">
                        <p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No students added yet</p>
                    </div>
                </div>
            </div>
            
            <!-- Assign Program Form -->
            <div id="assign-program-form" class="form-section">
                <h3>Assign Program to Student</h3>
                <div id="assign-success" class="success-message"></div>
                <form id="assign-form">
                    <div class="form-group">
                        <label for="select-student">Select Student</label>
                        <select id="select-student" class="form-control" required>
                            <option value="">Choose a student</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="select-program">Select Program</label>
                        <select id="select-program" class="form-control" required>
                            <option value="">Choose a program</option>
                        </select>
                    </div>
                    <div class="form-actions">
                        <button type="button" class="btn btn-secondary" onclick="hideForm('assign-program-form')">Cancel</button>
                        <button type="submit" class="btn">Assign Program</button>
                    </div>
                </form>
                
                <!-- Student Program List -->
                <div class="student-list">
                    <h4>Student Program Assignments</h4>
                    <div id="student-program-list-container">
                        <p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No students assigned yet</p>
                    </div>
                </div>
            </div>
            
            <!-- Change Password Form -->
            <div id="change-password-form" class="form-section">
                <h3>Change Password</h3>
                <div id="password-success" class="success-message"></div>
                <form id="password-form">
                    <div class="form-group">
                        <label for="current-password">Current Password</label>
                        <input type="password" id="current-password" class="form-control" placeholder="Enter current password" required>
                    </div>
                    <div class="form-group">
                        <label for="new-password">New Password</label>
                        <input type="password" id="new-password" class="form-control" placeholder="Enter new password" required>
                    </div>
                    <div class="form-group">
                        <label for="confirm-password">Confirm New Password</label>
                        <input type="password" id="confirm-password" class="form-control" placeholder="Confirm new password" required>
                    </div>
                    <div class="form-actions">
                        <button type="button" class="btn btn-secondary" onclick="hideForm('change-password-form')">Cancel</button>
                        <button type="submit" class="btn">Change Password</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Student Dashboard Modal -->
    <div id="student-dashboard" class="student-dashboard">
        <div class="student-dashboard-container">
            <button class="close-dashboard" onclick="closeStudentDashboard()">&times;</button>
            <div class="student-dashboard-header">
                <h2>Student Dashboard</h2>
                <p>Welcome to your student portal</p>
            </div>
            
            <div class="student-info">
                <h3>Student Information</h3>
                <div class="student-details">
                    <div class="student-detail-item">
                        <span class="student-detail-label">Name:</span>
                        <span class="student-detail-value" id="student-name-display">-</span>
                    </div>
                    <div class="student-detail-item">
                        <span class="student-detail-label">Program:</span>
                        <span class="student-detail-value" id="student-program-display">Not assigned</span>
                    </div>
                </div>
            </div>
            
            <div class="student-info">
                <h3>Program Details</h3>
                <div id="student-program-details">
                    <p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No program assigned</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Data storage
        let students = [];
        let programs = [];
        let studentPrograms = {};
        let adminPassword = 'Zeeshan Raza U1582';
        let currentLoggedInStudent = null;
        
        // Load data from localStorage on page load
        function loadData() {
            const savedStudents = localStorage.getItem('hebronStudents');
            const savedPrograms = localStorage.getItem('hebronPrograms');
            const savedStudentPrograms = localStorage.getItem('hebronStudentPrograms');
            const savedPassword = localStorage.getItem('hebronAdminPassword');
            
            if (savedStudents) {
                students = JSON.parse(savedStudents);
            }
            
            if (savedPrograms) {
                programs = JSON.parse(savedPrograms);
            }
            
            if (savedStudentPrograms) {
                studentPrograms = JSON.parse(savedStudentPrograms);
            }
            
            if (savedPassword) {
                adminPassword = savedPassword;
            }
        }
        
        // Save data to localStorage
        function saveData() {
            localStorage.setItem('hebronStudents', JSON.stringify(students));
            localStorage.setItem('hebronPrograms', JSON.stringify(programs));
            localStorage.setItem('hebronStudentPrograms', JSON.stringify(studentPrograms));
            localStorage.setItem('hebronAdminPassword', adminPassword);
        }
        
        function showWonMessage() {
            const wonMessage = document.getElementById('won-message');
            wonMessage.classList.add('show');
            
            // Hide the message after 3 seconds
            setTimeout(() => {
                wonMessage.classList.remove('show');
            }, 3000);
        }
        
        function showKufaSuccessMessage() {
            const kufaSuccessMessage = document.getElementById('kufa-success-message');
            kufaSuccessMessage.classList.add('show');
            
            // Hide the message after 3 seconds
            setTimeout(() => {
                kufaSuccessMessage.classList.remove('show');
            }, 3000);
        }
        
        // Login Modal functionality
        const loginModal = document.getElementById('login-modal');
        const loginForm = document.getElementById('login-form');
        const loginAlert = document.getElementById('login-alert');
        const cancelLoginBtn = document.getElementById('cancel-login-btn');
        const dashboard = document.getElementById('dashboard');
        
        // Students Login Modal functionality
        const studentsLoginModal = document.getElementById('students-login-modal');
        const studentsLoginForm = document.getElementById('students-login-form');
        const studentsLoginAlert = document.getElementById('students-login-alert');
        const cancelStudentsLoginBtn = document.getElementById('cancel-students-login-btn');
        
        // Student Dashboard
        const studentDashboard = document.getElementById('student-dashboard');
        
        function showLoginModal() {
            loginModal.style.display = 'flex';
        }
        
        function hideLoginModal() {
            loginModal.style.display = 'none';
            document.getElementById('username').value = '';
            document.getElementById('password').value = '';
            loginAlert.style.display = 'none';
        }
        
        function showStudentLoginModal() {
            studentsLoginModal.style.display = 'flex';
        }
        
        function hideStudentLoginModal() {
            studentsLoginModal.style.display = 'none';
            document.getElementById('students-username').value = '';
            document.getElementById('students-password').value = '';
            studentsLoginAlert.style.display = 'none';
        }
        
        function closeDashboard() {
            dashboard.style.display = 'none';
            hideAllForms();
        }
        
        function closeStudentDashboard() {
            studentDashboard.style.display = 'none';
            currentLoggedInStudent = null;
        }
        
        function hideAllForms() {
            document.getElementById('add-program-form').style.display = 'none';
            document.getElementById('add-student-form').style.display = 'none';
            document.getElementById('assign-program-form').style.display = 'none';
            document.getElementById('change-password-form').style.display = 'none';
        }
        
        function hideForm(formId) {
            document.getElementById(formId).style.display = 'none';
        }
        
        function showSuccessMessage(elementId, message) {
            const element = document.getElementById(elementId);
            element.textContent = message;
            element.style.display = 'block';
            
            setTimeout(() => {
                element.style.display = 'none';
            }, 3000);
        }
        
        // Update dropdowns and lists
        function updateStudentDropdown() {
            const selectStudent = document.getElementById('select-student');
            if (selectStudent) {
                selectStudent.innerHTML = '<option value="">Choose a student</option>';
                
                students.forEach(student => {
                    const option = document.createElement('option');
                    option.value = student.name;
                    option.textContent = student.name;
                    selectStudent.appendChild(option);
                });
            }
        }
        
        function updateProgramDropdown() {
            const selectProgram = document.getElementById('select-program');
            if (selectProgram) {
                selectProgram.innerHTML = '<option value="">Choose a program</option>';
                
                programs.forEach(program => {
                    const option = document.createElement('option');
                    option.value = program.name;
                    option.textContent = program.name;
                    selectProgram.appendChild(option);
                });
            }
        }
        
        function updateStudentList() {
            const container = document.getElementById('student-list-container');
            
            if (students.length === 0) {
                container.innerHTML = '<p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No students added yet</p>';
                return;
            }
            
            container.innerHTML = '';
            
            students.forEach(student => {
                const studentItem = document.createElement('div');
                studentItem.className = 'student-item';
                
                studentItem.innerHTML = `
                    <div>
                        <div class="student-name">${student.name}</div>
                        <div class="student-details">Password: ${student.password}</div>
                    </div>
                    <button class="remove-btn" onclick="removeStudent('${student.name}')">Remove</button>
                `;
                
                container.appendChild(studentItem);
            });
        }
        
        function updateProgramList() {
            const container = document.getElementById('program-list-container');
            
            if (programs.length === 0) {
                container.innerHTML = '<p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No programs added yet</p>';
                return;
            }
            
            container.innerHTML = '';
            
            programs.forEach(program => {
                const programItem = document.createElement('div');
                programItem.className = 'program-item';
                
                programItem.innerHTML = `
                    <div>
                        <div class="program-name">${program.name}</div>
                        <div class="program-details">Code: ${program.code}, Duration: ${program.duration} years</div>
                    </div>
                    <button class="remove-btn" onclick="removeProgram('${program.name}')">Remove</button>
                `;
                
                container.appendChild(programItem);
            });
        }
        
        function updateStudentProgramList() {
            const container = document.getElementById('student-program-list-container');
            
            if (Object.keys(studentPrograms).length === 0) {
                container.innerHTML = '<p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No students assigned yet</p>';
                return;
            }
            
            container.innerHTML = '';
            
            Object.keys(studentPrograms).forEach(studentName => {
                const programName = studentPrograms[studentName];
                
                const studentItem = document.createElement('div');
                studentItem.className = 'student-item';
                
                studentItem.innerHTML = `
                    <div>
                        <div class="student-name">${studentName}</div>
                        <div class="student-program">${programName}</div>
                    </div>
                    <button class="remove-btn" onclick="removeProgramAssignment('${studentName}')">Remove</button>
                `;
                
                container.appendChild(studentItem);
            });
        }
        
        function removeStudent(studentName) {
            students = students.filter(student => student.name !== studentName);
            
            // Remove any program assignments for this student
            if (studentPrograms[studentName]) {
                delete studentPrograms[studentName];
            }
            
            saveData();
            updateStudentList();
            updateStudentDropdown();
            updateStudentProgramList();
            showSuccessMessage('student-success', `Student "${studentName}" has been removed.`);
        }
        
        function removeProgram(programName) {
            programs = programs.filter(program => program.name !== programName);
            
            // Remove any program assignments for this program
            Object.keys(studentPrograms).forEach(studentName => {
                if (studentPrograms[studentName] === programName) {
                    delete studentPrograms[studentName];
                }
            });
            
            saveData();
            updateProgramList();
            updateProgramDropdown();
            updateStudentProgramList();
            showSuccessMessage('program-success', `Program "${programName}" has been removed.`);
        }
        
        function removeProgramAssignment(studentName) {
            delete studentPrograms[studentName];
            saveData();
            updateStudentProgramList();
            showSuccessMessage('assign-success', `Program assignment for ${studentName} has been removed.`);
        }
        
        function displayStudentDashboard(studentName) {
            currentLoggedInStudent = studentName;
            
            // Set student name
            document.getElementById('student-name-display').textContent = studentName;
            
            // Check if student has a program assigned
            if (studentPrograms[studentName]) {
                const programName = studentPrograms[studentName];
                document.getElementById('student-program-display').textContent = programName;
                
                // Find program details
                const program = programs.find(p => p.name === programName);
                if (program) {
                    document.getElementById('student-program-details').innerHTML = `
                        <div class="student-detail-item">
                            <span class="student-detail-label">Program Name:</span>
                            <span class="student-detail-value">${program.name}</span>
                        </div>
                        <div class="student-detail-item">
                            <span class="student-detail-label">Program Code:</span>
                            <span class="student-detail-value">${program.code}</span>
                        </div>
                        <div class="student-detail-item">
                            <span class="student-detail-label">Duration:</span>
                            <span class="student-detail-value">${program.duration} years</span>
                        </div>
                    `;
                } else {
                    document.getElementById('student-program-details').innerHTML = `
                        <p style="text-align: center; color: rgba(255, 255, 255, 0.6);">Program details not found</p>
                    `;
                }
            } else {
                document.getElementById('student-program-display').textContent = 'Not assigned';
                document.getElementById('student-program-details').innerHTML = `
                    <p style="text-align: center; color: rgba(255, 255, 255, 0.6);">No program assigned</p>
                `;
            }
            
            // Show student dashboard
            studentDashboard.style.display = 'flex';
        }
        
        // Cancel login
        cancelLoginBtn.addEventListener('click', hideLoginModal);
        cancelStudentsLoginBtn.addEventListener('click', hideStudentLoginModal);
        
        // Close modal when clicking outside
        loginModal.addEventListener('click', function(e) {
            if (e.target === loginModal) {
                hideLoginModal();
            }
        });
        
        studentsLoginModal.addEventListener('click', function(e) {
            if (e.target === studentsLoginModal) {
                hideStudentLoginModal();
            }
        });
        
        // Close dashboard when clicking outside
        dashboard.addEventListener('click', function(e) {
            if (e.target === dashboard) {
                closeDashboard();
            }
        });
        
        studentDashboard.addEventListener('click', function(e) {
            if (e.target === studentDashboard) {
                closeStudentDashboard();
            }
        });
        
        // Login form submission
        loginForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value.trim();
            const password = document.getElementById('password').value.trim();
            
            // Check credentials
            if (username === 'Zeeshan Raza U1582' && password === adminPassword) {
                // Successful login
                hideLoginModal();
                dashboard.style.display = 'flex';
            } else {
                // Failed login
                loginAlert.textContent = 'Invalid username or password. Please try again.';
                loginAlert.style.display = 'block';
                
                // Hide alert after 3 seconds
                setTimeout(() => {
                    loginAlert.style.display = 'none';
                }, 3000);
            }
        });
        
        // Students login form submission
        studentsLoginForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('students-username').value.trim();
            const password = document.getElementById('students-password').value.trim();
            
            // Check if student exists
            const student = students.find(s => s.name === username && s.password === password);
            
            if (student) {
                // Successful login
                hideStudentLoginModal();
                showKufaSuccessMessage();
                
                // Display student dashboard after a short delay
                setTimeout(() => {
                    displayStudentDashboard(username);
                }, 1500);
            } else {
                // Failed login
                studentsLoginAlert.textContent = 'Invalid username or password. Please try again.';
                studentsLoginAlert.style.display = 'block';
                
                // Hide alert after 3 seconds
                setTimeout(() => {
                    studentsLoginAlert.style.display = 'none';
                }, 3000);
            }
        });
        
        // Dashboard button functionality
        document.getElementById('add-program-btn').addEventListener('click', function() {
            hideAllForms();
            updateProgramList();
            document.getElementById('add-program-form').style.display = 'block';
        });
        
        document.getElementById('add-student-btn').addEventListener('click', function() {
            hideAllForms();
            updateStudentList();
            document.getElementById('add-student-form').style.display = 'block';
        });
        
        document.getElementById('assign-program-btn').addEventListener('click', function() {
            hideAllForms();
            updateStudentDropdown();
            updateProgramDropdown();
            updateStudentProgramList();
            document.getElementById('assign-program-form').style.display = 'block';
        });
        
        document.getElementById('change-password-btn').addEventListener('click', function() {
            hideAllForms();
            document.getElementById('change-password-form').style.display = 'block';
        });
        
        // Program form submission
        document.getElementById('program-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const programName = document.getElementById('program-name').value.trim();
            const programCode = document.getElementById('program-code').value.trim();
            const programDuration = document.getElementById('program-duration').value.trim();
            
            // Check if program already exists
            if (programs.some(program => program.name === programName)) {
                showSuccessMessage('program-success', `Program "${programName}" already exists.`);
                return;
            }
            
            // Add to programs array
            programs.push({
                name: programName,
                code: programCode,
                duration: programDuration
            });
            
            saveData();
            
            // Show success message
            showSuccessMessage('program-success', `Program "${programName}" has been successfully added.`);
            
            // Reset form
            document.getElementById('program-form').reset();
            
            // Update program list
            updateProgramList();
            
            // Hide form after 2 seconds
            setTimeout(() => {
                hideForm('add-program-form');
            }, 2000);
        });
        
        // Student form submission
        document.getElementById('student-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const studentName = document.getElementById('student-name').value.trim();
            const studentPassword = document.getElementById('student-password').value.trim();
            
            // Check if student already exists
            if (students.some(student => student.name === studentName)) {
                showSuccessMessage('student-success', `Student "${studentName}" already exists.`);
                return;
            }
            
            // Add to students array
            students.push({
                name: studentName,
                password: studentPassword
            });
            
            saveData();
            
            // Show success message
            showSuccessMessage('student-success', `Student "${studentName}" has been successfully added.`);
            
            // Reset form
            document.getElementById('student-form').reset();
            
            // Update student list
            updateStudentList();
            
            // Hide form after 2 seconds
            setTimeout(() => {
                hideForm('add-student-form');
            }, 2000);
        });
        
        // Assign program form submission
        document.getElementById('assign-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const studentName = document.getElementById('select-student').value;
            const programName = document.getElementById('select-program').value;
            
            // Assign program to student
            studentPrograms[studentName] = programName;
            
            saveData();
            
            // Show success message
            showSuccessMessage('assign-success', `Program "${programName}" has been assigned to ${studentName}.`);
            
            // Reset form
            document.getElementById('assign-form').reset();
            
            // Update student program list
            updateStudentProgramList();
            
            // Hide form after 2 seconds
            setTimeout(() => {
                hideForm('assign-program-form');
            }, 2000);
        });
        
        // Password form submission
        document.getElementById('password-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const currentPassword = document.getElementById('current-password').value.trim();
            const newPassword = document.getElementById('new-password').value.trim();
            const confirmPassword = document.getElementById('confirm-password').value.trim();
            
            // Check if current password is correct
            if (currentPassword !== adminPassword) {
                alert('Current password is incorrect. Please try again.');
                return;
            }
            
            // Check if new passwords match
            if (newPassword !== confirmPassword) {
                alert('New passwords do not match. Please try again.');
                return;
            }
            
            // Update password
            adminPassword = newPassword;
            saveData();
            
            // Show success message
            showSuccessMessage('password-success', 'Password has been successfully changed.');
            
            // Reset form
            document.getElementById('password-form').reset();
            
            // Hide form after 2 seconds
            setTimeout(() => {
                hideForm('change-password-form');
            }, 2000);
        });
        
        // Initialize data on page load
        window.addEventListener('load', function() {
            loadData();
        });
    </script>
</body>
</html>
