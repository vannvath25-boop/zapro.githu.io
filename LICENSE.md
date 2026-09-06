<!DOCTYPE html>
<html lang="km">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SMM Pro - Multi Bot Panel</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Kantumruy+Pro:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style> body { font-family: 'Kantumruy Pro', sans-serif; } </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen p-4">

    <div class="max-w-4xl mx-auto space-y-6">
        
        <!-- Header & User Info Bar -->
        <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center bg-slate-800 border border-slate-700 p-6 rounded-2xl shadow-xl gap-4">
            <div>
                <h1 class="text-xl font-bold text-indigo-400">SMM Pro - បញ្ជាទិញ & ដាក់ប្រាក់</h1>
                <p class="text-sm text-slate-400" id="welcome-user">សូមស្វាគមន៍! (មិនទាន់បានចូលគណនី)</p>
            </div>
            <div class="flex items-center gap-4">
                <div class="bg-slate-900 border border-slate-700 px-4 py-2 rounded-xl">
                    <span class="text-xs text-slate-400 block">សមតុល្យទឹកប្រាក់</span>
                    <span id="user-balance" class="text-emerald-400 font-bold text-lg">$0.00</span>
                </div>
                <button onclick="logout()" class="bg-red-600/20 hover:bg-red-600 text-red-400 hover:text-white px-3 py-2 rounded-xl text-sm transition">
                    ចាកចេញ
                </button>
            </div>
        </div>

        <!-- AUTH SECTION -->
        <div id="auth-section" class="bg-slate-800 border border-slate-700 rounded-2xl p-6 shadow-xl max-w-md mx-auto space-y-6">
            <div class="flex border-b border-slate-700">
                <button onclick="switchTab('login')" id="tab-login" class="flex-1 pb-3 font-bold text-indigo-400 border-b-2 border-indigo-500 transition">ចូលគណនី</button>
                <button onclick="switchTab('register')" id="tab-register" class="flex-1 pb-3 font-semibold text-slate-400 transition">ចុះឈ្មោះ</button>
            </div>

            <!-- Login Form -->
            <form id="form-login" onsubmit="handleLogin(event)" class="space-y-4">
                <div>
                    <label class="block text-sm text-slate-300 mb-1">Username</label>
                    <input type="text" id="login-username" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                </div>
                <div>
                    <label class="block text-sm text-slate-300 mb-1">Password</label>
                    <input type="password" id="login-password" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                </div>
                <button type="submit" class="w-full bg-indigo-600 hover:bg-indigo-500 text-white font-semibold py-3 rounded-xl transition">
                    ចូលប្រព័ន្ធ
                </button>
            </form>

            <!-- Register Form -->
            <form id="form-register" onsubmit="handleRegister(event)" class="space-y-4 hidden">
                <div>
                    <label class="block text-sm text-slate-300 mb-1">ឈ្មោះពេញ (Full Name)</label>
                    <input type="text" id="reg-fullname" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                </div>
                <div>
                    <label class="block text-sm text-slate-300 mb-1">Username</label>
                    <input type="text" id="reg-username" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                </div>
                <div>
                    <label class="block text-sm text-slate-300 mb-1">Password</label>
                    <input type="password" id="reg-password" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                </div>
                <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white font-semibold py-3 rounded-xl transition">
                    ចុះឈ្មោះគណនី
                </button>
            </form>
        </div>

        <!-- DASHBOARD CONTENT -->
        <div id="dashboard-section" class="space-y-6 hidden">
            
            <!-- Navigation Tabs -->
            <div class="flex bg-slate-800 border border-slate-700 p-2 rounded-2xl shadow-xl gap-2">
                <button onclick="switchDashboardTab('order')" id="dash-tab-order" class="flex-1 py-3 rounded-xl font-bold bg-indigo-600 text-white transition">
                    🛒 បញ្ជាទិញសេវាកម្ម
                </button>
                <button onclick="switchDashboardTab('deposit')" id="dash-tab-deposit" class="flex-1 py-3 rounded-xl font-semibold text-slate-400 hover:text-white transition">
                    💳 ដាក់ប្រាក់ (Deposit)
                </button>
            </div>

            <!-- 1. ORDER SECTION -->
            <div id="section-order" class="bg-slate-800 border border-slate-700 rounded-2xl p-6 shadow-xl space-y-6">
                <h2 class="text-lg font-bold text-slate-200">បង្កើតការបញ្ជាទិញថ្មី (New Order)</h2>
                
                <form onsubmit="submitOrder(event)" class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-1">ជ្រើសរើស Category</label>
                        <select id="order-category" onchange="updateServicesDropdown()" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                            <option value="facebook">Facebook Services</option>
                            <option value="tiktok">TikTok Services</option>
                        </select>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-1">ជ្រើសរើសសេវាកម្ម (Service)</label>
                        <select id="order-service" onchange="calculateTotal()" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                            <!-- Populated dynamically -->
                        </select>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-1">តំណភ្ជាប់ (Link)</label>
                        <input type="url" id="order-link" required placeholder="https://..." class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-1">ចំនួន (Quantity)</label>
                        <input type="number" id="order-quantity" oninput="calculateTotal()" value="1000" min="100" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-indigo-500">
                    </div>

                    <div class="bg-slate-900/60 border border-slate-700 p-4 rounded-xl flex justify-between items-center">
                        <span class="text-slate-400">តម្លៃសរុប (Total Price):</span>
                        <span id="order-total-price" class="text-2xl font-bold text-emerald-400">$0.00</span>
                    </div>

                    <button type="submit" class="w-full bg-indigo-600 hover:bg-indigo-500 text-white font-semibold py-3.5 rounded-xl transition">
                        បញ្ជាទិញឥឡូវនេះ (Submit Order)
                    </button>
                </form>
            </div>

            <!-- 2. DEPOSIT SECTION -->
            <div id="section-deposit" class="bg-slate-800 border border-slate-700 rounded-2xl p-6 shadow-xl space-y-6 hidden">
                <h2 class="text-lg font-bold text-slate-200">ស្នើសុំដាក់ប្រាក់បន្ថែម (Add Funds / Deposit)</h2>

                <div class="bg-slate-900/80 border border-slate-700 p-6 rounded-2xl flex flex-col sm:flex-row items-center gap-6">
                    <div class="bg-white p-3 rounded-2xl shadow-lg shrink-0">
                        <img src="https://i.postimg.cc/vZBZMWDf/IMG-0958.jpg" alt="ABA QR Code" class="w-36 h-36 object-contain rounded-xl">
                    </div>
                    <div class="space-y-3 text-center sm:text-left">
                        <h3 class="text-base font-bold text-slate-100">ស្កេន QR Code ដើម្បីទូទាត់ប្រាក់</h3>
                        <p class="text-xs text-amber-400 bg-amber-500/10 p-2.5 rounded-lg border border-amber-500/20">
                            ⚠️ បន្ទាប់ពីស្កេនបង់ប្រាក់រួច សូមបំពេញចំនួនទឹកប្រាក់ និង Upload រូបភាពវិក្កយបត្រ (Slip) ខាងក្រោម។
                        </p>
                    </div>
                </div>
                
                <form onsubmit="submitDeposit(event)" class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-1">ចំនួនទឹកប្រាក់ដែលបានដាក់ ($)</label>
                        <input type="number" step="0.01" id="deposit-amount" required placeholder="10.00" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-200 focus:outline-none focus:border-emerald-500">
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-1">ភ្ជាប់រូបភាពវិក្កយបត្រ (Upload Payment Slip)</label>
                        <input type="file" id="deposit-slip" accept="image/*" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-2.5 text-slate-300 text-sm">
                    </div>

                    <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white font-semibold py-3.5 rounded-xl transition">
                        ស្នើសុំដាក់ប្រាក់ចូល Telegram Bot
                    </button>
                </form>
            </div>

        </div>

    </div>

    <script>
        const ORDER_BOT_TOKEN = '8960855547:AAHX0xQqYqUvTwkYwsVD4iUw1-WXnT2oLg0'; 
        const ORDER_CHAT_ID = '8621369358';
        const DEPOSIT_BOT_TOKEN = '8712683121:AAEdJfI8UNpfdpIJaT4TLMBGMlKRmEQs_rw'; 
        const DEPOSIT_CHAT_ID = '8621369358';

        window.onload = function() {
            checkAuth();
            updateServicesDropdown();
        };

        function switchDashboardTab(tab) {
            const secOrder = document.getElementById('section-order');
            const secDeposit = document.getElementById('section-deposit');
            const tabOrder = document.getElementById('dash-tab-order');
            const tabDeposit = document.getElementById('dash-tab-deposit');

            if (tab === 'order') {
                secOrder.classList.remove('hidden');
                secDeposit.classList.add('hidden');
                tabOrder.className = "flex-1 py-3 rounded-xl font-bold bg-indigo-600 text-white transition";
                tabDeposit.className = "flex-1 py-3 rounded-xl font-semibold text-slate-400 hover:text-white transition";
            } else {
                secOrder.classList.add('hidden');
                secDeposit.classList.remove('hidden');
                tabDeposit.className = "flex-1 py-3 rounded-xl font-bold bg-emerald-600 text-white transition";
                tabOrder.className = "flex-1 py-3 rounded-xl font-semibold text-slate-400 hover:text-white transition";
            }
        }

        function switchTab(tab) {
            const loginForm = document.getElementById('form-login');
            const regForm = document.getElementById('form-register');
            const tabLogin = document.getElementById('tab-login');
            const tabReg = document.getElementById('tab-register');

            if (tab === 'login') {
                loginForm.classList.remove('hidden');
                regForm.classList.add('hidden');
                tabLogin.className = "flex-1 pb-3 font-bold text-indigo-400 border-b-2 border-indigo-500 transition";
                tabReg.className = "flex-1 pb-3 font-semibold text-slate-400 transition";
            } else {
                loginForm.classList.add('hidden');
                regForm.classList.remove('hidden');
                tabReg.className = "flex-1 pb-3 font-bold text-emerald-400 border-b-2 border-emerald-500 transition";
                tabLogin.className = "flex-1 pb-3 font-semibold text-slate-400 transition";
            }
        }

        function handleRegister(e) {
            e.preventDefault();
            const fullname = document.getElementById('reg-fullname').value.trim();
            const username = document.getElementById('reg-username').value.trim();
            const password = document.getElementById('reg-password').value.trim();

            let users = JSON.parse(localStorage.getItem('smm_users')) || [];
            if (users.some(u => u.username === username)) {
                alert('Username នេះមានអ្នកប្រើប្រាស់រួចហើយ!');
                return;
            }

            const newUser = { fullname, username, password, balance: 0.00 };
            users.push(newUser);
            localStorage.setItem('smm_users', JSON.stringify(users));
            localStorage.setItem('smm_current_user', JSON.stringify(newUser));

            alert('ចុះឈ្មោះជោគជ័យ!');
            checkAuth();
        }

        function handleLogin(e) {
            e.preventDefault();
            const username = document.getElementById('login-username').value.trim();
            const password = document.getElementById('login-password').value.trim();

            let users = JSON.parse(localStorage.getItem('smm_users')) || [];
            let user = users.find(u => u.username === username && u.password === password);

            if (user) {
                localStorage.setItem('smm_current_user', JSON.stringify(user));
                checkAuth();
            } else {
                alert('Username ឬ Password មិនត្រឹមត្រូវទេ!');
            }
        }

        function logout() {
            localStorage.removeItem('smm_current_user');
            checkAuth();
        }

        function checkAuth() {
            let currentUser = JSON.parse(localStorage.getItem('smm_current_user'));
            if (currentUser) {
                let users = JSON.parse(localStorage.getItem('smm_users')) || [];
                let freshUser = users.find(u => u.username === currentUser.username);
                if (freshUser) {
                    currentUser = freshUser;
                    localStorage.setItem('smm_current_user', JSON.stringify(currentUser));
                }

                document.getElementById('auth-section').classList.add('hidden');
                document.getElementById('dashboard-section').classList.remove('hidden');
                document.getElementById('welcome-user').innerText = `សួស្តី, ${currentUser.fullname || currentUser.username}`;
                document.getElementById('user-balance').innerText = `$${(currentUser.balance || 0).toFixed(2)}`;
            } else {
                document.getElementById('auth-section').classList.remove('hidden');
                document.getElementById('dashboard-section').classList.add('hidden');
                document.getElementById('welcome-user').innerText = `សូមស្វាគមន៍! (មិនទាន់បានចូលគណនី)`;
            }
        }

        function updateServicesDropdown() {
            const catId = document.getElementById('order-category').value;
            const servSelect = document.getElementById('order-service');
            servSelect.innerHTML = '';

            let services = {
                'facebook': [{ name: 'Facebook Page Likes', pricePer1k: 2.5 }],
                'tiktok': [{ name: 'TikTok Followers', pricePer1k: 3.0 }]
            };

            if (services[catId]) {
                services[catId].forEach((serv, index) => {
                    servSelect.innerHTML += `<option value="${index}" data-price="${serv.pricePer1k}">${serv.name} ($${serv.pricePer1k}/1k)</option>`;
                });
            }
            calculateTotal();
        }

        function calculateTotal() {
            const servSelect = document.getElementById('order-service');
            const selectedOption = servSelect.options[servSelect.selectedIndex];
            const pricePer1k = parseFloat(selectedOption ? selectedOption.getAttribute('data-price') || 0 : 0);
            const quantity = parseInt(document.getElementById('order-quantity').value) || 0;

            const totalPrice = (pricePer1k / 1000) * quantity;
            document.getElementById('order-total-price').innerText = `$${totalPrice.toFixed(2)}`;
        }

        function submitOrder(e) {
            e.preventDefault();
            let currentUser = JSON.parse(localStorage.getItem('smm_current_user'));
            if (!currentUser) return;

            const catSelect = document.getElementById('order-category');
            const servSelect = document.getElementById('order-service');
            const link = document.getElementById('order-link').value;
            const quantity = parseInt(document.getElementById('order-quantity').value);
            
            const categoryName = catSelect.options[catSelect.selectedIndex].text;
            const serviceOption = servSelect.options[servSelect.selectedIndex];
            const serviceName = serviceOption.text.split(' ($')[0];
            const pricePer1k = parseFloat(serviceOption.getAttribute('data-price') || 0);
            const totalPrice = (pricePer1k / 1000) * quantity;

            if ((currentUser.balance || 0) < totalPrice) {
                alert('ទឹកប្រាក់ក្នុងកាបូបរបស់អ្នកមិនគ្រប់គ្រាន់ទេ! សូមដាក់ប្រាក់បន្ថែម។');
                return;
            }

            currentUser.balance -= totalPrice;
            
            let users = JSON.parse(localStorage.getItem('smm_users')) || [];
            users = users.map(u => u.username === currentUser.username ? currentUser : u);
            localStorage.setItem('smm_users', JSON.stringify(users));
            localStorage.setItem('smm_current_user', JSON.stringify(currentUser));

            checkAuth();

            sendTelegram(`🚨 <b>ការបញ្ជាទិញថ្មី!</b>\n👤 អតិថិជន: ${currentUser.username}\n📦 សេវាកម្ម: ${serviceName}\n🔗 លីង: ${link}\n🔢 ចំនួន: ${quantity}\n💰 សរុប: $${totalPrice.toFixed(2)}`, ORDER_BOT_TOKEN, ORDER_CHAT_ID);

            alert('ការបញ្ជាទិញបានជោគជ័យ!');
            document.getElementById('order-link').value = '';
        }

        function submitDeposit(e) {
            e.preventDefault();
            let currentUser = JSON.parse(localStorage.getItem('smm_current_user'));
            if (!currentUser) return;

            const amount = parseFloat(document.getElementById('deposit-amount').value);
            const slipInput = document.getElementById('deposit-slip');

            if (isNaN(amount) || amount <= 0) {
                alert('សូមបញ្ចូលចំនួនទឹកប្រាក់ឱ្យបានត្រឹមត្រូវ!');
                return;
            }

            const caption = `💳 <b>សំណើដាក់ប្រាក់ថ្មី!</b>\n👤 អតិថិជន: ${currentUser.username}\n💵 ចំនួន: $${amount.toFixed(2)}`;

            if (slipInput.files && slipInput.files[0]) {
                const reader = new FileReader();
                reader.onload = function(event) {
                    sendTelegramPhoto(event.target.result, caption);
                };
                reader.readAsDataURL(slipInput.files[0]);
            } else {
                sendTelegram(caption, DEPOSIT_BOT_TOKEN, DEPOSIT_CHAT_ID);
            }

            alert('សំណើដាក់ប្រាក់ត្រូវបានបញ្ជូនទៅកាន់ Admin ហើយ!');
            document.getElementById('deposit-amount').value = '';
            slipInput.value = '';
            switchDashboardTab('order');
        }

        function sendTelegram(message, token, chatId) {
            fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ chat_id: chatId, text: message, parse_mode: 'HTML' })
            }).catch(err => console.error(err));
        }

        function sendTelegramPhoto(base64Data, caption) {
            fetch(base64Data)
                .then(res => res.blob())
                .then(blob => {
                    const formData = new FormData();
                    formData.append('chat_id', DEPOSIT_CHAT_ID);
                    formData.append('photo', blob, 'slip.jpg');
                    formData.append('caption', caption);
                    formData.append('parse_mode', 'HTML');

                    return fetch(`https://api.telegram.org/bot${DEPOSIT_BOT_TOKEN}/sendPhoto`, {
                        method: 'POST',
                        body: formData
                    });
                }).catch(err => console.error(err));
        }
    </script>
</body>
</html>
