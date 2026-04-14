# Cadets-Men-Fellowship-
for growth
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadets Men Fellowship • Iron Sharpens Iron</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap');
        
        body { font-family: 'Inter', system_ui, sans-serif; }
        .logo-font { font-family: 'Space Grotesk', sans-serif; }

        .hero-bg {
            background: linear-gradient(rgba(15, 23, 42, 0.9), rgba(15, 23, 42, 0.95)), 
                        url('https://picsum.photos/id/1016/2000/1200') center/cover no-repeat;
        }

        .glass {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(12px);
        }

        .member-card {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .member-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 30px 60px -15px rgb(245 158 11 / 0.4);
        }

        .modal {
            animation: modalPop 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
        }
        
        @keyframes modalPop {
            from { opacity: 0; transform: scale(0.8) translateY(40px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100">

    <!-- NAVBAR -->
    <nav class="sticky top-0 z-50 bg-slate-950/95 backdrop-blur-lg border-b border-amber-400/20">
        <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
            <div class="flex items-center gap-x-3">
                <div class="w-11 h-11 bg-gradient-to-br from-amber-400 to-orange-500 rounded-3xl flex items-center justify-center text-4xl shadow-xl">⚔️</div>
                <div>
                    <h1 class="logo-font text-3xl font-bold tracking-tighter">CADETS</h1>
                    <p class="text-xs text-amber-400 tracking-[3px] -mt-1">MEN FELLOWSHIP</p>
                </div>
            </div>

            <div class="hidden md:flex items-center gap-x-9 text-sm font-medium">
                <a onclick="scrollToSection('home')" class="hover:text-amber-400 cursor-pointer">Home</a>
                <a onclick="scrollToSection('members')" class="hover:text-amber-400 cursor-pointer">Members</a>
                <a onclick="scrollToSection('announcements')" class="hover:text-amber-400 cursor-pointer">Announcements</a>
                <a onclick="scrollToSection('socialize')" class="hover:text-amber-400 cursor-pointer">Socialize</a>
                <a onclick="scrollToSection('grow')" class="hover:text-amber-400 cursor-pointer">Grow</a>
            </div>

            <button onclick="showJoinModal()" 
                    class="bg-gradient-to-r from-amber-400 to-orange-500 text-slate-950 font-bold px-8 py-3.5 rounded-3xl text-sm tracking-wider hover:scale-105">
                JOIN THE BROTHERHOOD
            </button>
        </div>
    </nav>

    <!-- HERO -->
    <section id="home" class="hero-bg min-h-screen flex items-center">
        <div class="max-w-7xl mx-auto px-6 text-center md:text-left">
            <h1 class="text-6xl md:text-7xl font-bold logo-font leading-none tracking-tighter mb-6">
                UNITED AS ONE.<br>STRONGER TOGETHER.
            </h1>
            <p class="max-w-xl mx-auto md:mx-0 text-2xl text-slate-300">A fellowship of men committed to faith, accountability, and purposeful living.</p>
        </div>
    </section>

    <!-- MEMBERS SECTION -->
    <section id="members" class="py-24 bg-slate-900">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-end mb-12">
                <div>
                    <span class="inline-block px-6 py-2 bg-amber-400 text-slate-950 font-bold rounded-3xl text-sm">BROTHERHOOD DIRECTORY</span>
                    <h2 class="text-5xl font-bold logo-font mt-4">Our Cadets</h2>
                </div>
            </div>

            <!-- Leadership Team -->
            <div class="mb-16">
                <h3 class="text-2xl font-semibold mb-8 flex items-center gap-x-3">
                    <i class="fa-solid fa-crown text-amber-400"></i> Leadership Team
                </h3>
                <div id="leadership-grid" class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- JS populated -->
                </div>
            </div>

            <!-- Filters -->
            <div class="flex flex-wrap gap-4 mb-10">
                <input id="search-input" onkeyup="applyFilters()" 
                       placeholder="Search name or bio..." 
                       class="flex-1 min-w-[280px] bg-slate-800 border border-slate-700 focus:border-amber-400 px-6 py-4 rounded-3xl outline-none">

                <select id="location-filter" onchange="applyFilters()" 
                        class="bg-slate-800 border border-slate-700 px-6 py-4 rounded-3xl outline-none">
                    <option value="">All Locations</option>
                    <option value="Nairobi">Nairobi</option>
                    <option value="Kiambu">Kiambu</option>
                    <option value="Nakuru">Nakuru</option>
                    <option value="Machakos">Machakos</option>
                </select>

                <select id="role-filter" onchange="applyFilters()" 
                        class="bg-slate-800 border border-slate-700 px-6 py-4 rounded-3xl outline-none">
                    <option value="">All Roles</option>
                    <option value="Coordinator">Coordinator</option>
                    <option value="Leader">Leader</option>
                    <option value="Facilitator">Facilitator</option>
                </select>

                <select id="joined-filter" onchange="applyFilters()" 
                        class="bg-slate-800 border border-slate-700 px-6 py-4 rounded-3xl outline-none">
                    <option value="">Joined Any Time</option>
                    <option value="2025">2025</option>
                    <option value="2024">2024</option>
                    <option value="2023">2023</option>
                </select>

                <button onclick="resetFilters()" 
                        class="px-8 py-4 bg-slate-700 hover:bg-slate-600 rounded-3xl text-sm font-medium">
                    Reset
                </button>
            </div>

            <!-- Members Grid -->
            <div id="members-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                <!-- Populated by JS -->
            </div>
        </div>
    </section>

    <!-- MEMBER PROFILE MODAL -->
    <div id="profile-modal" class="hidden fixed inset-0 bg-black/80 backdrop-blur-sm z-[9999] flex items-center justify-center p-4">
        <div class="modal bg-slate-900 max-w-2xl w-full rounded-3xl overflow-hidden">
            <div class="h-2 bg-gradient-to-r from-amber-400 to-orange-500"></div>
            
            <div class="p-10">
                <div class="flex justify-end">
                    <button onclick="closeModal()" class="text-3xl text-slate-400 hover:text-white">×</button>
                </div>
                
                <div id="modal-content" class="text-center md:text-left">
                    <!-- Dynamic content injected here by JS -->
                </div>
            </div>
        </div>
    </div>

    <!-- Keep your previous sections (Announcements, Socialize, Grow, Gallery) here if you want the full page -->
    <!-- For this response, the focus is on the enhanced Members section. You can merge with previous code. -->

    <script>
        // Full Members Data
        let allMembers = [
            { id: 1, name: "Samuel Kiprono", role: "Fellowship Coordinator", location: "Nairobi", joined: "2024", avatar: "👑", bio: "Visionary leader passionate about raising strong, godly men who lead with integrity.", status: "online", quote: "The strength of the pack is the wolf, and the strength of the wolf is the pack." },
            { id: 2, name: "Kevin Omondi", role: "Prayer & Worship Leader", location: "Kiambu", joined: "2024", avatar: "🙏", bio: "Creating atmospheres of genuine worship and intercession among men.", status: "online", quote: "Prayer is not preparation for the battle. Prayer is the battle." },
            { id: 3, name: "Michael Waweru", role: "Outreach Coordinator", location: "Nakuru", joined: "2023", avatar: "🌍", bio: "Extending the hand of fellowship to men in different counties and walks of life.", status: "offline", quote: "Go and make disciples of all nations." },
            { id: 4, name: "David Mutua", role: "Bible Study Facilitator", location: "Nairobi", joined: "2024", avatar: "📖", bio: "Helping men fall deeper in love with the Word of God through systematic study.", status: "online", quote: "Your word is a lamp to my feet and a light to my path." },
            { id: 5, name: "Joseph Kamau", role: "Events & Logistics Leader", location: "Machakos", joined: "2023", avatar: "🏔️", bio: "Organizing life-changing hikes, retreats, and fellowship gatherings.", status: "offline", quote: "Faith without works is dead." },
            { id: 6, name: "Paul Ndung'u", role: "Accountability Group Leader", location: "Nairobi", joined: "2025", avatar: "🔥", bio: "Running multiple small accountability groups focused on transparency and growth.", status: "online", quote: "Iron sharpens iron, so one man sharpens another." }
        ]

        let leadership = allMembers.slice(0, 3) // First 3 are leaders

        function renderLeadership() {
            const container = document.getElementById('leadership-grid')
            container.innerHTML = ''
            leadership.forEach(member => {
                const card = document.createElement('div')
                card.className = "glass border border-amber-400/30 rounded-3xl p-8 text-center"
                card.innerHTML = `
                    <div class="text-6xl mb-6">${member.avatar}</div>
                    <h4 class="font-semibold text-xl">${member.name}</h4>
                    <p class="text-amber-400 text-sm">${member.role}</p>
                    <button onclick="showProfile(${member.id})" class="mt-6 text-xs uppercase tracking-widest border border-amber-400 px-6 py-3 rounded-3xl hover:bg-amber-400 hover:text-slate-950">View Profile</button>
                `
                container.appendChild(card)
            })
        }

        function renderMembers(membersToShow) {
            const container = document.getElementById('members-grid')
            container.innerHTML = ''

            membersToShow.forEach(member => {
                const div = document.createElement('div')
                div.className = `member-card bg-slate-800 border border-slate-700 rounded-3xl overflow-hidden cursor-pointer`
                div.onclick = () => showProfile(member.id)
                div.innerHTML = `
                    <div class="px-8 pt-8 pb-6">
                        <div class="flex justify-between">
                            <div class="text-6xl">${member.avatar}</div>
                            ${member.status === 'online' ? `<div class="flex items-center gap-x-1.5 text-emerald-400 text-xs"><div class="w-2.5 h-2.5 bg-emerald-400 rounded-full animate-pulse"></div> ONLINE</div>` : ''}
                        </div>
                        <h3 class="mt-8 text-2xl font-semibold">${member.name}</h3>
                        <p class="text-amber-400">${member.role}</p>
                        <p class="text-slate-400 text-sm mt-1">${member.location} • Joined ${member.joined}</p>
                    </div>
                `
                container.appendChild(div)
            })
        }

        function showProfile(id) {
            const member = allMembers.find(m => m.id === id)
            if (!member) return

            const modalContent = document.getElementById('modal-content')
            modalContent.innerHTML = `
                <div class="flex flex-col md:flex-row gap-10 items-center md:items-start">
                    <div class="text-[120px] md:text-[140px] flex-shrink-0">${member.avatar}</div>
                    <div class="flex-1">
                        <h2 class="text-4xl font-bold">${member.name}</h2>
                        <p class="text-2xl text-amber-400">${member.role}</p>
                        <div class="flex gap-x-6 mt-6 text-sm">
                            <div><span class="text-slate-400">Location:</span><br>${member.location}</div>
                            <div><span class="text-slate-400">Joined:</span><br>${member.joined}</div>
                        </div>
                        <div class="mt-8">
                            <p class="italic text-slate-300">"${member.quote}"</p>
                        </div>
                        <div class="mt-10">
                            <p class="font-medium mb-3">About</p>
                            <p class="text-slate-300 leading-relaxed">${member.bio}</p>
                        </div>
                    </div>
                </div>
                
                <div class="mt-12 pt-8 border-t border-slate-700 flex gap-x-4">
                    <button onclick="closeModal()" class="flex-1 py-5 border border-slate-600 rounded-3xl font-medium">Close</button>
                    <button onclick="connectWithBrother(${member.id});closeModal()" class="flex-1 py-5 bg-amber-400 text-slate-950 rounded-3xl font-bold">Connect with Brother</button>
                </div>
            `

            document.getElementById('profile-modal').classList.remove('hidden')
            document.getElementById('profile-modal').classList.add('flex')
        }

        function closeModal() {
            const modal = document.getElementById('profile-modal')
            modal.classList.add('hidden')
            modal.classList.remove('flex')
        }

        function connectWithBrother(id) {
            alert("✅ Connection request sent!\n\nIn a real app this would add you to a private chat or WhatsApp group with this brother.")
        }

        function applyFilters() {
            const search = document.getElementById('search-input').value.toLowerCase()
            const location = document.getElementById('location-filter').value
            const role = document.getElementById('role-filter').value
            const joined = document.getElementById('joined-filter').value

            let filtered = allMembers.filter(member => {
                const matchSearch = !search || 
                    member.name.toLowerCase().includes(search) || 
                    member.bio.toLowerCase().includes(search)
                
                const matchLocation = !location || member.location === location
                const matchRole = !role || member.role.includes(role)
                const matchJoined = !joined || member.joined === joined

                return matchSearch && matchLocation && matchRole && matchJoined
            })

            renderMembers(filtered)
        }

        function resetFilters() {
            document.getElementById('search-input').value = ''
            document.getElementById('location-filter').value = ''
            document.getElementById('role-filter').value = ''
            document.getElementById('joined-filter').value = ''
            renderMembers(allMembers)
        }

        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' })
        }

        function showJoinModal() {
            alert("🎉 Welcome to the Cadets Men Fellowship!\n\nYour name has been added to the brotherhood directory.")
        }

        // Initialize
        function initializePremiumApp() {
            renderLeadership()
            renderMembers(allMembers)
            console.log('%cCadets Men Fellowship — Premium Edition Loaded ⚔️', 'color:#fbbf24; font-size:15px;')
        }

        window.onload = initializePremiumApp
    </script>
</body>
</html>
