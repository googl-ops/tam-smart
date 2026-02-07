// Create Gold Particles
function createGoldParticles() {
    const container = document.getElementById('goldParticles');
    for (let i = 0; i < 50; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.left = Math.random() * 100 + '%';
        particle.style.animationDelay = Math.random() * 8 + 's';
        particle.style.animationDuration = (8 + Math.random() * 4) + 's';
        container.appendChild(particle);
    }
}
createGoldParticles();

// Create Musnad Particles - حروف مسند ذهبية تتطاير في الخلفية
function createMusnadParticles() {
    const container = document.getElementById('musnadParticles');
    // الحروف المسندية الصحيحة
    const musnadChars = ['𐩠', '𐩡', '𐩢', '𐩣', '𐩤', '𐩥', '𐩦', '𐩧', '𐩨', '𐩩', '𐩪', '𐩫', '𐩬', '𐩭', '𐩮', '𐩯', '𐩰', '𐩱', '𐩲', '𐩳', '𐩴', '𐩵', '𐩶', '𐩷', '𐩸', '𐩹', '𐩺', '𐩻', '𐩼'];
    
    for (let i = 0; i < 25; i++) {
        const char = document.createElement('div');
        char.className = 'musnad-char';
        char.textContent = musnadChars[Math.floor(Math.random() * musnadChars.length)];
        char.style.left = Math.random() * 100 + '%';
        char.style.top = Math.random() * 100 + '%';
        char.style.animationDelay = Math.random() * 20 + 's';
        char.style.animationDuration = (15 + Math.random() * 15) + 's';
        char.style.fontSize = (0.6 + Math.random() * 1.2) + 'rem';
        char.style.color = '#C8A44D';
        char.style.textShadow = '0 0 10px rgba(200, 164, 77, 0.6)';
        container.appendChild(char);
    }
}
createMusnadParticles();

// Create Golden Wolves - الوعل الذهبي من الصورة
function createGoldenWolves() {
    const container = document.getElementById('wolvesContainer');
    
    // SVG للوعل الذهبي مشابه للصورة
    const wolfSVG = `data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
        <path d="M30,80 Q25,60 35,50 Q30,40 40,30 Q45,20 50,25 Q55,20 60,30 Q70,40 65,50 Q75,60 70,80 Z" 
        fill="%23C8A44D" stroke="%23B8941F" stroke-width="2"/>
        <circle cx="45" cy="35" r="3" fill="%23000"/>
        <circle cx="55" cy="35" r="3" fill="%23000"/>
        <path d="M48,42 Q50,45 52,42" stroke="%23000" fill="none"/>
        <path d="M40,25 Q35,15 45,20" fill="%23C8A44D" stroke="%23B8941F"/>
        <path d="M60,25 Q65,15 55,20" fill="%23C8A44D" stroke="%23B8941F"/>
    </svg>`;
    
    for (let i = 0; i < 10; i++) {
        const wolf = document.createElement('div');
        wolf.className = 'golden-wolf';
        wolf.style.backgroundImage = `url('${wolfSVG}')`;
        wolf.style.left = '-15%';
        wolf.style.top = (5 + Math.random() * 70) + '%';
        wolf.style.animationDelay = Math.random() * 25 + 's';
        wolf.style.animationDuration = (20 + Math.random() * 15) + 's';
        wolf.style.width = (40 + Math.random() * 40) + 'px';
        wolf.style.height = wolf.style.width;
        container.appendChild(wolf);
    }
}
createGoldenWolves();

// Hide Loader
window.addEventListener('load', () => {
    setTimeout(() => {
        document.getElementById('loader').classList.add('hidden');
    }, 2500);
});

// Custom Cursor
const cursor = document.getElementById('cursor');
const cursorGlow = document.getElementById('cursorGlow');
const isTouchDevice = window.matchMedia("(pointer: coarse)").matches;

if (!isTouchDevice) {
    cursor.style.display = 'block';
    cursorGlow.style.display = 'block';
    
    document.addEventListener('mousemove', (e) => {
        cursor.style.left = e.clientX - 10 + 'px';
        cursor.style.top = e.clientY - 10 + 'px';
        setTimeout(() => {
            cursorGlow.style.left = e.clientX - 20 + 'px';
            cursorGlow.style.top = e.clientY - 20 + 'px';
        }, 80);
    });
}

// Menu
const menuTrigger = document.getElementById('menuTrigger');
const sideMenu = document.getElementById('sideMenu');
const menuOverlay = document.getElementById('menuOverlay');

menuTrigger.addEventListener('click', () => {
    menuTrigger.classList.toggle('active');
    sideMenu.classList.toggle('active');
    menuOverlay.classList.toggle('active');
});

menuOverlay.addEventListener('click', () => {
    menuTrigger.classList.remove('active');
    sideMenu.classList.remove('active');
    menuOverlay.classList.remove('active');
});

// Governorates Data - تم تعديل الأيقونات حسب المطلوب
const governorates = [
    { name: "أمانة العاصمة", nickname: "آزال", icon: "fa-crown", poets: 45 },
    { name: "صنعاء", nickname: "مدينة سام", icon: "fa-building", poets: 32 },
    { name: "عدن", nickname: "عين اليمن", icon: "fa-water", poets: 28 },
    { name: "تعز", nickname: "الجند", icon: "fa-chess-rook", poets: 38 },
    { name: "إب", nickname: "ذو جبلة", icon: "fa-leaf", poets: 22 },
    { name: "حضرموت", nickname: "الأحقاف", icon: "fa-city", poets: 42 },
    // مارب - معبد أوام: أيقونة أعمدة/معبد
    { name: "مأرب", nickname: "أرض الجنتين", icon: "fa-columns", poets: 35 },
    { name: "الحديدة", nickname: "زبيد", icon: "fa-mosque", poets: 18 },
    { name: "الجوف", nickname: "مَعين", icon: "fa-scroll", poets: 15 },
    // ذمار - تمثال الملك ذمار علي: أيقونة تمثال/نصب تذكاري
    { name: "ذمار", nickname: "كرسي حمير", icon: "fa-monument", poets: 20 },
    { name: "شبوة", nickname: "عاصمة الملح والبخور", icon: "fa-fire-alt", poets: 25 },
    { name: "الضالع", nickname: "ريدان", icon: "fa-shield-alt", poets: 12 },
    { name: "البيضاء", nickname: "سرو مذحج", icon: "fa-mountain", poets: 16 },
    { name: "لحج", nickname: "المحروسة", icon: "fa-seedling", poets: 14 },
    // أبين - مملكة قديمة: أيقونة قلعة/حصن
    { name: "أبين", nickname: "دثينة", icon: "fa-fort-awesome", poets: 19 },
    { name: "المهرة", nickname: "البوابة الشرقية", icon: "fa-door-open", poets: 10 },
    { name: "صعدة", nickname: "صعدة الحديد", icon: "fa-archway", poets: 21 },
    { name: "عمران", nickname: "ظفار", icon: "fa-chair", poets: 17 },
    { name: "حجة", nickname: "حصن الملوك", icon: "fa-dungeon", poets: 23 },
    { name: "المحويت", nickname: "معانقة الغيم", icon: "fa-cloud", poets: 13 },
    { name: "ريمة", nickname: "الحدائق المعلقة", icon: "fa-layer-group", poets: 11 }
];

// Render Governorates
function renderGovernorates(containerId, portalType) {
    const container = document.getElementById(containerId);
    if (!container) return;
    
    container.innerHTML = governorates.map((gov, index) => `
        <div class="gov-card" onclick="openGovernorate(${index}, '${portalType}')" data-index="${index}">
            <i class="fas ${gov.icon} gov-icon"></i>
            <h3 class="gov-name">${gov.name}</h3>
            <p class="gov-nickname">${gov.nickname}</p>
            <div class="view-counter">
                <i class="fas fa-eye"></i>
                <span>${Math.floor(Math.random() * 5000) + 1000}</span>
            </div>
        </div>
    `).join('');
}

renderGovernorates('governoratesGrid', 'poetry');
renderGovernorates('storiesGovGrid', 'stories');
renderGovernorates('proverbsGovGrid', 'proverbs');
renderGovernorates('theaterGovGrid', 'theater');
renderGovernorates('childrenGovGrid', 'children');
renderGovernorates('artGovGrid', 'art');

// Fill Governorate Select
const uploadGovSelect = document.getElementById('uploadGovernorate');
if (uploadGovSelect) {
    governorates.forEach(gov => {
        const option = document.createElement('option');
        option.value = gov.name;
        option.textContent = gov.name;
        uploadGovSelect.appendChild(option);
    });
}

// Open Governorate - مع تأثير حركة التحرك
function openGovernorate(index, portalType) {
    const gov = governorates[index];
    
    // تأثير حركة التحرك
    const card = document.querySelector(`[data-index="${index}"]`);
    if (card) {
        card.style.transform = 'translateY(-20px) scale(0.95)';
        setTimeout(() => {
            card.style.transform = '';
        }, 200);
    }
    
    setTimeout(() => {
        if (portalType === 'poetry') {
            document.getElementById('poetryGovTitle').textContent = gov.name + ' - ' + gov.nickname;
            showPage('governorate-poetry-page');
        } else if (portalType === 'stories') {
            document.getElementById('storiesGovTitle').textContent = gov.name + ' - ' + gov.nickname;
            showPage('governorate-stories-page');
        } else if (portalType === 'proverbs') {
            document.getElementById('proverbsGovTitle').textContent = gov.name + ' - ' + gov.nickname;
            showPage('governorate-proverbs-page');
        } else if (portalType === 'theater') {
            document.getElementById('theaterGovTitle').textContent = gov.name + ' - ' + gov.nickname;
            showPage('governorate-theater-page');
        } else if (portalType === 'children') {
            document.getElementById('childrenGovTitle').textContent = gov.name + ' - ' + gov.nickname;
            showPage('governorate-children-page');
        } else if (portalType === 'art') {
            document.getElementById('artGovTitle').textContent = gov.name + ' - ' + gov.nickname;
            showPage('governorate-art-page');
        }
    }, 300);
}

// Navigation
function showPage(pageId) {
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });
    
    const targetPage = document.getElementById(pageId);
    if (targetPage) {
        targetPage.classList.add('active');
    }
    
    menuTrigger.classList.remove('active');
    sideMenu.classList.remove('active');
    menuOverlay.classList.remove('active');
    
    window.scrollTo(0, 0);
}

// Show Category
function showCategory(category) {
    const messages = {
        'faseeh-amoudi': 'سيتم فتح قسم الشعر الفصيح العمودي مع الفراهيدي الذكي للتحقق العروضي',
        'faseeh-tafila': 'سيتم فتح قسم الشعر الفصيح التفعيلة مع الفراهيدي الذكي',
        'nathr': 'سيتم فتح قسم النثر الأدبي مع المدقق اللغوي الذكي',
        'himyari': 'سيتم فتح قسم الشعر الحميني (النشر المباشر بدون فحص عروضي)',
        'novel': 'سيتم فتح قسم الروايات من هذه المحافظة',
        'short-story': 'سيتم فتح قسم القصص القصيرة من هذه المحافظة',
        'flash-fiction': 'سيتم فتح قسم القصص القصيرة جداً من هذه المحافظة',
        'thought': 'سيتم فتح قسم الخواطر والمقالات من هذه المحافظة',
        'general-proverbs': 'سيتم فتح قسم الأمثال العامة من هذه المحافظة',
        'agricultural-proverbs': 'سيتم فتح قسم الأمثال الزراعية من هذه المحافظة',
        'social-proverbs': 'سيتم فتح قسم الأمثال الاجتماعية من هذه المحافظة',
        'weather-proverbs': 'سيتم فتح قسم الأمثال المناخية من هذه المحافظة',
        'theater-plays': 'سيتم فتح قسم المسرحيات من هذه المحافظة',
        'drama-films': 'سيتم فتح قسم الأفلام الدرامية من هذه المحافظة',
        'theater-teams': 'سيتم فتح قسم الفرق المسرحية من هذه المحافظة',
        'actors': 'سيتم فتح قسم الممثلين من هذه المحافظة',
        'folktales': 'سيتم فتح قسم الحكايات الشعبية من هذه المحافظة',
        'riddles': 'سيتم فتح قسم الألغاز والأحاجي من هذه المحافظة',
        'educational-stories': 'سيتم فتح قسم القصص التعليمية من هذه المحافظة',
        'songs': 'سيتم فتح قسم الأناشيد والأغاني من هذه المحافظة',
        'abstract-art': 'سيتم فتح قسم الفن التجريدي من هذه المحافظة',
        'realism-art': 'سيتم فتح قسم الفن الواقعي من هذه المحافظة',
        'impressionism-art': 'سيتم فتح قسم الفن الانطباعي من هذه المحافظة',
        'expressionism-art': 'سيتم فتح قسم الفن التعبيري من هذه المحافظة',
        'surrealism-art': 'سيتم فتح قسم الفن السريالي من هذه المحافظة',
        'calligraphy': 'سيتم فتح قسم الخط العربي من هذه المحافظة',
        'poetry-studies': 'سيتم فتح قسم الدراسات الشعرية',
        'narrative-studies': 'سيتم فتح قسم الدراسات السردية',
        'theater-studies': 'سيتم فتح قسم دراسات المسرح',
        'comparative-studies': 'سيتم فتح قسم الدراسات المقارنة',
        'rhetoric-studies': 'سيتم فتح قسم دراسات البلاغة والنقد القديم',
        'cultural-studies': 'سيتم فتح قسم الدراسات الثقافية'
    };
    
    alert(messages[category] || 'قيد التطوير');
}

// Update Upload Form
function updateUploadForm() {
    const type = document.getElementById('uploadType').value;
    const info = document.querySelector('.ai-checker-info p');
    
    if (type.includes('poem')) {
        info.textContent = 'سيتم فحص القصيدة عروضياً ونحوياً وإملائياً بواسطة الفراهيدي الذكي قبل النشر';
    } else {
        info.textContent = 'سيتم فحص النص نحوياً وإملائياً بواسطة المدقق اللغوي الذكي قبل النشر';
    }
}

// Show Upload Type
function showUploadType(type) {
    document.querySelectorAll('.upload-tab').forEach(tab => tab.classList.remove('active'));
    event.target.classList.add('active');
    
    document.getElementById('upload-writing-section').style.display = 'none';
    document.getElementById('upload-book-section').style.display = 'none';
    document.getElementById('upload-media-section').style.display = 'none';
    
    document.getElementById('upload-' + type + '-section').style.display = 'block';
}

// Submit Upload
function submitUpload() {
    const type = document.getElementById('uploadType').value;
    const gov = document.getElementById('uploadGovernorate').value;
    const title = document.getElementById('uploadTitle').value;
    const content = document.getElementById('uploadContent').value;
    const author = document.getElementById('uploadAuthor').value;
    
    if (!type || !gov || !title || !content || !author) {
        alert('يرجى ملء جميع الحقول المطلوبة بما فيها الاسم');
        return;
    }
    
    if (type.includes('poem')) {
        alert(`جاري فحص القصيدة بواسطة الفراهيدي الذكي...\n\n✓ فحص البحر العروضي\n✓ فحص القافية\n✓ فحص نحوي وإملائي\n\nبعد الموافقة، ستنشر تلقائياً في قسم ${gov}`);
    } else {
        alert(`جاري فحص النص بواسطة المدقق اللغوي الذكي...\n\n✓ فحص نحوي\n✓ فحص إملائي\n\nبعد الموافقة، ستنشر تلقائياً في قسم ${gov}`);
    }
}

// Books Data
const modernBooks = [
    { title: 'ديوان البردوني', author: 'عبدالله البردوني', category: 'شعر فصيح' },
    { title: 'انثيالات في محراب تام', author: 'مجموعة شعراء', category: 'أنطولوجيا' },
    { title: 'حكايات يمنية', author: 'تراث شعبي', category: 'أدب أطفال' },
    { title: 'أمثال اليمن', author: 'مجموعة مؤلفين', category: 'تراث شعبي' },
    { title: 'مسرحية صنعاء', author: 'أحمد اليمني', category: 'مسرح' },
    { title: 'صنعاء عاصمة العرب', author: 'محمد عبدالوهاب', category: 'تاريخ' },
    { title: 'الأدب اليمني الحديث', author: 'د. عبدالله الحبشي', category: 'نقد أدبي' },
    { title: 'يمن القرن العشرين', author: 'د. محمد عزان', category: 'تاريخ' }
];

const classicalBooks = [
    { title: 'ديوان النابغة الجعدي', author: 'النابغة الجعدي', category: 'شعر قديم' },
    { title: 'ديوان ذي الرمة', author: 'ذي الرمة', category: 'شعر جاهلي' },
    { title: 'الأغاني', author: 'أبو الفرج الأصفهاني', category: 'أدب قديم' },
    { title: 'ديوان عنترة بن شداد', author: 'عنترة بن شداد', category: 'شعر جاهلي' },
    { title: 'المعلقات السبع', author: 'شعراء جاهليون', category: 'شعر جاهلي' },
    { title: 'ديوان امرؤ القيس', author: 'امرؤ القيس', category: 'شعر جاهلي' },
    { title: 'الكامل في التاريخ', author: 'ابن الأثير', category: 'تاريخ' },
    { title: 'صبح الأعشى', author: 'القلقشندي', category: 'أدب قديم' }
];

function renderBooks() {
    const modernGrid = document.getElementById('modernBooksGrid');
    const classicalGrid = document.getElementById('classicalBooksGrid');
    
    if (modernGrid) {
        modernGrid.innerHTML = modernBooks.map(book => `
            <div class="book-card">
                <div class="book-cover"><i class="fas fa-book" style="color: var(--aged-gold);"></i></div>
                <h4 style="color: var(--sandstone-cream);">${book.title}</h4>
                <p style="color: var(--electric-turquoise); font-size: 1rem;">${book.author}</p>
                <span style="color: rgba(245, 240, 227, 0.7); font-size: 0.9rem;">${book.category}</span>
                <div class="book-actions">
                    <button class="btn-small btn-read"><i class="fas fa-eye"></i> قراءة</button>
                    <button class="btn-small btn-download"><i class="fas fa-download"></i> تحميل</button>
                </div>
            </div>
        `).join('');
    }
    
    if (classicalGrid) {
        classicalGrid.innerHTML = classicalBooks.map(book => `
            <div class="book-card">
                <div class="book-cover"><i class="fas fa-scroll" style="color: var(--aged-gold);"></i></div>
                <h4 style="color: var(--sandstone-cream);">${book.title}</h4>
                <p style="color: var(--electric-turquoise); font-size: 1rem;">${book.author}</p>
                <span style="color: rgba(245, 240, 227, 0.7); font-size: 0.9rem;">${book.category}</span>
                <div class="book-actions">
                    <button class="btn-small btn-read"><i class="fas fa-eye"></i> قراءة</button>
                    <button class="btn-small btn-download"><i class="fas fa-download"></i> تحميل</button>
                </div>
            </div>
        `).join('');
    }
}
renderBooks();

// Show Library Section
function showLibrarySection(section) {
    document.querySelectorAll('.upload-tab').forEach(tab => tab.classList.remove('active'));
    event.target.classList.add('active');
    
    document.querySelectorAll('.library-section').forEach(s => s.style.display = 'none');
    document.getElementById('library-' + section).style.display = 'block';
}

// Upload Book
function uploadBook() {
    const title = document.getElementById('bookTitle').value;
    const author = document.getElementById('bookAuthor').value;
    const category = document.getElementById('bookCategory').value;
    
    if (!title || !author || !category) {
        alert('يرجى ملء جميع الحقول المطلوبة');
        return;
    }
    
    alert(`تم رفع الكتاب "${title}" بنجاح!\n\nسيتم مراجعته قبل النشر.`);
}

// Search Writers
function searchWriters() {
    const query = document.getElementById('writerSearchInput').value;
    const resultsContainer = document.getElementById('searchResults');
    
    if (!query.trim()) {
        alert('يرجى إدخال كلمة البحث');
        return;
    }
    
    const sampleResults = [
        { name: 'عبدالله البردوني', type: 'شاعر', bio: 'أحد أبرز شعراء اليمن في العصر الحديث' },
        { name: 'الزبيري', type: 'شاعر', bio: 'شاعر يمني معاصر' },
        { name: 'ديوان البردوني', type: 'كتاب', bio: 'مجموعة شعرية' }
    ];
    
    resultsContainer.innerHTML = sampleResults.map(r => `
        <div class="result-card">
            <span class="result-type">${r.type}</span>
            <h4 style="color: var(--aged-gold); margin: 0.8rem 0;">${r.name}</h4>
            <p style="color: rgba(245, 240, 227, 0.8);">${r.bio}</p>
        </div>
    `).join('');
}

// AI Assistant Chat
function openAIChat() {
    alert('المساعد الذكي: مرحباً بك في تام الثقافية! 🤖\n\nأنا هنا لمساعدتك في:\n• البحث عن شعراء وكتاب وقصائد\n• التحليل العروضي (الفراهيدي الذكي)\n• التدقيق اللغوي\n• رفع المشاركات والكتب\n• تصفح المحتوى الثقافي\n• قراءة وتحميل الكتب\n\nكيف يمكنني مساعدتك اليوم؟');
}

// AI Assistant Bubble Animation Cycle
const aiBubble = document.getElementById('aiBubble');
const bubbleMessages = [
    'أنا المساعد الذكي',
    'مرحباً بك في تام الثقافية'
];
let bubbleCycleCount = 0;
let bubbleTimeout;

function showBubbleMessage(message, duration, callback) {
    if (!aiBubble) return;
    aiBubble.textContent = message;
    aiBubble.classList.add('show');
    
    setTimeout(() => {
        aiBubble.classList.remove('show');
        if (callback) {
            setTimeout(callback, 300);
        }
    }, duration);
}

function runBubbleCycle() {
    if (bubbleCycleCount >= 3) return;
    
    showBubbleMessage(bubbleMessages[0], 4000, () => {
        showBubbleMessage(bubbleMessages[1], 4000, () => {
            bubbleCycleCount++;
            
            let pauseDuration;
            if (bubbleCycleCount === 1) {
                pauseDuration = 5000;
            } else if (bubbleCycleCount === 2) {
                pauseDuration = 10000;
            } else {
                setTimeout(() => {
                    bubbleCycleCount = 0;
                    runBubbleCycle();
                }, 30 * 60 * 1000);
                return;
            }
            
            bubbleTimeout = setTimeout(runBubbleCycle, pauseDuration);
        });
    });
}

setTimeout(runBubbleCycle, 3000);

// تأثيرات إضافية للنقر على البوابات والمحافظات
document.addEventListener('DOMContentLoaded', () => {
    // إضافة تأثير النقر للبوابات
    const portalCards = document.querySelectorAll('.portal-card');
    portalCards.forEach(card => {
        card.addEventListener('click', function(e) {
            const ripple = document.createElement('div');
            ripple.style.position = 'absolute';
            ripple.style.borderRadius = '50%';
            ripple.style.background = 'rgba(200, 164, 77, 0.3)';
            ripple.style.transform = 'scale(0)';
            ripple.style.animation = 'ripple 0.6s linear';
            ripple.style.pointerEvents = 'none';
            
            const rect = this.getBoundingClientRect();
            const size = Math.max(rect.width, rect.height);
            ripple.style.width = ripple.style.height = size + 'px';
            ripple.style.left = (e.clientX - rect.left - size/2) + 'px';
            ripple.style.top = (e.clientY - rect.top - size/2) + 'px';
            
            this.appendChild(ripple);
            
            setTimeout(() => ripple.remove(), 600);
        });
    });
    
    // إضافة تأثير النقر للمحافظات
    const govCards = document.querySelectorAll('.gov-card');
    govCards.forEach(card => {
        card.addEventListener('click', function(e) {
            const ripple = document.createElement('div');
            ripple.style.position = 'absolute';
            ripple.style.borderRadius = '50%';
            ripple.style.background = 'rgba(200, 164, 77, 0.3)';
            ripple.style.transform = 'scale(0)';
            ripple.style.animation = 'ripple 0.6s linear';
            ripple.style.pointerEvents = 'none';
            
            const rect = this.getBoundingClientRect();
            const size = Math.max(rect.width, rect.height);
            ripple.style.width = ripple.style.height = size + 'px';
            ripple.style.left = (e.clientX - rect.left - size/2) + 'px';
            ripple.style.top = (e.clientY - rect.top - size/2) + 'px';
            
            this.appendChild(ripple);
            
            setTimeout(() => ripple.remove(), 600);
        });
    });
});

// CSS animation for ripple effect
const style = document.createElement('style');
style.textContent = `
    @keyframes ripple {
        to {
            transform: scale(4);
            opacity: 0;
        }
    }
`;
document.head.appendChild(style);

window.addEventListener('resize', () => {});
