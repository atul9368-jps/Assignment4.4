<!DOCTYPE html>
<html lang="en">
<head>
  <!-- 1. UTF-8 Character Encoding -->
  <meta charset="UTF-8">
  <!-- 2. Responsive Mobile Viewport -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- 3. Meaningful Title -->
  <title>Assignment 4.4 - Metadata & Page Setup Hub</title>
  <!-- 4. Meta Description -->
  <meta name="description" content="Assignment 4.4 metadata implementation hub featuring interactive HTML code viewer, browser preview simulations, and metadata documentation for updated web pages.">
  <!-- 5. Favicon Link (SVG Data URI) -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%232563eb'/><path d='M30 30h40v10H30zM30 48h40v8H30zM30 64h25v8H30z' fill='%23ffffff'/><circle cx='70' cy='68' r='7' fill='%2310b981'/></svg>">
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Inter & JetBrains Mono -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
  
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
    code, pre {
      font-family: 'JetBrains Mono', monospace;
    }
    /* Custom scrollbars */
    ::-webkit-scrollbar {
      width: 8px;
      height: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #0f172a;
    }
    ::-webkit-scrollbar-thumb {
      background: #334155;
      border-radius: 4px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #475569;
    }
  </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col selection:bg-blue-500 selection:text-white">

  <!-- Toast Notification Container -->
  <div id="toast" class="fixed top-5 right-5 z-50 transform translate-y-[-100px] opacity-0 transition-all duration-300 ease-in-out pointer-events-none">
    <div class="bg-emerald-500 text-slate-950 font-semibold px-4 py-3 rounded-xl shadow-2xl flex items-center space-x-2 border border-emerald-400">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 13l4 4L19 7"></path>
      </svg>
      <span id="toastMessage">Copied to clipboard!</span>
    </div>
  </div>

  <!-- Header Section -->
  <header class="border-b border-slate-800 bg-slate-900/80 backdrop-blur-md sticky top-0 z-40">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4">
        <div class="flex items-center space-x-3">
          <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-blue-600 to-indigo-500 flex items-center justify-center shadow-lg shadow-blue-500/20 ring-1 ring-white/20">
            <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
            </svg>
          </div>
          <div>
            <div class="flex items-center space-x-2">
              <span class="bg-blue-500/10 text-blue-400 text-xs font-bold px-2.5 py-0.5 rounded-full border border-blue-500/20">Assignment 4.4</span>
              <span class="text-xs text-slate-400 hidden sm:inline">• Metadata & Page Setup Hub</span>
            </div>
            <h1 class="text-xl sm:text-2xl font-extrabold text-white tracking-tight">HTML Metadata Workbench</h1>
          </div>
        </div>

        <!-- Quick Info Pills -->
        <div class="flex items-center space-x-2 text-xs">
          <div class="bg-slate-800/80 border border-slate-700/60 px-3 py-1.5 rounded-lg flex items-center space-x-2">
            <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
            <span class="text-slate-300 font-medium">UTF-8 & Viewport Active</span>
          </div>
          <div class="bg-slate-800/80 border border-slate-700/60 px-3 py-1.5 rounded-lg text-slate-300 font-medium hidden md:flex items-center space-x-1">
            <span>3 Pages Updated</span>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!-- Main Content Layout -->
  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-8">

    <!-- Page Selection Tabs -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl p-2 shadow-xl">
      <div class="flex flex-col md:flex-row items-stretch md:items-center justify-between gap-3">
        <div class="grid grid-cols-1 sm:grid-cols-3 gap-2 flex-1" role="tablist">
          
          <button 
            id="tab-page1" 
            onclick="switchPage('page1')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all bg-blue-600 text-white shadow-lg shadow-blue-600/25"
          >
            <div class="flex items-center space-x-3 truncate">
              <span class="p-1.5 rounded-lg bg-white/10 text-white">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
              </span>
              <span class="truncate">1. Registration Form</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-2 py-0.5 rounded bg-white/20 text-white ml-2">registration.html</span>
          </button>

          <button 
            id="tab-page2" 
            onclick="switchPage('page2')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60"
          >
            <div class="flex items-center space-x-3 truncate">
              <span class="p-1.5 rounded-lg bg-slate-800 text-slate-400 border border-slate-700">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 1321 13V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2v4l4-4h9a2 2 0 002-2z"></path></svg>
              </span>
              <span class="truncate">2. Job Application</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700 ml-2">application.html</span>
          </button>

          <button 
            id="tab-page3" 
            onclick="switchPage('page3')"
            class="tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60"
          >
            <div class="flex items-center space-x-3 truncate">
              <span class="p-1.5 rounded-lg bg-slate-800 text-slate-400 border border-slate-700">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h18M3 14h18m-9-4v8m-7 0h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
              </span>
              <span class="truncate">3. Marksheet Table</span>
            </div>
            <span class="text-[10px] uppercase tracking-wider font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700 ml-2">marksheet.html</span>
          </button>

        </div>

        <!-- Mode Toggle Switcher -->
        <div class="flex items-center bg-slate-950 p-1.5 rounded-xl border border-slate-800 self-center md:self-auto">
          <button 
            id="view-preview-btn" 
            onclick="switchViewMode('preview')"
            class="px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 bg-blue-600 text-white transition-all shadow-sm"
          >
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path></svg>
            <span>Live Preview</span>
          </button>
          <button 
            id="view-code-btn" 
            onclick="switchViewMode('code')"
            class="px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 text-slate-400 hover:text-slate-200 transition-all"
          >
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path></svg>
            <span>Full HTML Source</span>
          </button>
        </div>
      </div>
    </div>

    <!-- Active Metadata Spotlight Bar -->
    <div class="bg-gradient-to-r from-blue-900/30 via-slate-900 to-indigo-900/30 border border-blue-500/20 rounded-2xl p-5 relative overflow-hidden">
      <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-blue-500/10 rounded-full blur-3xl pointer-events-none"></div>
      
      <div class="flex flex-col lg:flex-row lg:items-center justify-between gap-4">
        <div class="space-y-1">
          <div class="flex items-center space-x-2">
            <span class="text-xs font-bold uppercase tracking-wider text-blue-400">Page Metadata Metadata Focus</span>
            <span class="text-slate-600">•</span>
            <span id="spotlight-filename" class="text-xs font-mono text-emerald-400 font-semibold">registration.html</span>
          </div>
          <h2 id="spotlight-title" class="text-lg font-bold text-white">Student Registration Form — Metadata Overview</h2>
        </div>

        <!-- Quick Copy Head Tag Button -->
        <button 
          onclick="copyActiveMetadataHead()" 
          class="inline-flex items-center justify-center space-x-2 bg-slate-800 hover:bg-slate-700 active:bg-slate-900 text-slate-200 text-xs font-semibold px-4 py-2.5 rounded-xl border border-slate-700/80 transition shadow-sm self-start lg:self-auto cursor-pointer"
        >
          <svg class="w-4 h-4 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
          </svg>
          <span>Copy &lt;head&gt; Metadata Block</span>
        </button>
      </div>

      <!-- Metadata Attributes Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-3 mt-4 pt-4 border-t border-slate-800/80">
        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Encoding</div>
          <div class="text-xs font-mono text-slate-200 truncate" id="meta-encoding">&lt;meta charset="UTF-8"&gt;</div>
        </div>

        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Viewport Setup</div>
          <div class="text-xs font-mono text-slate-200 truncate" id="meta-viewport">width=device-width, initial-scale=1.0</div>
        </div>

        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Page Title</div>
          <div class="text-xs font-mono text-emerald-300 truncate" id="meta-title">Assignment 4.1 - Student Registration</div>
        </div>

        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800/60">
          <div class="text-[10px] uppercase tracking-wider text-slate-500 font-bold mb-1">Favicon Asset</div>
          <div class="text-xs font-mono text-blue-300 flex items-center space-x-1.5 truncate">
            <span id="meta-favicon-icon" class="w-3.5 h-3.5 flex-shrink-0"></span>
            <span class="truncate">SVG Embedded Data URI</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Main Workspace Container (Preview vs Code Toggle) -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl shadow-2xl overflow-hidden">
      
      <!-- Interactive Simulated Browser Frame (Preview Mode) -->
      <div id="preview-container" class="block">
        
        <!-- Browser Top Header Bar with Simulated Tab & URL Bar -->
        <div class="bg-slate-900 border-b border-slate-800 p-3 flex flex-col sm:flex-row items-stretch sm:items-center justify-between gap-3">
          
          <!-- Browser Tab Bar Simulation -->
          <div class="flex items-center space-x-2">
            <!-- Mac window controls -->
            <div class="flex items-center space-x-1.5 mr-3">
              <span class="w-3 h-3 rounded-full bg-rose-500/80 inline-block"></span>
              <span class="w-3 h-3 rounded-full bg-amber-500/80 inline-block"></span>
              <span class="w-3 h-3 rounded-full bg-emerald-500/80 inline-block"></span>
            </div>

            <!-- Active Simulated Tab -->
            <div class="bg-slate-950 text-slate-200 text-xs font-semibold px-3 py-2 rounded-t-xl border-t border-x border-slate-800 flex items-center space-x-2 max-w-[240px] sm:max-w-xs truncate shadow-inner">
              <div id="browser-tab-icon" class="w-4 h-4 flex-shrink-0">
                <!-- SVG Icon inserted dynamically -->
              </div>
              <span id="browser-tab-title" class="truncate text-slate-200">Assignment 4.1 - Student Registration</span>
            </div>
          </div>

          <!-- Browser URL Bar Simulation -->
          <div class="flex-1 max-w-xl bg-slate-950 border border-slate-800 rounded-lg px-3 py-1.5 flex items-center space-x-2 text-xs font-mono text-slate-400 shadow-inner">
            <svg class="w-3.5 h-3.5 text-emerald-400 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
            </svg>
            <span class="text-slate-500">https://university-portal.edu/assignments/</span>
            <span id="browser-url-path" class="text-blue-400">registration.html</span>
          </div>

          <!-- Zoom/Fullscreen Simulator -->
          <div class="flex items-center space-x-2 text-slate-500 text-xs">
            <span class="bg-slate-950 border border-slate-800 px-2 py-1 rounded text-[11px] font-mono">iframe viewport</span>
          </div>
        </div>

        <!-- Rendered Iframe Content -->
        <div class="relative w-full bg-slate-100 min-h-[600px] h-[650px]">
          <iframe 
            id="page-iframe" 
            class="w-full h-full border-none"
            title="Page Live Preview"
          ></iframe>
        </div>
      </div>

      <!-- Syntax Highlighted Code Viewer Container (Code Mode) -->
      <div id="code-container" class="hidden">
        
        <!-- Code Toolbar -->
        <div class="bg-slate-950 border-b border-slate-800 px-4 py-3 flex items-center justify-between">
          <div class="flex items-center space-x-3">
            <span class="w-3 h-3 rounded-full bg-blue-500 inline-block"></span>
            <span id="code-filename-label" class="text-xs font-mono text-slate-300 font-semibold">registration.html</span>
            <span class="text-xs text-slate-600">•</span>
            <span class="text-xs text-slate-500 font-mono">Complete HTML Source with Metadata</span>
          </div>

          <div class="flex items-center space-x-3">
            <button 
              onclick="copyFullSourceCode()" 
              class="bg-blue-600 hover:bg-blue-500 active:scale-95 text-white text-xs font-semibold px-3 py-1.5 rounded-lg transition shadow flex items-center space-x-1.5"
            >
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
              </svg>
              <span>Copy Full Code</span>
            </button>
          </div>
        </div>

        <!-- Code Content Block -->
        <div class="p-4 bg-slate-950 overflow-x-auto max-h-[650px]">
          <pre><code id="source-code-block" class="text-xs text-slate-300 font-mono leading-relaxed">Loading page source...</code></pre>
        </div>
      </div>

    </div>

    <!-- Metadata Technical Documentation & Requirements Checklist Section -->
    <div class="bg-slate-900 border border-slate-800 rounded-2xl p-6 sm:p-8 space-y-6 shadow-xl">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 border-b border-slate-800 pb-5">
        <div>
          <div class="inline-flex items-center space-x-2 text-emerald-400 text-xs font-bold uppercase tracking-wider mb-1">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span>Assignment 4.4 Reference Guide</span>
          </div>
          <h2 class="text-xl sm:text-2xl font-bold text-white">Metadata Element Requirements & Explanation</h2>
        </div>
        <div class="text-xs text-slate-400 bg-slate-950 px-3 py-2 rounded-xl border border-slate-800 font-mono">
          Standard: HTML5 W3C Specification
        </div>
      </div>

      <!-- Grid of Metadata Explanations -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        
        <!-- Requirement 1: Character Encoding -->
        <div class="bg-slate-950 p-5 rounded-2xl border border-slate-800/80 space-y-3 flex flex-col justify-between">
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold font-mono text-blue-400 bg-blue-500/10 px-2 py-0.5 rounded border border-blue-500/20">Step 1</span>
              <span class="text-[10px] text-emerald-400 font-semibold uppercase tracking-wider">Mandatory Tag</span>
            </div>
            <h3 class="font-bold text-white text-sm">Character Encoding (UTF-8)</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Specifies the character encoding for the HTML document. UTF-8 covers almost all characters, symbols, and emojis across worldwide languages, preventing garbled text rendering.
            </p>
          </div>
          <div class="bg-slate-900 p-2.5 rounded-xl border border-slate-800/80">
            <code class="text-[11px] text-indigo-300 font-mono">&lt;meta charset="UTF-8"&gt;</code>
          </div>
        </div>

        <!-- Requirement 2: Viewport Meta Tag -->
        <div class="bg-slate-950 p-5 rounded-2xl border border-slate-800/80 space-y-3 flex flex-col justify-between">
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold font-mono text-blue-400 bg-blue-500/10 px-2 py-0.5 rounded border border-blue-500/20">Step 2</span>
              <span class="text-[10px] text-emerald-400 font-semibold uppercase tracking-wider">Responsive Design</span>
            </div>
            <h3 class="font-bold text-white text-sm">Mobile Viewport Setup</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Configures the visible area of the browser page to match screen width on mobile devices, setting the initial zoom level to 1.0 and enabling proper fluid layout scaling.
            </p>
          </div>
          <div class="bg-slate-900 p-2.5 rounded-xl border border-slate-800/80 overflow-x-auto">
            <code class="text-[11px] text-indigo-300 font-mono">&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;</code>
          </div>
        </div>

        <!-- Requirement 3: Meaningful Title -->
        <div class="bg-slate-950 p-5 rounded-2xl border border-slate-800/80 space-y-3 flex flex-col justify-between">
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold font-mono text-blue-400 bg-blue-500/10 px-2 py-0.5 rounded border border-blue-500/20">Step 3</span>
              <span class="text-[10px] text-emerald-400 font-semibold uppercase tracking-wider">SEO & UX</span>
            </div>
            <h3 class="font-bold text-white text-sm">Unique Page Title</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Defines the text displayed on browser tabs and search engine result titles. Each document must have a distinct, highly contextual description of its contents.
            </p>
          </div>
          <div class="bg-slate-900 p-2.5 rounded-xl border border-slate-800/80">
            <code class="text-[11px] text-indigo-300 font-mono">&lt;title&gt;Assignment 4.1 - Student Registration&lt;/title&gt;</code>
          </div>
        </div>

        <!-- Requirement 4: Meta Description -->
        <div class="bg-slate-950 p-5 rounded-2xl border border-slate-800/80 space-y-3 flex flex-col justify-between">
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold font-mono text-blue-400 bg-blue-500/10 px-2 py-0.5 rounded border border-blue-500/20">Step 4</span>
              <span class="text-[10px] text-emerald-400 font-semibold uppercase tracking-wider">Search Snippet</span>
            </div>
            <h3 class="font-bold text-white text-sm">Meta Description</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Provides a concise summary (typically 50-160 characters) of the page content used by search engines to generate search snippets and preview text.
            </p>
          </div>
          <div class="bg-slate-900 p-2.5 rounded-xl border border-slate-800/80 overflow-x-auto">
            <code class="text-[11px] text-indigo-300 font-mono">&lt;meta name="description" content="..."&gt;</code>
          </div>
        </div>

        <!-- Requirement 5: Favicon Integration -->
        <div class="bg-slate-950 p-5 rounded-2xl border border-slate-800/80 space-y-3 flex flex-col justify-between">
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold font-mono text-blue-400 bg-blue-500/10 px-2 py-0.5 rounded border border-blue-500/20">Step 5</span>
              <span class="text-[10px] text-emerald-400 font-semibold uppercase tracking-wider">Branding</span>
            </div>
            <h3 class="font-bold text-white text-sm">Favicon Integration (SVG)</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Links a small visual graphic displayed next to the page title on browser tabs, bookmark lists, and search results using an embedded SVG Data URI for crisp zero-dependency rendering.
            </p>
          </div>
          <div class="bg-slate-900 p-2.5 rounded-xl border border-slate-800/80 overflow-x-auto">
            <code class="text-[11px] text-indigo-300 font-mono">&lt;link rel="icon" type="image/svg+xml" href="data:image/svg+xml..."&gt;</code>
          </div>
        </div>

        <!-- Requirement 6: Verified Assets -->
        <div class="bg-slate-950 p-5 rounded-2xl border border-slate-800/80 space-y-3 flex flex-col justify-between">
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="text-xs font-bold font-mono text-blue-400 bg-blue-500/10 px-2 py-0.5 rounded border border-blue-500/20">Step 6</span>
              <span class="text-[10px] text-emerald-400 font-semibold uppercase tracking-wider">Asset Integrity</span>
            </div>
            <h3 class="font-bold text-white text-sm">External CSS & Asset Linking</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Ensures stylesheet links (`&lt;link rel="stylesheet"&gt;`), CDN references (Tailwind CSS, Google Fonts), and file paths are correctly structured and accessible without broken references.
            </p>
          </div>
          <div class="bg-slate-900 p-2.5 rounded-xl border border-slate-800/80 overflow-x-auto">
            <code class="text-[11px] text-indigo-300 font-mono">&lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;</code>
          </div>
        </div>

      </div>
    </div>

  </main>

  <!-- Footer -->
  <footer class="border-t border-slate-800 bg-slate-900/60 py-6 text-center text-xs text-slate-500">
    <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-3">
      <div>
        <span>Assignment 4.4 — Metadata & Page Setup</span>
      </div>
      <div class="flex items-center space-x-4">
        <span class="text-slate-400">All 3 HTML Pages Fully Validated & Updated</span>
      </div>
    </div>
  </footer>

  <!-- Embedded Full HTML Pages Source Store & Interactive Logic -->
  <script>
    // Embedded SVG Favicon Data Strings
    const SVG_FAVICON_PAGE1 = `<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%232563eb'/><path d='M50 25a15 15 0 100 30 15 15 0 000-30zM30 75c0-11 9-20 20-20s20 9 20 20H30z' fill='%23ffffff'/></svg>`;
    const SVG_FAVICON_PAGE2 = `<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%23059669'/><path d='M30 35h40v40H30z' fill='none' stroke='%23ffffff' stroke-width='6'/><path d='M40 35V25a10 10 0 0120 0v10' fill='none' stroke='%23ffffff' stroke-width='6'/></svg>`;
    const SVG_FAVICON_PAGE3 = `<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%237c3aed'/><path d='M25 25h50v50H25z' fill='none' stroke='%23ffffff' stroke-width='6'/><path d='M25 50h50M50 25v50' stroke='%23ffffff' stroke-width='6'/></svg>`;

    // Database of complete updated HTML pages with metadata
    const pagesData = {
      page1: {
        filename: "registration.html",
        title: "Assignment 4.1 - Student Registration",
        description: "Official student registration portal for enrollment, academic stream selection, and profile creation.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_PAGE1,
        code: `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- 1. UTF-8 Character Encoding -->
  <meta charset="UTF-8">
  <!-- 2. Mobile Viewport Setting -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- 3. Meaningful Unique Title -->
  <title>Assignment 4.1 - Student Registration</title>
  <!-- 4. Meta Description -->
  <meta name="description" content="Official student registration portal for enrollment, academic stream selection, and profile creation.">
  <!-- 5. SVG Favicon Link -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%232563eb'/><path d='M50 25a15 15 0 100 30 15 15 0 000-30zM30 75c0-11 9-20 20-20s20 9 20 20H30z' fill='%23ffffff'/></svg>">
  
  <!-- 6. Verified External Assets & Frameworks -->
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Inter', sans-serif; }
  </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen py-10 px-4 sm:px-6">

  <div class="max-w-2xl mx-auto bg-slate-800 rounded-2xl p-6 sm:p-8 shadow-2xl border border-slate-700">
    <!-- Header -->
    <div class="border-b border-slate-700 pb-6 mb-6 text-center">
      <span class="bg-blue-500/10 text-blue-400 text-xs font-semibold px-3 py-1 rounded-full border border-blue-500/20">Assignment 4.1</span>
      <h1 class="text-2xl sm:text-3xl font-bold text-white mt-2">Student Registration Form</h1>
      <p class="text-xs sm:text-sm text-slate-400 mt-1">Complete your profile setup for the upcoming academic term</p>
    </div>

    <!-- Registration Form -->
    <form class="space-y-5" onsubmit="event.preventDefault(); alert('Registration Submitted Successfully!');">
      
      <!-- Full Name -->
      <div>
        <label for="fullName" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Full Name *</label>
        <input type="text" id="fullName" required placeholder="e.g. Alex Johnson" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
      </div>

      <!-- Email & Phone -->
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
        <div>
          <label for="email" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Email Address *</label>
          <input type="email" id="email" required placeholder="alex@university.edu" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
        </div>
        <div>
          <label for="phone" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Phone Number</label>
          <input type="tel" id="phone" placeholder="+1 (555) 000-0000" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
        </div>
      </div>

      <!-- Academic Department -->
      <div>
        <label for="dept" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Academic Department *</label>
        <select id="dept" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-blue-500">
          <option value="">Select Department...</option>
          <option value="cs">Computer Science & Engineering</option>
          <option value="ee">Electrical Engineering</option>
          <option value="me">Mechanical Engineering</option>
          <option value="math">Mathematics & Analytics</option>
        </select>
      </div>

      <!-- Submit Button -->
      <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 active:scale-98 text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-blue-600/30 transition text-sm">
        Complete Registration
      </button>
    </form>
  </div>

</body>
</html>`
      },
      page2: {
        filename: "application.html",
        title: "Assignment 4.2 - Job Application Form",
        description: "Official career application portal for software engineering and technical roles.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_PAGE2,
        code: `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- 1. UTF-8 Character Encoding -->
  <meta charset="UTF-8">
  <!-- 2. Mobile Viewport Setting -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- 3. Meaningful Unique Title -->
  <title>Assignment 4.2 - Job Application Form</title>
  <!-- 4. Meta Description -->
  <meta name="description" content="Official career application portal for software engineering and technical roles.">
  <!-- 5. SVG Favicon Link -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%23059669'/><path d='M30 35h40v40H30z' fill='none' stroke='%23ffffff' stroke-width='6'/><path d='M40 35V25a10 10 0 0120 0v10' fill='none' stroke='%23ffffff' stroke-width='6'/></svg>">
  
  <!-- 6. Verified External Assets & Frameworks -->
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Inter', sans-serif; }
  </style>
</head>
<body class="bg-emerald-950 text-emerald-100 min-h-screen py-10 px-4 sm:px-6">

  <div class="max-w-2xl mx-auto bg-slate-900 rounded-2xl p-6 sm:p-8 shadow-2xl border border-emerald-800/60">
    <!-- Header -->
    <div class="border-b border-slate-800 pb-6 mb-6 text-center">
      <span class="bg-emerald-500/10 text-emerald-400 text-xs font-semibold px-3 py-1 rounded-full border border-emerald-500/20">Assignment 4.2</span>
      <h1 class="text-2xl sm:text-3xl font-bold text-white mt-2">Job Application Form</h1>
      <p class="text-xs sm:text-sm text-slate-400 mt-1">Apply for Frontend Developer position at TechCorp Inc.</p>
    </div>

    <!-- Application Form -->
    <form class="space-y-5" onsubmit="event.preventDefault(); alert('Application Submitted!');">
      
      <!-- Position Applied -->
      <div>
        <label for="role" class="block text-xs font-semibold uppercase tracking-wider text-emerald-300 mb-2">Target Position *</label>
        <input type="text" id="role" readonly value="Senior Frontend Engineer (React/Tailwind)" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-emerald-400 font-semibold cursor-not-allowed">
      </div>

      <!-- Applicant Name & Portfolio -->
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
        <div>
          <label for="appName" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Applicant Full Name *</label>
          <input type="text" id="appName" required placeholder="Jane Doe" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-emerald-500">
        </div>
        <div>
          <label for="portfolio" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Portfolio / GitHub URL</label>
          <input type="url" id="portfolio" placeholder="https://github.com/username" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-emerald-500">
        </div>
      </div>

      <!-- Experience & Cover Note -->
      <div>
        <label for="experience" class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Years of Relevant Experience</label>
        <select id="experience" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:ring-2 focus:ring-emerald-500">
          <option value="entry">0-2 Years (Junior)</option>
          <option value="mid" selected>3-5 Years (Mid-level)</option>
          <option value="senior">5+ Years (Senior)</option>
        </select>
      </div>

      <!-- Submit Button -->
      <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-500 active:scale-98 text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-emerald-600/30 transition text-sm">
        Submit Application
      </button>
    </form>
  </div>

</body>
</html>`
      },
      page3: {
        filename: "marksheet.html",
        title: "Assignment 4.3 - Student Marksheet Table",
        description: "Departmental academic performance evaluation table for semester I results.",
        encoding: 'UTF-8',
        viewport: 'width=device-width, initial-scale=1.0',
        faviconSvg: SVG_FAVICON_PAGE3,
        code: `<!DOCTYPE html>
<html lang="en">
<head>
  <!-- 1. UTF-8 Character Encoding -->
  <meta charset="UTF-8">
  <!-- 2. Mobile Viewport Setting -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- 3. Meaningful Unique Title -->
  <title>Assignment 4.3 - Student Marksheet Table</title>
  <!-- 4. Meta Description -->
  <meta name="description" content="Departmental academic performance evaluation table for semester I results.">
  <!-- 5. SVG Favicon Link -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='20' fill='%237c3aed'/><path d='M25 25h50v50H25z' fill='none' stroke='%23ffffff' stroke-width='6'/><path d='M25 50h50M50 25v50' stroke='%23ffffff' stroke-width='6'/></svg>">
  
  <!-- 6. Verified External Assets & Frameworks -->
  <script src="https://cdn.tailwindcss.com"><\/script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Inter', sans-serif; }
  </style>
</head>
<body class="bg-slate-100 min-h-screen py-8 px-4 sm:px-6">

  <div class="max-w-4xl mx-auto space-y-6">
    <div class="bg-white rounded-2xl shadow-xl border border-slate-200 overflow-hidden">
      
      <table class="w-full text-left border-collapse">
        <caption class="p-4 bg-indigo-600 text-white font-semibold text-sm tracking-wide text-left">
          Department of Computer Science — Student Performance Report 2026
        </caption>

        <thead class="bg-slate-800 text-slate-200 uppercase text-xs tracking-wider">
          <tr>
            <th scope="col" class="py-3 px-4">Roll No</th>
            <th scope="col" class="py-3 px-4">Student Name</th>
            <th scope="col" class="py-3 px-4 text-center">Maths</th>
            <th scope="col" class="py-3 px-4 text-center">Physics</th>
            <th scope="col" class="py-3 px-4 text-center">CS</th>
            <th scope="col" class="py-3 px-4 text-center">Total</th>
          </tr>
        </thead>

        <tbody class="divide-y divide-slate-100 text-xs sm:text-sm text-slate-700">
          <tr class="hover:bg-slate-50">
            <td class="py-3 px-4 font-medium text-slate-500">CS-101</td>
            <td class="py-3 px-4 font-semibold text-slate-900">Alex Johnson</td>
            <td class="py-3 px-4 text-center">92</td>
            <td class="py-3 px-4 text-center">88</td>
            <td class="py-3 px-4 text-center">95</td>
            <td class="py-3 px-4 text-center font-bold text-blue-700">275 / 300</td>
          </tr>
          <tr class="hover:bg-slate-50">
            <td class="py-3 px-4 font-medium text-slate-500">CS-102</td>
            <td class="py-3 px-4 font-semibold text-slate-900">Sophia Martinez</td>
            <td class="py-3 px-4 text-center">78</td>
            <td class="py-3 px-4 text-center">82</td>
            <td class="py-3 px-4 text-center">89</td>
            <td class="py-3 px-4 text-center font-bold text-blue-700">249 / 300</td>
          </tr>
          <tr class="hover:bg-slate-50">
            <td class="py-3 px-4 font-medium text-slate-500">CS-103</td>
            <td class="py-3 px-4 font-semibold text-slate-900">Liam Williams</td>
            <td class="py-3 px-4 text-center">64</td>
            <td class="py-3 px-4 text-center">70</td>
            <td class="py-3 px-4 text-center">68</td>
            <td class="py-3 px-4 text-center font-bold text-blue-700">202 / 300</td>
          </tr>
          <tr class="hover:bg-slate-50">
            <td class="py-3 px-4 font-medium text-slate-500">CS-104</td>
            <td class="py-3 px-4 font-semibold text-slate-900">Emma Brown</td>
            <td class="py-3 px-4 text-center">85</td>
            <td class="py-3 px-4 text-center">91</td>
            <td class="py-3 px-4 text-center">94</td>
            <td class="py-3 px-4 text-center font-bold text-blue-700">270 / 300</td>
          </tr>
          <tr class="hover:bg-slate-50">
            <td class="py-3 px-4 font-medium text-slate-500">CS-105</td>
            <td class="py-3 px-4 font-semibold text-slate-900">Noah Miller</td>
            <td class="py-3 px-4 text-center text-rose-600 font-semibold">38</td>
            <td class="py-3 px-4 text-center">52</td>
            <td class="py-3 px-4 text-center">60</td>
            <td class="py-3 px-4 text-center font-bold text-blue-700">150 / 300</td>
          </tr>
        </tbody>

        <tfoot class="bg-slate-900 text-slate-200 text-xs font-semibold">
          <tr>
            <td colspan="2" class="py-3 px-4 text-right uppercase">Subject Class Average:</td>
            <td class="py-3 px-4 text-center text-blue-300">71.4</td>
            <td class="py-3 px-4 text-center text-blue-300">76.6</td>
            <td class="py-3 px-4 text-center text-blue-300">81.2</td>
            <td class="py-3 px-4 text-center text-emerald-400 font-bold">229.2 Avg</td>
          </tr>
        </tfoot>
      </table>

    </div>
  </div>

</body>
</html>`
      }
    };

    let currentPageKey = 'page1';
    let currentViewMode = 'preview'; // 'preview' | 'code'

    // Initialize Hub
    document.addEventListener('DOMContentLoaded', () => {
      renderActivePage();
    });

    // Switch Page Tab
    function switchPage(pageKey) {
      currentPageKey = pageKey;
      
      // Update Tab Styles
      ['page1', 'page2', 'page3'].forEach(key => {
        const btn = document.getElementById(`tab-${key}`);
        if (key === pageKey) {
          btn.className = "tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all bg-blue-600 text-white shadow-lg shadow-blue-600/25";
        } else {
          btn.className = "tab-btn px-4 py-3 rounded-xl font-semibold text-xs sm:text-sm flex items-center justify-between transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/60";
        }
      });

      renderActivePage();
    }

    // Switch View Mode (Preview vs Full Code)
    function switchViewMode(mode) {
      currentViewMode = mode;
      const previewContainer = document.getElementById('preview-container');
      const codeContainer = document.getElementById('code-container');
      const previewBtn = document.getElementById('view-preview-btn');
      const codeBtn = document.getElementById('view-code-btn');

      if (mode === 'preview') {
        previewContainer.classList.remove('hidden');
        previewContainer.classList.add('block');
        codeContainer.classList.add('hidden');
        codeContainer.classList.remove('block');

        previewBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 bg-blue-600 text-white transition-all shadow-sm";
        codeBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 text-slate-400 hover:text-slate-200 transition-all";
      } else {
        previewContainer.classList.add('hidden');
        previewContainer.classList.remove('block');
        codeContainer.classList.remove('hidden');
        codeContainer.classList.add('block');

        codeBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 bg-blue-600 text-white transition-all shadow-sm";
        previewBtn.className = "px-3.5 py-1.5 rounded-lg text-xs font-semibold flex items-center space-x-1.5 text-slate-400 hover:text-slate-200 transition-all";
      }
    }

    // Render active page data into spotlight, iframe, and code blocks
    function renderActivePage() {
      const data = pagesData[currentPageKey];

      // 1. Update Spotlight Info
      document.getElementById('spotlight-filename').innerText = data.filename;
      document.getElementById('spotlight-title').innerText = `${data.title} — Metadata Overview`;
      document.getElementById('meta-encoding').innerText = `<meta charset="${data.encoding}">`;
      document.getElementById('meta-viewport').innerText = data.viewport;
      document.getElementById('meta-title').innerText = data.title;
      document.getElementById('meta-favicon-icon').innerHTML = data.faviconSvg;

      // 2. Update Browser Simulation Header
      document.getElementById('browser-tab-icon').innerHTML = data.faviconSvg;
      document.getElementById('browser-tab-title').innerText = data.title;
      document.getElementById('browser-url-path').innerText = data.filename;

      // 3. Update Iframe Srcdoc
      const iframe = document.getElementById('page-iframe');
      iframe.srcdoc = data.code;

      // 4. Update Source Code Viewer
      document.getElementById('code-filename-label').innerText = data.filename;
      document.getElementById('source-code-block').textContent = data.code;
    }

    // Copy Head Block Metadata
    function copyActiveMetadataHead() {
      const data = pagesData[currentPageKey];
      const headSnippet = `<head>
  <meta charset="${data.encoding}">
  <meta name="viewport" content="${data.viewport}">
  <title>${data.title}</title>
  <meta name="description" content="${data.description}">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,${encodeURIComponent(data.faviconSvg)}">
</head>`;
      
      copyToClipboard(headSnippet, "Copied <head> metadata block to clipboard!");
    }

    // Copy Full Source Code
    function copyFullSourceCode() {
      const data = pagesData[currentPageKey];
      copyToClipboard(data.code, `Copied complete ${data.filename} source code!`);
    }

    // Copy Helper Utility
    function copyToClipboard(text, successMsg) {
      const textarea = document.createElement('textarea');
      textarea.value = text;
      document.body.appendChild(textarea);
      textarea.select();
      document.execCommand('copy');
      document.body.removeChild(textarea);

      // Trigger Toast
      const toast = document.getElementById('toast');
      const toastMessage = document.getElementById('toastMessage');
      toastMessage.innerText = successMsg;

      toast.classList.remove('translate-y-[-100px]', 'opacity-0');
      toast.classList.add('translate-y-0', 'opacity-100');

      setTimeout(() => {
        toast.classList.remove('translate-y-0', 'opacity-100');
        toast.classList.add('translate-y-[-100px]', 'opacity-0');
      }, 2500);
    }
  </script>
</body>
</html>