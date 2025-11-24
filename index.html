import React, { useState, useMemo, useEffect } from 'react';
import { Search, Download, X, Play, Layers, Smartphone, Monitor, Zap, Star, Menu, Filter } from 'lucide-react';

// --- Mock Data Generation ---
// Using the user's uploaded file metadata for the first entry
const REAL_XML_CONTENT = `<?xml version='1.0' encoding='UTF-8' ?><scene title="ADITYA EDITZZ 3K EDITING PACK " width="1440" height="1800" exportWidth="1440" exportHeight="1800" precompose="dynamicResolution" bgcolor="#ff000000" totalTime="57950" fps="60" modifiedTime="1749829674592" amver="1002351" ffver="106" am="com.alightcreative.motion/5.0.270.1002578" amplatform="android" retime="freeze" retimeAdaptFPS="false">...</scene>`;

const INITIAL_TEMPLATES = [
  {
    id: 1,
    title: "ADITYA EDITZZ 3K PACK",
    author: "Aditya Editzz",
    category: "Full Pack",
    downloads: "12.5k",
    rating: 4.9,
    fps: 60,
    resolution: "1440x1800",
    layers: 150,
    size: "2.4 MB",
    tags: ["3k", "xml", "preset", "shake"],
    description: "The ultimate editing pack featuring shake effects, color corrections (CC), and glitch overlays. Optimized for high-end mobile editing.",
    color: "from-purple-500 to-pink-500",
    xml: REAL_XML_CONTENT
  },
  {
    id: 2,
    title: "Cyberpunk Glitch Transitions",
    author: "Motion Master",
    category: "Transitions",
    downloads: "8.2k",
    rating: 4.7,
    fps: 60,
    resolution: "1080x1080",
    layers: 45,
    size: "1.1 MB",
    tags: ["glitch", "cyber", "transition"],
    description: "High-energy glitch transitions perfect for AMVs and tech reviews.",
    color: "from-cyan-500 to-blue-600",
    xml: "<scene>Mock XML for Glitch Pack</scene>"
  },
  {
    id: 3,
    title: "Soft AESTHETIC CC",
    author: "Lofi Girl",
    category: "Color Correction",
    downloads: "25k",
    rating: 4.5,
    fps: 30,
    resolution: "1080x1920",
    layers: 12,
    size: "500 KB",
    tags: ["cc", "aesthetic", "soft"],
    description: "Dreamy, soft color correction presets to give your edits a nostalgic vibe.",
    color: "from-rose-400 to-orange-300",
    xml: "<scene>Mock XML for CC</scene>"
  },
  {
    id: 4,
    title: "Dynamic Typography V2",
    author: "TypeBeast",
    category: "Text",
    downloads: "5.4k",
    rating: 4.8,
    fps: 60,
    resolution: "1080x1080",
    layers: 80,
    size: "3.2 MB",
    tags: ["text", "typography", "motion"],
    description: "Complex text animations made easy. Just edit the text group and render.",
    color: "from-emerald-400 to-teal-600",
    xml: "<scene>Mock XML for Typography</scene>"
  },
  {
    id: 5,
    title: "HDR Shake Pack",
    author: "ShakeGod",
    category: "Shake",
    downloads: "15k",
    rating: 4.6,
    fps: 60,
    resolution: "1080x1080",
    layers: 25,
    size: "800 KB",
    tags: ["shake", "hdr", "impact"],
    description: "Hard hitting shakes with built-in HDR correction.",
    color: "from-red-500 to-orange-600",
    xml: "<scene>Mock XML for Shakes</scene>"
  },
  {
    id: 6,
    title: "Velocity Edit Helper",
    author: "SpeedDemon",
    category: "Utility",
    downloads: "3.1k",
    rating: 4.2,
    fps: 60,
    resolution: "1080x1920",
    layers: 5,
    size: "200 KB",
    tags: ["velocity", "twixtor", "slowmo"],
    description: "Graphs and curves pre-setup for smooth velocity edits.",
    color: "from-blue-600 to-indigo-800",
    xml: "<scene>Mock XML for Velocity</scene>"
  }
];

// --- Components ---

const Badge = ({ children, className }) => (
  <span className={`px-2 py-1 rounded-md text-xs font-bold tracking-wider uppercase ${className}`}>
    {children}
  </span>
);

const Modal = ({ template, onClose }) => {
  if (!template) return null;

  const handleDownload = () => {
    const element = document.createElement("a");
    const file = new Blob([template.xml], { type: 'text/xml' });
    element.href = URL.createObjectURL(file);
    element.download = `${template.title.replace(/\s+/g, '_')}.xml`;
    document.body.appendChild(element);
    element.click();
    document.body.removeChild(element);
  };

  return (
    <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-sm animate-in fade-in duration-200">
      <div 
        className="bg-gray-900 border border-gray-800 w-full max-w-2xl rounded-2xl overflow-hidden shadow-2xl transform transition-all scale-100"
        onClick={(e) => e.stopPropagation()}
      >
        {/* Modal Header */}
        <div className={`h-32 bg-gradient-to-r ${template.color} relative`}>
          <button 
            onClick={onClose}
            className="absolute top-4 right-4 p-2 bg-black/20 hover:bg-black/40 rounded-full text-white transition-colors backdrop-blur-md"
          >
            <X size={20} />
          </button>
          <div className="absolute bottom-4 left-6">
            <h2 className="text-3xl font-black text-white tracking-tighter drop-shadow-lg">{template.title}</h2>
            <p className="text-white/90 font-medium flex items-center gap-2">
              by {template.author} 
              <span className="bg-white/20 px-2 py-0.5 rounded text-xs">{template.category}</span>
            </p>
          </div>
        </div>

        {/* Modal Content */}
        <div className="p-6 space-y-6">
          <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
            <div className="bg-gray-800/50 p-3 rounded-xl text-center border border-gray-700/50">
              <Monitor className="w-5 h-5 mx-auto text-blue-400 mb-1" />
              <div className="text-xs text-gray-400">Resolution</div>
              <div className="font-bold text-gray-200">{template.resolution}</div>
            </div>
            <div className="bg-gray-800/50 p-3 rounded-xl text-center border border-gray-700/50">
              <Zap className="w-5 h-5 mx-auto text-yellow-400 mb-1" />
              <div className="text-xs text-gray-400">FPS</div>
              <div className="font-bold text-gray-200">{template.fps}</div>
            </div>
            <div className="bg-gray-800/50 p-3 rounded-xl text-center border border-gray-700/50">
              <Layers className="w-5 h-5 mx-auto text-purple-400 mb-1" />
              <div className="text-xs text-gray-400">Layers</div>
              <div className="font-bold text-gray-200">{template.layers}</div>
            </div>
            <div className="bg-gray-800/50 p-3 rounded-xl text-center border border-gray-700/50">
              <Smartphone className="w-5 h-5 mx-auto text-green-400 mb-1" />
              <div className="text-xs text-gray-400">Size</div>
              <div className="font-bold text-gray-200">{template.size}</div>
            </div>
          </div>

          <div className="space-y-2">
            <h3 className="text-gray-400 text-sm uppercase tracking-wider font-bold">Description</h3>
            <p className="text-gray-300 leading-relaxed">{template.description}</p>
          </div>

          <div className="flex flex-wrap gap-2">
            {template.tags.map(tag => (
              <span key={tag} className="text-xs text-gray-500 bg-gray-800 px-2 py-1 rounded-md">#{tag}</span>
            ))}
          </div>

          <button 
            onClick={handleDownload}
            className="w-full py-4 bg-white text-black font-bold rounded-xl hover:bg-gray-200 transition-all active:scale-[0.98] flex items-center justify-center gap-2 group"
          >
            <Download className="group-hover:animate-bounce" size={20} />
            Download XML Preset
          </button>
        </div>
      </div>
    </div>
  );
};

export default function App() {
  const [search, setSearch] = useState("");
  const [activeCategory, setActiveCategory] = useState("All");
  const [selectedTemplate, setSelectedTemplate] = useState(null);
  const [isMenuOpen, setIsMenuOpen] = useState(false);

  const categories = ["All", "Full Pack", "Transitions", "Color Correction", "Text", "Shake"];

  const filteredTemplates = useMemo(() => {
    return INITIAL_TEMPLATES.filter(t => {
      const matchesSearch = t.title.toLowerCase().includes(search.toLowerCase()) || 
                            t.author.toLowerCase().includes(search.toLowerCase()) ||
                            t.tags.some(tag => tag.toLowerCase().includes(search.toLowerCase()));
      const matchesCategory = activeCategory === "All" || t.category === activeCategory;
      return matchesSearch && matchesCategory;
    });
  }, [search, activeCategory]);

  return (
    <div className="min-h-screen bg-black text-gray-100 font-sans selection:bg-purple-500/30">
      
      {/* Navbar */}
      <nav className="sticky top-0 z-40 bg-black/80 backdrop-blur-lg border-b border-gray-800">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-center justify-between h-16">
            <div className="flex items-center gap-2">
              <div className="w-8 h-8 bg-gradient-to-tr from-purple-600 to-blue-500 rounded-lg flex items-center justify-center">
                <Zap size={20} className="text-white" fill="currentColor" />
              </div>
              <span className="text-xl font-bold tracking-tight bg-clip-text text-transparent bg-gradient-to-r from-white to-gray-400">
                AM<span className="font-light">Hub</span>
              </span>
            </div>

            {/* Desktop Search */}
            <div className="hidden md:flex flex-1 max-w-lg mx-8 relative">
              <Search className="absolute left-3 top-1/2 -translate-y-1/2 text-gray-500" size={18} />
              <input 
                type="text"
                placeholder="Search templates, authors, tags..."
                className="w-full bg-gray-900/50 border border-gray-700 text-sm rounded-full pl-10 pr-4 py-2 focus:outline-none focus:border-purple-500 focus:ring-1 focus:ring-purple-500 transition-all text-gray-200 placeholder-gray-600"
                value={search}
                onChange={(e) => setSearch(e.target.value)}
              />
            </div>

            <div className="flex items-center gap-4">
              <button className="hidden md:flex items-center gap-2 px-4 py-2 rounded-full bg-gray-800 hover:bg-gray-700 transition-colors text-sm font-medium">
                <Download size={16} />
                Import XML
              </button>
              <button 
                className="md:hidden p-2 text-gray-400 hover:text-white"
                onClick={() => setIsMenuOpen(!isMenuOpen)}
              >
                <Menu size={24} />
              </button>
            </div>
          </div>
        </div>

        {/* Mobile Menu & Search */}
        {isMenuOpen && (
          <div className="md:hidden p-4 border-t border-gray-800 bg-black animate-in slide-in-from-top-5">
            <div className="relative mb-4">
              <Search className="absolute left-3 top-1/2 -translate-y-1/2 text-gray-500" size={18} />
              <input 
                type="text"
                placeholder="Search..."
                className="w-full bg-gray-900 border border-gray-700 rounded-xl pl-10 pr-4 py-3 focus:outline-none focus:border-purple-500 text-white"
                value={search}
                onChange={(e) => setSearch(e.target.value)}
              />
            </div>
            <div className="flex flex-col gap-2">
              <button className="w-full py-3 rounded-xl bg-purple-600 font-bold">Upload Template</button>
            </div>
          </div>
        )}
      </nav>

      {/* Category Bar */}
      <div className="border-b border-gray-800 bg-black/50 backdrop-blur overflow-x-auto no-scrollbar">
        <div className="max-w-7xl mx-auto px-4 py-3 flex gap-2 min-w-max">
          {categories.map(cat => (
            <button
              key={cat}
              onClick={() => setActiveCategory(cat)}
              className={`px-4 py-1.5 rounded-full text-sm font-medium transition-all whitespace-nowrap ${
                activeCategory === cat 
                  ? 'bg-white text-black shadow-lg shadow-white/10' 
                  : 'bg-gray-900 text-gray-400 hover:bg-gray-800 hover:text-gray-200'
              }`}
            >
              {cat}
            </button>
          ))}
        </div>
      </div>

      {/* Main Content */}
      <main className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
        
        {/* Header Stats/Banner */}
        <div className="mb-8 p-6 md:p-10 rounded-3xl bg-gradient-to-br from-purple-900/20 via-black to-black border border-purple-500/20 relative overflow-hidden group">
          <div className="absolute top-0 right-0 w-64 h-64 bg-purple-600/20 rounded-full blur-3xl -translate-y-1/2 translate-x-1/2 pointer-events-none"></div>
          <div className="relative z-10">
            <h1 className="text-4xl md:text-5xl font-black tracking-tighter mb-2 bg-clip-text text-transparent bg-gradient-to-r from-white to-gray-500">
              Canvas Mode
            </h1>
            <p className="text-gray-400 max-w-lg text-lg">
              Browse high-quality Alight Motion presets. Zero lag. Instant downloads.
            </p>
          </div>
        </div>

        {/* Grid */}
        {filteredTemplates.length > 0 ? (
          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            {filteredTemplates.map((t) => (
              <div 
                key={t.id}
                onClick={() => setSelectedTemplate(t)}
                className="group bg-gray-900/50 border border-gray-800 hover:border-purple-500/50 rounded-2xl overflow-hidden transition-all duration-300 hover:shadow-2xl hover:shadow-purple-500/10 hover:-translate-y-1 cursor-pointer flex flex-col"
              >
                {/* Thumbnail Area */}
                <div className={`h-40 bg-gradient-to-br ${t.color} relative overflow-hidden`}>
                  <div className="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 bg-black/20 backdrop-blur-[2px]">
                    <div className="bg-white/20 backdrop-blur-md rounded-full p-3">
                      <Play className="text-white fill-white" size={24} />
                    </div>
                  </div>
                  <div className="absolute bottom-3 right-3 bg-black/60 backdrop-blur-md px-2 py-1 rounded text-xs font-mono text-white border border-white/10">
                    {t.resolution}
                  </div>
                  {t.id === 1 && (
                    <div className="absolute top-3 left-3">
                      <Badge className="bg-yellow-500/20 text-yellow-300 border border-yellow-500/30">Featured</Badge>
                    </div>
                  )}
                </div>

                {/* Details */}
                <div className="p-5 flex-1 flex flex-col">
                  <div className="flex justify-between items-start mb-2">
                    <div>
                      <h3 className="font-bold text-lg text-gray-100 leading-tight group-hover:text-purple-400 transition-colors line-clamp-1">{t.title}</h3>
                      <p className="text-sm text-gray-500">{t.author}</p>
                    </div>
                    <div className="flex items-center gap-1 text-yellow-500 text-xs font-bold bg-yellow-500/10 px-2 py-1 rounded-lg">
                      <Star size={10} fill="currentColor" />
                      {t.rating}
                    </div>
                  </div>

                  <div className="flex gap-3 my-3">
                    <div className="flex items-center gap-1.5 text-xs text-gray-400 bg-gray-800 px-2 py-1 rounded border border-gray-700">
                      <Layers size={12} />
                      {t.layers} Layers
                    </div>
                    <div className="flex items-center gap-1.5 text-xs text-gray-400 bg-gray-800 px-2 py-1 rounded border border-gray-700">
                      <Zap size={12} />
                      {t.fps} FPS
                    </div>
                  </div>

                  <div className="mt-auto pt-4 flex items-center justify-between border-t border-gray-800/50">
                    <div className="text-xs text-gray-500 font-mono">
                      {t.downloads} Downloads
                    </div>
                    <button className="text-purple-400 hover:text-purple-300 text-sm font-bold flex items-center gap-1 transition-colors">
                      View
                    </button>
                  </div>
                </div>
              </div>
            ))}
          </div>
        ) : (
          <div className="text-center py-20">
            <div className="w-16 h-16 bg-gray-900 rounded-full flex items-center justify-center mx-auto mb-4">
              <Filter className="text-gray-600" size={24} />
            </div>
            <h3 className="text-xl font-bold text-gray-300 mb-2">No templates found</h3>
            <p className="text-gray-500">Try searching for "shake" or "glitch"</p>
            <button 
              onClick={() => {setSearch(""); setActiveCategory("All")}}
              className="mt-6 text-purple-400 hover:text-purple-300 text-sm font-medium"
            >
              Clear filters
            </button>
          </div>
        )}
      </main>

      {/* Footer */}
      <footer className="border-t border-gray-800 bg-gray-900/30 py-8 mt-12">
        <div className="max-w-7xl mx-auto px-4 text-center text-gray-600 text-sm">
          <p>© 2025 Alight Motion Template Hub. Created for Designers.</p>
        </div>
      </footer>

      {/* Modal */}
      {selectedTemplate && (
        <Modal template={selectedTemplate} onClose={() => setSelectedTemplate(null)} />
      )}
    </div>
  );
}

