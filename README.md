<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>7ames - README</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE'
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
        }
        .gradient-text {
            background: linear-gradient(135deg, #5D5CDE 0%, #8B5CF6 50%, #EC4899 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .hero-glow {
            background: radial-gradient(circle at center, rgba(93, 92, 222, 0.1) 0%, transparent 70%);
        }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 min-h-screen transition-colors duration-300">
    <div class="min-h-screen flex items-center justify-center px-4 hero-glow">
        <div class="text-center max-w-4xl mx-auto">
            <!-- Main Logo/Title -->
            <div class="mb-8">
                <h1 class="text-7xl md:text-8xl lg:text-9xl font-bold gradient-text mb-4 tracking-tight">
                    7ames
                </h1>
                <div class="w-32 h-1 bg-gradient-to-r from-primary to-purple-500 mx-auto rounded-full"></div>
            </div>
            
            <!-- Subtitle -->
            <p class="text-xl md:text-2xl text-gray-600 dark:text-gray-300 mb-12 font-light leading-relaxed">
                Building the future, one game at a time
            </p>
            
            <!-- Badges -->
            <div class="flex flex-wrap justify-center gap-4 mb-12">
                <span class="px-4 py-2 bg-gray-100 dark:bg-gray-800 text-gray-700 dark:text-gray-300 rounded-full text-sm font-medium">
                    🎮 Game Development
                </span>
                <span class="px-4 py-2 bg-gray-100 dark:bg-gray-800 text-gray-700 dark:text-gray-300 rounded-full text-sm font-medium">
                    ✨ Innovation
                </span>
                <span class="px-4 py-2 bg-gray-100 dark:bg-gray-800 text-gray-700 dark:text-gray-300 rounded-full text-sm font-medium">
                    🚀 Performance
                </span>
            </div>
            
            <!-- CTA Buttons -->
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#" class="px-8 py-4 bg-primary hover:bg-purple-600 text-white rounded-lg font-semibold transition-all duration-200 transform hover:scale-105 shadow-lg">
                    Get Started
                </a>
                <a href="#" class="px-8 py-4 border-2 border-gray-300 dark:border-gray-600 text-gray-700 dark:text-gray-300 hover:border-primary hover:text-primary rounded-lg font-semibold transition-all duration-200">
                    View Documentation
                </a>
            </div>
            
            <!-- Stats -->
            <div class="mt-16 grid grid-cols-3 gap-8 max-w-md mx-auto">
                <div class="text-center">
                    <div class="text-3xl font-bold text-primary mb-2">7+</div>
                    <div class="text-sm text-gray-500 dark:text-gray-400">Projects</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold text-primary mb-2">∞</div>
                    <div class="text-sm text-gray-500 dark:text-gray-400">Possibilities</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold text-primary mb-2">1</div>
                    <div class="text-sm text-gray-500 dark:text-gray-400">Vision</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode support
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });

        // Add subtle animation on load
        window.addEventListener('load', () => {
            const elements = document.querySelectorAll('h1, p, .flex');
            elements.forEach((el, index) => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                setTimeout(() => {
                    el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                    el.style.opacity = '1';
                    el.style.transform = 'translateY(0)';
                }, index * 200);
            });
        });
    </script>
</body>
</html>
