# carol
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>【1號 陳明輝】桃園市中寧里里長候選人 - 線上競選總部與管理後台</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Font Noto Sans TC -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700;900&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'campaign-blue': '#1E56A0',
                        'campaign-light-blue': '#D6E4F0',
                        'campaign-orange': '#F6893B',
                        'campaign-warm': '#FDFBF7'
                    },
                    fontFamily: {
                        sans: ['Noto Sans TC', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Noto Sans TC', sans-serif;
            background-color: #FDFBF7;
        }
        .custom-scroll::-webkit-scrollbar {
            width: 6px;
        }
        .custom-scroll::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }
        .custom-scroll::-webkit-scrollbar-thumb {
            background: #F6893B;
            border-radius: 10px;
        }
        .tab-btn.active {
            background-color: #1E56A0;
            color: white;
        }
    </style>
</head>
<body class="text-gray-800 antialiased min-h-screen flex flex-col relative">

    <!-- Top Announcement Bar -->
    <div class="bg-campaign-orange text-white py-2 px-4 text-center font-bold text-sm md:text-base shadow-sm relative z-20">
        <i class="fa-solid fa-heart mr-1 animate-pulse"></i> <span id="display-top-announcement">實體服務處熱情開放中！歡迎里民隨時來作夥喝茶、聊里政！</span>
    </div>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 bg-white/95 backdrop-blur-md shadow-sm border-b border-gray-100">
        <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-3">
                <span class="bg-red-600 text-white font-black text-xl w-9 h-9 rounded-full flex items-center justify-center border-2 border-white shadow">1</span>
                <div>
                    <h1 class="font-bold text-lg md:text-xl text-campaign-blue leading-tight" id="display-candidate-name">陳明輝</h1>
                    <p class="text-xs text-gray-500 font-medium">桃園市中寧里里長候選人</p>
                </div>
            </div>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-6 text-sm font-medium text-gray-700">
                <a href="#hero" class="hover:text-campaign-blue transition">首頁</a>
                <a href="#vision" class="hover:text-campaign-blue transition">政見理念</a>
                <a href="#gallery" class="hover:text-campaign-blue transition">活動紀錄相簿</a>
                <a href="#tea-wall" class="hover:text-campaign-blue transition">線上奉茶許願牆</a>
                <a href="#goods" class="hover:text-campaign-blue transition">競選小物</a>
                <a href="#contact" class="hover:text-campaign-blue transition">服務處資訊</a>
            </nav>

            <div class="flex items-center space-x-2">
                <button onclick="toggleAdminModal()" class="bg-gray-800 hover:bg-gray-900 text-white text-xs md:text-sm font-bold py-2 px-3 rounded-full shadow transition flex items-center space-x-1">
                    <i class="fa-solid fa-gear text-campaign-orange"></i>
                    <span>後台管理</span>
                </button>
                <a href="#tea-wall" class="bg-campaign-orange hover:bg-orange-600 text-white text-xs md:text-sm font-bold py-2 px-3.5 rounded-full shadow transition flex items-center space-x-1">
                    <i class="fa-solid fa-mug-hot"></i>
                    <span class="hidden sm:inline">線上奉茶</span>
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero" class="relative bg-gradient-to-b from-blue-50 to-campaign-warm py-10 md:py-16">
        <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-12 gap-8 items-center">
            
            <!-- Left Info -->
            <div class="md:col-span-7 space-y-5 text-center md:text-left">
                <div class="inline-flex items-center space-x-2 bg-blue-100 text-campaign-blue px-3 py-1 rounded-full text-xs md:text-sm font-bold">
                    <i class="fa-solid fa-house-user"></i>
                    <span id="display-slogan-tag">低調傾聽 ‧ 溫馨服務 ‧ 深耕中寧</span>
                </div>
                
                <h2 class="text-3xl md:text-5xl font-black text-gray-900 leading-tight" id="display-hero-title">
                    把里民當家人<br>
                    <span class="text-campaign-blue">用心打造安心、溫馨的中寧里</span>
                </h2>

                <p class="text-gray-600 text-base md:text-lg leading-relaxed" id="display-hero-desc">
                    親愛的中寧里鄉親好！我是 1 號 陳明輝。競選不需要花俏造勢，最重要的就是把服務做好。歡迎您來到我們的「線上競選總部」，留言許願、線上喝杯茶，我們一起讓社區變得更好！
                </p>

                <!-- Countdown Timer Card -->
                <div class="bg-white p-4 md:p-6 rounded-2xl shadow-md border border-gray-100 max-w-lg mx-auto md:mx-0">
                    <div class="flex items-center justify-between mb-3 border-b pb-2">
                        <span class="font-bold text-gray-700 text-sm md:text-base">
                            <i class="fa-regular fa-calendar-check text-campaign-orange mr-1"></i> 11/28 投票日倒數
                        </span>
                        <span class="text-xs font-semibold bg-red-100 text-red-600 px-2 py-0.5 rounded">挺 1 號 陳明輝</span>
                    </div>
                    <div class="grid grid-cols-4 gap-2 text-center" id="countdown-timer">
                        <div class="bg-blue-50 p-2 rounded-xl">
                            <span id="days" class="block text-2xl md:text-3xl font-black text-campaign-blue">--</span>
                            <span class="text-xs text-gray-500">天</span>
                        </div>
                        <div class="bg-blue-50 p-2 rounded-xl">
                            <span id="hours" class="block text-2xl md:text-3xl font-black text-campaign-blue">--</span>
                            <span class="text-xs text-gray-500">時</span>
                        </div>
                        <div class="bg-blue-50 p-2 rounded-xl">
                            <span id="minutes" class="block text-2xl md:text-3xl font-black text-campaign-blue">--</span>
                            <span class="text-xs text-gray-500">分</span>
                        </div>
                        <div class="bg-blue-50 p-2 rounded-xl">
                            <span id="seconds" class="block text-2xl md:text-3xl font-black text-campaign-blue">--</span>
                            <span class="text-xs text-gray-500">秒</span>
                        </div>
                    </div>
                </div>

                <!-- Call to Action Buttons -->
                <div class="flex flex-wrap gap-4 justify-center md:justify-start pt-2">
                    <a href="#vision" class="bg-campaign-blue hover:bg-blue-800 text-white font-bold px-6 py-3 rounded-xl shadow-md transition flex items-center">
                        查看四大政見 <i class="fa-solid fa-arrow-right ml-2"></i>
                    </a>
                    <a href="#contact" class="bg-white border-2 border-campaign-blue text-campaign-blue hover:bg-blue-50 font-bold px-6 py-3 rounded-xl transition flex items-center">
                        <i class="fa-solid fa-location-dot mr-2"></i> 前往服務處
                    </a>
                </div>
            </div>

            <!-- Right Candidate Avatar Card -->
            <div class="md:col-span-5 flex justify-center">
                <div class="relative max-w-sm w-full bg-white rounded-3xl p-4 shadow-xl border-4 border-white">
                    <div class="absolute -top-4 -left-4 bg-red-600 text-white w-14 h-14 rounded-full flex items-center justify-center font-black text-3xl shadow-lg border-4 border-white z-10">
                        1
                    </div>
                    
                    <div class="overflow-hidden rounded-2xl bg-gray-100 aspect-[4/5] relative">
                        <img id="display-candidate-img" 
                             src="https://placehold.co/400x500/1E56A0/FFFFFF?text=%E9%99%B3%E6%98%8E%E8%BC%9D+%E9%87%8C%E9%95%B7%E5%80%99%E9%81%B8%E4%BA%BA" 
                             alt="陳明輝里長候選人" 
                             class="w-full h-full object-cover">
                    </div>

                    <div class="mt-4 text-center">
                        <h3 class="text-2xl font-black text-gray-800">陳明輝</h3>
                        <p class="text-sm font-semibold text-campaign-orange mt-1" id="display-quote">「一人當選，全家熱忱服務！」</p>
                        <div class="mt-3 flex justify-center space-x-2">
                            <span class="bg-gray-100 text-gray-600 text-xs px-2.5 py-1 rounded-full">親切傾聽</span>
                            <span class="bg-gray-100 text-gray-600 text-xs px-2.5 py-1 rounded-full">在地深耕</span>
                            <span class="bg-gray-100 text-gray-600 text-xs px-2.5 py-1 rounded-full">行動服務</span>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- Vision Section -->
    <section id="vision" class="py-14 bg-white">
        <div class="max-w-6xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-12">
                <span class="text-campaign-orange font-bold text-sm uppercase tracking-wider">Four Core Commitments</span>
                <h2 class="text-3xl font-black text-gray-900 mt-1">【服務理念與四大政見】</h2>
                <p class="text-gray-500 mt-2">不造作、不做作，用最實在的行動改善中寧里的每一個小細節</p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6" id="display-policies-container">
                <!-- Dynamic Policies rendered by JS -->
            </div>
        </div>
    </section>

    <!-- Activity Gallery Section (New feature controlled by CMS) -->
    <section id="gallery" class="py-14 bg-gray-50 border-y border-gray-100">
        <div class="max-w-6xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-10">
                <span class="text-campaign-orange font-bold text-sm uppercase">Community Gallery</span>
                <h2 class="text-3xl font-black text-gray-900 mt-1">【服務紀錄與鄰里活動牆】</h2>
                <p class="text-gray-500 mt-2">記錄服務處日常、環境清潔、長者關懷與社區點滴</p>
            </div>

            <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-6" id="display-gallery-container">
                <!-- Dynamic Photo Album rendered by JS -->
            </div>
        </div>
    </section>

    <!-- Tea & Wish Wall Interactive Section -->
    <section id="tea-wall" class="py-14 bg-gradient-to-b from-campaign-warm to-blue-50">
        <div class="max-w-6xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-10">
                <span class="text-campaign-orange font-bold text-sm uppercase">Interactive Zone</span>
                <h2 class="text-3xl font-black text-gray-900 mt-1">【線上奉茶與里民許願牆】</h2>
                <p class="text-gray-600 mt-2">人沒到沒關係，線上為陳明輝喝杯茶打打氣，或是留下您的心願建議！</p>
            </div>

            <div class="grid lg:grid-cols-12 gap-8 items-start">
                
                <!-- Left: Virtual Tea Counter -->
                <div class="lg:col-span-5 bg-white p-6 md:p-8 rounded-3xl shadow-lg border border-gray-100 text-center">
                    <div class="inline-block p-4 bg-orange-50 rounded-full text-campaign-orange mb-4">
                        <i class="fa-solid fa-mug-hot text-5xl"></i>
                    </div>
                    
                    <h3 class="text-2xl font-bold text-gray-800">作夥來泡茶打氣！</h3>
                    <p class="text-gray-500 text-sm mt-1">每一杯茶都是對明輝的一份支持與信任</p>

                    <div class="my-6 bg-blue-50 py-4 px-6 rounded-2xl">
                        <p class="text-xs text-gray-500 font-medium">目前已收到線上奉茶</p>
                        <span id="tea-count" class="text-4xl md:text-5xl font-black text-campaign-blue">1,288</span>
                        <span class="text-gray-600 font-bold ml-1">杯</span>
                    </div>

                    <button id="btn-pour-tea" onclick="pourTea()" class="w-full bg-campaign-orange hover:bg-orange-600 active:scale-95 text-white font-bold py-3.5 px-6 rounded-xl shadow-md transition flex items-center justify-center space-x-2 text-lg">
                        <i class="fa-solid fa-hand-holding-hand"></i>
                        <span>按一下：線上奉茶打氣！</span>
                    </button>
                    <p class="text-xs text-gray-400 mt-2">點擊按鈕即可為陳明輝增加人氣</p>
                </div>

                <!-- Right: Wish & Message Wall -->
                <div class="lg:col-span-7 bg-white p-6 md:p-8 rounded-3xl shadow-lg border border-gray-100">
                    <h3 class="text-xl font-bold text-gray-800 mb-4 flex items-center justify-between">
                        <span><i class="fa-solid fa-comment-dots text-campaign-blue mr-2"></i>里民加油與許願牆</span>
                        <span class="text-xs font-normal text-gray-400">實時留言</span>
                    </h3>

                    <!-- Message Form -->
                    <form id="wish-form" onsubmit="submitWish(event)" class="mb-6 space-y-3">
                        <div class="grid grid-cols-2 gap-3">
                            <input type="text" id="user-name" placeholder="您的稱呼 (例：陳太太)" required class="w-full p-2.5 text-sm border border-gray-200 rounded-xl focus:outline-none focus:ring-2 focus:ring-campaign-blue">
                            <select id="user-location" class="w-full p-2.5 text-sm border border-gray-200 rounded-xl focus:outline-none focus:ring-2 focus:ring-campaign-blue">
                                <option value="中寧里鄉親">中寧里鄉親</option>
                                <option value="鄰近好朋友">鄰近好朋友</option>
                                <option value="志工夥伴">志工夥伴</option>
                            </select>
                        </div>
                        <textarea id="user-msg" placeholder="寫下給陳明輝的加油語，或是對中寧里的許願建議..." required rows="2" class="w-full p-2.5 text-sm border border-gray-200 rounded-xl focus:outline-none focus:ring-2 focus:ring-campaign-blue"></textarea>
                        <button type="submit" class="w-full bg-campaign-blue hover:bg-blue-800 text-white font-bold py-2.5 rounded-xl text-sm transition">
                            貼上許願貼紙 <i class="fa-solid fa-paper-plane ml-1"></i>
                        </button>
                    </form>

                    <!-- Message Feed -->
                    <div id="wish-list" class="space-y-3 max-h-72 overflow-y-auto custom-scroll pr-1">
                        <!-- Rendered by JS -->
                    </div>
                </div>

            </div>

        </div>
    </section>

    <!-- Campaign Goods Section -->
    <section id="goods" class="py-14 bg-white">
        <div class="max-w-6xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-12">
                <span class="text-campaign-orange font-bold text-sm uppercase">Practical Gifts</span>
                <h2 class="text-3xl font-black text-gray-900 mt-1">【競選實用小物與服務處設施】</h2>
                <p class="text-gray-500 mt-2">不鋪張浪費，只送里民最用得到的實用生活好物！</p>
            </div>

            <div class="grid md:grid-cols-3 gap-6" id="display-goods-container">
                <!-- Rendered dynamically by JS -->
            </div>
        </div>
    </section>

    <!-- Contact & Service Location Info -->
    <section id="contact" class="py-14 bg-gray-900 text-white">
        <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-10 items-center">
            
            <div class="space-y-4">
                <span class="bg-campaign-orange text-white text-xs font-bold px-3 py-1 rounded-full">實體服務據點</span>
                <h2 class="text-3xl font-black">歡迎隨時來「中寧里服務處」坐坐</h2>
                <p class="text-gray-400 text-sm leading-relaxed" id="display-office-desc">
                    我們沒有吵雜的造勢喇叭，只有親切的茶香味與熱情的問候。無論是社區建議、服務需求，都歡迎您蒞臨指教！
                </p>

                <div class="space-y-3 pt-2 text-sm text-gray-300">
                    <div class="flex items-start space-x-3">
                        <i class="fa-solid fa-location-dot text-campaign-orange mt-1"></i>
                        <span><strong>地址：</strong><span id="display-office-addr">桃園市桃園區中寧里服務處 (中正路巷內)</span></span>
                    </div>
                    <div class="flex items-start space-x-3">
                        <i class="fa-solid fa-clock text-campaign-orange mt-1"></i>
                        <span><strong>開放時間：</strong><span id="display-office-hours">每日 08:30 - 20:30 (免費奉茶)</span></span>
                    </div>
                    <div class="flex items-start space-x-3">
                        <i class="fa-solid fa-phone text-campaign-orange mt-1"></i>
                        <span><strong>服務熱線：</strong><span id="display-office-phone">歡迎直接親臨或透過 LINE 聯絡</span></span>
                    </div>
                </div>

                <div class="pt-4">
                    <button onclick="copyLineId()" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-xl shadow transition flex items-center space-x-2 text-sm">
                        <i class="fa-brands fa-line text-xl"></i>
                        <span>加入 1號陳明輝 LINE 官方服務</span>
                    </button>
                    <p id="copy-msg" class="text-xs text-green-400 mt-2 hidden">✓ 已複製 LINE 搜尋資訊！</p>
                </div>
            </div>

            <!-- Service Center Photo -->
            <div class="bg-gray-800 p-4 rounded-3xl border border-gray-700 text-center">
                <div class="overflow-hidden rounded-2xl bg-gray-700 aspect-[4/3] relative mb-3">
                    <img id="display-office-img" 
                         src="https://placehold.co/600x450/1E56A0/FFFFFF?text=%E4%B8%AD%E5%AF%A7%E9%87%8C%E6%9C%8D%E5%8B%99%E8%99%95+%E6%BA%AB%E9%A6%A9%E5%A5%89%E8%8C%B6" 
                         alt="服務處照片" 
                         class="w-full h-full object-cover">
                </div>
                <p class="text-xs text-gray-400">溫馨服務處現場 ‧ 歡迎鄉親隨時作夥來泡茶</p>
            </div>

        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 text-gray-500 text-xs py-6 text-center border-t border-gray-800">
        <div class="max-w-6xl mx-auto px-4 space-y-1">
            <p>1號 桃園市中寧里里長候選人 陳明輝 競選籌備辦公室 版權所有</p>
            <p>11/28(六) 請投票支持 1號 陳明輝 ‧ 共同打造溫馨中寧里</p>
        </div>
    </footer>


    <!-- ========================================== -->
    <!-- ADMIN CMS MODAL (後台內容管理面板) -->
    <!-- ========================================== -->
    <div id="admin-modal" class="fixed inset-0 bg-black/70 z-50 flex items-center justify-center p-3 md:p-6 hidden">
        <div class="bg-white rounded-3xl max-w-4xl w-full max-h-[90vh] flex flex-col shadow-2xl overflow-hidden">
            
            <!-- Modal Header -->
            <div class="bg-gray-900 text-white px-6 py-4 flex justify-between items-center border-b border-gray-800">
                <div class="flex items-center space-x-2">
                    <i class="fa-solid fa-sliders text-campaign-orange text-lg"></i>
                    <h3 class="font-bold text-lg">網站內容更新後台 (CMS Dashboard)</h3>
                    <span class="text-xs bg-campaign-orange text-white px-2 py-0.5 rounded font-mono">Live Sync</span>
                </div>
                <button onclick="toggleAdminModal()" class="text-gray-400 hover:text-white text-xl">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <!-- Tabs Navigation -->
            <div class="bg-gray-100 px-6 pt-3 flex space-x-2 border-b border-gray-200 overflow-x-auto text-xs md:text-sm">
                <button onclick="switchTab('tab-photos')" id="btn-tab-photos" class="tab-btn active px-4 py-2.5 rounded-t-xl font-bold transition">照片圖片管理</button>
                <button onclick="switchTab('tab-texts')" id="btn-tab-texts" class="tab-btn px-4 py-2.5 rounded-t-xl font-bold transition text-gray-600 hover:bg-gray-200">文字與政見</button>
                <button onclick="switchTab('tab-wishes')" id="btn-tab-wishes" class="tab-btn px-4 py-2.5 rounded-t-xl font-bold transition text-gray-600 hover:bg-gray-200">留言審核</button>
                <button onclick="switchTab('tab-goods')" id="btn-tab-goods" class="tab-btn px-4 py-2.5 rounded-t-xl font-bold transition text-gray-600 hover:bg-gray-200">競選小物</button>
            </div>

            <!-- Modal Content Scroll Body -->
            <div class="p-6 overflow-y-auto custom-scroll flex-1 space-y-6">
                
                <!-- TAB 1: PHOTO MANAGER -->
                <div id="tab-photos" class="tab-content space-y-6">
                    <div class="bg-blue-50 p-4 rounded-xl border border-blue-100 text-xs text-blue-800">
                        <i class="fa-solid fa-circle-info mr-1"></i> 您可以上傳檔案或貼上圖片網址來更新候選人相片、服務處環境照以及社區活動記錄相簿。
                    </div>

                    <!-- 1. Key Photos Update -->
                    <div class="grid md:grid-cols-2 gap-6">
                        <!-- Candidate Photo -->
                        <div class="border p-4 rounded-2xl bg-gray-50 space-y-3">
                            <h4 class="font-bold text-sm text-gray-800"><i class="fa-solid fa-user-tie text-campaign-blue mr-1"></i> 候選人主視覺照</h4>
                            <div class="h-36 bg-gray-200 rounded-xl overflow-hidden relative">
                                <img id="preview-candidate-img" src="" class="w-full h-full object-cover">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-600 mb-1">上傳圖檔或輸入網址：</label>
                                <input type="file" accept="image/*" onchange="handleFileUpload(event, 'candidateImg')" class="text-xs mb-2 w-full">
                                <input type="text" id="input-candidate-img" placeholder="或貼上圖片 URL" onchange="updatePhotoFromUrl('candidateImg', this.value)" class="w-full text-xs p-2 border rounded-lg">
                            </div>
                        </div>

                        <!-- Office Photo -->
                        <div class="border p-4 rounded-2xl bg-gray-50 space-y-3">
                            <h4 class="font-bold text-sm text-gray-800"><i class="fa-solid fa-building text-campaign-orange mr-1"></i> 服務處現場照</h4>
                            <div class="h-36 bg-gray-200 rounded-xl overflow-hidden relative">
                                <img id="preview-office-img" src="" class="w-full h-full object-cover">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-600 mb-1">上傳圖檔或輸入網址：</label>
                                <input type="file" accept="image/*" onchange="handleFileUpload(event, 'officeImg')" class="text-xs mb-2 w-full">
                                <input type="text" id="input-office-img" placeholder="或貼上圖片 URL" onchange="updatePhotoFromUrl('officeImg', this.value)" class="w-full text-xs p-2 border rounded-lg">
                            </div>
                        </div>
                    </div>

                    <!-- 2. Community Gallery Manager -->
                    <div class="border p-4 rounded-2xl bg-gray-50 space-y-4">
                        <h4 class="font-bold text-sm text-gray-800 flex justify-between items-center">
                            <span><i class="fa-solid fa-images text-green-600 mr-1"></i> 社區活動相簿管理</span>
                        </h4>
                        
                        <!-- Add Photo to Gallery -->
                        <div class="bg-white p-3 rounded-xl border grid md:grid-cols-3 gap-2 items-end">
                            <div>
                                <label class="block text-xs font-bold text-gray-600 mb-1">照片描述</label>
                                <input type="text" id="new-photo-title" placeholder="例如：里內環境大掃除" class="w-full text-xs p-2 border rounded-lg">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-600 mb-1">圖片檔案 / URL</label>
                                <input type="text" id="new-photo-url" placeholder="貼上網址或上傳" class="w-full text-xs p-2 border rounded-lg mb-1">
                                <input type="file" accept="image/*" onchange="handleGalleryUpload(event)" class="text-xs">
                            </div>
                            <button onclick="addGalleryPhoto()" class="bg-campaign-blue text-white text-xs font-bold py-2 px-4 rounded-lg hover:bg-blue-800">
                                <i class="fa-solid fa-plus mr-1"></i> 新增至相簿
                            </button>
                        </div>

                        <!-- Gallery Items List -->
                        <div class="grid grid-cols-2 md:grid-cols-4 gap-3" id="admin-gallery-list">
                            <!-- Rendered by JS -->
                        </div>
                    </div>
                </div>

                <!-- TAB 2: TEXT & POLICIES -->
                <div id="tab-texts" class="tab-content hidden space-y-6">
                    <div class="border p-4 rounded-2xl bg-gray-50 space-y-3">
                        <h4 class="font-bold text-sm text-gray-800">廣播與首頁宣示語</h4>
                        <div class="grid gap-3 text-xs">
                            <div>
                                <label class="block font-bold text-gray-600 mb-1">頂部橫幅跑馬燈訊息：</label>
                                <input type="text" id="input-top-announcement" class="w-full p-2 border rounded-lg">
                            </div>
                            <div>
                                <label class="block font-bold text-gray-600 mb-1">首頁競選主標題：</label>
                                <input type="text" id="input-hero-title" class="w-full p-2 border rounded-lg">
                            </div>
                            <div>
                                <label class="block font-bold text-gray-600 mb-1">服務處地址：</label>
                                <input type="text" id="input-office-addr" class="w-full p-2 border rounded-lg">
                            </div>
                            <div>
                                <label class="block font-bold text-gray-600 mb-1">開放時間：</label>
                                <input type="text" id="input-office-hours" class="w-full p-2 border rounded-lg">
                            </div>
                            <div>
                                <label class="block font-bold text-gray-600 mb-1">候選人精神標語 (Quote)：</label>
                                <input type="text" id="input-quote" class="w-full p-2 border rounded-lg">
                            </div>
                            <div>
                                <label class="block font-bold text-gray-600 mb-1">簡介說明文字：</label>
                                <textarea id="input-hero-desc" rows="2" class="w-full p-2 border rounded-lg"></textarea>
                            </div>
                        </div>
                    </div>

                    <!-- Four Policies Editor -->
                    <div class="border p-4 rounded-2xl bg-gray-50 space-y-4">
                        <h4 class="font-bold text-sm text-gray-800">四大政見編輯器</h4>
                        <div class="grid md:grid-cols-2 gap-4" id="admin-policies-list">
                            <!-- Rendered by JS -->
                        </div>
                    </div>
                </div>

                <!-- TAB 3: WISHES / GUESTBOOK ADMIN -->
                <div id="tab-wishes" class="tab-content hidden space-y-4">
                    <div class="flex justify-between items-center">
                        <h4 class="font-bold text-sm text-gray-800">里民留言列表與審核</h4>
                        <span class="text-xs text-gray-500">可在後台刪除不當留言</span>
                    </div>

                    <div class="space-y-3 max-h-96 overflow-y-auto" id="admin-wishes-list">
                        <!-- Rendered by JS -->
                    </div>
                </div>

                <!-- TAB 4: SWAG / GOODS MANAGER -->
                <div id="tab-goods" class="tab-content hidden space-y-4">
                    <h4 class="font-bold text-sm text-gray-800">競選小物與招待設施管理</h4>
                    <div class="space-y-3" id="admin-goods-list">
                        <!-- Rendered by JS -->
                    </div>
                </div>

            </div>

            <!-- Modal Footer -->
            <div class="bg-gray-100 px-6 py-4 flex justify-between items-center border-t border-gray-200">
                <button onclick="resetToDefaultData()" class="text-xs text-red-600 hover:underline font-bold">
                    <i class="fa-solid fa-rotate-left mr-1"></i> 重置所有內容至初始預設
                </button>
                <div class="flex space-x-3">
                    <button onclick="toggleAdminModal()" class="bg-gray-200 hover:bg-gray-300 text-gray-700 text-xs font-bold py-2.5 px-5 rounded-xl transition">
                        關閉面板
                    </button>
                    <button onclick="saveAdminChanges()" class="bg-campaign-blue hover:bg-blue-800 text-white text-xs font-bold py-2.5 px-5 rounded-xl shadow transition">
                        <i class="fa-solid fa-floppy-disk mr-1"></i> 儲存並發布更新
                    </button>
                </div>
            </div>

        </div>
    </div>

    <!-- JavaScript Logic & CMS Data Controller -->
    <script>
        // Real upload photos provided by user
        const USER_PHOTO_SERVICE = "S__40476678_0.jpg"; // Medical & Service center
        const USER_PHOTO_DOCTOR  = "S__40476679_0.jpg"; // Candidate with Doctor
        const USER_PHOTO_SWEEP1  = "S__40476680_0.jpg"; // Environmental sweep banner
        const USER_PHOTO_SWEEP2  = "S__40476681_0.jpg"; // Candidate discussing with residents
        const USER_PHOTO_SWEEP3  = "S__40476682_0.jpg"; // Candidate giving briefing to sweep team

        // -------------------------------------------------------------
        // DEFAULT INITIAL DATA STORE
        // -------------------------------------------------------------
        const DEFAULT_DATA = {
            candidateName: "陳明輝",
            sloganTag: "低調傾聽 ‧ 溫馨服務 ‧ 深耕中寧",
            topAnnouncement: "實體服務處熱情開放中！歡迎里民隨時來作夥喝茶、聊里政！",
            heroTitle: "把里民當家人，用心打造安心、溫馨的中寧里",
            heroDesc: "親愛的中寧里鄉親好！我是 1 號 陳明輝。競選不需要花俏造勢，最重要的就是把服務做好。歡迎您來到我們的「線上競選總部」，留言許願、線上喝杯茶，我們一起讓社區變得更好！",
            candidateQuote: "「一人當選，全家熱忱服務！」",
            candidateImg: USER_PHOTO_DOCTOR,
            officeImg: USER_PHOTO_SERVICE,
            officeDesc: "我們沒有吵雜的造勢喇叭，只有親切的茶香味與熱情的問候。無論是社區建議、服務需求，都歡迎您蒞臨指教！",
            officeAddr: "桃園市桃園區大興西路二段69巷5號",
            officeHours: "每日 09:30 - 12:30 (免費奉茶)",
            officePhone: "歡迎親臨服務處或加 LINE 洽詢",
            teaCount: 1288,
            policies: [
                { icon: "fa-broom", title: "環境清潔與整頓", desc: "定期巡視清理巷弄積水與水溝，辦理環境大掃除，確保里內通風乾淨無死角。" },
                { icon: "fa-hand-holding-heart", title: "長者關懷與奉茶", desc: "服務處長期設置養生奉茶區，推動銀髮族健康講座、定期關懷獨居長者健康。" },
                { icon: "fa-shield-halved", title: "社區巡守與安全", desc: "強化夜間巷弄照明，爭取監視器維護升級，組織志工巡守隊保障婦幼安全。" },
                { icon: "fa-comments", title: "數位里政與溝通", desc: "建立 LINE 官方帳號通報機制，停水停電或社區公告即時通知，處理零時差。" }
            ],
            gallery: [
                { id: 1, title: "輝哥里長環保日：志工隊清掃街道", url: USER_PHOTO_SWEEP1 },
                { id: 2, title: "出勤前里長親自為環保志工做說明與集氣", url: USER_PHOTO_SWEEP3 },
                { id: 3, title: "社區流感疫苗免費接種與義診現場關懷", url: USER_PHOTO_DOCTOR },
                { id: 4, title: "服務處現場熱心關懷鄉親健康", url: USER_PHOTO_SWEEP2 },
                { id: 5, title: "服務處溫馨熱鬧的長者茶話與諮詢現場", url: USER_PHOTO_SERVICE }
            ],
            goods: [
                { icon: "fa-box-tissue", title: "客製袖珍包衛生紙", tag: "好評發放中", tagColor: "bg-blue-100 text-campaign-blue", desc: "外出攜帶最方便，背面印有服務處電話與政見。" },
                { icon: "fa-note-sticky", title: "政見名片與便條紙", tag: "實用好物", tagColor: "bg-orange-100 text-campaign-orange", desc: "隨手記錄事項，附有明輝的 Line 官方帳號 QR code。" },
                { icon: "fa-mug-saucer", title: "熱情養生茶桶奉茶", tag: "服務處專屬", tagColor: "bg-green-100 text-green-600", desc: "服務處現場每日準備熱茶與古早味餅乾招待里民。" }
            ],
            wishes: [
                { id: 1, name: "張大姐", location: "中寧里鄉親", time: "10分鐘前", msg: "加油！陳大哥平時就很熱心幫忙社區水溝清潔，這次一定支持 1 號！" },
                { id: 2, name: "李先生", location: "鄰近好朋友", time: "1小時前", msg: "希望當選後可以多辦幾場銀髮族健康講座與奉茶活動！1號加油！" },
                { id: 3, name: "王小弟媽媽", location: "中寧里鄉親", time: "3小時前", msg: "收到競選小物的袖珍衛生紙跟菜瓜布超實用！明輝哥加油！" }
            ]
        };

        // App State loaded from LocalStorage or default
        let appState = JSON.parse(localStorage.getItem('chen_campaign_cms_data')) || DEFAULT_DATA;
        
        // Ensure old stored cached imagery gets refreshed if it holds fallback URL
        if (appState.gallery && appState.gallery[0] && appState.gallery[0].url.includes('unsplash.com')) {
            appState = DEFAULT_DATA;
            localStorage.setItem('chen_campaign_cms_data', JSON.stringify(appState));
        }

        // -------------------------------------------------------------
        // RENDER FRONTEND PORTAL
        // -------------------------------------------------------------
        function renderFrontend() {
            document.getElementById('display-candidate-name').innerText = appState.candidateName;
            document.getElementById('display-slogan-tag').innerText = appState.sloganTag;
            document.getElementById('display-top-announcement').innerText = appState.topAnnouncement;
            document.getElementById('display-hero-title').innerText = appState.heroTitle;
            document.getElementById('display-hero-desc').innerText = appState.heroDesc;
            document.getElementById('display-quote').innerText = appState.candidateQuote;

            // Photos
            document.getElementById('display-candidate-img').src = appState.candidateImg;
            document.getElementById('display-office-img').src = appState.officeImg;

            // Office info
            document.getElementById('display-office-desc').innerText = appState.officeDesc;
            document.getElementById('display-office-addr').innerText = appState.officeAddr;
            document.getElementById('display-office-hours').innerText = appState.officeHours;
            document.getElementById('display-office-phone').innerText = appState.officePhone;
            document.getElementById('tea-count').innerText = Number(appState.teaCount).toLocaleString();

            // Render Policies
            const policiesContainer = document.getElementById('display-policies-container');
            policiesContainer.innerHTML = appState.policies.map(p => `
                <div class="bg-gray-50 p-6 rounded-2xl border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 bg-blue-100 text-campaign-blue rounded-xl flex items-center justify-center text-xl font-bold mb-4">
                        <i class="fa-solid ${p.icon}"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-2">${escapeHtml(p.title)}</h3>
                    <p class="text-gray-600 text-sm leading-relaxed">${escapeHtml(p.desc)}</p>
                </div>
            `).join('');

            // Render Photo Gallery
            const galleryContainer = document.getElementById('display-gallery-container');
            if (galleryContainer) {
                galleryContainer.innerHTML = appState.gallery.map(g => `
                    <div class="bg-white rounded-2xl overflow-hidden shadow-sm border border-gray-100 group">
                        <div class="h-56 overflow-hidden bg-gray-100">
                            <img src="${g.url}" alt="${escapeHtml(g.title)}" class="w-full h-full object-cover group-hover:scale-105 transition duration-300">
                        </div>
                        <div class="p-4">
                            <h4 class="font-bold text-gray-800 text-sm">${escapeHtml(g.title)}</h4>
                        </div>
                    </div>
                `).join('');
            }

            // Wishes Feed
            renderWishesFeed();

            // Goods Items
            const goodsContainer = document.getElementById('display-goods-container');
            goodsContainer.innerHTML = appState.goods.map(g => `
                <div class="border border-gray-100 rounded-2xl p-5 bg-campaign-warm hover:shadow-md transition">
                    <div class="w-full h-40 bg-blue-50 rounded-xl mb-4 flex items-center justify-center text-campaign-blue text-4xl">
                        <i class="fa-solid ${g.icon}"></i>
                    </div>
                    <span class="${g.tagColor || 'bg-blue-100 text-campaign-blue'} text-xs font-bold px-2.5 py-1 rounded-full">${escapeHtml(g.tag)}</span>
                    <h3 class="text-lg font-bold text-gray-800 mt-2">${escapeHtml(g.title)}</h3>
                    <p class="text-xs text-gray-500 mt-1">${escapeHtml(g.desc)}</p>
                </div>
            `).join('');
        }

        function renderWishesFeed() {
            const list = document.getElementById('wish-list');
            list.innerHTML = appState.wishes.map(w => `
                <div class="bg-yellow-50 p-3.5 rounded-2xl border border-yellow-100 text-xs md:text-sm">
                    <div class="flex justify-between items-center mb-1">
                        <span class="font-bold text-gray-800">${escapeHtml(w.name)} <span class="text-xs text-gray-400 font-normal">(${escapeHtml(w.location)})</span></span>
                        <span class="text-xs text-gray-400">${escapeHtml(w.time)}</span>
                    </div>
                    <p class="text-gray-700">${escapeHtml(w.msg)}</p>
                </div>
            `).join('');
        }

        // -------------------------------------------------------------
        // ADMIN DASHBOARD CONTROLLER
        // -------------------------------------------------------------
        function toggleAdminModal() {
            const modal = document.getElementById('admin-modal');
            modal.classList.toggle('hidden');
            if (!modal.classList.contains('hidden')) {
                populateAdminInputs();
            }
        }

        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(el => el.classList.add('hidden'));
            document.querySelectorAll('.tab-btn').forEach(el => {
                el.classList.remove('active');
                el.classList.add('text-gray-600');
            });

            document.getElementById(tabId).classList.remove('hidden');
            const activeBtn = document.getElementById('btn-' + tabId);
            activeBtn.classList.add('active');
            activeBtn.classList.remove('text-gray-600');
        }

        function populateAdminInputs() {
            // Photos
            document.getElementById('preview-candidate-img').src = appState.candidateImg;
            document.getElementById('input-candidate-img').value = appState.candidateImg;

            document.getElementById('preview-office-img').src = appState.officeImg;
            document.getElementById('input-office-img').value = appState.officeImg;

            // Admin Gallery List
            renderAdminGalleryList();

            // Text Inputs
            document.getElementById('input-top-announcement').value = appState.topAnnouncement;
            document.getElementById('input-hero-title').value = appState.heroTitle;
            document.getElementById('input-office-addr').value = appState.officeAddr;
            document.getElementById('input-office-hours').value = appState.officeHours;
            document.getElementById('input-quote').value = appState.candidateQuote;
            document.getElementById('input-hero-desc').value = appState.heroDesc;

            // Policies Editor
            const polList = document.getElementById('admin-policies-list');
            polList.innerHTML = appState.policies.map((p, idx) => `
                <div class="bg-white p-3 border rounded-xl space-y-2">
                    <span class="font-bold text-xs text-campaign-blue">政見 ${idx + 1}</span>
                    <input type="text" id="pol-title-${idx}" value="${escapeHtml(p.title)}" class="w-full text-xs p-2 border rounded font-bold">
                    <textarea id="pol-desc-${idx}" rows="2" class="w-full text-xs p-2 border rounded">${escapeHtml(p.desc)}</textarea>
                </div>
            `).join('');

            // Admin Wishes List
            const wishesAdmin = document.getElementById('admin-wishes-list');
            wishesAdmin.innerHTML = appState.wishes.map(w => `
                <div class="bg-white p-3 border rounded-xl flex justify-between items-center text-xs">
                    <div>
                        <span class="font-bold text-gray-800">${escapeHtml(w.name)}</span>
                        <span class="text-gray-400"> (${escapeHtml(w.location)})</span>
                        <p class="text-gray-600 mt-1">${escapeHtml(w.msg)}</p>
                    </div>
                    <button onclick="deleteWish(${w.id})" class="text-red-500 hover:text-red-700 font-bold px-2 py-1">
                        <i class="fa-solid fa-trash-can"></i>
                    </button>
                </div>
            `).join('');

            // Admin Goods List
            const goodsAdmin = document.getElementById('admin-goods-list');
            goodsAdmin.innerHTML = appState.goods.map((g, idx) => `
                <div class="bg-white p-3 border rounded-xl grid md:grid-cols-3 gap-2 text-xs">
                    <input type="text" id="good-title-${idx}" value="${escapeHtml(g.title)}" class="p-2 border rounded font-bold">
                    <input type="text" id="good-tag-${idx}" value="${escapeHtml(g.tag)}" class="p-2 border rounded">
                    <input type="text" id="good-desc-${idx}" value="${escapeHtml(g.desc)}" class="p-2 border rounded">
                </div>
            `).join('');
        }

        // File Upload Handlers (Base64)
        function handleFileUpload(event, targetKey) {
            const file = event.target.files[0];
            if (!file) return;

            const reader = new FileReader();
            reader.onload = function(e) {
                const base64Url = e.target.result;
                appState[targetKey] = base64Url;
                if (targetKey === 'candidateImg') {
                    document.getElementById('preview-candidate-img').src = base64Url;
                    document.getElementById('input-candidate-img').value = '';
                } else if (targetKey === 'officeImg') {
                    document.getElementById('preview-office-img').src = base64Url;
                    document.getElementById('input-office-img').value = '';
                }
            };
            reader.readAsDataURL(file);
        }

        function updatePhotoFromUrl(targetKey, url) {
            if (!url) return;
            appState[targetKey] = url;
            if (targetKey === 'candidateImg') document.getElementById('preview-candidate-img').src = url;
            if (targetKey === 'officeImg') document.getElementById('preview-office-img').src = url;
        }

        // Gallery Admin Actions
        let pendingGalleryBase64 = '';
        function handleGalleryUpload(e) {
            const file = e.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = function(ev) {
                pendingGalleryBase64 = ev.target.result;
                document.getElementById('new-photo-url').value = "(本地檔案已就緒)";
            }
            reader.readAsDataURL(file);
        }

        function addGalleryPhoto() {
            const titleInput = document.getElementById('new-photo-title');
            const urlInput = document.getElementById('new-photo-url');
            
            const title = titleInput.value.trim() || '服務現場紀錄';
            const url = pendingGalleryBase64 || urlInput.value.trim();

            if (!url) {
                alert('請上傳照片或輸入網址！');
                return;
            }

            appState.gallery.unshift({
                id: Date.now(),
                title: title,
                url: url
            });

            pendingGalleryBase64 = '';
            titleInput.value = '';
            urlInput.value = '';
            renderAdminGalleryList();
        }

        function removeGalleryPhoto(id) {
            appState.gallery = appState.gallery.filter(item => item.id !== id);
            renderAdminGalleryList();
        }

        function renderAdminGalleryList() {
            const list = document.getElementById('admin-gallery-list');
            list.innerHTML = appState.gallery.map(item => `
                <div class="relative bg-white border rounded-xl overflow-hidden p-1 text-center">
                    <img src="${item.url}" class="h-20 w-full object-cover rounded-lg">
                    <p class="text-[10px] font-bold truncate mt-1">${escapeHtml(item.title)}</p>
                    <button onclick="removeGalleryPhoto(${item.id})" class="absolute top-2 right-2 bg-red-600 text-white w-5 h-5 rounded-full text-xs flex items-center justify-center shadow">
                        ✕
                    </button>
                </div>
            `).join('');
        }

        function deleteWish(id) {
            appState.wishes = appState.wishes.filter(w => w.id !== id);
            populateAdminInputs();
        }

        // Save Admin Data & Sync Front-end
        function saveAdminChanges() {
            // Save Texts
            appState.topAnnouncement = document.getElementById('input-top-announcement').value;
            appState.heroTitle = document.getElementById('input-hero-title').value;
            appState.officeAddr = document.getElementById('input-office-addr').value;
            appState.officeHours = document.getElementById('input-office-hours').value;
            appState.candidateQuote = document.getElementById('input-quote').value;
            appState.heroDesc = document.getElementById('input-hero-desc').value;

            // Save Policies
            appState.policies.forEach((p, idx) => {
                const titleEl = document.getElementById(`pol-title-${idx}`);
                const descEl = document.getElementById(`pol-desc-${idx}`);
                if (titleEl) p.title = titleEl.value;
                if (descEl) p.desc = descEl.value;
            });

            // Save Goods
            appState.goods.forEach((g, idx) => {
                const titleEl = document.getElementById(`good-title-${idx}`);
                const tagEl = document.getElementById(`good-tag-${idx}`);
                const descEl = document.getElementById(`good-desc-${idx}`);
                if (titleEl) g.title = titleEl.value;
                if (tagEl) g.tag = tagEl.value;
                if (descEl) g.desc = descEl.value;
            });

            // Persist to LocalStorage
            localStorage.setItem('chen_campaign_cms_data', JSON.stringify(appState));
            
            // Re-render Portal
            renderFrontend();
            toggleAdminModal();

            // Simple Notification toast
            showToast("網站內容已成功發布並更新！");
        }

        function resetToDefaultData() {
            if (confirm("確定要將所有內容恢復為初始預設值嗎？此動作無法復原。")) {
                appState = JSON.parse(JSON.stringify(DEFAULT_DATA));
                localStorage.removeItem('chen_campaign_cms_data');
                renderFrontend();
                populateAdminInputs();
                showToast("已重置所有內容至預設值！");
            }
        }

        function showToast(msg) {
            const toast = document.createElement('div');
            toast.className = 'fixed bottom-5 right-5 bg-green-600 text-white font-bold px-4 py-3 rounded-2xl shadow-xl z-50 text-sm animate-bounce';
            toast.innerText = msg;
            document.body.appendChild(toast);
            setTimeout(() => toast.remove(), 3000);
        }

        // -------------------------------------------------------------
        // INTERACTIVE FRONTEND LOGIC (Pour Tea / Countdown / Wish Form)
        // -------------------------------------------------------------
        const electionDate = new Date('2026-11-28T08:00:00').getTime();

        function updateCountdown() {
            const now = new Date().getTime();
            const distance = electionDate - now;

            if (distance < 0) {
                document.getElementById('countdown-timer').innerHTML = "<div class='col-span-4 font-bold text-red-600'>今日為投票日！請踴躍投票！</div>";
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById('days').innerText = days;
            document.getElementById('hours').innerText = String(hours).padStart(2, '0');
            document.getElementById('minutes').innerText = String(minutes).padStart(2, '0');
            document.getElementById('seconds').innerText = String(seconds).padStart(2, '0');
        }

        function pourTea() {
            appState.teaCount++;
            document.getElementById('tea-count').innerText = Number(appState.teaCount).toLocaleString();
            localStorage.setItem('chen_campaign_cms_data', JSON.stringify(appState));

            const countEl = document.getElementById('tea-count');
            countEl.classList.add('scale-125', 'text-campaign-orange');
            setTimeout(() => {
                countEl.classList.remove('scale-125', 'text-campaign-orange');
            }, 200);
        }

        function submitWish(event) {
            event.preventDefault();
            const name = document.getElementById('user-name').value.trim();
            const location = document.getElementById('user-location').value;
            const msg = document.getElementById('user-msg').value.trim();

            if (!name || !msg) return;

            appState.wishes.unshift({
                id: Date.now(),
                name: name,
                location: location,
                time: "剛剛",
                msg: msg
            });

            localStorage.setItem('chen_campaign_cms_data', JSON.stringify(appState));
            renderWishesFeed();
            document.getElementById('wish-form').reset();
            pourTea();
        }

        function copyLineId() {
            const dummy = document.createElement('input');
            document.body.appendChild(dummy);
            dummy.value = '桃園市中寧里里長候選人陳明輝官方號';
            dummy.select();
            document.execCommand('copy');
            document.body.removeChild(dummy);

            const copyMsg = document.getElementById('copy-msg');
            copyMsg.classList.remove('hidden');
            setTimeout(() => {
                copyMsg.classList.add('hidden');
            }, 3000);
        }

        function escapeHtml(text) {
            if (!text) return '';
            return String(text).replace(/[&<>"']/g, function(m) {
                return {
                    '&': '&amp;',
                    '<': '&lt;',
                    '>': '&gt;',
                    '"': '&quot;',
                    "'": '&#039;'
                }[m];
            });
        }

        // Initialize Page
        window.onload = function() {
            renderFrontend();
            setInterval(updateCountdown, 1000);
            updateCountdown();
        };
    </script>
</body>
</html>
