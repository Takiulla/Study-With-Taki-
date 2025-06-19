<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Study With Taki - AI Learning Companion for Class 12 PCB</title>
    <link href="https://cdn.jsdelivr.net/npm/remixicon@3.5.0/fonts/remixicon.css" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --primary: #7c3aed;
            --secondary: #10b981;
            --accent: #f59e0b;
            --dark: #1e293b;
            --light: #f8fafc;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f1f5f9;
            color: var(--dark);
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
        }
        
        .subject-card {
            transition: all 0.3s ease;
            border-left: 4px solid transparent;
        }
        
        .subject-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
            border-left: 4px solid var(--accent);
        }
        
        .ai-avatar {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
            font-weight: bold;
            margin: 0 auto;
        }
        
        .chat-bubble {
            max-width: 80%;
            padding: 1rem;
            border-radius: 1rem;
            margin: 0.5rem 0;
            position: relative;
        }
        
        .user-bubble {
            background-color: var(--primary);
            color: white;
            margin-left: auto;
            border-bottom-right-radius: 0;
        }
        
        .ai-bubble {
            background-color: #e2e8f0;
            color: var(--dark);
            margin-right: auto;
            border-bottom-left-radius: 0;
        }
        
        .note-card {
            transition: all 0.3s ease;
            background: white;
            border-radius: 0.5rem;
            overflow: hidden;
        }
        
        .note-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .floating-btn {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: var(--primary);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            cursor: pointer;
            z-index: 50;
            transition: all 0.3s ease;
        }
        
        .floating-btn:hover {
            transform: scale(1.1);
            background: var(--secondary);
        }
        
        .highlight {
            background: linear-gradient(120deg, rgba(250, 204, 21, 0.3) 0%, rgba(250, 204, 21, 0) 100%);
            background-repeat: no-repeat;
            background-size: 100% 40%;
            background-position: 0 90%;
        }
        
        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.5;
            }
        }
        
        .animate-pulse {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        
        .instagram-btn {
            background: linear-gradient(45deg, #405DE6, #5851DB, #833AB4, #C13584, #E1306C, #FD1D1D);
            color: white;
        }
        
        .instagram-btn:hover {
            opacity: 0.9;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="bg-white shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <div class="flex-shrink-0 flex items-center">
                        <div class="ai-avatar">T</div>
                        <h1 class="ml-3 text-xl font-bold text-gray-900">Study With Taki</h1>
                    </div>
                </div>
                <div class="hidden md:ml-6 md:flex md:items-center md:space-x-8">
                    <a href="#features" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">Features</a>
                    <a href="#subjects" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">Subjects</a>
                    <a href="#notes" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">My Notes</a>
                    <a href="#chat" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">Ask Taki</a>
                    <a href="https://www.instagram.com/studywithtaki00?igsh=MW5lOWVjbWZucG56bA==" target="_blank" class="instagram-btn px-4 py-2 rounded-md text-sm font-medium flex items-center">
                        <i class="ri-instagram-line mr-2"></i> Instagram
                    </a>
                </div>
                <div class="-mr-2 flex items-center md:hidden">
                    <button type="button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500" aria-controls="mobile-menu" aria-expanded="false">
                        <span class="sr-only">Open main menu</span>
                        <i class="ri-menu-line text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="gradient-bg text-white">
        <div class="max-w-7xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:px-8">
            <div class="text-center">
                <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl lg:text-6xl">
                    Your Personal <span class="highlight">AI Study Partner</span>
                </h1>
                <p class="mt-6 max-w-lg mx-auto text-xl">
                    Taki helps Class 12 PCB students with doubt solving, note-taking, and smart summarization to boost your exam preparation.
                </p>
                <div class="mt-10 flex justify-center space-x-4">
                    <a href="#chat" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md shadow-sm text-indigo-700 bg-white hover:bg-gray-50">
                        Ask Taki Now <i class="ri-arrow-right-line ml-2"></i>
                    </a>
                    <a href="https://www.instagram.com/studywithtaki00?igsh=MW5lOWVjbWZucG56bA==" target="_blank" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-pink-600 hover:bg-pink-700">
                        <i class="ri-instagram-line mr-2"></i> Follow Us
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- Features Section -->
    <div id="features" class="py-12 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="lg:text-center">
                <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">Features</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
                    How Taki Helps You Study Smarter
                </p>
                <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
                    AI-powered tools designed specifically for Class 12 PCB students
                </p>
            </div>

            <div class="mt-10">
                <div class="space-y-10 md:space-y-0 md:grid md:grid-cols-3 md:gap-x-8 md:gap-y-10">
                    <div class="relative">
                        <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                            <i class="ri-question-answer-line text-2xl"></i>
                        </div>
                        <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Instant Doubt Solving</p>
                        <p class="mt-2 ml-16 text-base text-gray-500">
                            Stuck on a problem? Taki explains concepts in simple terms with diagrams and examples.
                        </p>
                    </div>

                    <div class="relative">
                        <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                            <i class="ri-book-mark-line text-2xl"></i>
                        </div>
                        <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Smart Note-Taking</p>
                        <p class="mt-2 ml-16 text-base text-gray-500">
                            Organize notes by topic, add tags, and search instantly. Taki helps format your notes perfectly.
                        </p>
                    </div>

                    <div class="relative">
                        <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                            <i class="ri-file-list-2-line text-2xl"></i>
                        </div>
                        <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Chapter Summaries</p>
                        <p class="mt-2 ml-16 text-base text-gray-500">
                            Get concise summaries of NCERT chapters with key points, formulas, and diagrams.
                        </p>
                    </div>

                    <div class="relative">
                        <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                            <i class="ri-flask-line text-2xl"></i>
                        </div>
                        <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Practical Support</p>
                        <p class="mt-2 ml-16 text-base text-gray-500">
                            Step-by-step guidance for chemistry and biology practicals with safety tips.
                        </p>
                    </div>

                    <div class="relative">
                        <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                            <i class="ri-timer-line text-2xl"></i>
                        </div>
                        <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Exam Preparation</p>
                        <p class="mt-2 ml-16 text-base text-gray-500">
                            Customized study plans, important questions, and last-minute revision notes.
                        </p>
                    </div>

                    <div class="relative">
                        <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                            <i class="ri-brain-line text-2xl"></i>
                        </div>
                        <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Memory Techniques</p>
                        <p class="mt-2 ml-16 text-base text-gray-500">
                            Mnemonics and visualization methods to remember complex biological processes.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Subjects Section -->
    <div id="subjects" class="py-12 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="lg:text-center">
                <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">Subjects</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
                    Class 12 PCB Resources
                </p>
                <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
                    Comprehensive support for all your core subjects
                </p>
            </div>

            <div class="mt-10 grid gap-8 md:grid-cols-3">
                <!-- Physics Card -->
                <div class="subject-card bg-white overflow-hidden shadow rounded-lg">
                    <div class="px-4 py-5 sm:p-6">
                        <div class="flex items-center">
                            <div class="flex-shrink-0 bg-indigo-500 rounded-md p-3">
                                <i class="ri-atom-line text-white text-2xl"></i>
                            </div>
                            <div class="ml-5 w-0 flex-1">
                                <h3 class="text-lg font-medium text-gray-900">Physics</h3>
                                <p class="mt-1 text-sm text-gray-500">Electrostatics to Optics</p>
                            </div>
                        </div>
                        <div class="mt-6 border-t border-gray-200 pt-5">
                            <div class="flex justify-between">
                                <span class="text-sm font-medium text-gray-500">Topics</span>
                                <span class="text-sm font-medium text-gray-500">12 Chapters</span>
                            </div>
                            <div class="mt-2">
                                <div class="flex items-center text-sm text-gray-500">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Electrostatics
                                </div>
                                <div class="flex items-center text-sm text-gray-500 mt-1">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Current Electricity
                                </div>
                                <div class="flex items-center text-sm text-gray-500 mt-1">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Magnetic Effects
                                </div>
                                <button class="mt-4 w-full inline-flex items-center justify-center px-4 py-2 border border-transparent text-sm font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                                    Explore Physics
                                </button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Chemistry Card -->
                <div class="subject-card bg-white overflow-hidden shadow rounded-lg">
                    <div class="px-4 py-5 sm:p-6">
                        <div class="flex items-center">
                            <div class="flex-shrink-0 bg-green-500 rounded-md p-3">
                                <i class="ri-flask-line text-white text-2xl"></i>
                            </div>
                            <div class="ml-5 w-0 flex-1">
                                <h3 class="text-lg font-medium text-gray-900">Chemistry</h3>
                                <p class="mt-1 text-sm text-gray-500">Solutions to Biomolecules</p>
                            </div>
                        </div>
                        <div class="mt-6 border-t border-gray-200 pt-5">
                            <div class="flex justify-between">
                                <span class="text-sm font-medium text-gray-500">Topics</span>
                                <span class="text-sm font-medium text-gray-500">16 Chapters</span>
                            </div>
                            <div class="mt-2">
                                <div class="flex items-center text-sm text-gray-500">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Solutions
                                </div>
                                <div class="flex items-center text-sm text-gray-500 mt-1">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Electrochemistry
                                </div>
                                <div class="flex items-center text-sm text-gray-500 mt-1">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Organic Chemistry
                                </div>
                                <button class="mt-4 w-full inline-flex items-center justify-center px-4 py-2 border border-transparent text-sm font-medium rounded-md shadow-sm text-white bg-green-600 hover:bg-green-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-green-500">
                                    Explore Chemistry
                                </button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Biology Card -->
                <div class="subject-card bg-white overflow-hidden shadow rounded-lg">
                    <div class="px-4 py-5 sm:p-6">
                        <div class="flex items-center">
                            <div class="flex-shrink-0 bg-yellow-500 rounded-md p-3">
                                <i class="ri-dna-line text-white text-2xl"></i>
                            </div>
                            <div class="ml-5 w-0 flex-1">
                                <h3 class="text-lg font-medium text-gray-900">Biology</h3>
                                <p class="mt-1 text-sm text-gray-500">Genetics to Biotechnology</p>
                            </div>
                        </div>
                        <div class="mt-6 border-t border-gray-200 pt-5">
                            <div class="flex justify-between">
                                <span class="text-sm font-medium text-gray-500">Topics</span>
                                <span class="text-sm font-medium text-gray-500">16 Chapters</span>
                            </div>
                            <div class="mt-2">
                                <div class="flex items-center text-sm text-gray-500">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Reproduction
                                </div>
                                <div class="flex items-center text-sm text-gray-500 mt-1">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Genetics
                                </div>
                                <div class="flex items-center text-sm text-gray-500 mt-1">
                                    <i class="ri-check-line text-green-500 mr-2"></i>
                                    Biotechnology
                                </div>
                                <button class="mt-4 w-full inline-flex items-center justify-center px-4 py-2 border border-transparent text-sm font-medium rounded-md shadow-sm text-white bg-yellow-600 hover:bg-yellow-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-yellow-500">
                                    Explore Biology
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Notes Section -->
    <div id="notes" class="py-12 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="lg:text-center">
                <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">Notes</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
                    Your Personal Notebook
                </p>
                <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
                    Organize, edit, and access your notes anytime
                </p>
            </div>

            <div class="mt-10">
                <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
                    <!-- Note Card 1 -->
                    <div class="note-card shadow">
                        <div class="bg-indigo-100 px-4 py-3">
                            <h3 class="text-lg font-medium text-indigo-800">Electrostatics Formulas</h3>
                            <p class="text-sm text-indigo-600">Physics - Chapter 1</p>
                        </div>
                        <div class="p-4">
                            <p class="text-gray-600 text-sm">Coulomb's Law, Electric Field, Gauss's Theorem...</p>
                            <div class="mt-4 flex justify-between items-center">
                                <span class="text-xs text-gray-500">Last updated: 2 days ago</span>
                                <div class="flex space-x-2">
                                    <button class="text-indigo-600 hover:text-indigo-800">
                                        <i class="ri-edit-line"></i>
                                    </button>
                                    <button class="text-green-600 hover:text-green-800">
                                        <i class="ri-download-line"></i>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Note Card 2 -->
                    <div class="note-card shadow">
                        <div class="bg-green-100 px-4 py-3">
                            <h3 class="text-lg font-medium text-green-800">Organic Reactions</h3>
                            <p class="text-sm text-green-600">Chemistry - Chapter 10</p>
                        </div>
                        <div class="p-4">
                            <p class="text-gray-600 text-sm">Named reactions, mechanisms, important conversions...</p>
                            <div class="mt-4 flex justify-between items-center">
                                <span class="text-xs text-gray-500">Last updated: 1 week ago</span>
                                <div class="flex space-x-2">
                                    <button class="text-indigo-600 hover:text-indigo-800">
                                        <i class="ri-edit-line"></i>
                                    </button>
                                    <button class="text-green-600 hover:text-green-800">
                                        <i class="ri-download-line"></i>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Note Card 3 -->
                    <div class="note-card shadow">
                        <div class="bg-yellow-100 px-4 py-3">
                            <h3 class="text-lg font-medium text-yellow-800">Genetics Summary</h3>
                            <p class="text-sm text-yellow-600">Biology - Chapter 5</p>
                        </div>
                        <div class="p-4">
                            <p class="text-gray-600 text-sm">Mendel's laws, DNA replication, genetic disorders...</p>
                            <div class="mt-4 flex justify-between items-center">
                                <span class="text-xs text-gray-500">Last updated: 3 days ago</span>
                                <div class="flex space-x-2">
                                    <button class="text-indigo-600 hover:text-indigo-800">
                                        <i class="ri-edit-line"></i>
                                    </button>
                                    <button class="text-green-600 hover:text-green-800">
                                        <i class="ri-download-line"></i>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Add New Note Card -->
                    <div class="note-card shadow border-2 border-dashed border-gray-300 hover:border-indigo-400 flex items-center justify-center">
                        <button class="flex flex-col items-center p-6 text-indigo-600 hover:text-indigo-800">
                            <i class="ri-add-circle-line text-3xl"></i>
                            <span class="mt-2 font-medium">Add New Note</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- AI Chat Section -->
    <div id="chat" class="py-12 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="lg:text-center">
                <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">Ask Taki</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
                    Your AI Study Assistant
                </p>
                <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
                    Get instant help with any PCB concept or problem
                </p>
            </div>

            <div class="mt-10 bg-white rounded-lg shadow-md p-6">
                <div class="flex items-center mb-6">
                    <div class="ai-avatar">T</div>
                    <div class="ml-4">
                        <h3 class="text-lg font-medium">Taki AI</h3>
                        <p class="text-sm text-gray-500">Ready to help with Physics, Chemistry or Biology</p>
                    </div>
                </div>

                <!-- Chat Messages -->
                <div class="h-96 overflow-y-auto mb-4 p-4 bg-gray-50 rounded-lg">
                    <!-- AI Welcome Message -->
                    <div class="ai-bubble">
                        <p>Hi there! I'm Taki, your AI study assistant. How can I help you with your Class 12 PCB studies today?</p>
                        <p class="mt-2">You can ask me about:</p>
                        <ul class="list-disc list-inside mt-1 text-sm">
                            <li>Explaining concepts</li>
                            <li>Solving numerical problems</li>
                            <li>Summarizing chapters</li>
                            <li>Creating study notes</li>
                        </ul>
                    </div>

                    <!-- Sample User Question -->
                    <div class="user-bubble">
                        <p>Can you explain Faraday's law of electromagnetic induction?</p>
                    </div>

                    <!-- Sample AI Response -->
                    <div class="ai-bubble">
                        <p>Certainly! Faraday's law states that the induced electromotive force (emf) in any closed circuit is equal to the negative of the time rate of change of the magnetic flux through the circuit.</p>
                        <p class="mt-2">Mathematically: ε = -dΦ/dt</p>
                        <p class="mt-2">Where:<br>
                        ε = induced emf<br>
                        Φ = magnetic flux<br>
                        t = time</p>
                        <p class="mt-2">Would you like me to explain this with an example or diagram?</p>
                    </div>
                </div>

                <!-- Chat Input -->
                <div class="flex">
                    <input type="text" placeholder="Ask Taki anything about PCB..." class="flex-1 px-4 py-2 border border-gray-300 rounded-l-md focus:outline-none focus:ring-2 focus:ring-indigo-500">
                    <button class="bg-indigo-600 text-white px-4 py-2 rounded-r-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                        <i class="ri-send-plane-line"></i>
                    </button>
                </div>

                <div class="mt-4 flex flex-wrap gap-2">
                    <button class="px-3 py-1 bg-indigo-100 text-indigo-800 text-sm rounded-full hover:bg-indigo-200">
                        Explain Ohm's Law
                    </button>
                    <button class="px-3 py-1 bg-green-100 text-green-800 text-sm rounded-full hover:bg-green-200">
                        SN1 vs SN2 reactions
                    </button>
                    <button class="px-3 py-1 bg-yellow-100 text-yellow-800 text-sm rounded-full hover:bg-yellow-200">
                        DNA replication steps
                    </button>
                    <button class="px-3 py-1 bg-gray-100 text-gray-800 text-sm rounded-full hover:bg-gray-200">
                        Create summary notes
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Testimonials -->
    <div class="py-12 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="lg:text-center">
                <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">Testimonials</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
                    What Students Say
                </p>
            </div>

            <div class="mt-10 grid gap-8 md:grid-cols-3">
                <!-- Testimonial 1 -->
                <div class="bg-gray-50 p-6 rounded-lg">
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img class="h-12 w-12 rounded-full" src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-sm font-bold text-gray-900">Priya Sharma</h4>
                            <div class="flex text-yellow-400 mt-1">
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                            </div>
                        </div>
                    </div>
                    <p class="mt-4 text-gray-600">
                        "Taki helped me understand organic chemistry reactions so easily! The way it breaks down complex concepts is amazing."
                    </p>
                </div>

                <!-- Testimonial 2 -->
                <div class="bg-gray-50 p-6 rounded-lg">
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img class="h-12 w-12 rounded-full" src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-sm font-bold text-gray-900">Rahul Verma</h4>
                            <div class="flex text-yellow-400 mt-1">
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                            </div>
                        </div>
                    </div>
                    <p class="mt-4 text-gray-600">
                        "The physics numerical solver is a lifesaver! It doesn't just give answers but explains each step clearly."
                    </p>
                </div>

                <!-- Testimonial 3 -->
                <div class="bg-gray-50 p-6 rounded-lg">
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img class="h-12 w-12 rounded-full" src="https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-sm font-bold text-gray-900">Ananya Patel</h4>
                            <div class="flex text-yellow-400 mt-1">
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                                <i class="ri-star-fill"></i>
                            </div>
                        </div>
                    </div>
                    <p class="mt-4 text-gray-600">
                        "Biology has never been easier! Taki's summaries and mnemonics helped me score 95 in my boards."
                    </p>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white">
        <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Study With Taki</h3>
                    <p class="mt-4 text-sm text-gray-300">
                        Your AI-powered study companion for Class 12 PCB students.
                    </p>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Subjects</h3>
                    <ul class="mt-4 space-y-2">
                        <li><a href="#" class="text-sm text-gray-300 hover:text-white">Physics</a></li>
                        <li><a href="#" class="text-sm text-gray-300 hover:text-white">Chemistry</a></li>
                        <li><a href="#" class="text-sm text-gray-300 hover:text-white">Biology</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Features</h3>
                    <ul class="mt-4 space-y-2">
                        <li><a href="#" class="text-sm text-gray-300 hover:text-white">Doubt Solving</a></li>
                        <li><a href="#" class="text-sm text-gray-300 hover:text-white">Note Taking</a></li>
                        <li><a href="#" class="text-sm text-gray-300 hover:text-white">Summarization</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Connect</h3>
                    <div class="mt-4 flex space-x-6">
                        <a href="https://www.instagram.com/studywithtaki00?igsh=MW5lOWVjbWZucG56bA==" target="_blank" class="text-gray-400 hover:text-white">
                            <i class="ri-instagram-line text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="ri-facebook-line text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="ri-twitter-line text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="ri-youtube-line text-xl"></i>
                        </a>
                    </div>
                    <div class="mt-4">
                        <p class="text-sm text-gray-300">Email: support@studywithtaki.com</p>
                    </div>
                </div>
            </div>
            <div class="mt-8 border-t border-gray-700 pt-8 flex justify-between">
                <p class="text-sm text-gray-400">
                    &copy; 2023 Study With Taki. All rights reserved.
                </p>
                <div class="flex space-x-6">
                    <a href="#" class="text-sm text-gray-400 hover:text-white">Privacy Policy</a>
                    <a href="#" class="text-sm text-gray-400 hover:text-white">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Floating Action Button -->
    <div class="floating-btn">
        <i class="ri-question-answer-line text-2xl"></i>
    </div>

    <script>
        // Simple interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Floating button click handler
            const floatingBtn = document.querySelector('.floating-btn');
            if (floatingBtn) {
                floatingBtn.addEventListener('click', function() {
                    document.getElementById('chat').scrollIntoView({ behavior: 'smooth' });
                });
            }

            // Sample chat quick question buttons
            const quickQuestions = document.querySelectorAll('#chat button:not([type="submit"])');
            quickQuestions.forEach(button => {
                button.addEventListener('click', function() {
                    const question = this.textContent.trim();
                    const input = document.querySelector('#chat input');
                    if (input) {
                        input.value = question;
                        input.focus();
                    }
                });
            });

            // Subject card click handlers
            const subjectCards = document.querySelectorAll('.subject-card');
            subjectCards.forEach(card => {
                card.addEventListener('click', function(e) {
                    if (e.target.tagName !== 'BUTTON') {
                        const button = this.querySelector('button');
                        if (button) {
                            button.click();
                        }
                    }
                });
            });
        });
    </script>
</body>
</html>
