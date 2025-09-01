---
title: 
date: 2025-08-05 21:22:46
cover: "https://s21.ax1x.com/2025/08/05/pVUUBjO.jpg"  # URL加引号
aside: false
comments: false #此文件下禁用评论
layout: false  # 这很重要，避免使用主题的布局
---
<!-- <iframe width="100%" scrolling=no height="100%" frameborder="0" src="https://music.lzmhhh.com/"></iframe> -->
<!-- <!DOCTYPE html> -->
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>音乐殿堂</title>
    
    <!-- 使用您博客的favicon -->
    <link rel="icon" href="/avatar_32x32.ico" type="image/x-icon">
    <link rel="shortcut icon" href="/avatar_32x32.ico" type="image/x-icon">
    
    <!-- 引入钉钉进步体 -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Ma+Shan+Zheng&display=swap">
    
    <!-- Font Awesome CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* 基础样式重置 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        /* 设置全局字体为钉钉进步体，备选方案为其他中文字体 */
        body {
            font-family: "Ma Shan Zheng", "DingTalk JinBuTi", "Microsoft YaHei", "PingFang SC", "Hiragino Sans GB", "Heiti SC", sans-serif;
            background: #0f172a;
            color: #e2e8f0;
            overflow: hidden;
            height: 100vh;
            display: flex;
            flex-direction: column;
            background-image: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f172a 100%);
        }
        
        /* 顶部导航栏样式 */
        .navbar {
            background: linear-gradient(135deg, rgba(40, 40, 80, 0.98) 0%, rgba(35, 35, 70, 0.98) 100%);
            border-bottom: 1px solid rgba(91, 39, 255, 0.3);
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
            flex-shrink: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }
        
        .logo {
            display: flex;
            align-items: center;
            font-size: 1.4rem;
            font-weight: bold;
            color: #ffffff;
            text-decoration: none;
            transition: all 0.3s ease;
            font-family: "Ma Shan Zheng", "DingTalk JinBuTi", cursive;
        }
        
        .logo:hover {
            opacity: 0.8;
            transform: translateY(-1px);
        }
        
        .grid-icon {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(3, 1fr);
            gap: 2px;
            width: 16px;
            height: 22px;
            margin-right: 10px;
        }
        
        .grid-square {
            background-color: #ffffff;
            border-radius: 1px;
        }
        
        /* 中间菜单部分 */
        .nav-menu {
            display: flex;
            list-style: none;
            height: 100%;
        }
        
        .nav-menu > li {
            position: relative;
            margin: 0 8px;
            height: 100%;
            display: flex;
            align-items: center;
        }
        
        .nav-menu > li > a {
            color: #ffffff;
            text-decoration: none;
            padding: 12px 22px;
            border-radius: 8px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            height: 60%;
            font-weight: 500;
            font-family: "Ma Shan Zheng", "DingTalk JinBuTi", cursive;
            font-size: 1.1rem;
        }
        
        .nav-menu > li > a:hover {
            background: #5b27ff;
            color: #ffffff;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(91, 39, 255, 0.4);
        }
        
        .nav-menu > li > a.active {
            background: rgba(91, 39, 255, 0.2);
            color: #ffffff;
        }
        
        /* 下拉菜单样式 */
        .dropdown {
            position: absolute;
            top: 100%;
            left: 50%;
            transform: translateX(-50%) translateY(10px);
            background: #ffffff;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 1000;
            display: flex;
            padding: 10px;
            white-space: nowrap;
            border: 1px solid #5b27ff;
        }
        
        .nav-menu > li:hover .dropdown {
            opacity: 1;
            visibility: visible;
            transform: translateX(-50%) translateY(0);
        }
        
        .dropdown a {
            display: block;
            padding: 10px 15px;
            color: #333333 !important;
            text-decoration: none;
            transition: all 0.3s ease;
            border-radius: 8px;
            margin: 0 4px;
            font-weight: 500;
            font-family: "Ma Shan Zheng", "DingTalk JinBuTi", cursive;
        }
        
        .dropdown a:hover {
            background: #5b27ff;
            color: #ffffff !important;
        }
        
        .dropdown i {
            color: #333333 !important;
            width: 18px;
            text-align: center;
            margin-right: 8px;
        }
        
        .dropdown a:hover i {
            color: #ffffff !important;
        }
        
        /* 右侧图标样式 */
        .nav-icons {
            display: flex;
            align-items: center;
        }
        
        .icon-btn {
            width: 42px;
            height: 42px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ffffff;
            background: transparent;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-left: 12px;
            font-size: 1.3rem;
        }
        
        .icon-btn:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
        }
        
        /* 自定义控制台图标 */
        .console-icon {
            width: 22px;
            height: 22px;
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        
        .console-top {
            width: 100%;
            height: 7px;
            background: #ffffff;
            border-radius: 1px;
        }
        
        .console-bottom {
            display: flex;
            justify-content: space-between;
            width: 100%;
            height: 11px;
        }
        
        .console-square {
            width: 9px;
            height: 11px;
            background: #ffffff;
            border-radius: 1px;
        }
        
        .console-rect {
            width: 18px;
            height: 11px;
            background: #ffffff;
            border-radius: 1px;
            margin-left: 5px;
        }
        
        /* 音乐容器全屏样式 */
        #music-container {
            flex: 1;
            position: relative;
            overflow: hidden;
        }
        
        #music-iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* 移动设备菜单 */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: #ffffff;
            font-size: 1.6rem;
            cursor: pointer;
        }
        
        /* 响应式调整 */
        @media (max-width: 1100px) {
            .nav-menu {
                position: fixed;
                top: 70px;
                left: 0;
                width: 100%;
                background: rgba(15, 23, 42, 0.98);
                flex-direction: column;
                padding: 20px;
                backdrop-filter: blur(10px);
                transform: translateY(-100%);
                transition: transform 0.3s ease;
                z-index: 999;
                height: auto;
            }
            
            .nav-menu.active {
                transform: translateY(0);
            }
            
            .nav-menu > li {
                width: 100%;
                margin: 8px 0;
                height: auto;
            }
            
            .dropdown {
                position: static;
                opacity: 1;
                visibility: visible;
                transform: none;
                display: none;
                margin-top: 8px;
                margin-left: 20px;
                width: calc(100% - 40px);
                flex-direction: column;
                background: rgba(255, 255, 255, 0.9);
                left: 0;
                transform: none !important;
            }
            
            .nav-menu > li:hover .dropdown {
                display: flex;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .nav-icons {
                display: none;
            }
        }
        
        @media (max-width: 600px) {
            .logo span {
                display: none;
            }
            
            .navbar {
                padding: 0 15px;
            }
        }
        
        /* 加载状态 */
        .loading {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            z-index: 10;
            font-family: "Ma Shan Zheng", "DingTalk JinBuTi", cursive;
        }
        
        .spinner {
            border: 4px solid rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            border-top: 4px solid #4cc9f0;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin: 0 auto 15px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* 修复通知消息样式 */
        .notification {
            position: fixed;
            top: 90px;
            right: 20px;
            padding: 15px 20px;
            background: rgba(76, 201, 240, 0.9);
            color: #0f172a;
            border-radius: 5px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            transform: translateX(calc(100% + 20px)); /* 确保完全隐藏在屏幕外 */
            transition: transform 0.3s ease;
            z-index: 1001;
            max-width: 300px; /* 添加最大宽度限制 */
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .notification.show {
            transform: translateX(0);
        }
        
        /* 预加载样式 */
        .preload {
            display: none;
        }
        
        /* 优化加载速度的样式 */
        .loading-bar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, #5b27ff, #4cc9f0, #5b27ff);
            background-size: 200% 100%;
            animation: loadingAnimation 1.5s infinite linear;
            z-index: 10000;
            display: none;
        }
        
        @keyframes loadingAnimation {
            0% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
    </style>
</head>
<body>
    <!-- 顶部加载进度条 -->
    <div class="loading-bar" id="loading-bar"></div>
    
    <!-- 预加载页面资源 -->
    <div class="preload">
        <!-- 预加载其他页面资源 -->
    </div>
    
    <!-- 顶部导航栏 -->
    <nav class="navbar">
        <a href="/" class="logo">
            <div class="grid-icon">
                <div class="grid-square"></div>
                <div class="grid-square"></div>
                <div class="grid-square"></div>
                <div class="grid-square"></div>
                <div class="grid-square"></div>
                <div class="grid-square"></div>
            </div>
            <span>音乐殿堂</span>
        </a>
        
        <button class="menu-toggle" id="menu-toggle">
            <i class="fas fa-bars"></i>
        </button>
        
        <ul class="nav-menu" id="nav-menu">
            <!-- 文章菜单 -->
            <li>
                <a href="#">文章</a>
                <div class="dropdown">
                    <a href="/archives/"><i class="fas fa-newspaper"></i>文章</a>
                    <a href="/categories/"><i class="fas fa-folder"></i>分类</a>
                    <a href="/tags/"><i class="fas fa-tags"></i>标签</a>
                </div>
            </li>
            
            <!-- 友链菜单 -->
            <li>
                <a href="#">友链</a>
                <div class="dropdown">
                    <a href="/link/"><i class="fas fa-user-friends"></i>友链</a>
                    <a href="/comments/"><i class="fas fa-comment"></i>留言板</a>
                </div>
            </li>
            
            <!-- 我的菜单 -->
            <li>
                <a href="#" class="active">我的</a>
                <div class="dropdown">
                    <a href="/music/" class="active"><i class="fas fa-music"></i>音乐馆</a>
                    <a href="/album/"><i class="fas fa-images"></i>相册集</a>
                    <a href="/movies/"><i class="fas fa-film"></i>音乐殿堂</a>
                </div>
            </li>
            
            <!-- 关于菜单 -->
            <li>
                <a href="#">关于</a>
                <div class="dropdown">
                    <a href="/about/"><i class="fas fa-user-circle"></i>关于本人</a>
                    <a href="#"><i class="fas fa-random"></i>随便逛逛</a>
                </div>
            </li>
        </ul>
        
        <div class="nav-icons">
            <button class="icon-btn">
                <i class="fas fa-dice"></i>
            </button>
            <button class="icon-btn">
                <i class="fas fa-search"></i>
            </button>
            <button class="icon-btn">
                <div class="console-icon">
                    <div class="console-top"></div>
                    <div class="console-bottom">
                        <div class="console-square"></div>
                        <div class="console-rect"></div>
                    </div>
                </div>
            </button>
        </div>
    </nav>
    
    <!-- 音乐容器 -->
    <div id="music-container">
        <div class="loading">
            <div class="spinner"></div>
            <p>音乐播放器加载中...</p>
        </div>
        <iframe id="music-iframe" src="https://music.lzmhhh.com/" width="100%" height="100%" frameborder="0" scrolling="no"></iframe>
    </div>
    
    <!-- 通知消息 -->
    <div class="notification" id="notification">
        音乐播放器已加载完成！
    </div>

    <script>
        // 页面加载完成后执行
        document.addEventListener('DOMContentLoaded', function() {
            const iframe = document.getElementById('music-iframe');
            const loading = document.querySelector('.loading');
            const menuToggle = document.getElementById('menu-toggle');
            const navMenu = document.getElementById('nav-menu');
            const notification = document.getElementById('notification');
            const loadingBar = document.getElementById('loading-bar');
            
            // 预加载其他页面资源
            function preloadPages() {
                const pages = [
                    '/archives/', '/categories/', '/tags/', 
                    '/link/', '/comments/', '/album/', 
                    '/movies/', '/about/'
                ];
                
                pages.forEach(page => {
                    // 使用XMLHttpRequest预加载页面
                    const xhr = new XMLHttpRequest();
                    xhr.open('GET', page, true);
                    xhr.send();
                    
                    // 同时使用link prefetch
                    const link = document.createElement('link');
                    link.rel = 'prefetch';
                    link.href = page;
                    document.head.appendChild(link);
                });
            }
            
            // 显示加载进度条
            function showLoadingBar() {
                loadingBar.style.display = 'block';
            }
            
            // 隐藏加载进度条
            function hideLoadingBar() {
                loadingBar.style.display = 'none';
            }
            
            // 移动端菜单切换
            menuToggle.addEventListener('click', function() {
                navMenu.classList.toggle('active');
            });
            
            // 点击菜单项后关闭移动菜单
            document.querySelectorAll('.nav-menu a').forEach(link => {
                link.addEventListener('click', function(e) {
                    // 如果是外部链接，添加加载提示
                    if (this.getAttribute('href') && this.getAttribute('href') !== '#') {
                        // 对于站内链接，使用更快的导航方式
                        if (this.getAttribute('href').startsWith('/')) {
                            e.preventDefault();
                            showLoadingBar();
                            
                            // 预加载目标页面
                            const targetUrl = this.getAttribute('href');
                            const xhr = new XMLHttpRequest();
                            xhr.open('GET', targetUrl, true);
                            xhr.onreadystatechange = function() {
                                if (xhr.readyState === 4) {
                                    // 使用setTimeout确保加载条显示
                                    setTimeout(() => {
                                        window.location.href = targetUrl;
                                    }, 100);
                                }
                            };
                            xhr.send();
                        }
                    }
                    
                    navMenu.classList.remove('active');
                });
            });
            
            // 隐藏加载提示当iframe加载完成时
            iframe.addEventListener('load', function() {
                loading.style.display = 'none';
                
                // 显示通知
                notification.classList.add('show');
                setTimeout(() => {
                    notification.classList.remove('show');
                }, 3000);
                
                // 预加载其他页面
                preloadPages();
            });
            
            // 处理可能的iframe加载错误
            iframe.addEventListener('error', function() {
                loading.innerHTML = `
                    <div style="color: #ff6b6b;">
                        <h3>加载失败</h3>
                        <p>音乐播放器无法加载，请检查网络连接或稍后重试</p>
                        <button onclick="window.location.reload()" class="icon-btn" style="background: #ff6b6b; margin-top: 10px;">
                            <i class="fas fa-redo"></i>
                        </button>
                    </div>
                `;
            });
            
            // 设置当前活动菜单项
            function setActiveMenu() {
                const currentPage = window.location.pathname;
                document.querySelectorAll('.nav-menu a').forEach(link => {
                    if (link.getAttribute('href') === currentPage) {
                        link.classList.add('active');
                    } else {
                        link.classList.remove('active');
                    }
                });
            }
            
            setActiveMenu();
            
            // 初始化预加载
            preloadPages();
            
            // 页面完全加载后隐藏加载条
            window.addEventListener('load', function() {
                hideLoadingBar();
            });
            
            // 添加快速导航功能
            document.addEventListener('keydown', function(e) {
                // 按ESC键刷新页面
                if (e.key === 'Escape') {
                    window.location.reload();
                }
            });
        });
    </script>
</body>
</html>