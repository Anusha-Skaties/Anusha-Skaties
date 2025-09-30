Based on the details from your existing portfolio, I've created a complete, professional, and visually stunning single-page web portfolio for you. It's designed to be hosted on a website and features a modern, interactive design that highlights your expertise in GenAI, Data Science, and MLOps.

This portfolio is built as a **Single Page Application (SPA)**, ensuring a seamless user experience without page reloads. The layout is structured to tell your professional story, starting with a powerful hero section and moving logically through your skills, experience, and projects.

You can copy and paste the entire code below into a single HTML file (e.g., `index.html`) to launch your new portfolio.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anusha Yaramala - GenAI & Data Science Architect</title>
    <meta name="description" content="Anusha Yaramala is a GenAI Specialist, Data Scientist, and MLOps Engineer with 4+ years of experience building next-gen AI solutions.">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --primary-color: #4A00E0; /* A deep, rich violet */
            --secondary-color: #8E2DE2; /* A vibrant purple */
            --text-dark: #1F2937;
            --text-light: #f9fafb;
            --bg-light: #FFFFFF;
            --bg-dark: #0F172A;
        }

        html { scroll-behavior: smooth; }
        body { font-family: 'Inter', sans-serif; background-color: var(--bg-light); color: var(--text-dark); }
        h1, h2 { font-family: 'Playfair Display', serif; }

        .btn-primary {
            background-image: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: var(--text-light);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .nav-link.active {
            color: var(--primary-color);
            border-bottom: 2px solid var(--primary-color);
        }
        .nav-link:hover {
            color: var(--primary-color);
        }
        .section-header {
            color: var(--primary-color);
            position: relative;
            display: inline-block;
        }
        .section-header::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
            width: 60%;
            height: 2px;
            background-color: var(--secondary-color);
        }

        .card {
            background-color: #F3F4F6;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        .icon {
            color: var(--primary-color);
            transition: transform 0.3s ease;
        }
        .card:hover .icon {
            transform: scale(1.1);
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .animate-on-scroll.is-visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body class="bg-gray-50">

    <nav id="navbar" class="fixed top-0 left-0 w-full bg-white bg-opacity-90 backdrop-blur-sm z-50 shadow-md">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#hero" class="text-2xl font-bold text-gray-800">ANUSHA</a>
            <div class="hidden md:flex space-x-8">
                <a href="#about" class="nav-link text-gray-600 font-medium transition-colors">About</a>
                <a href="#experience" class="nav-link text-gray-600 font-medium transition-colors">Experience</a>
                <a href="#projects" class="nav-link text-gray-600 font-medium transition-colors">Projects</a>
                <a href="#contact" class="nav-link text-gray-600 font-medium transition-colors">Contact</a>
            </div>
            <button id="mobile-menu-btn" class="md:hidden text-gray-800 focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </div>
        <div id="mobile-menu" class="hidden md:hidden bg-white">
            <a href="#about" class="block py-3 px-6 text-gray-600 font-medium">About</a>
            <a href="#experience" class="block py-3 px-6 text-gray-600 font-medium">Experience</a>
            <a href="#projects" class="block py-3 px-6 text-gray-600 font-medium">Projects</a>
            <a href="#contact" class="block py-3 px-6 text-gray-600 font-medium">Contact</a>
        </div>
    </nav>

    <main class="pt-24">
        <section id="hero" class="container mx-auto px-6 py-16 text-center animate-on-scroll">
            <div class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-white shadow-lg overflow-hidden">
                <img src="https://via.placeholder.com/150" alt="Anusha Yaramala" class="w-full h-full object-cover">
            </div>
            <h1 class="text-5xl font-extrabold text-gray-900 leading-tight">
                Anusha Yaramala
            </h1>
            <p class="mt-4 text-xl text-gray-600 max-w-2xl mx-auto">
                Certified GenAI Specialist | Data Scientist | MLOps Engineer
            </p>
            <div class="mt-8 space-x-4">
                <a href="#projects" class="btn-primary inline-block py-3 px-8 rounded-full font-semibold text-lg">
                    View My Work
                </a>
                <a href="#contact" class="inline-block py-3 px-8 rounded-full border-2 border-gray-400 text-gray-700 font-semibold text-lg hover:bg-gray-100 transition">
                    Get in Touch
                </a>
            </div>
        </section>

        <section id="about" class="container mx-auto px-6 py-16 animate-on-scroll">
            <h2 class="text-4xl font-bold text-center section-header mb-12">About Me</h2>
            <div class="bg-white rounded-xl shadow-lg p-8 md:p-12">
                <p class="text-lg text-gray-600 leading-relaxed mb-6">
                    With over 4 years of hands-on experience, I am a GenAI specialist and data science architect with a proven track record of designing and deploying cutting-edge AI/ML solutions. My expertise spans the entire lifecycle, from building robust ETL pipelines to architecting and fine-tuning large language models.
                </p>
                <p class="text-lg text-gray-600 leading-relaxed">
                    I thrive on solving complex business problems with measurable impact, as demonstrated by my work in reducing operational costs, optimizing performance, and driving innovation at companies like Brighthouse Financial, Texas Instruments, and Deutsche Bank. My passion lies in architecting next-gen GenAI solutions that transform data into intelligence at scale.
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mt-12">
                    <div class="text-center">
                        <span class="text-5xl font-bold text-primary-color">4+</span>
                        <p class="text-gray-500 mt-2 font-medium">Years of Experience</p>
                    </div>
                    <div class="text-center">
                        <span class="text-5xl font-bold text-primary-color">91.68%</span>
                        <p class="text-gray-500 mt-2 font-medium">Highest F1 Score</p>
                    </div>
                    <div class="text-center">
                        <span class="text-5xl font-bold text-primary-color">40%</span>
                        <p class="text-gray-500 mt-2 font-medium">Reduction in Manual Calls</p>
                    </div>
                    <div class="text-center">
                        <span class="text-5xl font-bold text-primary-color">1</span>
                        <p class="text-gray-500 mt-2 font-medium">Research Publication</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="experience" class="container mx-auto px-6 py-16 animate-on-scroll">
            <h2 class="text-4xl font-bold text-center section-header mb-12">Professional Experience</h2>
            <div class="grid grid-cols-1 gap-12">
                <div class="card p-6 rounded-xl shadow-md">
                    <div class="md:flex md:justify-between md:items-start">
                        <div>
                            <h3 class="text-2xl font-bold text-gray-800">GenAI Specialist</h3>
                            <p class="text-lg text-gray-600">Brighthouse Financial | Sept 2024 – Present</p>
                        </div>
                        <span class="mt-2 md:mt-0 px-4 py-1 text-sm font-semibold text-white bg-primary-color rounded-full">Current Role</span>
                    </div>
                    <ul class="list-disc list-inside mt-4 text-gray-700 space-y-2">
                        <li>Architected and deployed a multi-modal RAG system using GPT-4, Claude, and BERT, resulting in a **40% reduction in manual customer service calls**.</li>
                        <li>Optimized GPU memory usage by **70%** and reduced model training time by **30%** through fine-tuning techniques like QLoRA and RLHF.</li>
                        <li>Developed and orchestrated intelligent chatbot agents using LangChain and vector databases like Pinecone and FAISS.</li>
                    </ul>
                </div>

                <div class="card p-6 rounded-xl shadow-md">
                    <div class="md:flex md:justify-between md:items-start">
                        <div>
                            <h3 class="text-2xl font-bold text-gray-800">Neural Network Engineer</h3>
                            <p class="text-lg text-gray-600">Texas Instruments | Feb 2023 – Jul 2024</p>
                        </div>
                    </div>
                    <ul class="list-disc list-inside mt-4 text-gray-700 space-y-2">
                        <li>Led the development of deep learning models in Keras and PyTorch, achieving a peak **91.68% F1 score**.</li>
                        <li>Improved text analysis efficiency by **70%** by implementing custom Named Entity Recognition (NER) and sentiment analysis pipelines.</li>
                        <li>Automated MLOps pipelines on Azure and AWS SageMaker, cutting model production deployment time by **30%**.</li>
                    </ul>
                </div>

                <div class="card p-6 rounded-xl shadow-md">
                    <div class="md:flex md:justify-between md:items-start">
                        <div>
                            <h3 class="text-2xl font-bold text-gray-800">Data Engineer</h3>
                            <p class="text-lg text-gray-600">Deutsche Bank | May 2021 – Jul 2022</p>
                        </div>
                    </div>
                    <ul class="list-disc list-inside mt-4 text-gray-700 space-y-2">
                        <li>Optimized SQL queries and PySpark workflows, resulting in a **35% performance improvement** and a **40% reduction** in data transformation time.</li>
                        <li>Developed and automated over **100 Airflow workflows** to handle large-scale ETL, processing up to 2 million records in minutes.</li>
                        <li>Designed real-time data streaming architectures using Kafka and Google Cloud Pub/Sub.</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="projects" class="container mx-auto px-6 py-16 animate-on-scroll">
            <h2 class="text-4xl font-bold text-center section-header mb-12">Flagship Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <div class="card p-8 rounded-xl shadow-md">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">YouTube Trend Analysis</h3>
                    <p class="text-gray-600 mb-4">Scalable Data Pipeline on AWS</p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>Engineered a fully automated serverless ETL pipeline using AWS Glue and Lambda.</li>
                        <li>Processed over **1 million records daily** with sub-minute data ingestion.</li>
                        <li>Developed interactive dashboards in AWS QuickSight to visualize real-time trends.</li>
                    </ul>
                    <div class="mt-6 flex space-x-4">
                        <a href="https://github.com/anushayaramala" target="_blank" class="text-gray-600 hover:text-primary-color transition-colors">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.418 2.864 8.125 6.83 9.497.5.092.682-.217.682-.483 0-.237-.008-.867-.013-1.7-2.782.604-3.37-1.34-3.37-1.34-.454-1.156-1.11-1.465-1.11-1.465-.908-.62.069-.608.069-.608 1.004.07 1.532 1.03 1.532 1.03.89 1.528 2.336 1.087 2.906.832.09-.64.35-1.087.636-1.334-2.217-.253-4.555-1.108-4.555-4.933 0-1.087.387-1.979 1.026-2.674-.103-.253-.446-1.266.098-2.635 0 0 .84-.268 2.75 1.025.798-.223 1.649-.335 2.498-.339 2.503.004 3.354.116 4.152.339 1.91-1.293 2.748-1.025 2.748-1.025.545 1.37.202 2.382.099 2.635.64.695 1.025 1.587 1.025 2.674 0 3.834-2.34 4.68-4.562 4.925.358.307.676.917.676 1.848 0 1.335-.012 2.415-.012 2.742 0 .267.18.579.688.484 3.96-1.372 6.825-5.078 6.825-9.496C22 6.484 17.523 2 12 2Z" clip-rule="evenodd" /></svg>
                        </a>
                        </div>
                </div>

                <div class="card p-8 rounded-xl shadow-md">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">Research Publication</h3>
                    <p class="text-gray-600 mb-4">AI Application in Materials Science</p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>Authored and published a research paper on using neural networks to model hybrid composite materials.</li>
                        <li>Developed a custom ANN architecture to predict material properties with high accuracy.</li>
                        <li>Contributed to the field of AI-driven materials discovery and manufacturing optimization.</li>
                    </ul>
                    <div class="mt-6 flex space-x-4">
                        <a href="https://scholar.google.com" target="_blank" class="text-gray-600 hover:text-primary-color transition-colors">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 12c-2.21 0-4 1.79-4 4s1.79 4 4 4 4-1.79 4-4-1.79-4-4-4zm-8-8v12h4V8h8V4H4zm16 0H12v4h8V4z" fill-rule="evenodd" clip-rule="evenodd"></path></svg>
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="container mx-auto px-6 py-16 animate-on-scroll">
            <h2 class="text-4xl font-bold text-center section-header mb-12">Core Competencies</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md border-l-4 border-primary-color">
                    <div class="flex items-center mb-3">
                        <svg class="w-8 h-8 mr-2 text-primary-color" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" /></svg>
                        <h3 class="text-xl font-bold">Generative AI</h3>
                    </div>
                    <ul class="text-gray-700 list-disc list-inside space-y-1">
                        <li>Multi-modal RAG</li>
                        <li>LLM Fine-tuning (QLoRA/RLHF)</li>
                        <li>Vector Databases</li>
                        <li>Prompt Engineering</li>
                    </ul>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border-l-4 border-primary-color">
                    <div class="flex items-center mb-3">
                        <svg class="w-8 h-8 mr-2 text-primary-color" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M12 8c1.657 0 3 1.343 3 3v2a3 3 0 01-3 3c-1.657 0-3-1.343-3-3v-2a3 3 0 013-3zM8 8V7a4 4 0 118 0v1" /></svg>
                        <h3 class="text-xl font-bold">Data Science</h3>
                    </div>
                    <ul class="text-gray-700 list-disc list-inside space-y-1">
                        <li>Deep Learning (CNN/RNN/ANN)</li>
                        <li>NLP & Computer Vision</li>
                        <li>Predictive Analytics</li>
                        <li>Statistical Modeling</li>
                    </ul>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border-l-4 border-primary-color">
                    <div class="flex items-center mb-3">
                        <svg class="w-8 h-8 mr-2 text-primary-color" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.227.608 3.223 0z" /><path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" /></svg>
                        <h3 class="text-xl font-bold">MLOps</h3>
                    </div>
                    <ul class="text-gray-700 list-disc list-inside space-y-1">
                        <li>Model Deployment</li>
                        <li>Pipeline Automation</li>
                        <li>CI/CD for ML</li>
                        <li>Cloud Infrastructure</li>
                    </ul>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border-l-4 border-primary-color">
                    <div class="flex items-center mb-3">
                        <svg class="w-8 h-8 mr-2 text-primary-color" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14m-6 0a2 2 0 002 2h2a2 2 0 002-2" /></svg>
                        <h3 class="text-xl font-bold">Data Engineering</h3>
                    </div>
                    <ul class="text-gray-700 list-disc list-inside space-y-1">
                        <li>ETL Pipelines</li>
                        <li>Big Data Processing</li>
                        <li>Real-time Streaming</li>
                        <li>Query Optimization</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="contact" class="container mx-auto px-6 py-16 animate-on-scroll">
            <h2 class="text-4xl font-bold text-center section-header mb-12">Let's Connect</h2>
            <div class="max-w-3xl mx-auto bg-white rounded-xl shadow-lg p-8 md:p-12 text-center">
                <p class="text-lg text-gray-600 mb-6">
                    I'm open to new opportunities and collaborations. Feel free to reach out to discuss how my expertise can help your organization.
                </p>
                <div class="flex justify-center space-x-6">
                    <a href="https://linkedin.com/in/anushayaramala" target="_blank" class="text-gray-600 hover:text-primary-color transition-colors">
                        <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.564-4 0v5.604h-3v-11h3v1.765c1.395-2.536 4-2.764 4-2.764-2.209 0-4.004-.84-4.523-2.144z"/></svg>
                    </a>
                    <a href="https://github.com/anushayaramala" target="_blank" class="text-gray-600 hover:text-primary-color transition-colors">
                        <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.418 2.864 8.125 6.83 9.497.5.092.682-.217.682-.483 0-.237-.008-.867-.013-1.7-2.782.604-3.37-1.34-3.37-1.34-.454-1.156-1.11-1.465-1.11-1.465-.908-.62.069-.608.069-.608 1.004.07 1.532 1.03 1.532 1.03.89 1.528 2.336 1.087 2.906.832.09-.64.35-1.087.636-1.334-2.217-.253-4.555-1.108-4.555-4.933 0-1.087.387-1.979 1.026-2.674-.103-.253-.446-1.266.098-2.635 0 0 .84-.268 2.75 1.025.798-.223 1.649-.335 2.498-.339 2.503.004 3.354.116 4.152.339 1.91-1.293 2.748-1.025 2.748-1.025.545 1.37.202 2.382.099 2.635.64.695 1.025 1.587 1.025 2.674 0 3.834-2.34 4.68-4.562 4.925.358.307.676.917.676 1.848 0 1.335-.012 2.415-.012 2.742 0 .267.18.579.688.484 3.96-1.372 6.825-5.078 6.825-9.496C22 6.484 17.523 2 12 2Z" clip-rule="evenodd" /></svg>
                    </a>
                    <a href="mailto:anushayaramala31@gmail.com" class="text-gray-600 hover:text-primary-color transition-colors">
                        <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M22 6c0-1.1-.9-2-2-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6zm-2 0l-8 5-8-5h16zm0 12H4V8l8 5 8-5v10z" /></svg>
                    </a>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-800 text-gray-300 py-8 text-center mt-12">
        <div class="container mx-auto px-6">
            <p>&copy; 2024 Anusha Yaramala. All rights reserved.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Mobile Menu Toggle
            const mobileMenuBtn = document.getElementById('mobile-menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuBtn.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });
            mobileMenu.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });

            // Smooth Scroll & Active Nav Link
            const navLinks = document.querySelectorAll('#navbar a');
            navLinks.forEach(link => {
                link.addEventListener('click', (e) => {
                    const href = link.getAttribute('href');
                    if (href.startsWith('#')) {
                        e.preventDefault();
                        const targetId = href.substring(1);
                        const targetSection = document.getElementById(targetId);
                        if (targetSection) {
                            window.scrollTo({
                                top: targetSection.offsetTop - document.getElementById('navbar').offsetHeight,
                                behavior: 'smooth'
                            });
                        }
                    }
                });
            });

            const sections = document.querySelectorAll('section[id]');
            const observerOptions = {
                root: null,
                threshold: 0.3,
                rootMargin: `-${document.getElementById('navbar').offsetHeight}px 0px 0px 0px`
            };

            const observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const activeId = entry.target.id;
                        navLinks.forEach(link => {
                            if (link.getAttribute('href') === `#${activeId}`) {
                                link.classList.add('active');
                            } else {
                                link.classList.remove('active');
                            }
                        });
                        entry.target.classList.add('is-visible');
                    }
                });
            }, observerOptions);

            sections.forEach(section => {
                observer.observe(section);
            });
        });
    </script>

</body>
</html>
```
