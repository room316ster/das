<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ผู้ช่วยอัจฉริยะสำหรับผู้พิการทางสายตา</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Sarabun', sans-serif;
            touch-action: manipulation;
            background-color: #000000;
        }
        .loader {
            border: 8px solid #444;
            border-radius: 50%;
            border-top: 8px solid #facc15; /* yellow-400 */
            width: 80px;
            height: 80px;
            animation: spin 1.5s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .tab-button.active {
            background-color: #eab308; /* yellow-500 */
            color: #000000;
            border-bottom-color: #eab308;
        }
        .main-button {
            background-color: #facc15; /* yellow-400 */
            color: #000000;
        }
        .main-button:hover {
            background-color: #eab308; /* yellow-500 */
        }
        .main-button:disabled {
            background-color: #4b5563; /* gray-600 */
            color: #d1d5db; /* gray-300 */
            cursor: not-allowed;
        }
        #mic-btn.listening, #ask-mic-btn.listening {
            background-color: #ef4444; /* red-500 */
            color: white;
        }
        .gemini-feature-btn {
            background-color: #8b5cf6; /* violet-500 */
            color: white;
        }
        .gemini-feature-btn:hover {
            background-color: #7c3aed; /* violet-600 */
        }
    </style>
</head>
<body class="bg-black text-white flex flex-col items-center min-h-screen p-4">

    <div class="w-full max-w-lg mx-auto bg-black rounded-2xl p-4">
        <h1 class="text-3xl md:text-4xl font-bold text-center mb-6 text-yellow-400">ผู้ช่วยอัจฉริยะ</h1>

        <!-- Tab Navigation -->
        <div class="flex border-b-2 border-gray-700 mb-6" role="tablist" aria-label="เมนูหลัก">
            <button id="tab-recognize" role="tab" aria-selected="true" aria-controls="recognition-content" class="tab-button flex-1 py-4 text-xl font-bold text-gray-300 transition-colors duration-300 active">ระบุสิ่งของ</button>
            <button id="tab-navigate" role="tab" aria-selected="false" aria-controls="navigation-content" class="tab-button flex-1 py-4 text-xl font-bold text-gray-300 transition-colors duration-300">นำทาง</button>
        </div>

        <!-- Recognition Tab Content -->
        <div id="recognition-content" role="tabpanel" aria-labelledby="tab-recognize" class="tab-content space-y-6">
             <p class="text-center text-gray-300 text-lg">ส่องกล้องไปยังสิ่งที่ต้องการทราบ แล้วกดปุ่ม "วิเคราะห์ภาพ"</p>
            <div id="camera-container" class="relative w-full aspect-video bg-gray-800 rounded-xl overflow-hidden border-2 border-gray-700">
                <video id="video" class="w-full h-full object-cover" playsinline autoplay muted></video>
                <div id="status-text" class="absolute inset-0 flex items-center justify-center bg-black bg-opacity-75 text-white text-xl font-semibold">กำลังเปิดกล้อง...</div>
            </div>
            <canvas id="canvas" class="hidden"></canvas>
            <button id="capture-button" aria-label="วิเคราะห์ภาพที่แสดงในกล้อง" class="main-button w-full font-bold py-5 px-6 rounded-xl text-2xl transition-all duration-300 shadow-lg disabled:opacity-50">วิเคราะห์ภาพ</button>
            <button id="ask-more-btn" aria-label="ถามเพิ่มเติมเกี่ยวกับภาพนี้ด้วยเสียง" class="gemini-feature-btn w-full font-bold py-4 px-6 rounded-xl text-xl transition-all duration-300 shadow-lg mt-4 hidden">✨ ถามเกี่ยวกับภาพนี้</button>
        </div>

        <!-- Navigation Tab Content -->
        <div id="navigation-content" role="tabpanel" aria-labelledby="tab-navigate" class="tab-content hidden">
            <div class="space-y-6">
                <div class="text-center">
                    <p class="text-gray-300 text-lg">ช่วยเตรียมเส้นทางการเดินเท้า</p>
                </div>
                <button id="get-location-btn" aria-label="ค้นหาตำแหน่งปัจจุบันของฉันอีกครั้ง" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 px-4 rounded-lg text-xl transition">หาตำแหน่งอีกครั้ง</button>
                <div id="location-display" aria-live="polite" class="text-center text-gray-200 text-lg p-4 bg-gray-800 rounded-lg min-h-[60px]"></div>
                <div>
                    <label for="destination-input" class="block mb-2 text-xl font-semibold text-gray-200">จุดหมายปลายทาง:</label>
                    <div class="flex items-center space-x-2">
                        <input type="text" id="destination-input" class="w-full p-4 bg-gray-800 border-2 border-gray-600 rounded-lg text-xl focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 text-white" placeholder="พูดเพื่อบอกสถานที่...">
                        <button id="mic-btn" aria-label="พูดอีกครั้ง" class="p-4 bg-gray-600 hover:bg-gray-500 rounded-lg text-3xl transition">🎤</button>
                    </div>
                </div>
                <button id="find-route-btn" class="main-button w-full font-bold py-4 px-4 rounded-lg text-xl transition hidden">ค้นหาเส้นทาง</button>
            </div>
            <div id="route-result" class="mt-6 space-y-4"></div>
             <div id="trip-plan-result" class="mt-6"></div>
            <div class="mt-8 p-4 bg-red-900/50 border-2 border-red-500 rounded-lg text-center">
                <p class="font-bold text-red-300 text-xl">ข้อควรระวัง</p>
                <p class="text-red-300">ฟังก์ชันนี้เป็นเพียงผู้ช่วยเปิดแอปแผนที่ โปรดใช้ความระมัดระวังสูงสุดในการเดินทางเสมอ</p>
            </div>
        </div>
        
        <!-- Common Result Section -->
        <div id="result-section" class="mt-6">
            <div id="loader" class="hidden loader mx-auto"></div>
            <div id="result-container" tabindex="-1" aria-live="polite" class="bg-gray-800 p-4 rounded-xl hidden">
                <h2 id="result-title" class="text-2xl font-bold mb-3 text-yellow-400">ผลการวิเคราะห์:</h2>
                <p id="result-text" class="text-xl text-gray-200 whitespace-pre-wrap"></p>
            </div>
        </div>
    </div>

    <script>
        const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbyzo6onR4HCNwbahdSvOVEb5QJUPPb37hVasw-oMSfdDlPDGt9Hivm2VWNWCARlSpWVMw/exec';
        const GEMINI_API_KEY = "AIzaSyCIOLwOmFKzBz1U05KchcczG-W-nT-7EcU";

        // Elements
        const loader = document.getElementById('loader');
        const resultContainer = document.getElementById('result-container');
        const resultTitle = document.getElementById('result-title');
        const resultText = document.getElementById('result-text');
        const tabRecognize = document.getElementById('tab-recognize');
        const tabNavigate = document.getElementById('tab-navigate');
        const recognitionContent = document.getElementById('recognition-content');
        const navigationContent = document.getElementById('navigation-content');
        const video = document.getElementById('video');
        const canvas = document.getElementById('canvas');
        const captureButton = document.getElementById('capture-button');
        const askMoreBtn = document.getElementById('ask-more-btn');
        const statusText = document.getElementById('status-text');
        const getLocationBtn = document.getElementById('get-location-btn');
        const locationDisplay = document.getElementById('location-display');
        const destinationInput = document.getElementById('destination-input');
        const findRouteBtn = document.getElementById('find-route-btn');
        const routeResult = document.getElementById('route-result');
        const tripPlanResult = document.getElementById('trip-plan-result');
        const micBtn = document.getElementById('mic-btn');

        let stream;
        let thaiVoice = null;
        let isAudioUnlocked = false;
        let currentLocation = null;
        let lastCapturedImageData = null;
        const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
        let recognition;

        // --- Core Accessibility Functions ---
        function speakText(text) {
            if (!isAudioUnlocked) return;
            window.speechSynthesis.cancel();
            const utterance = new SpeechSynthesisUtterance(text);
            utterance.lang = 'th-TH';
            utterance.rate = 1.1;
            if (thaiVoice) utterance.voice = thaiVoice;
            window.speechSynthesis.speak(utterance);
        }
        
        function unlockAudio() {
            if (isAudioUnlocked) return;
            const silentUtterance = new SpeechSynthesisUtterance("");
            window.speechSynthesis.speak(silentUtterance);
            isAudioUnlocked = true;
        }

        function vibrate(duration = 50) {
            if ('vibrate' in navigator) {
                navigator.vibrate(duration);
            }
        }

        function showLoader(show) {
            loader.classList.toggle('hidden', !show);
        }

        function displayResult(title, text, isError = false) {
            resultTitle.textContent = title;
            resultText.textContent = text;
            resultContainer.className = `p-4 rounded-xl mt-6 ${isError ? 'bg-red-900' : 'bg-gray-800'}`;
            resultContainer.focus();
        }

        // --- Speech Recognition ---
        function startVoiceInput(prompt, onResultCallback) {
            if (recognition) {
                unlockAudio();
                vibrate();
                speakText(prompt);
                
                recognition.onresult = (event) => {
                    const transcript = event.results[0][0].transcript;
                    onResultCallback(transcript);
                };

                recognition.start();
                return true;
            }
            return false;
        }

        if (SpeechRecognition) {
            recognition = new SpeechRecognition();
            recognition.continuous = false;
            recognition.lang = 'th-TH';
            recognition.interimResults = false;
            recognition.maxAlternatives = 1;
            recognition.onspeechend = () => recognition.stop();
            recognition.onerror = (event) => speakText(`เกิดข้อผิดพลาดในการรับเสียง: ${event.error}`);
        }

        // --- Tab Management ---
        function switchTab(activeTabId) {
            const isRec = activeTabId === 'recognize';
            tabRecognize.setAttribute('aria-selected', isRec);
            tabNavigate.setAttribute('aria-selected', !isRec);
            tabRecognize.classList.toggle('active', isRec);
            tabNavigate.classList.toggle('active', !isRec);

            recognitionContent.classList.toggle('hidden', !isRec);
            navigationContent.classList.toggle('hidden', isRec);
            
            resultContainer.classList.add('hidden'); 
            routeResult.innerHTML = ''; 
            tripPlanResult.innerHTML = '';

            if (isRec) {
                speakText("เปิดแท็บ ระบุสิ่งของ");
                initCamera();
            } else {
                speakText("เปิดแท็บ นำทาง");
                stopCamera();
                startLocationSearch(); 
            }
        }

        tabRecognize.addEventListener('click', () => { vibrate(); switchTab('recognize'); });
        tabNavigate.addEventListener('click', () => { vibrate(); switchTab('navigate'); });

        // --- Object Recognition & Gemini Features ---
        async function initCamera() {
            if (stream || recognitionContent.classList.contains('hidden')) return;
            statusText.textContent = 'กำลังเปิดกล้อง...';
            statusText.classList.remove('hidden');
            try {
                stream = await navigator.mediaDevices.getUserMedia({ video: { facingMode: 'environment' } });
                video.srcObject = stream;
                video.onloadeddata = () => {
                    statusText.classList.add('hidden');
                    captureButton.disabled = false;
                    speakText("กล้องพร้อมใช้งาน");
                };
            } catch (err) {
                statusText.textContent = "ไม่สามารถเข้าถึงกล้องได้";
                speakText("ไม่สามารถเข้าถึงกล้องได้ โปรดอนุญาตในหน้าตั้งค่า");
            }
        }

        function stopCamera() {
            if (stream) {
                stream.getTracks().forEach(track => track.stop());
                stream = null;
            }
        }

        captureButton.addEventListener('click', async () => {
            unlockAudio();
            vibrate(100);
            if (!stream) return;
            
            captureButton.disabled = true;
            askMoreBtn.classList.add('hidden');
            showLoader(true);
            resultContainer.classList.add('hidden');

            canvas.width = video.videoWidth;
            canvas.height = video.videoHeight;
            canvas.getContext('2d').drawImage(video, 0, 0, canvas.width, canvas.height);
            lastCapturedImageData = canvas.toDataURL('image/jpeg', 0.8).split(',')[1];
            
            await analyzeImage(lastCapturedImageData);
            
            captureButton.disabled = false;
            showLoader(false);
        });

        async function analyzeImage(imageData) {
            const prompt = `นี่คือภาพจากกล้องของผู้พิการทางสายตา โปรดช่วยบรรยายสิ่งที่เห็นในภาพนี้ให้ละเอียดที่สุดเท่าที่จะทำได้ ถ้ามีข้อความใดๆ ในภาพ ให้ถอดข้อความนั้นออกมาด้วย และให้อยู่ในหัวข้อ "ข้อความที่พบ:" เริ่มการบรรยายภาพได้เลย`;
            const payload = { contents: [{ role: "user", parts: [{ text: prompt }, { inlineData: { mimeType: "image/jpeg", data: imageData } }] }] };
            try {
                const analysisText = await callGeminiAPI(payload);
                displayResult("ผลการวิเคราะห์:", analysisText);
                speakText(analysisText);
                askMoreBtn.classList.remove('hidden');
                sendDataToGoogleSheet(analysisText);
            } catch (error) {
                const userErrorMessage = `เกิดข้อผิดพลาดในการเชื่อมต่อกับ AI ค่ะ\n\nรายละเอียด: ${error.message}`;
                displayResult("เกิดข้อผิดพลาด:", userErrorMessage, true);
                speakText("เกิดข้อผิดพลาดในการเชื่อมต่อกับ AI ค่ะ");
            }
        }
        
        askMoreBtn.addEventListener('click', () => {
             micBtn.classList.remove('listening');
             micBtn.textContent = '🎤';
             micBtn.disabled = false;

            if (startVoiceInput("คุณต้องการทราบอะไรเพิ่มเติมเกี่ยวกับภาพนี้", async (question) => {
                showLoader(true);
                resultContainer.classList.add('hidden');
                speakText(`กำลังค้นหาคำตอบสำหรับคำถาม: ${question}`);
                const prompt = `จากภาพเดิมนี้ ช่วยตอบคำถามต่อไปนี้หน่อย: "${question}"`;
                const payload = { contents: [{ role: "user", parts: [{ text: prompt }, { inlineData: { mimeType: "image/jpeg", data: lastCapturedImageData } }] }] };
                try {
                    const answer = await callGeminiAPI(payload);
                    displayResult(`คำตอบสำหรับ "${question}":`, answer);
                    speakText(answer);
                } catch (error) {
                    const userErrorMessage = `เกิดข้อผิดพลาด: ${error.message}`;
                    displayResult("เกิดข้อผิดพลาด:", userErrorMessage, true);
                    speakText("ขออภัยค่ะ ไม่สามารถตอบคำถามนี้ได้");
                } finally {
                    showLoader(false);
                }
            })) {
                 // Speech recognition started
            }
        });

        // --- Navigation & Gemini Features ---
        function startLocationSearch() {
            unlockAudio();
            vibrate(100);
            locationDisplay.textContent = 'กำลังค้นหาตำแหน่ง...';
            speakText("กำลังค้นหาตำแหน่ง");
            navigator.geolocation.getCurrentPosition(
                async (position) => {
                    currentLocation = { lat: position.coords.latitude, lon: position.coords.longitude };
                    findRouteBtn.disabled = false; 
                    try {
                        const response = await fetch(`https://nominatim.openstreetmap.org/reverse?format=json&lat=${currentLocation.lat}&lon=${currentLocation.lon}&accept-language=th`);
                        const data = await response.json();
                        const address = data.display_name || 'ไม่พบชื่อที่อยู่';
                        locationDisplay.textContent = `ตำแหน่งปัจจุบัน: ${address}`;
                        speakText(`พบตำแหน่งปัจจุบันแล้ว คือ ${address}`);
                        setTimeout(() => {
                            if (startVoiceInput("คุณต้องการไปที่ใด", handleDestinationVoiceInput)) {
                                micBtn.classList.add('listening');
                                micBtn.textContent = '...';
                                micBtn.disabled = true;
                                recognition.onend = () => {
                                     micBtn.classList.remove('listening');
                                     micBtn.textContent = '🎤';
                                     micBtn.disabled = false;
                                };
                            }
                        }, 1200);
                    } catch (error) {
                        locationDisplay.textContent = 'ไม่สามารถแปลงพิกัดเป็นที่อยู่ได้';
                    }
                },
                (error) => {
                    const msg = error.code === 1 ? 'คุณไม่ได้อนุญาตให้เข้าถึงตำแหน่ง' : 'เกิดข้อผิดพลาดในการระบุตำแหน่ง';
                    locationDisplay.textContent = msg;
                    speakText(msg);
                },
                { enableHighAccuracy: true, timeout: 15000, maximumAge: 0 }
            );
        }
        
        getLocationBtn.addEventListener('click', startLocationSearch);

        function handleDestinationVoiceInput(transcript) {
            destinationInput.value = transcript;
            speakText(`รับข้อมูลแล้ว คือ ${transcript}, กำลังค้นหาเส้นทาง`);
            findRouteBtn.click();
        }
        
        micBtn.addEventListener('click', () => {
             if (startVoiceInput("กรุณาพูดชื่อสถานที่อีกครั้ง", handleDestinationVoiceInput)) {
                micBtn.classList.add('listening');
                micBtn.textContent = '...';
                micBtn.disabled = true;
                 recognition.onend = () => {
                     micBtn.classList.remove('listening');
                     micBtn.textContent = '🎤';
                     micBtn.disabled = false;
                };
             }
        });

        findRouteBtn.addEventListener('click', () => {
            vibrate();
            const destination = destinationInput.value.trim();
            if (!destination) return speakText("กรุณาป้อนจุดหมายปลายทาง");
            if (!currentLocation) return speakText("กรุณารอให้ระบบค้นหาตำแหน่งปัจจุบันให้เสร็จก่อน");
            
            const mapsUrl = `https://www.google.com/maps/dir/?api=1&origin=${currentLocation.lat},${currentLocation.lon}&destination=${encodeURIComponent(destination)}&travelmode=walking`;
            
            routeResult.innerHTML = `
                <a href="${mapsUrl}" target="_blank" aria-label="เปิดเส้นทางเดินเท้าไปยัง ${destination} ในแอปพลิเคชัน Google Maps" class="block w-full text-center bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-5 px-6 rounded-xl text-2xl transition">
                    เปิดใน Google Maps
                </a>
                <button id="plan-trip-btn" aria-label="ขอคำแนะนำเพิ่มเติมสำหรับการเดินทางนี้" class="gemini-feature-btn w-full font-bold py-4 px-6 rounded-xl text-xl transition-all duration-300 shadow-lg mt-4">✨ ขอคำแนะนำการเดินทาง</button>
            `;
            speakText(`เส้นทางไปยัง ${destination} พร้อมแล้ว กดปุ่มเพื่อเปิดใน Google Maps หรือ ขอคำแนะนำการเดินทาง`);
            
            document.getElementById('plan-trip-btn').addEventListener('click', planTripWithGemini);
            setTimeout(() => document.querySelector('#route-result a')?.focus(), 200);
        });

        async function planTripWithGemini() {
            vibrate();
            const destination = destinationInput.value.trim();
            speakText(`กำลังขอคำแนะนำการเดินทางไปยัง ${destination}`);
            showLoader(true);
            tripPlanResult.innerHTML = '';

            const prompt = `ในฐานะผู้เชี่ยวชาญด้านการเดินทางสำหรับผู้พิการทางสายตา โปรดให้คำแนะนำที่เป็นประโยชน์และข้อควรระวังสำหรับการเดินเท้าไปยัง "${destination}" โดยละเอียด เน้นสิ่งที่สำคัญ เช่น จุดสังเกตที่ชัดเจน (ใช้เสียงหรือสัมผัสได้), ลักษณะทางเท้า, ประตูทางเข้าที่เหมาะสม, หรือจุดที่ต้องระมัดระวังเป็นพิเศษ`;
            const payload = { contents: [{ role: "user", parts: [{ text: prompt }] }] };

            try {
                const advice = await callGeminiAPI(payload);
                tripPlanResult.innerHTML = `
                    <div class="bg-gray-800 p-4 rounded-xl">
                        <h3 class="text-2xl font-bold mb-3 text-yellow-400">✨ คำแนะนำการเดินทาง:</h3>
                        <p class="text-xl text-gray-200 whitespace-pre-wrap">${advice}</p>
                    </div>`;
                speakText("นี่คือคำแนะนำการเดินทางจาก AI ค่ะ");
                setTimeout(() => speakText(advice, true), 1000); // Speak the full advice
            } catch (error) {
                tripPlanResult.innerHTML = `<p class="text-red-400">ขออภัยค่ะ ไม่สามารถให้คำแนะนำได้ในขณะนี้</p>`;
                speakText("ขออภัยค่ะ ไม่สามารถให้คำแนะนำได้ในขณะนี้");
            } finally {
                showLoader(false);
            }
        }
        
        // --- Generic Gemini API Caller ---
        async function callGeminiAPI(payload) {
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${GEMINI_API_KEY}`;
            const response = await fetch(apiUrl, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload) });
            if (!response.ok) {
                 const errorBody = await response.json().catch(() => ({error: {message: `Request failed with status: ${response.status}`}}));
                 throw new Error(errorBody.error.message);
            }
            const result = await response.json();
            const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
            if (!text) {
                throw new Error("ไม่ได้รับคำตอบจาก AI หรือคำตอบอาจไม่เหมาะสม");
            }
            return text;
        }

        // --- Utility ---
        function sendDataToGoogleSheet(text) {
            fetch(SCRIPT_URL, { method: 'POST', mode: 'no-cors', body: JSON.stringify({ text: text }) })
            .catch(error => console.error('Error sending data to Google Sheet:', error));
        }

        function loadVoices() {
            const setVoice = () => {
                thaiVoice = window.speechSynthesis.getVoices().find(v => v.lang === 'th-TH');
                if (thaiVoice) console.log('Thai voice found:', thaiVoice.name);
            };
            setVoice();
            speechSynthesis.onvoiceschanged = setVoice;
        }

        // --- Start ---
        loadVoices();
        switchTab('recognize');
    </script>
</body>
</html>
