<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SahabatBot - AI Psikolog Terpercaya</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        body { font-family: 'Inter', sans-serif; }
        .gradient-bg { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
        .card-hover { transition: transform 0.3s ease, box-shadow 0.3s ease; }
        .card-hover:hover { transform: translateY(-5px); box-shadow: 0 20px 40px rgba(0,0,0,0.1); }
        .chat-bubble { animation: fadeInUp 0.5s ease-out; }
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .typing-indicator {
            display: inline-block;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: #9CA3AF;
            animation: typing 1.4s infinite ease-in-out;
        }
        .typing-indicator:nth-child(1) { animation-delay: -0.32s; }
        .typing-indicator:nth-child(2) { animation-delay: -0.16s; }
        @keyframes typing {
            0%, 80%, 100% { transform: scale(0); opacity: 0.5; }
            40% { transform: scale(1); opacity: 1; }
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Navigation -->
    <nav class="bg-white shadow-sm sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <div class="text-2xl font-bold text-indigo-600">🤖 SahabatBot</div>
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="text-gray-700 hover:text-indigo-600 transition-colors">Beranda</a>
                    <a href="#features" class="text-gray-700 hover:text-indigo-600 transition-colors">Fitur</a>
                    <a href="#pricing" class="text-gray-700 hover:text-indigo-600 transition-colors">Harga</a>
                    <a href="#safety" class="text-gray-700 hover:text-indigo-600 transition-colors">Keamanan</a>
                </div>
                <div class="flex space-x-4">
                    <button onclick="showLogin()" class="text-indigo-600 hover:text-indigo-800 font-medium">Masuk</button>
                    <button onclick="showRegister()" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition-colors">Daftar</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="gradient-bg text-white py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <h1 class="text-5xl font-bold mb-6">Konsultasi Psikologi dengan AI Terpercaya</h1>
                    <p class="text-xl mb-8 text-indigo-100">SahabatBot menggunakan AI yang dilatih dari buku-buku psikologi terbaik dunia untuk memberikan dukungan mental 24/7</p>
                    <div class="flex space-x-4">
                        <button onclick="startTrial()" class="bg-white text-indigo-600 px-8 py-3 rounded-lg font-semibold hover:bg-gray-100 transition-colors">Coba Gratis 1 Hari</button>
                        <button onclick="showDemo()" class="border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-indigo-600 transition-colors">Lihat Demo</button>
                    </div>
                </div>
                <div class="bg-white rounded-2xl p-6 shadow-2xl">
                    <div id="chatDemo" class="h-96 overflow-y-auto mb-4 space-y-4">
                        <div class="flex items-start space-x-3">
                            <div class="w-8 h-8 bg-indigo-600 rounded-full flex items-center justify-center text-white text-sm">🤖</div>
                            <div class="bg-gray-100 rounded-lg p-3 max-w-xs">
                                <p class="text-gray-800">Halo! Saya SahabatBot, asisten psikologi AI Anda. Bagaimana perasaan Anda hari ini?</p>
                            </div>
                        </div>
                    </div>
                    <div class="flex space-x-2">
                        <input id="demoInput" type="text" placeholder="Ketik pesan Anda..." class="flex-1 border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500 text-gray-800">
                        <button onclick="sendDemoMessage()" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition-colors">Kirim</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold text-gray-900 mb-4">Mengapa Memilih SahabatBot?</h2>
                <p class="text-xl text-gray-600">Platform psikologi AI yang komprehensif dengan dukungan profesional</p>
            </div>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="card-hover bg-white p-8 rounded-xl shadow-lg border">
                    <div class="w-16 h-16 bg-indigo-100 rounded-lg flex items-center justify-center mb-6">
                        <span class="text-2xl">🧠</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">AI Berdasarkan Literatur Terbaik</h3>
                    <p class="text-gray-600">Dilatih dari ratusan buku psikologi terbaik dunia dan teknik terapi terbukti efektif</p>
                </div>
                <div class="card-hover bg-white p-8 rounded-xl shadow-lg border">
                    <div class="w-16 h-16 bg-green-100 rounded-lg flex items-center justify-center mb-6">
                        <span class="text-2xl">👨‍⚕️</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Rujukan ke Psikiater</h3>
                    <p class="text-gray-600">Akses langsung ke psikiater profesional ketika diperlukan penanganan lebih lanjut</p>
                </div>
                <div class="card-hover bg-white p-8 rounded-xl shadow-lg border">
                    <div class="w-16 h-16 bg-red-100 rounded-lg flex items-center justify-center mb-6">
                        <span class="text-2xl">🚨</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Sistem Keamanan Darurat</h3>
                    <p class="text-gray-600">Deteksi otomatis situasi berisiko tinggi dengan akses langsung ke layanan darurat 112</p>
                </div>
                <div class="card-hover bg-white p-8 rounded-xl shadow-lg border">
                    <div class="w-16 h-16 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
                        <span class="text-2xl">⏰</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Tersedia 24/7</h3>
                    <p class="text-gray-600">Dukungan psikologi kapan saja Anda membutuhkannya, tanpa perlu menunggu jadwal</p>
                </div>
                <div class="card-hover bg-white p-8 rounded-xl shadow-lg border">
                    <div class="w-16 h-16 bg-purple-100 rounded-lg flex items-center justify-center mb-6">
                        <span class="text-2xl">🔒</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Privasi Terjamin</h3>
                    <p class="text-gray-600">Semua percakapan dienkripsi dan dijaga kerahasiaannya sesuai standar medis</p>
                </div>
                <div class="card-hover bg-white p-8 rounded-xl shadow-lg border">
                    <div class="w-16 h-16 bg-yellow-100 rounded-lg flex items-center justify-center mb-6">
                        <span class="text-2xl">💰</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Harga Terjangkau</h3>
                    <p class="text-gray-600">Akses konsultasi psikologi dengan biaya jauh lebih terjangkau dari terapi tradisional</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold text-gray-900 mb-4">Pilih Paket yang Sesuai</h2>
                <p class="text-xl text-gray-600">Mulai dengan uji coba gratis, lanjutkan dengan paket berlangganan</p>
            </div>
            <div class="grid md:grid-cols-4 gap-8">
                <div class="bg-white rounded-xl shadow-lg p-8 border-2 border-green-200">
                    <div class="text-center">
                        <h3 class="text-2xl font-bold text-gray-900 mb-2">Uji Coba</h3>
                        <div class="text-4xl font-bold text-green-600 mb-4">GRATIS</div>
                        <p class="text-gray-600 mb-6">1 Hari</p>
                        <button onclick="selectPlan('trial')" class="w-full bg-green-600 text-white py-3 rounded-lg font-semibold hover:bg-green-700 transition-colors">Mulai Gratis</button>
                    </div>
                    <ul class="mt-8 space-y-3">
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Chat unlimited dengan AI</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Akses fitur dasar</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Sistem keamanan darurat</li>
                    </ul>
                </div>
                <div class="bg-white rounded-xl shadow-lg p-8 border">
                    <div class="text-center">
                        <h3 class="text-2xl font-bold text-gray-900 mb-2">Mingguan</h3>
                        <div class="text-4xl font-bold text-indigo-600 mb-4">Rp 49K</div>
                        <p class="text-gray-600 mb-6">Per Minggu</p>
                        <button onclick="selectPlan('weekly')" class="w-full bg-indigo-600 text-white py-3 rounded-lg font-semibold hover:bg-indigo-700 transition-colors">Pilih Paket</button>
                    </div>
                    <ul class="mt-8 space-y-3">
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Semua fitur uji coba</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Analisis mood harian</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Rujukan psikiater</li>
                    </ul>
                </div>
                <div class="bg-white rounded-xl shadow-lg p-8 border-2 border-indigo-500 relative">
                    <div class="absolute -top-4 left-1/2 transform -translate-x-1/2">
                        <span class="bg-indigo-500 text-white px-4 py-1 rounded-full text-sm font-semibold">POPULER</span>
                    </div>
                    <div class="text-center">
                        <h3 class="text-2xl font-bold text-gray-900 mb-2">Bulanan</h3>
                        <div class="text-4xl font-bold text-indigo-600 mb-4">Rp 149K</div>
                        <p class="text-gray-600 mb-6">Per Bulan</p>
                        <button onclick="selectPlan('monthly')" class="w-full bg-indigo-600 text-white py-3 rounded-lg font-semibold hover:bg-indigo-700 transition-colors">Pilih Paket</button>
                    </div>
                    <ul class="mt-8 space-y-3">
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Semua fitur mingguan</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Laporan progress bulanan</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Prioritas rujukan psikiater</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Hemat 25%</li>
                    </ul>
                </div>
                <div class="bg-white rounded-xl shadow-lg p-8 border">
                    <div class="text-center">
                        <h3 class="text-2xl font-bold text-gray-900 mb-2">Tahunan</h3>
                        <div class="text-4xl font-bold text-indigo-600 mb-4">Rp 1.2JT</div>
                        <p class="text-gray-600 mb-6">Per Tahun</p>
                        <button onclick="selectPlan('yearly')" class="w-full bg-indigo-600 text-white py-3 rounded-lg font-semibold hover:bg-indigo-700 transition-colors">Pilih Paket</button>
                    </div>
                    <ul class="mt-8 space-y-3">
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Semua fitur bulanan</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Konsultasi psikiater gratis 2x</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Laporan tahunan komprehensif</li>
                        <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Hemat 45%</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Safety Section -->
    <section id="safety" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold text-gray-900 mb-4">Keamanan & Perlindungan</h2>
                <p class="text-xl text-gray-600">Sistem keamanan berlapis untuk melindungi kesehatan mental Anda</p>
            </div>
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <div class="space-y-8">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 bg-red-100 rounded-lg flex items-center justify-center flex-shrink-0">
                                <span class="text-xl">🚨</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-semibold mb-2">Deteksi Risiko Tinggi</h3>
                                <p class="text-gray-600">Sistem AI mendeteksi indikasi bunuh diri atau bahaya diri dan langsung menghubungkan ke layanan darurat 112</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
                                <span class="text-xl">👨‍⚕️</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-semibold mb-2">Rujukan Otomatis</h3>
                                <p class="text-gray-600">Untuk kasus trauma berat atau kondisi kompleks, sistem otomatis merujuk ke psikiater manusia</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center flex-shrink-0">
                                <span class="text-xl">💰</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-semibold mb-2">Sistem Bagi Hasil</h3>
                                <p class="text-gray-600">90% fee konsultasi langsung ke psikiater, 10% untuk platform - memastikan kualitas layanan terbaik</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="bg-gray-50 rounded-2xl p-8">
                    <h3 class="text-2xl font-bold mb-6 text-center">Protokol Keamanan</h3>
                    <div class="space-y-4">
                        <div class="bg-white rounded-lg p-4 border-l-4 border-red-500">
                            <div class="font-semibold text-red-700">Level 1: Risiko Tinggi</div>
                            <div class="text-sm text-gray-600">Koneksi langsung ke 112 + notifikasi keluarga</div>
                        </div>
                        <div class="bg-white rounded-lg p-4 border-l-4 border-yellow-500">
                            <div class="font-semibold text-yellow-700">Level 2: Perlu Perhatian</div>
                            <div class="text-sm text-gray-600">Rujukan ke psikiater dalam 24 jam</div>
                        </div>
                        <div class="bg-white rounded-lg p-4 border-l-4 border-green-500">
                            <div class="font-semibold text-green-700">Level 3: Dukungan Rutin</div>
                            <div class="text-sm text-gray-600">Konseling AI dengan monitoring berkala</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-4 gap-8">
                <div>
                    <div class="text-2xl font-bold mb-4">🤖 SahabatBot</div>
                    <p class="text-gray-400">Platform konsultasi psikologi AI terpercaya dengan dukungan profesional 24/7</p>
                </div>
                <div>
                    <h3 class="font-semibold mb-4">Layanan</h3>
                    <ul class="space-y-2 text-gray-400">
                        <li>Konseling AI</li>
                        <li>Rujukan Psikiater</li>
                        <li>Layanan Darurat</li>
                        <li>Monitoring Kesehatan Mental</li>
                    </ul>
                </div>
                <div>
                    <h3 class="font-semibold mb-4">Dukungan</h3>
                    <ul class="space-y-2 text-gray-400">
                        <li>Pusat Bantuan</li>
                        <li>Kontak Darurat: 112</li>
                        <li>Email: help@sahabatbot.com</li>
                        <li>WhatsApp: +62-811-xxx-xxxx</li>
                    </ul>
                </div>
                <div>
                    <h3 class="font-semibold mb-4">Legal</h3>
                    <ul class="space-y-2 text-gray-400">
                        <li>Kebijakan Privasi</li>
                        <li>Syarat Layanan</li>
                        <li>Kode Etik Psikologi</li>
                        <li>Sertifikasi Keamanan</li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
                <p>&copy; 2024 SahabatBot. Semua hak dilindungi. Terdaftar di Kementerian Kesehatan RI.</p>
            </div>
        </div>
    </footer>

    <!-- Modals -->
    <!-- Login Modal -->
    <div id="loginModal" class="fixed inset-0 bg-black bg-opacity-50 hidden items-center justify-center z-50">
        <div class="bg-white rounded-2xl p-8 max-w-md w-full mx-4">
            <h2 class="text-2xl font-bold mb-6 text-center">Masuk ke SahabatBot</h2>
            <form onsubmit="handleLogin(event)">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-medium mb-2">Email</label>
                    <input type="email" required class="w-full border border-gray-300 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                </div>
                <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-medium mb-2">Password</label>
                    <input type="password" required class="w-full border border-gray-300 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                </div>
                <button type="submit" class="w-full bg-indigo-600 text-white py-3 rounded-lg font-semibold hover:bg-indigo-700 transition-colors">Masuk</button>
            </form>
            <div class="text-center mt-4">
                <button onclick="closeModal('loginModal')" class="text-gray-500 hover:text-gray-700">Tutup</button>
            </div>
        </div>
    </div>

    <!-- Register Modal -->
    <div id="registerModal" class="fixed inset-0 bg-black bg-opacity-50 hidden items-center justify-center z-50">
        <div class="bg-white rounded-2xl p-8 max-w-md w-full mx-4">
            <h2 class="text-2xl font-bold mb-6 text-center">Daftar SahabatBot</h2>
            <form onsubmit="handleRegister(event)">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-medium mb-2">Nama Lengkap</label>
                    <input type="text" required class="w-full border border-gray-300 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-medium mb-2">Email</label>
                    <input type="email" required class="w-full border border-gray-300 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-medium mb-2">Password</label>
                    <input type="password" required class="w-full border border-gray-300 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                </div>
                <div class="mb-6">
                    <label class="flex items-center">
                        <input type="checkbox" required class="mr-2">
                        <span class="text-sm text-gray-600">Saya setuju dengan syarat dan ketentuan serta kebijakan privasi</span>
                    </label>
                </div>
                <button type="submit" class="w-full bg-indigo-600 text-white py-3 rounded-lg font-semibold hover:bg-indigo-700 transition-colors">Daftar & Mulai Uji Coba</button>
            </form>
            <div class="text-center mt-4">
                <button onclick="closeModal('registerModal')" class="text-gray-500 hover:text-gray-700">Tutup</button>
            </div>
        </div>
    </div>

    <!-- Emergency Modal -->
    <div id="emergencyModal" class="fixed inset-0 bg-red-600 bg-opacity-95 hidden items-center justify-center z-50">
        <div class="bg-white rounded-2xl p-8 max-w-lg w-full mx-4 text-center">
            <div class="text-6xl mb-4">🚨</div>
            <h2 class="text-3xl font-bold text-red-600 mb-4">PERINGATAN DARURAT</h2>
            <p class="text-lg mb-6">Sistem mendeteksi Anda mungkin dalam situasi berbahaya. Kami akan menghubungkan Anda dengan layanan darurat.</p>
            <div class="space-y-4">
                <button onclick="callEmergency()" class="w-full bg-red-600 text-white py-4 rounded-lg font-bold text-xl hover:bg-red-700 transition-colors">HUBUNGI 112 SEKARANG</button>
                <button onclick="connectPsychiatrist()" class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors">Hubungkan ke Psikiater</button>
                <button onclick="closeModal('emergencyModal')" class="w-full border-2 border-gray-300 text-gray-700 py-3 rounded-lg font-semibold hover:bg-gray-50 transition-colors">Saya Baik-baik Saja</button>
            </div>
        </div>
    </div>

    <script>
        // Demo chat functionality
        const demoResponses = [
            "Terima kasih sudah berbagi. Saya memahami perasaan Anda. Bisakah Anda ceritakan lebih detail?",
            "Itu adalah reaksi yang normal. Mari kita eksplorasi lebih dalam tentang situasi ini.",
            "Saya mendengar bahwa Anda sedang mengalami kesulitan. Apa yang paling mengganggu Anda saat ini?",
            "Berdasarkan yang Anda ceritakan, saya merekomendasikan teknik pernapasan dalam. Apakah Anda ingin mencobanya?",
            "Untuk kasus seperti ini, mungkin akan lebih baik jika Anda berkonsultasi dengan psikiater profesional. Saya dapat membantu mencarikan rujukan."
        ];

        let demoResponseIndex = 0;

        function sendDemoMessage() {
            const input = document.getElementById('demoInput');
            const chatDemo = document.getElementById('chatDemo');
            const message = input.value.trim();
            
            if (!message) return;

            // Add user message
            const userMessage = document.createElement('div');
            userMessage.className = 'flex items-start space-x-3 justify-end chat-bubble';
            userMessage.innerHTML = `
                <div class="bg-indigo-600 text-white rounded-lg p-3 max-w-xs">
                    <p>${message}</p>
                </div>
                <div class="w-8 h-8 bg-gray-300 rounded-full flex items-center justify-center text-sm">👤</div>
            `;
            chatDemo.appendChild(userMessage);

            // Clear input
            input.value = '';

            // Check for emergency keywords
            const emergencyKeywords = ['bunuh diri', 'mati', 'mengakhiri hidup', 'tidak ingin hidup', 'ingin mati'];
            if (emergencyKeywords.some(keyword => message.toLowerCase().includes(keyword))) {
                setTimeout(() => showEmergencyModal(), 1000);
                return;
            }

            // Add typing indicator
            const typingDiv = document.createElement('div');
            typingDiv.className = 'flex items-start space-x-3';
            typingDiv.innerHTML = `
                <div class="w-8 h-8 bg-indigo-600 rounded-full flex items-center justify-center text-white text-sm">🤖</div>
                <div class="bg-gray-100 rounded-lg p-3">
                    <div class="flex space-x-1">
                        <div class="typing-indicator"></div>
                        <div class="typing-indicator"></div>
                        <div class="typing-indicator"></div>
                    </div>
                </div>
            `;
            chatDemo.appendChild(typingDiv);
            chatDemo.scrollTop = chatDemo.scrollHeight;

            // Add bot response after delay
            setTimeout(() => {
                chatDemo.removeChild(typingDiv);
                
                const botMessage = document.createElement('div');
                botMessage.className = 'flex items-start space-x-3 chat-bubble';
                botMessage.innerHTML = `
                    <div class="w-8 h-8 bg-indigo-600 rounded-full flex items-center justify-center text-white text-sm">🤖</div>
                    <div class="bg-gray-100 rounded-lg p-3 max-w-xs">
                        <p class="text-gray-800">${demoResponses[demoResponseIndex % demoResponses.length]}</p>
                    </div>
                `;
                chatDemo.appendChild(botMessage);
                chatDemo.scrollTop = chatDemo.scrollHeight;
                demoResponseIndex++;
            }, 2000);

            chatDemo.scrollTop = chatDemo.scrollHeight;
        }

        // Enter key support for demo
        document.getElementById('demoInput').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendDemoMessage();
            }
        });

        // Modal functions
        function showLogin() {
            document.getElementById('loginModal').classList.remove('hidden');
            document.getElementById('loginModal').classList.add('flex');
        }

        function showRegister() {
            document.getElementById('registerModal').classList.remove('hidden');
            document.getElementById('registerModal').classList.add('flex');
        }

        function showEmergencyModal() {
            document.getElementById('emergencyModal').classList.remove('hidden');
            document.getElementById('emergencyModal').classList.add('flex');
        }

        function closeModal(modalId) {
            document.getElementById(modalId).classList.add('hidden');
            document.getElementById(modalId).classList.remove('flex');
        }

        function handleLogin(event) {
            event.preventDefault();
            alert('Demo: Login berhasil! Anda akan diarahkan ke dashboard.');
            closeModal('loginModal');
        }

        function handleRegister(event) {
            event.preventDefault();
            alert('Demo: Registrasi berhasil! Uji coba gratis 1 hari telah dimulai.');
            closeModal('registerModal');
        }

        function startTrial() {
            showRegister();
        }

        function showDemo() {
            document.getElementById('demoInput').focus();
        }

        function selectPlan(plan) {
            const plans = {
                trial: 'Uji Coba Gratis 1 Hari',
                weekly: 'Paket Mingguan - Rp 49.000',
                monthly: 'Paket Bulanan - Rp 149.000',
                yearly: 'Paket Tahunan - Rp 1.200.000'
            };
            alert(`Demo: Anda memilih ${plans[plan]}. Silakan daftar untuk melanjutkan.`);
            showRegister();
        }

        function callEmergency() {
            alert('Demo: Menghubungkan ke layanan darurat 112...\n\nDalam aplikasi nyata, ini akan langsung menghubungi layanan darurat.');
            closeModal('emergencyModal');
        }

        function connectPsychiatrist() {
            alert('Demo: Menghubungkan ke psikiater terdekat...\n\nAnda akan segera dihubungi oleh psikiater profesional.');
            closeModal('emergencyModal');
        }

        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'96c7ae1d5480ef6c',t:'MTc1NDc0Njk4Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
