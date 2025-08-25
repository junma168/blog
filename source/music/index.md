---
title: 音乐馆
date: 2021-04-24 21:41:30
type: music
aplayer: true
top_img: false
comments: false
aside: false
---
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>紧凑型音乐播放器</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #8a2be2;
            --secondary: #ff6ec7;
            --accent: #4cc9f0;
            --dark: #121212;
            --light: #f8f8f8;
            --glass: rgba(255, 255, 255, 0.1);
            --glass-border: rgba(255, 255, 255, 0.2);
            --glass-hover: rgba(255, 255, 255, 0.15);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
            padding: 15px;
        }

        .container {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 20px;
            width: 100%;
            max-width: 1200px;
            max-height: 700px;
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid var(--glass-border);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3), 
                        0 0 15px var(--primary);
            overflow: hidden;
            padding: 18px;
        }

        @media (max-width: 900px) {
            .container {
                grid-template-columns: 1fr;
                max-height: none;
            }
        }

        /* 左侧歌曲列表样式 */
        .song-list-container {
            background: var(--glass);
            border-radius: 18px;
            padding: 18px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            border: 1px solid var(--glass-border);
            height: 100%;
        }

        .search-container {
            margin-bottom: 15px;
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }

        .search-input {
            flex: 1;
            min-width: 120px;
            padding: 10px 15px;
            border-radius: 50px;
            border: 1px solid var(--glass-border);
            background: rgba(0, 0, 0, 0.2);
            color: var(--light);
            outline: none;
            font-size: 0.9rem;
        }

        .search-input:focus {
            border-color: var(--primary);
        }

        .platform-select {
            background: rgba(0, 0, 0, 0.2);
            color: var(--light);
            border: 1px solid var(--glass-border);
            padding: 10px 12px;
            border-radius: 50px;
            outline: none;
            font-size: 0.9rem;
        }

        .search-btn {
            padding: 10px 16px;
            border-radius: 50px;
            border: none;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            color: white;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
            font-size: 0.9rem;
            white-space: nowrap;
        }

        .search-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.4);
        }

        .song-list-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            padding-bottom: 12px;
            border-bottom: 1px solid var(--glass-border);
        }

        .song-list-header h2 {
            font-size: 1.3rem;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }

        .song-list {
            list-style: none;
            overflow-y: auto;
            flex: 1;
            padding-right: 5px;
        }

        .song-list::-webkit-scrollbar {
            width: 5px;
        }

        .song-list::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 10px;
        }

        .song-item {
            display: flex;
            align-items: center;
            padding: 12px;
            border-radius: 12px;
            margin-bottom: 8px;
            background: var(--glass);
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid transparent;
        }

        .song-item:hover {
            background: var(--glass-hover);
            border-color: var(--primary);
            transform: translateX(3px);
        }

        .song-item.active {
            background: linear-gradient(90deg, rgba(138, 43, 226, 0.2), rgba(255, 110, 199, 0.2));
            border-color: var(--primary);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.2);
        }

        .song-number {
            font-weight: bold;
            color: var(--primary);
            margin-right: 12px;
            min-width: 22px;
            font-size: 1rem;
        }

        .song-info {
            flex: 1;
            overflow: hidden;
        }

        .song-name {
            font-weight: 600;
            margin-bottom: 4px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            font-size: 0.95rem;
        }

        .song-artist {
            font-size: 0.8rem;
            color: rgba(255, 255, 255, 0.7);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .load-more {
            text-align: center;
            padding: 12px;
            color: var(--primary);
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
            font-size: 0.9rem;
            margin-top: 10px;
        }

        .load-more:hover {
            color: var(--secondary);
        }

        /* 右侧播放器样式 */
        .player-container {
            display: flex;
            flex-direction: column;
            padding: 18px;
            height: 100%;
        }

        .player-header {
            text-align: center;
            margin-bottom: 20px;
        }

        .player-header h1 {
            font-size: 1.8rem;
            background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 8px;
            font-weight: 800;
        }

        .player-header p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }

        .album-container {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }

        .album-cover {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            overflow: hidden;
            box-shadow: 0 0 25px rgba(138, 43, 226, 0.5);
            border: 3px solid var(--primary);
            animation: rotate 20s linear infinite;
            animation-play-state: paused;
            position: relative;
        }

        .album-cover::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, transparent 60%, rgba(0, 0, 0, 0.8));
            z-index: 1;
        }

        .album-cover.playing {
            animation-play-state: running;
        }

        @keyframes rotate {
            100% {
                transform: rotate(360deg);
            }
        }

        .album-cover img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .music-info {
            text-align: center;
            margin-bottom: 20px;
        }

        .music-info h2 {
            font-size: 1.5rem;
            margin-bottom: 8px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            font-weight: 700;
        }

        .music-info p {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 4px;
            font-size: 0.9rem;
        }

        .progress-container {
            margin-bottom: 15px;
        }

        .progress-bar {
            width: 100%;
            height: 6px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            overflow: hidden;
            cursor: pointer;
            margin-bottom: 8px;
            position: relative;
        }

        .progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            width: 0%;
            transition: width 0.1s linear;
            border-radius: 10px;
        }

        .progress-bar:hover .progress {
            background: linear-gradient(90deg, var(--accent), var(--primary));
        }

        .time-display {
            display: flex;
            justify-content: space-between;
            font-size: 0.8rem;
            color: rgba(255, 255, 255, 0.7);
        }

        .controls {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-bottom: 20px;
        }

        .control-btn {
            background: var(--glass);
            border: 1px solid var(--glass-border);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            cursor: pointer;
            color: var(--light);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
        }

        .control-btn:hover {
            background: var(--glass-hover);
            transform: scale(1.1);
            color: var(--accent);
            border-color: var(--accent);
        }

        .play-pause {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            font-size: 1.6rem;
            border: none;
        }

        .play-pause:hover {
            background: linear-gradient(135deg, var(--secondary), var(--primary));
            box-shadow: 0 0 15px rgba(138, 43, 226, 0.7);
            color: white;
        }

        .volume-control {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 15px;
            background: var(--glass);
            padding: 8px 15px;
            border-radius: 50px;
            border: 1px solid var(--glass-border);
        }

        .volume-icon {
            color: var(--primary);
            font-size: 1.1rem;
        }

        .volume-slider {
            flex: 1;
            -webkit-appearance: none;
            height: 4px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            outline: none;
        }

        .volume-slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background: var(--primary);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .volume-slider::-webkit-slider-thumb:hover {
            background: var(--secondary);
            transform: scale(1.2);
        }

        .lyrics-container {
            max-height: 150px;
            overflow-y: auto;
            padding: 15px;
            border-radius: 15px;
            background: var(--glass);
            text-align: center;
            font-size: 0.9rem;
            line-height: 1.6;
            border: 1px solid var(--glass-border);
            margin-top: auto;
        }

        .lyric-line {
            margin-bottom: 8px;
            color: rgba(255, 255, 255, 0.7);
            transition: all 0.3s ease;
            padding: 4px 8px;
            border-radius: 8px;
        }

        .lyric-line.active {
            color: var(--light);
            background: linear-gradient(90deg, rgba(138, 43, 226, 0.3), rgba(255, 110, 199, 0.3));
            font-weight: 600;
            transform: scale(1.05);
        }

        /* 加载动画 */
        .loading {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 80px;
        }

        .spinner {
            width: 40px;
            height: 40px;
            border: 3px solid rgba(138, 43, 226, 0.3);
            border-radius: 50%;
            border-top-color: var(--primary);
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to {
                transform: rotate(360deg);
            }
        }

        /* 背景模糊效果 */
        .background-blur {
            position: absolute;
            top: 0;
            right: 0;
            width: 40%;
            height: 100%;
            background: rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(5px);
            z-index: -1;
            border-radius: 0 20px 20px 0;
        }

        /* 响应式调整 */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            .album-cover {
                width: 180px;
                height: 180px;
            }
            
            .player-header h1 {
                font-size: 1.6rem;
            }
            
            .music-info h2 {
                font-size: 1.3rem;
            }
            
            .controls {
                gap: 15px;
            }
            
            .control-btn {
                width: 40px;
                height: 40px;
            }
            
            .play-pause {
                width: 55px;
                height: 55px;
            }
            
            .search-container {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 背景模糊效果 -->
        <div class="background-blur"></div>
        
        <!-- 左侧歌曲列表 -->
        <div class="song-list-container">
            <div class="search-container">
                <input type="text" class="search-input" id="search-input" placeholder="搜索歌曲...">
                <select class="platform-select" id="platform-select">
                    <option value="wy">网易云</option>
                    <option value="qq">QQ音乐</option>
                    <option value="kw">酷我音乐</option>
                    <option value="mg">咪咕音乐</option>
                    <option value="qi">千千音乐</option>
                </select>
                <button class="search-btn" id="search-btn">
                    <i class="fas fa-search"></i> 搜索
                </button>
            </div>
            
            <div class="song-list-header">
                <h2>热门榜单</h2>
            </div>
            
            <ul class="song-list" id="song-list">
                <div class="loading">
                    <div class="spinner"></div>
                </div>
            </ul>
            
            <div class="load-more" id="load-more">
                加载更多...
            </div>
        </div>

        <!-- 右侧播放器 -->
        <div class="player-container">
            <div class="player-header">
                <h1>音乐播放器</h1>
                <p>所有功能一目了然</p>
            </div>

            <div class="album-container">
                <div class="album-cover" id="album-cover">
                    <img id="cover" src="https://p1.music.126.net/6y-UleORITEDbvrOLV0Q8A==/5639395138885805.jpg" alt="专辑封面">
                </div>
            </div>

            <div class="music-info">
                <h2 id="title">选择歌曲开始播放</h2>
                <p id="artist">歌手</p>
                <p id="album">专辑</p>
            </div>

            <div class="progress-container">
                <div class="progress-bar" id="progress-bar">
                    <div class="progress" id="progress"></div>
                </div>
                <div class="time-display">
                    <span id="current-time">0:00</span>
                    <span id="duration">0:00</span>
                </div>
            </div>

            <div class="controls">
                <button class="control-btn" id="prev">
                    <i class="fas fa-step-backward"></i>
                </button>
                <button class="control-btn play-pause" id="play">
                    <i class="fas fa-play"></i>
                </button>
                <button class="control-btn" id="next">
                    <i class="fas fa-step-forward"></i>
                </button>
            </div>

            <div class="volume-control">
                <i class="fas fa-volume-up volume-icon"></i>
                <input type="range" class="volume-slider" id="volume" min="0" max="1" step="0.01" value="0.7">
            </div>

            <div class="lyrics-container" id="lyrics">
                <p>歌词加载中...</p>
            </div>

            <audio id="audio"></audio>
        </div>
    </div>

    <script>
        // DOM元素
        const songListEl = document.getElementById('song-list');
        const searchInput = document.getElementById('search-input');
        const platformSelect = document.getElementById('platform-select');
        const searchBtn = document.getElementById('search-btn');
        const loadMoreBtn = document.getElementById('load-more');
        const coverEl = document.getElementById('cover');
        const albumCover = document.getElementById('album-cover');
        const titleEl = document.getElementById('title');
        const artistEl = document.getElementById('artist');
        const albumEl = document.getElementById('album');
        const playBtn = document.getElementById('play');
        const prevBtn = document.getElementById('prev');
        const nextBtn = document.getElementById('next');
        const audioEl = document.getElementById('audio');
        const progressEl = document.getElementById('progress');
        const progressContainerEl = document.getElementById('progress-bar');
        const currentTimeEl = document.getElementById('current-time');
        const durationEl = document.getElementById('duration');
        const volumeSliderEl = document.getElementById('volume');
        const lyricsContainerEl = document.getElementById('lyrics');

        // 状态变量
        let songs = [];
        let currentSongIndex = 0;
        let isPlaying = false;
        let lyrics = [];
        let currentPage = 1;
        let isSearchMode = false;
        let currentSearchQuery = '';
        let currentPlatform = 'wy';

        // 初始化
        function init() {
            fetchHotSongs(8); // 减少初始加载数量以适应屏幕
            bindEvents();
        }

        // 获取热歌榜单
        async function fetchHotSongs(count) {
            try {
                songListEl.innerHTML = '<div class="loading"><div class="spinner"></div></div>';
                
                const response = await fetch(`https://api.jkyai.top/API/qqrgbd.php?count=${count}`);
                const data = await response.json();
                
                if (data.code === 1) {
                    songs = data.data;
                    renderSongList();
                    // 默认加载第一首歌
                    if (songs.length > 0) {
                        loadSong(0);
                    }
                } else {
                    throw new Error(data.msg || '获取歌曲失败');
                }
            } catch (error) {
                songListEl.innerHTML = `<p class="error">加载失败: ${error.message}</p>`;
            }
        }

        // 搜索歌曲
        async function searchSongs(query, platform, page = 1, limit = 8) { // 减少每页数量
            try {
                songListEl.innerHTML = '<div class="loading"><div class="spinner"></div></div>';
                
                const response = await fetch(`https://api.jkyai.top/API/hqyyid.php?name=${encodeURIComponent(query)}&type=${platform}&page=${page}&limit=${limit}`);
                const data = await response.json();
                
                if (data.code === 1) {
                    if (page === 1) {
                        songs = data.data;
                    } else {
                        songs = [...songs, ...data.data];
                    }
                    renderSongList();
                    
                    // 如果有歌曲，加载第一首
                    if (songs.length > 0 && page === 1) {
                        loadSong(0);
                    }
                    
                    // 更新页面状态
                    currentPage = page;
                    currentSearchQuery = query;
                    currentPlatform = platform;
                    isSearchMode = true;
                    
                    // 隐藏或显示加载更多按钮
                    if (data.data.length < limit) {
                        loadMoreBtn.style.display = 'none';
                    } else {
                        loadMoreBtn.style.display = 'block';
                    }
                } else {
                    throw new Error(data.msg || '搜索歌曲失败');
                }
            } catch (error) {
                songListEl.innerHTML = `<p class="error">搜索失败: ${error.message}</p>`;
            }
        }

        // 渲染歌曲列表
        function renderSongList() {
            songListEl.innerHTML = '';
            
            if (songs.length === 0) {
                songListEl.innerHTML = '<p class="no-results">没有找到歌曲</p>';
                return;
            }
            
            songs.forEach((song, index) => {
                const li = document.createElement('li');
                li.className = 'song-item';
                
                // 根据是否是搜索结果显示不同的信息
                if (isSearchMode) {
                    li.innerHTML = `
                        <span class="song-number">${index + 1}</span>
                        <div class="song-info">
                            <div class="song-name">${song.name}</div>
                            <div class="song-artist">${song.artist} - ${song.album}</div>
                        </div>
                    `;
                } else {
                    li.innerHTML = `
                        <span class="song-number">${index + 1}</span>
                        <div class="song-info">
                            <div class="song-name">${song.name}</div>
                            <div class="song-artist">${song.albumname}</div>
                        </div>
                    `;
                }
                
                li.addEventListener('click', () => {
                    loadSong(index);
                });
                
                songListEl.appendChild(li);
            });
        }

        // 加载歌曲
        async function loadSong(index) {
            try {
                // 更新UI状态
                titleEl.textContent = '加载中...';
                artistEl.textContent = '';
                albumEl.textContent = '';
                lyricsContainerEl.innerHTML = '<p>歌词加载中...</p>';
                
                // 高亮当前歌曲
                document.querySelectorAll('.song-item').forEach((item, i) => {
                    if (i === index) {
                        item.classList.add('active');
                    } else {
                        item.classList.remove('active');
                    }
                });
                
                const song = songs[index];
                currentSongIndex = index;
                
                let songId, songType;
                
                if (isSearchMode) {
                    songId = song.id;
                    songType = song.type;
                } else {
                    songId = song.songmid;
                    songType = 'qq';
                }
                
                // 获取歌曲详情
                const response = await fetch(`https://api.jkyai.top/API/yyjhss.php?id=${songId}&type=${songType}`);
                const data = await response.json();
                
                if (data.code === 1) {
                    const songData = data.data;
                    
                    // 更新UI
                    titleEl.textContent = songData.name;
                    artistEl.textContent = songData.artist;
                    albumEl.textContent = songData.album;
                    coverEl.src = songData.pic;
                    
                    // 设置音频源
                    audioEl.src = songData.url;
                    
                    // 解析和显示歌词
                    if (songData.lrc) {
                        lyrics = parseLyrics(songData.lrc);
                        displayLyrics(lyrics);
                    } else {
                        lyricsContainerEl.innerHTML = '<p>暂无歌词</p>';
                    }
                    
                    // 预加载下一首
                    preloadNextSong();
                    
                    // 自动播放
                    audioEl.play()
                        .then(() => {
                            isPlaying = true;
                            playBtn.innerHTML = '<i class="fas fa-pause"></i>';
                            albumCover.classList.add('playing');
                        })
                        .catch(err => {
                            console.log('自动播放失败:', err);
                        });
                } else {
                    throw new Error('获取歌曲详情失败');
                }
            } catch (error) {
                titleEl.textContent = '加载失败';
                lyricsContainerEl.innerHTML = `<p>错误: ${error.message}</p>`;
            }
        }

        // 预加载下一首歌曲
        function preloadNextSong() {
            const nextIndex = (currentSongIndex + 1) % songs.length;
            const nextSong = songs[nextIndex];
            
            if (isSearchMode) {
                // 创建预加载链接
                const preloadLink = document.createElement('link');
                preloadLink.rel = 'prefetch';
                preloadLink.href = `https://api.jkyai.top/API/yyjhss.php?id=${nextSong.id}&type=${nextSong.type}`;
                document.head.appendChild(preloadLink);
            } else {
                // 创建预加载链接
                const preloadLink = document.createElement('link');
                preloadLink.rel = 'prefetch';
                preloadLink.href = `https://api.jkyai.top/API/yyjhss.php?id=${nextSong.songmid}&type=qq`;
                document.head.appendChild(preloadLink);
            }
        }

        // 解析歌词
        function parseLyrics(lrc) {
            const lines = lrc.split('\n');
            const result = [];
            
            lines.forEach(line => {
                const timeMatches = line.match(/\[(\d+):(\d+\.\d+)\]/);
                if (timeMatches) {
                    const minutes = parseFloat(timeMatches[1]);
                    const seconds = parseFloat(timeMatches[2]);
                    const time = minutes * 60 + seconds;
                    
                    const text = line.replace(timeMatches[0], '').trim();
                    if (text) {
                        result.push({ time, text });
                    }
                }
            });
            
            return result;
        }

        // 显示歌词
        function displayLyrics(lyrics) {
            lyricsContainerEl.innerHTML = '';
            
            lyrics.forEach(lyric => {
                const p = document.createElement('p');
                p.className = 'lyric-line';
                p.dataset.time = lyric.time;
                p.textContent = lyric.text;
                lyricsContainerEl.appendChild(p);
            });
        }

        // 更新歌词高亮
        function updateLyricsHighlight(currentTime) {
            const lines = document.querySelectorAll('.lyric-line');
            let activeLine = null;
            
            // 找到当前应该高亮的歌词
            for (let i = lyrics.length - 1; i >= 0; i--) {
                if (currentTime >= lyrics[i].time) {
                    activeLine = i;
                    break;
                }
            }
            
            // 移除所有高亮
            lines.forEach(line => line.classList.remove('active'));
            
            // 添加当前高亮
            if (activeLine !== null && lines[activeLine]) {
                lines[activeLine].classList.add('active');
                
                // 滚动到当前歌词
                lines[activeLine].scrollIntoView({
                    behavior: 'smooth',
                    block: 'center'
                });
            }
        }

        // 格式化时间
        function formatTime(seconds) {
            const mins = Math.floor(seconds / 60);
            const secs = Math.floor(seconds % 60);
            return `${mins}:${secs < 10 ? '0' : ''}${secs}`;
        }

        // 事件绑定
        function bindEvents() {
            // 播放/暂停
            playBtn.addEventListener('click', togglePlay);
            
            // 上一首/下一首
            prevBtn.addEventListener('click', playPrevSong);
            nextBtn.addEventListener('click', playNextSong);
            
            // 进度条
            audioEl.addEventListener('timeupdate', updateProgress);
            progressContainerEl.addEventListener('click', setProgress);
            
            // 音量控制
            volumeSliderEl.addEventListener('input', () => {
                audioEl.volume = volumeSliderEl.value;
            });
            
            // 歌曲结束
            audioEl.addEventListener('ended', playNextSong);
            
            // 搜索按钮
            searchBtn.addEventListener('click', () => {
                const query = searchInput.value.trim();
                const platform = platformSelect.value;
                
                if (query) {
                    searchSongs(query, platform, 1, 8);
                }
            });
            
            // 回车键搜索
            searchInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') {
                    searchBtn.click();
                }
            });
            
            // 加载更多
            loadMoreBtn.addEventListener('click', () => {
                if (isSearchMode) {
                    searchSongs(currentSearchQuery, currentPlatform, currentPage + 1, 8);
                } else {
                    // 对于热门榜单，加载更多歌曲
                    fetchHotSongs(songs.length + 8);
                }
            });
            
            // 无限滚动
            songListEl.addEventListener('scroll', () => {
                const scrollTop = songListEl.scrollTop;
                const scrollHeight = songListEl.scrollHeight;
                const clientHeight = songListEl.clientHeight;
                
                if (scrollTop + clientHeight >= scrollHeight - 10) {
                    loadMoreBtn.click();
                }
            });
        }

        // 播放/暂停切换
        function togglePlay() {
            if (isPlaying) {
                audioEl.pause();
                playBtn.innerHTML = '<i class="fas fa-play"></i>';
                albumCover.classList.remove('playing');
            } else {
                audioEl.play();
                playBtn.innerHTML = '<i class="fas fa-pause"></i>';
                albumCover.classList.add('playing');
            }
            isPlaying = !isPlaying;
        }

        // 播放上一首
        function playPrevSong() {
            currentSongIndex = (currentSongIndex - 1 + songs.length) % songs.length;
            loadSong(currentSongIndex);
        }

        // 播放下一首
        function playNextSong() {
            currentSongIndex = (currentSongIndex + 1) % songs.length;
            loadSong(currentSongIndex);
        }

        // 更新进度条
        function updateProgress() {
            const { currentTime, duration } = audioEl;
            const progressPercent = (currentTime / duration) * 100;
            progressEl.style.width = `${progressPercent}%`;
            
            // 更新时间显示
            currentTimeEl.textContent = formatTime(currentTime);
            durationEl.textcontent = formatTime(duration);
            
            // 更新歌词高亮
            if (lyrics && lyrics.length > 0) {
                updateLyricsHighlight(currentTime);
            }
        }

        // 设置进度
        function setProgress(e) {
            const width = this.clientWidth;
            const clickX = e.offsetX;
            const duration = audioEl.duration;
            audioEl.currentTime = (clickX / width) * duration;
        }

        // 初始化应用
        init();
    </script>
</body>
</html>