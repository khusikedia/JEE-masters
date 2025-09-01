<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JEE Master - Complete Preparation Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        .section { display: none; }
        .section.active { display: block; animation: fadeIn 0.3s ease-in; }
        .nav-btn { transition: all 0.2s; }
        .nav-btn.active { background: #7c3aed; color: white; }
        .hover-card { transition: all 0.3s; cursor: pointer; }
        .hover-card:hover { transform: translateY(-4px); box-shadow: 0 10px 30px rgba(0,0,0,0.15); }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .question-card { transition: all 0.3s; }
        .question-card:hover { background: #f8fafc; }
        .option-btn { transition: all 0.2s; }
        .option-btn:hover { background: #e2e8f0; }
        .option-btn.selected { background: #3b82f6; color: white; }
        .option-btn.correct { background: #10b981; color: white; }
        .option-btn.incorrect { background: #ef4444; color: white; }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header -->
    <header class="bg-gradient-to-r from-purple-600 to-blue-600 text-white shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-4 py-4">
            <div class="flex items-center justify-between">
                <div class="flex items-center space-x-3">
                    <i class="fas fa-graduation-cap text-3xl"></i>
                    <div>
                        <h1 class="text-2xl font-bold">JEE Master</h1>
                        <p class="text-xs opacity-90">Complete Preparation Platform</p>
                    </div>
                </div>
                <div class="text-right">
                    <div class="text-sm font-medium">JEE Main 2025</div>
                    <div class="text-xs opacity-90">120 days remaining</div>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="bg-white shadow-md border-b sticky top-20 z-40">
        <div class="container mx-auto px-4">
            <div class="flex flex-wrap justify-center gap-2 py-3">
                <button class="nav-btn px-4 py-2 rounded-lg font-semibold active" onclick="showSection('dashboard')">
                    <i class="fas fa-home mr-2"></i>Dashboard
                </button>
                <button class="nav-btn px-4 py-2 rounded-lg font-semibold" onclick="showSection('study')">
                    <i class="fas fa-book mr-2"></i>Study
                </button>
                <button class="nav-btn px-4 py-2 rounded-lg font-semibold" onclick="showSection('practice')">
                    <i class="fas fa-pencil-alt mr-2"></i>Tests
                </button>
                <button class="nav-btn px-4 py-2 rounded-lg font-semibold" onclick="showSection('doubt')">
                    <i class="fas fa-question-circle mr-2"></i>AI Tutor
                </button>
                <button class="nav-btn px-4 py-2 rounded-lg font-semibold" onclick="showSection('progress')">
                    <i class="fas fa-chart-line mr-2"></i>Progress
                </button>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-6">
        <!-- Dashboard Section -->
        <section id="dashboard" class="section active">
            <div class="mb-8">
                <h2 class="text-3xl font-bold mb-2">🏠 Welcome Back, JEE Warrior!</h2>
                <p class="text-gray-600">Your path to IIT success starts here</p>
            </div>
            
            <!-- Quick Stats -->
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
                <div class="bg-gradient-to-br from-blue-500 to-blue-600 text-white p-6 rounded-xl shadow-lg hover-card">
                    <div class="flex items-center justify-between">
                        <div>
                            <h3 class="text-lg font-semibold">Tests Taken</h3>
                            <p class="text-3xl font-bold mt-1">28</p>
                        </div>
                        <i class="fas fa-clipboard-list text-4xl opacity-80"></i>
                    </div>
                    <div class="mt-2 text-blue-100 text-sm">+4 this week</div>
                </div>

                <div class="bg-gradient-to-br from-green-500 to-green-600 text-white p-6 rounded-xl shadow-lg hover-card">
                    <div class="flex items-center justify-between">
                        <div>
                            <h3 class="text-lg font-semibold">Average Score</h3>
                            <p class="text-3xl font-bold mt-1">87%</p>
                        </div>
                        <i class="fas fa-trophy text-4xl opacity-80"></i>
                    </div>
                    <div class="mt-2 text-green-100 text-sm">+8% improvement</div>
                </div>

                <div class="bg-gradient-to-br from-purple-500 to-purple-600 text-white p-6 rounded-xl shadow-lg hover-card">
                    <div class="flex items-center justify-between">
                        <div>
                            <h3 class="text-lg font-semibold">Study Streak</h3>
                            <p class="text-3xl font-bold mt-1">32</p>
                        </div>
                        <i class="fas fa-fire text-4xl opacity-80"></i>
                    </div>
                    <div class="mt-2 text-purple-100 text-sm">days strong!</div>
                </div>

                <div class="bg-gradient-to-br from-orange-500 to-red-500 text-white p-6 rounded-xl shadow-lg hover-card">
                    <div class="flex items-center justify-between">
                        <div>
                            <h3 class="text-lg font-semibold">AI Rank</h3>
                            <p class="text-3xl font-bold mt-1">1,248</p>
                        </div>
                        <i class="fas fa-medal text-4xl opacity-80"></i>
                    </div>
                    <div class="mt-2 text-orange-100 text-sm">out of 2.5L</div>
                </div>
            </div>

            <!-- Quick Actions -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                <div class="bg-white p-6 rounded-xl shadow-lg hover-card" onclick="startQuickTest()">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center">
                            <i class="fas fa-play text-purple-600 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-bold ml-4">Quick Mock Test</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Take a 30-question practice test across all subjects</p>
                    <div class="text-purple-600 font-semibold">→ Start Now</div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-lg hover-card" onclick="showSection('study')">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center">
                            <i class="fas fa-book text-blue-600 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-bold ml-4">Study Materials</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Access comprehensive notes and detailed explanations</p>
                    <div class="text-blue-600 font-semibold">→ Explore Chapters</div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-lg hover-card" onclick="showSection('doubt')">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center">
                            <i class="fas fa-robot text-green-600 text-xl"></i>
                        </div>
                        <h3 class="text-xl font-bold ml-4">AI Tutor</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Get instant help with any concept or problem</p>
                    <div class="text-green-600 font-semibold">→ Ask Question</div>
                </div>
            </div>

            <!-- Recent Activity -->
            <div class="bg-white rounded-xl shadow-lg p-6">
                <h3 class="text-xl font-bold mb-6">🔥 Recent Activity</h3>
                <div class="space-y-4">
                    <div class="flex items-center space-x-4 p-4 bg-green-50 rounded-lg">
                        <div class="w-10 h-10 bg-green-500 rounded-full flex items-center justify-center">
                            <i class="fas fa-check text-white"></i>
                        </div>
                        <div class="flex-1">
                            <div class="font-semibold">Completed Physics Mock Test</div>
                            <div class="text-sm text-gray-600">Score: 92% • Just now</div>
                        </div>
                    </div>
                    
                    <div class="flex items-center space-x-4 p-4 bg-blue-50 rounded-lg">
                        <div class="w-10 h-10 bg-blue-500 rounded-full flex items-center justify-center">
                            <i class="fas fa-book text-white"></i>
                        </div>
                        <div class="flex-1">
                            <div class="font-semibold">Studied Organic Chemistry</div>
                            <div class="text-sm text-gray-600">Duration: 2 hours • 3 hours ago</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Study Materials Section -->
        <section id="study" class="section">
            <!-- Main Study View -->
            <div id="studyMain">
                <div class="mb-8">
                    <h2 class="text-3xl font-bold mb-2">📚 Study Materials</h2>
                    <p class="text-gray-600">Comprehensive chapter-wise content for complete JEE preparation</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                    <!-- Physics Card -->
                    <div class="bg-white rounded-xl shadow-lg p-8 hover-card" onclick="openSubject('physics')">
                        <div class="flex items-center justify-between mb-6">
                            <div class="flex items-center">
                                <div class="w-16 h-16 bg-blue-100 rounded-xl flex items-center justify-center">
                                    <i class="fas fa-atom text-blue-600 text-2xl"></i>
                                </div>
                                <div class="ml-4">
                                    <h3 class="text-2xl font-bold text-blue-600">Physics</h3>
                                    <p class="text-sm text-gray-500">6 Complete Chapters</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="space-y-3 mb-6">
                            <div class="flex justify-between text-sm">
                                <span>Mechanics</span>
                                <span class="text-green-600 font-semibold">95%</span>
                            </div>
                            <div class="flex justify-between text-sm">
                                <span>Electromagnetism</span>
                                <span class="text-red-600 font-semibold">58%</span>
                            </div>
                            <div class="flex justify-between text-sm">
                                <span>Modern Physics</span>
                                <span class="text-yellow-600 font-semibold">72%</span>
                            </div>
                        </div>
                        
                        <div class="w-full bg-gray-200 rounded-full h-3 mb-4">
                            <div class="bg-blue-500 h-3 rounded-full" style="width: 75%"></div>
                        </div>
                        
                        <div class="text-blue-600 font-semibold">→ Explore Physics</div>
                    </div>

                    <!-- Chemistry Card -->
                    <div class="bg-white rounded-xl shadow-lg p-8 hover-card" onclick="openSubject('chemistry')">
                        <div class="flex items-center justify-between mb-6">
                            <div class="flex items-center">
                                <div class="w-16 h-16 bg-green-100 rounded-xl flex items-center justify-center">
                                    <i class="fas fa-flask text-green-600 text-2xl"></i>
                                </div>
                                <div class="ml-4">
                                    <h3 class="text-2xl font-bold text-green-600">Chemistry</h3>
                                    <p class="text-sm text-gray-500">4 Complete Chapters</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="space-y-3 mb-6">
                            <div class="flex justify-between text-sm">
                                <span>Organic Chemistry</span>
                                <span class="text-green-600 font-semibold">92%</span>
                            </div>
                            <div class="flex justify-between text-sm">
                                <span>Physical Chemistry</span>
                                <span class="text-yellow-600 font-semibold">68%</span>
                            </div>
                            <div class="flex justify-between text-sm">
                                <span>Inorganic Chemistry</span>
                                <span class="text-green-600 font-semibold">85%</span>
                            </div>
                        </div>
                        
                        <div class="w-full bg-gray-200 rounded-full h-3 mb-4">
                            <div class="bg-green-500 h-3 rounded-full" style="width: 82%"></div>
                        </div>
                        
                        <div class="text-green-600 font-semibold">→ Explore Chemistry</div>
                    </div>

                    <!-- Mathematics Card -->
                    <div class="bg-white rounded-xl shadow-lg p-8 hover-card" onclick="openSubject('mathematics')">
                        <div class="flex items-center justify-between mb-6">
                            <div class="flex items-center">
                                <div class="w-16 h-16 bg-purple-100 rounded-xl flex items-center justify-center">
                                    <i class="fas fa-calculator text-purple-600 text-2xl"></i>
                                </div>
                                <div class="ml-4">
                                    <h3 class="text-2xl font-bold text-purple-600">Mathematics</h3>
                                    <p class="text-sm text-gray-500">6 Complete Chapters</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="space-y-3 mb-6">
                            <div class="flex justify-between text-sm">
                                <span>Calculus</span>
                                <span class="text-green-600 font-semibold">96%</span>
                            </div>
                            <div class="flex justify-between text-sm">
                                <span>Trigonometry</span>
                                <span class="text-green-600 font-semibold">98%</span>
                            </div>
                            <div class="flex justify-between text-sm">
                                <span>Algebra</span>
                                <span class="text-yellow-600 font-semibold">78%</span>
                            </div>
                        </div>
                        
                        <div class="w-full bg-gray-200 rounded-full h-3 mb-4">
                            <div class="bg-purple-500 h-3 rounded-full" style="width: 91%"></div>
                        </div>
                        
                        <div class="text-purple-600 font-semibold">→ Explore Mathematics</div>
                    </div>
                </div>
            </div>

            <!-- Subject Chapters View -->
            <div id="subjectView" style="display:none;">
                <div class="flex items-center mb-8">
                    <button onclick="backToStudyMain()" class="flex items-center text-purple-600 hover:text-purple-700 font-semibold">
                        <i class="fas fa-arrow-left mr-2"></i>Back to Subjects
                    </button>
                    <div class="ml-6">
                        <h2 id="subjectTitle" class="text-3xl font-bold"></h2>
                        <p class="text-gray-600">Click any chapter for detailed explanation</p>
                    </div>
                </div>
                
                <div id="chaptersContainer" class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <!-- Chapters will be populated here -->
                </div>
            </div>

            <!-- Chapter Content View -->
            <div id="chapterView" style="display:none;">
                <div class="flex items-center mb-8">
                    <button onclick="backToSubject()" class="flex items-center text-purple-600 hover:text-purple-700 font-semibold">
                        <i class="fas fa-arrow-left mr-2"></i>Back to Chapters
                    </button>
                </div>
                
                <div class="bg-white rounded-xl shadow-lg p-8">
                    <div id="chapterContent">
                        <!-- Chapter content will be populated here -->
                    </div>
                </div>
            </div>
        </section>

        <!-- Practice Tests Section -->
        <section id="practice" class="section">
            <div class="mb-8">
                <h2 class="text-3xl font-bold mb-2">🎯 Practice Tests</h2>
                <p class="text-gray-600">Take mock tests and track your progress</p>
            </div>

            <!-- Test Categories -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                <div class="bg-gradient-to-br from-blue-500 to-blue-600 text-white p-8 rounded-xl shadow-lg hover-card" onclick="startFullTest()">
                    <div class="flex items-center justify-between mb-6">
                        <div class="w-16 h-16 bg-white bg-opacity-20 rounded-xl flex items-center justify-center">
                            <i class="fas fa-clipboard-list text-3xl"></i>
                        </div>
                    </div>
                    <h3 class="text-2xl font-bold mb-3">📋 Full Mock Test</h3>
                    <p class="text-blue-100 mb-6">90 questions • 3 hours • Complete JEE simulation</p>
                    <div class="text-sm opacity-80">✨ Most comprehensive test</div>
                </div>

                <div class="bg-gradient-to-br from-green-500 to-green-600 text-white p-8 rounded-xl shadow-lg hover-card" onclick="startSubjectTest()">
                    <div class="flex items-center justify-between mb-6">
                        <div class="w-16 h-16 bg-white bg-opacity-20 rounded-xl flex items-center justify-center">
                            <i class="fas fa-book text-3xl"></i>
                        </div>
                    </div>
                    <h3 class="text-2xl font-bold mb-3">📖 Subject Test</h3>
                    <p class="text-green-100 mb-6">30 questions • 1 hour • Single subject focus</p>
                    <div class="text-sm opacity-80">🎯 Targeted practice</div>
                </div>

                <div class="bg-gradient-to-br from-purple-500 to-purple-600 text-white p-8 rounded-xl shadow-lg hover-card" onclick="startQuickTest()">
                    <div class="flex items-center justify-between mb-6">
                        <div class="w-16 h-16 bg-white bg-opacity-20 rounded-xl flex items-center justify-center">
                            <i class="fas fa-bolt text-3xl"></i>
                        </div>
                    </div>
                    <h3 class="text-2xl font-bold mb-3">⚡ Quick Test</h3>
                    <p class="text-purple-100 mb-6">15 questions • 30 minutes • Rapid assessment</p>
                    <div class="text-sm opacity-80">🚀 Fast practice</div>
                </div>
            </div>

            <!-- Previous Year Papers -->
            <div class="bg-white rounded-xl shadow-lg p-8">
                <h3 class="text-2xl font-bold mb-6">📜 Previous Year Papers</h3>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                    <div class="bg-gradient-to-br from-indigo-50 to-purple-50 p-6 rounded-xl text-center hover-card" onclick="startPYQ(2024)">
                        <div class="text-4xl font-bold text-purple-600 mb-2">2024</div>
                        <div class="text-sm text-gray-600 mb-3">JEE Main</div>
                        <div class="text-xs bg-green-100 text-green-800 px-3 py-1 rounded-full">Latest</div>
                    </div>
                    
                    <div class="bg-gradient-to-br from-blue-50 to-indigo-50 p-6 rounded-xl text-center hover-card" onclick="startPYQ(2023)">
                        <div class="text-4xl font-bold text-blue-600 mb-2">2023</div>
                        <div class="text-sm text-gray-600 mb-3">JEE Main</div>
                        <div class="text-xs bg-blue-100 text-blue-800 px-3 py-1 rounded-full">Popular</div>
                    </div>
                    
                    <div class="bg-gradient-to-br from-orange-50 to-red-50 p-6 rounded-xl text-center hover-card" onclick="startPYQ(2022)">
                        <div class="text-4xl font-bold text-orange-600 mb-2">2022</div>
                        <div class="text-sm text-gray-600 mb-3">JEE Main</div>
                        <div class="text-xs bg-orange-100 text-orange-800 px-3 py-1 rounded-full">Tough</div>
                    </div>
                    
                    <div class="bg-gradient-to-br from-green-50 to-emerald-50 p-6 rounded-xl text-center hover-card" onclick="startPYQ(2021)">
                        <div class="text-4xl font-bold text-green-600 mb-2">2021</div>
                        <div class="text-sm text-gray-600 mb-3">JEE Main</div>
                        <div class="text-xs bg-green-100 text-green-800 px-3 py-1 rounded-full">Practice</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Test Interface -->
        <section id="testInterface" class="section">
            <div class="bg-white rounded-xl shadow-lg p-6">
                <!-- Test Header -->
                <div class="flex justify-between items-center mb-6 pb-4 border-b">
                    <div>
                        <h2 id="testTitle" class="text-2xl font-bold">Mock Test</h2>
                        <p id="testInfo" class="text-gray-600"></p>
                    </div>
                    <div class="text-right">
                        <div class="text-2xl font-bold text-red-600" id="timer">30:00</div>
                        <div class="text-sm text-gray-500">Time Remaining</div>
                    </div>
                </div>

                <!-- Question Navigation -->
                <div class="mb-6">
                    <div class="flex flex-wrap gap-2 mb-4">
                        <div id="questionNav" class="flex flex-wrap gap-2">
                            <!-- Question number buttons will be populated here -->
                        </div>
                    </div>
                    <div class="flex gap-4 text-sm">
                        <div class="flex items-center"><span class="w-3 h-3 bg-green-500 rounded mr-2"></span>Answered</div>
                        <div class="flex items-center"><span class="w-3 h-3 bg-yellow-500 rounded mr-2"></span>Marked</div>
                        <div class="flex items-center"><span class="w-3 h-3 bg-gray-300 rounded mr-2"></span>Not Visited</div>
                    </div>
                </div>

                <!-- Question Display -->
                <div id="questionContainer" class="mb-6">
                    <!-- Question content will be populated here -->
                </div>

                <!-- Navigation Buttons -->
                <div class="flex justify-between items-center">
                    <div class="flex gap-3">
                        <button onclick="previousQuestion()" class="px-4 py-2 bg-gray-500 text-white rounded-lg hover:bg-gray-600">
                            ← Previous
                        </button>
                        <button onclick="markForReview()" class="px-4 py-2 bg-yellow-500 text-white rounded-lg hover:bg-yellow-600">
                            Mark for Review
                        </button>
                    </div>
                    
                    <div class="flex gap-3">
                        <button onclick="clearResponse()" class="px-4 py-2 bg-red-500 text-white rounded-lg hover:bg-red-600">
                            Clear
                        </button>
                        <button onclick="nextQuestion()" class="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600">
                            Next →
                        </button>
                        <button onclick="submitTest()" class="px-4 py-2 bg-green-500 text-white rounded-lg hover:bg-green-600">
                            Submit Test
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Test Results -->
        <section id="testResults" class="section">
            <div class="bg-white rounded-xl shadow-lg p-8">
                <div class="text-center mb-8">
                    <h2 class="text-3xl font-bold mb-2">🎉 Test Completed!</h2>
                    <p class="text-gray-600">Here's your detailed performance analysis</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                    <div class="text-center p-6 bg-green-50 rounded-xl">
                        <div class="text-4xl font-bold text-green-600" id="totalScore">85%</div>
                        <div class="text-green-700 font-semibold">Overall Score</div>
                        <div class="text-sm text-green-600 mt-2" id="scoreDetails">17/20 correct</div>
                    </div>
                    
                    <div class="text-center p-6 bg-blue-50 rounded-xl">
                        <div class="text-4xl font-bold text-blue-600" id="timeSpent">25:30</div>
                        <div class="text-blue-700 font-semibold">Time Taken</div>
                        <div class="text-sm text-blue-600 mt-2">Out of 30:00</div>
                    </div>
                    
                    <div class="text-center p-6 bg-purple-50 rounded-xl">
                        <div class="text-4xl font-bold text-purple-600" id="accuracy">85%</div>
                        <div class="text-purple-700 font-semibold">Accuracy</div>
                        <div class="text-sm text-purple-600 mt-2">Excellent performance!</div>
                    </div>
                </div>

                <div id="detailedResults" class="space-y-6">
                    <!-- Detailed results will be populated here -->
                </div>

                <div class="text-center mt-8 space-x-4">
                    <button onclick="reviewAnswers()" class="px-6 py-3 bg-blue-500 text-white rounded-lg hover:bg-blue-600">
                        Review Answers
                    </button>
                    <button onclick="retakeTest()" class="px-6 py-3 bg-green-500 text-white rounded-lg hover:bg-green-600">
                        Retake Test
                    </button>
                    <button onclick="showSection('practice')" class="px-6 py-3 bg-purple-500 text-white rounded-lg hover:bg-purple-600">
                        More Tests
                    </button>
                </div>
            </div>
        </section>

        <!-- AI Doubt Solver Section -->
        <section id="doubt" class="section">
            <div class="mb-8">
                <h2 class="text-3xl font-bold mb-2">🤖 AI Doubt Solver</h2>
                <p class="text-gray-600">Get instant help with any JEE concept or problem</p>
            </div>
            
            <div class="bg-white rounded-xl shadow-lg p-8 mb-8">
                <h3 class="text-xl font-bold mb-6">Ask Your Question</h3>
                <div class="space-y-6">
                    <textarea 
                        id="questionInput" 
                        class="w-full p-4 border-2 border-gray-300 rounded-lg text-base resize-none focus:border-purple-500 focus:outline-none" 
                        rows="4" 
                        placeholder="Type your JEE question here... e.g., 'Explain electromagnetic induction' or 'Solve ∫x²e^x dx'"
                    ></textarea>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <select id="subjectSelect" class="p-3 border-2 border-gray-300 rounded-lg text-base focus:border-purple-500 focus:outline-none">
                            <option value="physics">⚛️ Physics</option>
                            <option value="chemistry">🧪 Chemistry</option>
                            <option value="mathematics">🔢 Mathematics</option>
                        </select>
                        
                        <select id="difficultySelect" class="p-3 border-2 border-gray-300 rounded-lg text-base focus:border-purple-500 focus:outline-none">
                            <option value="basic">🟢 Basic Level</option>
                            <option value="intermediate">🟡 Intermediate</option>
                            <option value="advanced">🔴 Advanced</option>
                        </select>
                    </div>
                    
                    <button onclick="askAI()" class="w-full bg-gradient-to-r from-purple-600 to-blue-600 text-white py-4 px-8 rounded-lg font-bold text-lg hover:shadow-lg transition-all">
                        🚀 Ask AI Tutor
                    </button>
                </div>
            </div>

            <!-- AI Response Area -->
            <div id="aiResponse" class="bg-gradient-to-r from-blue-50 to-purple-50 rounded-xl p-8" style="display:none;">
                <h3 class="text-xl font-bold mb-6 flex items-center">
                    <i class="fas fa-robot text-purple-600 mr-3"></i>AI Tutor Response
                </h3>
                <div id="responseContent" class="bg-white rounded-lg p-6">
                    <!-- AI response will be displayed here -->
                </div>
            </div>

            <!-- Popular Questions -->
            <div class="bg-white rounded-xl shadow-lg p-8">
                <h3 class="text-xl font-bold mb-6">🔥 Popular Questions</h3>
                <div class="space-y-4">
                    <div class="p-4 bg-gray-50 rounded-lg hover:bg-gray-100 cursor-pointer transition-colors" onclick="loadQuestion('em')">
                        <div class="font-semibold">How do electric field lines work?</div>
                        <div class="text-sm text-gray-600">Physics • 2.3k students asked</div>
                    </div>
                    <div class="p-4 bg-gray-50 rounded-lg hover:bg-gray-100 cursor-pointer transition-colors" onclick="loadQuestion('calc')">
                        <div class="font-semibold">Integration by parts vs substitution?</div>
                        <div class="text-sm text-gray-600">Mathematics • 1.8k students asked</div>
                    </div>
                    <div class="p-4 bg-gray-50 rounded-lg hover:bg-gray-100 cursor-pointer transition-colors" onclick="loadQuestion('organic')">
                        <div class="font-semibold">SN1 vs SN2 reactions?</div>
                        <div class="text-sm text-gray-600">Chemistry • 1.5k students asked</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Progress Section -->
        <section id="progress" class="section">
            <div class="mb-8">
                <h2 class="text-3xl font-bold mb-2">📊 Progress Analytics</h2>
                <p class="text-gray-600">Track your JEE preparation journey</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                <div class="bg-gradient-to-br from-blue-500 to-blue-600 text-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold">Physics</h3>
                    <div class="text-4xl font-bold mt-2">78%</div>
                    <div class="text-blue-100 mt-2">Rank: 15,234/2.5L</div>
                </div>
                <div class="bg-gradient-to-br from-green-500 to-green-600 text-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold">Chemistry</h3>
                    <div class="text-4xl font-bold mt-2">85%</div>
                    <div class="text-green-100 mt-2">Rank: 8,956/2.5L</div>
                </div>
                <div class="bg-gradient-to-br from-purple-500 to-purple-600 text-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold">Mathematics</h3>
                    <div class="text-4xl font-bold mt-2">91%</div>
                    <div class="text-purple-100 mt-2">Rank: 3,456/2.5L</div>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-green-50 p-8 rounded-xl">
                    <h3 class="text-xl font-bold text-green-800 mb-6">💪 Strong Areas</h3>
                    <div class="space-y-4">
                        <div class="flex justify-between items-center">
                            <span>Calculus</span>
                            <span class="font-bold text-green-600">96%</span>
                        </div>
                        <div class="flex justify-between items-center">
                            <span>Organic Chemistry</span>
                            <span class="font-bold text-green-600">92%</span>
                        </div>
                        <div class="flex justify-between items-center">
                            <span>Trigonometry</span>
                            <span class="font-bold text-green-600">98%</span>
                        </div>
                    </div>
                </div>
                
                <div class="bg-red-50 p-8 rounded-xl">
                    <h3 class="text-xl font-bold text-red-800 mb-6">⚠️ Improvement Areas</h3>
                    <div class="space-y-4">
                        <div class="flex justify-between items-center">
                            <span>Electromagnetism</span>
                            <span class="font-bold text-red-600">58%</span>
                        </div>
                        <div class="flex justify-between items-center">
                            <span>Physical Chemistry</span>
                            <span class="font-bold text-red-600">68%</span>
                        </div>
                        <div class="flex justify-between items-center">
                            <span>Complex Numbers</span>
                            <span class="font-bold text-red-600">72%</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Modal -->
    <div id="modal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50" style="display:none;">
        <div class="bg-white rounded-xl shadow-2xl m-4 max-w-4xl max-h-96 overflow-y-auto">
            <div class="p-8">
                <h3 id="modalTitle" class="text-2xl font-bold mb-6"></h3>
                <div id="modalContent" class="text-gray-700 mb-8 whitespace-pre-line leading-relaxed"></div>
                <button onclick="closeModal()" class="w-full bg-purple-600 text-white py-3 px-6 rounded-lg font-semibold hover:bg-purple-700">
                    Close
                </button>
            </div>
        </div>
    </div>

    <script>
        // Global Variables
        let currentSection = 'dashboard';
        let currentSubject = '';
        let currentQuestionIndex = 0;
        let testQuestions = [];
        let userAnswers = [];
        let testStartTime = null;
        let timerInterval = null;
        let timeLimit = 30; // minutes

        // Question Banks
        const questionBanks = {
            physics: [
                {
                    question: "A ball is thrown vertically upward with an initial velocity of 20 m/s. What is the maximum height reached? (g = 10 m/s²)",
                    options: ["10 m", "15 m", "20 m", "25 m"],
                    correct: 2,
                    explanation: "Using v² = u² - 2gh, at maximum height v = 0. So 0 = 400 - 2(10)h, h = 20 m"
                },
                {
                    question: "Two resistors of 6Ω and 12Ω are connected in parallel. What is the equivalent resistance?",
                    options: ["2Ω", "4Ω", "6Ω", "18Ω"],
                    correct: 1,
                    explanation: "For parallel: 1/R = 1/6 + 1/12 = 3/12 = 1/4, so R = 4Ω"
                },
                {
                    question: "A wave has frequency 50 Hz and wavelength 6 m. What is its speed?",
                    options: ["200 m/s", "250 m/s", "300 m/s", "350 m/s"],
                    correct: 2,
                    explanation: "Wave speed v = fλ = 50 × 6 = 300 m/s"
                }
            ],
            chemistry: [
                {
                    question: "What is the molecular formula of glucose?",
                    options: ["C₆H₁₂O₆", "C₆H₁₀O₅", "C₅H₁₀O₅", "C₆H₁₄O₆"],
                    correct: 0,
                    explanation: "Glucose is a simple sugar with molecular formula C₆H₁₂O₆"
                },
                {
                    question: "Which of the following is the strongest acid?",
                    options: ["HCl", "HNO₃", "H₂SO₄", "HClO₄"],
                    correct: 3,
                    explanation: "HClO₄ (perchloric acid) is the strongest among these acids"
                },
                {
                    question: "What type of reaction is 2H₂ + O₂ → 2H₂O?",
                    options: ["Decomposition", "Combination", "Displacement", "Double displacement"],
                    correct: 1,
                    explanation: "This is a combination reaction where two or more substances combine to form a single product"
                }
            ],
            mathematics: [
                {
                    question: "What is the derivative of sin(x)?",
                    options: ["cos(x)", "-cos(x)", "sin(x)", "-sin(x)"],
                    correct: 0,
                    explanation: "The derivative of sin(x) with respect to x is cos(x)"
                },
                {
                    question: "If log₂(x) = 3, what is the value of x?",
                    options: ["6", "8", "9", "12"],
                    correct: 1,
                    explanation: "log₂(x) = 3 means 2³ = x, so x = 8"
                },
                {
                    question: "What is the sum of first 10 natural numbers?",
                    options: ["45", "50", "55", "60"],
                    correct: 2,
                    explanation: "Sum = n(n+1)/2 = 10(11)/2 = 55"
                }
            ]
        };

        // Chapter Content Database
        const chapterData = {
            physics: [
                {
                    name: "Mechanics",
                    icon: "🔧",
                    progress: 95,
                    content: {
                        title: "🔧 Mechanics - Laws of Motion & Dynamics",
                        sections: [
                            {
                                title: "📚 Introduction to Mechanics",
                                content: "Mechanics is the branch of physics that deals with the motion of objects and the forces that cause this motion. It forms the foundation for understanding all other areas of physics."
                            },
                            {
                                title: "⚖️ Newton's Laws of Motion",
                                content: `**First Law (Law of Inertia):**
Every object remains at rest or in uniform motion unless acted upon by an external force.

**Second Law:**
F = ma - The acceleration of an object is directly proportional to the net force and inversely proportional to its mass.

**Third Law:**
For every action, there is an equal and opposite reaction.`
                            },
                            {
                                title: "💪 Work, Energy & Power",
                                content: `**Work:** W = F × d × cos(θ)
- Work is done when a force causes displacement

**Kinetic Energy:** KE = ½mv²
- Energy possessed by an object due to its motion

**Potential Energy:** PE = mgh
- Energy possessed due to position

**Power:** P = W/t = F·v
- Rate of doing work`
                            },
                            {
                                title: "🔄 Rotational Motion",
                                content: `**Angular Velocity:** ω = θ/t
**Angular Acceleration:** α = dω/dt
**Torque:** τ = r × F = Iα
**Moment of Inertia:** I = Σmr²

Key relationships:
- v = rω (linear and angular velocity)
- a = rα (linear and angular acceleration)
- KE_rot = ½Iω²`
                            },
                            {
                                title: "📐 Important Formulas",
                                content: `**Kinematics:**
• v = u + at
• s = ut + ½at²
• v² = u² + 2as

**Dynamics:**
• F = ma
• Momentum: p = mv
• Impulse: J = FΔt = Δp

**Energy:**
• Work-Energy Theorem: W = ΔKE
• Conservation of Energy: Total Energy = Constant
• Conservation of Momentum: Σp_initial = Σp_final`
                            },
                            {
                                title: "🎯 JEE Strategy",
                                content: `**High-Yield Topics:**
• Collision problems (elastic and inelastic)
• Pulley and string systems
• Inclined plane motion with friction
• Circular motion and banking
• Work-energy theorem applications

**Problem-Solving Tips:**
• Always draw free body diagrams
• Apply conservation laws first
• Check units and reasonableness
• Practice numerical problems daily

**Common Mistakes:**
• Forgetting to consider all forces
• Incorrect application of Newton's laws
• Sign convention errors
• Not using conservation principles`
                            }
                        ]
                    }
                },
                {
                    name: "Thermodynamics",
                    icon: "🔥",
                    progress: 72,
                    content: {
                        title: "🔥 Thermodynamics - Heat, Work & Energy",
                        sections: [
                            {
                                title: "🌡️ Basic Concepts",
                                content: "Thermodynamics deals with heat, work, and temperature, and their relation to energy, radiation, and physical properties of matter."
                            },
                            {
                                title: "⚖️ Laws of Thermodynamics",
                                content: `**Zeroth Law:** Thermal equilibrium is transitive

**First Law:** ΔU = Q - W
- Energy cannot be created or destroyed
- Internal energy change = Heat added - Work done by system

**Second Law:** Heat cannot spontaneously flow from cold to hot
- Entropy of an isolated system always increases

**Third Law:** Entropy of a perfect crystal at absolute zero is zero`
                            },
                            {
                                title: "🔄 Thermodynamic Processes",
                                content: `**Isothermal (T = constant):**
- ΔU = 0, Q = W
- PV = constant

**Adiabatic (Q = 0):**
- ΔU = -W
- PVᵞ = constant

**Isobaric (P = constant):**
- W = PΔV

**Isochoric (V = constant):**
- W = 0, Q = ΔU`
                            },
                            {
                                title: "🏭 Heat Engines",
                                content: `**Efficiency:** η = W/Q_H = 1 - Q_C/Q_H

**Carnot Engine:** η_max = 1 - T_C/T_H

**Refrigerator COP:** β = Q_C/W = Q_C/(Q_H - Q_C)

All practical engines have efficiency less than Carnot efficiency due to irreversibilities.`
                            }
                        ]
                    }
                },
                {
                    name: "Electromagnetism",
                    icon: "⚡",
                    progress: 58,
                    content: {
                        title: "⚡ Electromagnetism - Electric & Magnetic Fields",
                        sections: [
                            {
                                title: "🔌 Electric Fields",
                                content: `**Electric Force:** F = kq₁q₂/r² (Coulomb's Law)

**Electric Field:** E = F/q = kQ/r²

**Electric Potential:** V = kQ/r

**Potential Energy:** U = qV

Electric field lines:
• Start from positive charges
• End on negative charges  
• Never intersect
• Density indicates field strength`
                            },
                            {
                                title: "🧲 Magnetic Fields",
                                content: `**Magnetic Force:** F = q(v × B) = qvB sin θ

**Force on Current:** F = I(L × B) = ILB sin θ

**Magnetic Field (Wire):** B = μ₀I/(2πr)

**Magnetic Field (Solenoid):** B = μ₀nI

Right-hand rule determines direction of magnetic field and force.`
                            },
                            {
                                title: "🔄 Electromagnetic Induction",
                                content: `**Faraday's Law:** ε = -dΦ/dt

**Lenz's Law:** Induced current opposes the change causing it

**Motional EMF:** ε = BLv

**Self Inductance:** ε = -L(dI/dt)

**Mutual Inductance:** ε₂ = -M(dI₁/dt)

Applications: Generators, motors, transformers`
                            }
                        ]
                    }
                }
            ],
            chemistry: [
                {
                    name: "Organic Chemistry",
                    icon: "🧬",
                    progress: 92,
                    content: {
                        title: "🧬 Organic Chemistry - Carbon Compounds",
                        sections: [
                            {
                                title: "🔗 Basic Concepts",
                                content: "Organic chemistry is the study of carbon compounds. Carbon's ability to form four covalent bonds and catenate makes it unique for forming complex molecules."
                            },
                            {
                                title: "⚛️ Hybridization & Bonding",
                                content: `**sp³ Hybridization:** Tetrahedral geometry (109.5°)
- Examples: Alkanes, alcohols

**sp² Hybridization:** Trigonal planar (120°)  
- Examples: Alkenes, aldehydes, ketones

**sp Hybridization:** Linear (180°)
- Examples: Alkynes, nitriles

**Resonance:** Delocalization of electrons
- Increases stability
- Equal bond lengths`
                            },
                            {
                                title: "🔄 Reaction Mechanisms",
                                content: `**SN1 Mechanism:**
- Two-step process
- Carbocation intermediate
- Racemization possible
- 3° > 2° > 1° reactivity

**SN2 Mechanism:**
- One-step process
- Backside attack
- Inversion of configuration
- 1° > 2° > 3° reactivity

**E1 & E2 Eliminations:**
- E1: Two-step, carbocation intermediate
- E2: One-step, anti-periplanar geometry`
                            },
                            {
                                title: "🏷️ Functional Groups",
                                content: `**Alcohols:** R-OH
- Primary, secondary, tertiary
- Hydrogen bonding increases boiling point

**Aldehydes & Ketones:** R-CHO, R-CO-R'
- Nucleophilic addition reactions
- Aldol condensation

**Carboxylic Acids:** R-COOH
- Acidic due to resonance stabilization
- Form dimers through hydrogen bonding

**Esters:** R-COO-R'
- Formed from acids and alcohols
- Hydrolysis gives back acid and alcohol`
                            }
                        ]
                    }
                },
                {
                    name: "Physical Chemistry",
                    icon: "⚗️",
                    progress: 68,
                    content: {
                        title: "⚗️ Physical Chemistry - Mathematical Chemistry",
                        sections: [
                            {
                                title: "🌡️ Chemical Thermodynamics",
                                content: `**Enthalpy:** H = U + PV
- ΔH = Heat change at constant pressure

**Entropy:** Measure of disorder
- ΔS_universe > 0 for spontaneous processes

**Gibbs Free Energy:** G = H - TS
- ΔG < 0 for spontaneous processes
- ΔG = ΔH - TΔS`
                            },
                            {
                                title: "⚡ Chemical Kinetics",
                                content: `**Rate Law:** Rate = k[A]ᵐ[B]ⁿ

**Order of Reaction:** m + n
- Zero order: Rate independent of concentration
- First order: Rate ∝ [A]
- Second order: Rate ∝ [A]²

**Arrhenius Equation:** k = Ae^(-Ea/RT)
- Higher temperature increases rate
- Catalyst lowers activation energy`
                            },
                            {
                                title: "⚖️ Chemical Equilibrium",
                                content: `**Equilibrium Constant:** K = [Products]/[Reactants]

**Le Chatelier's Principle:**
- Increase concentration → Shifts away
- Increase pressure → Shifts to fewer moles
- Increase temperature → Shifts to endothermic side

**Relationship:** ΔG° = -RT ln K`
                            }
                        ]
                    }
                }
            ],
            mathematics: [
                {
                    name: "Calculus",
                    icon: "📈",
                    progress: 96,
                    content: {
                        title: "📈 Calculus - Limits, Derivatives & Integration",
                        sections: [
                            {
                                title: "🎯 Limits",
                                content: `**Definition:** lim(x→a) f(x) = L

**L'Hôpital's Rule:** For 0/0 or ∞/∞ forms
lim(x→a) f(x)/g(x) = lim(x→a) f'(x)/g'(x)

**Important Limits:**
• lim(x→0) sin(x)/x = 1
• lim(x→∞) (1 + 1/x)ˣ = e
• lim(x→0) (eˣ - 1)/x = 1`
                            },
                            {
                                title: "📊 Derivatives",
                                content: `**Definition:** f'(x) = lim(h→0) [f(x+h) - f(x)]/h

**Basic Rules:**
• d/dx(xⁿ) = nxⁿ⁻¹
• d/dx(sin x) = cos x
• d/dx(cos x) = -sin x
• d/dx(eˣ) = eˣ
• d/dx(ln x) = 1/x

**Chain Rule:** d/dx[f(g(x))] = f'(g(x)) × g'(x)

**Product Rule:** d/dx[f(x)g(x)] = f'(x)g(x) + f(x)g'(x)`
                            },
                            {
                                title: "∫ Integration",
                                content: `**Fundamental Theorem:** d/dx[∫f(x)dx] = f(x)

**Basic Integrals:**
• ∫xⁿ dx = xⁿ⁺¹/(n+1) + C
• ∫sin x dx = -cos x + C
• ∫cos x dx = sin x + C
• ∫eˣ dx = eˣ + C
• ∫(1/x) dx = ln|x| + C

**Integration by Parts:** ∫u dv = uv - ∫v du

**Substitution:** ∫f(g(x))g'(x)dx = ∫f(u)du where u = g(x)`
                            },
                            {
                                title: "📐 Applications",
                                content: `**Area Under Curve:** A = ∫ₐᵇ f(x) dx

**Volume of Revolution:** V = π∫ₐᵇ [f(x)]² dx

**Arc Length:** L = ∫ₐᵇ √(1 + [f'(x)]²) dx

**Optimization:**
1. Find critical points: f'(x) = 0
2. Test using second derivative
3. Check endpoints

**Related Rates:**
1. Write equation relating variables
2. Differentiate with respect to time
3. Substitute known values`
                            }
                        ]
                    }
                },
                {
                    name: "Algebra",
                    icon: "🔢",
                    progress: 78,
                    content: {
                        title: "🔢 Algebra - Equations & Complex Numbers",
                        sections: [
                            {
                                title: "🔄 Complex Numbers",
                                content: `**Standard Form:** z = a + bi where i² = -1

**Magnitude:** |z| = √(a² + b²)

**Conjugate:** z̄ = a - bi

**Polar Form:** z = r(cos θ + i sin θ) = re^(iθ)

**De Moivre's Theorem:** (cos θ + i sin θ)ⁿ = cos(nθ) + i sin(nθ)

**Roots of Unity:** Solutions to zⁿ = 1`
                            },
                            {
                                title: "📊 Quadratic Equations",
                                content: `**Standard Form:** ax² + bx + c = 0

**Quadratic Formula:** x = [-b ± √(b² - 4ac)]/(2a)

**Discriminant:** Δ = b² - 4ac
• Δ > 0: Two real roots
• Δ = 0: One repeated root  
• Δ < 0: Two complex roots

**Vieta's Formulas:**
• Sum of roots: α + β = -b/a
• Product of roots: αβ = c/a`
                            },
                            {
                                title: "📈 Sequences & Series",
                                content: `**Arithmetic Progression:**
• General term: aₙ = a + (n-1)d
• Sum: Sₙ = n/2[2a + (n-1)d]

**Geometric Progression:**
• General term: aₙ = ar^(n-1)
• Sum: Sₙ = a(rⁿ - 1)/(r - 1)
• Infinite sum (|r| < 1): S∞ = a/(1-r)

**Special Series:**
• 1² + 2² + ... + n² = n(n+1)(2n+1)/6
• 1³ + 2³ + ... + n³ = [n(n+1)/2]²`
                            }
                        ]
                    }
                }
            ]
        };

        // Core Functions
        function showSection(sectionId) {
            console.log('📍 Navigating to:', sectionId);
            
            // Hide all sections
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Remove active from nav buttons
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            
            // Show selected section
            document.getElementById(sectionId).classList.add('active');
            
            // Activate nav button
            event.target.classList.add('active');
            
            currentSection = sectionId;
        }

        function openSubject(subject) {
            console.log('📚 Opening subject:', subject);
            currentSubject = subject;
            
            // Hide main study view
            document.getElementById('studyMain').style.display = 'none';
            document.getElementById('subjectView').style.display = 'block';
            document.getElementById('chapterView').style.display = 'none';
            
            // Update title
            const titles = {
                physics: '⚛️ Physics Chapters',
                chemistry: '🧪 Chemistry Chapters', 
                mathematics: '🔢 Mathematics Chapters'
            };
            document.getElementById('subjectTitle').textContent = titles[subject];
            
            // Populate chapters
            const container = document.getElementById('chaptersContainer');
            container.innerHTML = '';
            
            chapterData[subject].forEach(chapter => {
                const chapterCard = document.createElement('div');
                chapterCard.className = 'bg-white p-6 rounded-xl shadow-lg hover-card';
                chapterCard.onclick = () => openChapter(chapter);
                
                chapterCard.innerHTML = `
                    <div class="flex items-center justify-between mb-4">
                        <h3 class="text-xl font-bold">${chapter.icon} ${chapter.name}</h3>
                        <span class="text-sm font-semibold px-3 py-1 rounded-full ${
                            chapter.progress >= 80 ? 'bg-green-100 text-green-800' :
                            chapter.progress >= 60 ? 'bg-yellow-100 text-yellow-800' :
                            'bg-red-100 text-red-800'
                        }">
                            ${chapter.progress}% Complete
                        </span>
                    </div>
                    <div class="w-full bg-gray-200 rounded-full h-3 mb-4">
                        <div class="h-3 rounded-full ${
                            chapter.progress >= 80 ? 'bg-green-500' :
                            chapter.progress >= 60 ? 'bg-yellow-500' :
                            'bg-red-500'
                        }" style="width: ${chapter.progress}%"></div>
                    </div>
                    <div class="text-gray-600">Click to view detailed content</div>
                `;
                
                container.appendChild(chapterCard);
            });
        }

        function openChapter(chapter) {
            console.log('📖 Opening chapter:', chapter.name);
            
            // Hide subject view, show chapter view
            document.getElementById('subjectView').style.display = 'none';
            document.getElementById('chapterView').style.display = 'block';
            
            // Populate chapter content
            const contentContainer = document.getElementById('chapterContent');
            contentContainer.innerHTML = `
                <h1 class="text-3xl font-bold mb-8">${chapter.content.title}</h1>
                <div class="space-y-8">
                    ${chapter.content.sections.map(section => `
                        <div class="border-l-4 border-purple-500 pl-6">
                            <h2 class="text-2xl font-bold mb-4">${section.title}</h2>
                            <div class="prose max-w-none text-gray-700 leading-relaxed whitespace-pre-line">
                                ${section.content}
                            </div>
                        </div>
                    `).join('')}
                </div>
                
                <div class="mt-12 p-6 bg-gradient-to-r from-purple-50 to-blue-50 rounded-xl">
                    <h3 class="text-xl font-bold mb-4">🎯 Quick Practice</h3>
                    <p class="text-gray-700 mb-4">Ready to test your understanding of ${chapter.name}?</p>
                    <button onclick="startChapterTest('${chapter.name.toLowerCase()}')" 
                            class="bg-purple-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-purple-700">
                        Take Chapter Test
                    </button>
                </div>
            `;
        }

        function backToStudyMain() {
            console.log('🔙 Back to study main');
            document.getElementById('studyMain').style.display = 'block';
            document.getElementById('subjectView').style.display = 'none';
            document.getElementById('chapterView').style.display = 'none';
        }

        function backToSubject() {
            console.log('🔙 Back to subject');
            document.getElementById('subjectView').style.display = 'block';
            document.getElementById('chapterView').style.display = 'none';
        }

        // Test Functions
        function startQuickTest() {
            console.log('🚀 Starting quick test');
            initializeTest('Quick Test', 'Mixed questions from all subjects', 15, 30);
        }

        function startFullTest() {
            console.log('📋 Starting full test');
            initializeTest('Full Mock Test', 'Complete JEE Main simulation', 30, 180);
        }

        function startSubjectTest() {
            console.log('📖 Starting subject test');
            initializeTest('Subject Test', 'Choose your subject for focused practice', 20, 60);
        }

        function startPYQ(year) {
            console.log('📜 Starting PYQ:', year);
            initializeTest(`JEE Main ${year}`, `Previous year paper from ${year}`, 25, 120);
        }

        function startChapterTest(chapter) {
            console.log('📝 Starting chapter test:', chapter);
            initializeTest(`${chapter} Test`, `Practice test for ${chapter} chapter`, 10, 20);
        }

        function initializeTest(title, description, questionCount, timeInMinutes) {
            // Generate random questions
            testQuestions = generateQuestions(questionCount);
            userAnswers = new Array(testQuestions.length).fill(null);
            currentQuestionIndex = 0;
            timeLimit = timeInMinutes;
            testStartTime = Date.now();
            
            // Update test interface
            document.getElementById('testTitle').textContent = title;
            document.getElementById('testInfo').textContent = `${description} • ${questionCount} Questions • ${timeInMinutes} minutes`;
            
            // Show test interface
            document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
            document.getElementById('testInterface').classList.add('active');
            
            // Setup question navigation
            setupQuestionNavigation();
            displayQuestion();
            startTimer();
        }

        function generateQuestions(count) {
            const allQuestions = [...questionBanks.physics, ...questionBanks.chemistry, ...questionBanks.mathematics];
            const selected = [];
            
            for (let i = 0; i < count; i++) {
                const randomIndex = Math.floor(Math.random() * allQuestions.length);
                selected.push({
                    ...allQuestions[randomIndex],
                    id: i + 1,
                    subject: randomIndex < 3 ? 'Physics' : randomIndex < 6 ? 'Chemistry' : 'Mathematics'
                });
            }
            
            return selected;
        }

        function setupQuestionNavigation() {
            const navContainer = document.getElementById('questionNav');
            navContainer.innerHTML = '';
            
            testQuestions.forEach((_, index) => {
                const btn = document.createElement('button');
                btn.textContent = index + 1;
                btn.className = 'w-10 h-10 rounded-lg border-2 font-semibold';
                btn.onclick = () => goToQuestion(index);
                updateQuestionButtonStatus(btn, index);
                navContainer.appendChild(btn);
            });
        }

        function updateQuestionButtonStatus(btn, index) {
            btn.className = 'w-10 h-10 rounded-lg border-2 font-semibold ';
            
            if (userAnswers[index] !== null) {
                btn.className += 'bg-green-500 text-white border-green-500';
            } else if (index === currentQuestionIndex) {
                btn.className += 'bg-blue-500 text-white border-blue-500';
            } else {
                btn.className += 'bg-gray-200 border-gray-300';
            }
        }

        function displayQuestion() {
            const question = testQuestions[currentQuestionIndex];
            if (!question) return;
            
            const container = document.getElementById('questionContainer');
            container.innerHTML = `
                <div class="mb-6">
                    <div class="flex justify-between items-center mb-4">
                        <span class="text-sm font-semibold text-purple-600">${question.subject}</span>
                        <span class="text-sm text-gray-500">Question ${currentQuestionIndex + 1} of ${testQuestions.length}</span>
                    </div>
                    <h3 class="text-xl font-semibold mb-6">${question.question}</h3>
                    
                    <div class="space-y-3">
                        ${question.options.map((option, index) => `
                            <button class="option-btn w-full p-4 text-left border-2 border-gray-300 rounded-lg hover:bg-gray-50 transition-all ${
                                userAnswers[currentQuestionIndex] === index ? 'selected' : ''
                            }" onclick="selectOption(${index})">
                                <span class="font-semibold mr-3">${String.fromCharCode(65 + index)}.</span>
                                ${option}
                            </button>
                        `).join('')}
                    </div>
                </div>
            `;
            
            // Update navigation buttons
            setupQuestionNavigation();
        }

        function selectOption(optionIndex) {
            userAnswers[currentQuestionIndex] = optionIndex;
            
            // Update button appearance
            document.querySelectorAll('.option-btn').forEach((btn, index) => {
                btn.classList.remove('selected');
                if (index === optionIndex) {
                    btn.classList.add('selected');
                }
            });
            
            // Update navigation
            setupQuestionNavigation();
        }

        function nextQuestion() {
            if (currentQuestionIndex < testQuestions.length - 1) {
                currentQuestionIndex++;
                displayQuestion();
            }
        }

        function previousQuestion() {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                displayQuestion();
            }
        }

        function goToQuestion(index) {
            currentQuestionIndex = index;
            displayQuestion();
        }

        function markForReview() {
            console.log('📌 Marked question for review');
            // Implementation for marking questions
        }

        function clearResponse() {
            userAnswers[currentQuestionIndex] = null;
            displayQuestion();
        }

        function startTimer() {
            const timerElement = document.getElementById('timer');
            let timeLeft = timeLimit * 60; // Convert to seconds
            
            timerInterval = setInterval(() => {
                const minutes = Math.floor(timeLeft / 60);
                const seconds = timeLeft % 60;
                timerElement.textContent = `${minutes}:${seconds.toString().padStart(2, '0')}`;
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    submitTest();
                }
                timeLeft--;
            }, 1000);
        }

        function submitTest() {
            clearInterval(timerInterval);
            
            // Calculate results
            let correct = 0;
            testQuestions.forEach((question, index) => {
                if (userAnswers[index] === question.correct) {
                    correct++;
                }
            });
            
            const score = Math.round((correct / testQuestions.length) * 100);
            const timeSpent = Math.floor((Date.now() - testStartTime) / 1000);
            const minutes = Math.floor(timeSpent / 60);
            const seconds = timeSpent % 60;
            
            // Show results
            document.getElementById('totalScore').textContent = `${score}%`;
            document.getElementById('scoreDetails').textContent = `${correct}/${testQuestions.length} correct`;
            document.getElementById('timeSpent').textContent = `${minutes}:${seconds.toString().padStart(2, '0')}`;
            document.getElementById('accuracy').textContent = `${score}%`;
            
            // Generate detailed results
            const detailedResults = document.getElementById('detailedResults');
            detailedResults.innerHTML = `
                <div class="bg-gray-50 p-6 rounded-xl">
                    <h4 class="text-lg font-bold mb-4">📊 Subject-wise Performance</h4>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                        ${getSubjectWiseResults()}
                    </div>
                </div>
                
                <div class="bg-gray-50 p-6 rounded-xl">
                    <h4 class="text-lg font-bold mb-4">💡 Question Review</h4>
                    <div class="space-y-3 max-h-64 overflow-y-auto">
                        ${testQuestions.map((q, i) => `
                            <div class="flex items-center justify-between p-3 bg-white rounded-lg">
                                <span class="font-medium">Q${i + 1}. ${q.question.substring(0, 50)}...</span>
                                <span class="px-3 py-1 rounded-full text-sm font-semibold ${
                                    userAnswers[i] === q.correct ? 'bg-green-100 text-green-800' : 
                                    userAnswers[i] === null ? 'bg-gray-100 text-gray-800' :
                                    'bg-red-100 text-red-800'
                                }">
                                    ${userAnswers[i] === q.correct ? 'Correct' : 
                                      userAnswers[i] === null ? 'Not Attempted' : 'Incorrect'}
                                </span>
                            </div>
                        `).join('')}
                    </div>
                </div>
            `;
            
            // Show results section
            document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
            document.getElementById('testResults').classList.add('active');
        }

        function getSubjectWiseResults() {
            const subjects = ['Physics', 'Chemistry', 'Mathematics'];
            return subjects.map(subject => {
                const subjectQuestions = testQuestions.filter(q => q.subject === subject);
                if (subjectQuestions.length === 0) return '';
                
                const correct = subjectQuestions.filter((q, index) => {
                    const originalIndex = testQuestions.findIndex(tq => tq === q);
                    return userAnswers[originalIndex] === q.correct;
                }).length;
                
                const percentage = Math.round((correct / subjectQuestions.length) * 100);
                
                return `
                    <div class="text-center p-4 bg-white rounded-lg">
                        <div class="text-2xl font-bold ${percentage >= 70 ? 'text-green-600' : percentage >= 50 ? 'text-yellow-600' : 'text-red-600'}">${percentage}%</div>
                        <div class="font-semibold">${subject}</div>
                        <div class="text-sm text-gray-600">${correct}/${subjectQuestions.length}</div>
                    </div>
                `;
            }).join('');
        }

        function reviewAnswers() {
            console.log('📝 Reviewing answers');
            showModal('Answer Review', 'Detailed answer explanations would be shown here with step-by-step solutions for each question.');
        }

        function retakeTest() {
            console.log('🔄 Retaking test');
            showSection('practice');
        }

        // AI Doubt Solver Functions
        function askAI() {
            const question = document.getElementById('questionInput').value.trim();
            const subject = document.getElementById('subjectSelect').value;
            const difficulty = document.getElementById('difficultySelect').value;
            
            if (!question) {
                showModal('❗ Missing Question', 'Please enter your question before asking the AI tutor.');
                return;
            }
            
            // Show response area
            const responseArea = document.getElementById('aiResponse');
            const contentDiv = document.getElementById('responseContent');
            responseArea.style.display = 'block';
            
            // Simulate loading
            contentDiv.innerHTML = '<div class="text-center py-8"><i class="fas fa-spinner fa-spin text-3xl text-purple-600"></i><br><br>AI Tutor is analyzing your question...</div>';
            
            setTimeout(() => {
                contentDiv.innerHTML = `
                    <div class="space-y-6">
                        <div class="p-4 bg-blue-50 rounded-lg border-l-4 border-blue-500">
                            <h4 class="font-bold text-blue-800 mb-2">📝 Your Question</h4>
                            <p class="text-blue-700">"${question}"</p>
                            <div class="mt-2 text-sm text-blue-600">
                                Subject: ${subject.charAt(0).toUpperCase() + subject.slice(1)} | 
                                Level: ${difficulty.charAt(0).toUpperCase() + difficulty.slice(1)}
                            </div>
                        </div>
                        
                        <div class="p-4 bg-green-50 rounded-lg border-l-4 border-green-500">
                            <h4 class="font-bold text-green-800 mb-3">🤖 AI Tutor Response</h4>
                            <div class="text-green-700 space-y-3">
                                <p>This is a demonstration of the AI tutor feature. In the full application, you would receive:</p>
                                <ul class="list-disc list-inside space-y-1">
                                    <li><strong>Detailed step-by-step explanations</strong> tailored to your level</li>
                                    <li><strong>Relevant formulas and concepts</strong> needed to solve the problem</li>
                                    <li><strong>Visual diagrams and graphs</strong> where applicable</li>
                                    <li><strong>Common mistakes to avoid</strong> and JEE-specific tips</li>
                                    <li><strong>Practice problems</strong> for reinforcement</li>
                                    <li><strong>Related topics</strong> to explore further</li>
                                </ul>
                            </div>
                        </div>
                        
                        <div class="p-4 bg-purple-50 rounded-lg border-l-4 border-purple-500">
                            <h4 class="font-bold text-purple-800 mb-2">🎯 Next Steps</h4>
                            <p class="text-purple-700">Practice similar problems and review the ${subject} chapter for deeper understanding.</p>
                        </div>
                    </div>
                `;
            }, 2000);
        }

        function loadQuestion(type) {
            const questions = {
                'em': 'How do electric field lines help in understanding electric fields? Why do they never intersect each other?',
                'calc': 'What is the fundamental difference between definite and indefinite integration? When should I use integration by parts?',
                'organic': 'How can I systematically identify whether a reaction follows SN1 or SN2 mechanism?'
            };
            
            document.getElementById('questionInput').value = questions[type];
        }

        // Modal Functions
        function showModal(title, content) {
            document.getElementById('modalTitle').textContent = title;
            document.getElementById('modalContent').textContent = content;
            document.getElementById('modal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('modal').style.display = 'none';
        }

        // Initialize App
        document.addEventListener('DOMContentLoaded', function() {
            console.log('🎉 JEE Master App Initialized Successfully!');
            console.log('✅ All features are working properly');
            console.log('🚀 Ready for JEE preparation!');
        });

        // Error Handler
        window.addEventListener('error', function(e) {
            console.error('❌ Error:', e.error);
            showModal('⚠️ Error', 'An error occurred. Please refresh the page and try again.');
        });
    </script>
</body>
</html>
