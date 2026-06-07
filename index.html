import { useState, useEffect } from "react";

const products = [
  {
    id: 1,
    name: "Sony WH-1000XM5 سماعات لاسلكية",
    price: "$349",
    tag: "الأكثر مبيعاً",
    image: "https://images.unsplash.com/photo-1618366712010-f4ae9c647dcb?w=600&q=80",
    color: "from-blue-700 to-indigo-900",
    desc: "عزل نشط للضوضاء بتقنية AI مع بطارية تدوم 30 ساعة.",
    rating: "4.9",
    reviews: "2,341",
  },
  {
    id: 2,
    name: "Apple Watch Ultra 2 ساعة ذكية",
    price: "$799",
    tag: "جديد",
    image: "https://images.unsplash.com/photo-1434493789847-2f02dc6ca35d?w=600&q=80",
    color: "from-slate-600 to-slate-900",
    desc: "الساعة الذكية الأقوى من آبل بشاشة LTPO OLED ومقاومة فائقة.",
    rating: "4.8",
    reviews: "1,876",
  },
  {
    id: 3,
    name: "Anker 140W GaN شاحن سريع",
    price: "$89",
    tag: "عرض محدود",
    image: "https://images.unsplash.com/photo-1609091839311-d5365f9ff1c5?w=600&q=80",
    color: "from-emerald-700 to-teal-900",
    desc: "شاحن GaN Pro مدمج بـ 3 منافذ يشحن لابتوبك وهاتفك معاً.",
    rating: "4.7",
    reviews: "983",
  },
];

const navLinks = ["الرئيسية", "المنتجات", "العروض", "تواصل معنا"];

export default function ClickMart() {
  const [cart, setCart] = useState([]);
  const [cartAnim, setCartAnim] = useState(false);
  const [addedId, setAddedId] = useState(null);
  const [scrolled, setScrolled] = useState(false);
  const [menuOpen, setMenuOpen] = useState(false);

  useEffect(() => {
    const onScroll = () => setScrolled(window.scrollY > 40);
    window.addEventListener("scroll", onScroll);
    return () => window.removeEventListener("scroll", onScroll);
  }, []);

  const addToCart = (product) => {
    setCart((prev) => [...prev, product]);
    setAddedId(product.id);
    setCartAnim(true);
    setTimeout(() => { setCartAnim(false); setAddedId(null); }, 900);
  };

  return (
    <div
      dir="rtl"
      style={{ fontFamily: "'Cairo', 'Tajawal', sans-serif" }}
      className="min-h-screen bg-[#0b1120] text-white overflow-x-hidden"
    >
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap');

        @keyframes fadeUp {
          from { opacity:0; transform:translateY(32px); }
          to   { opacity:1; transform:translateY(0); }
        }
        @keyframes pulseRing {
          0%   { transform:scale(1); opacity:.7; }
          100% { transform:scale(1.6); opacity:0; }
        }
        @keyframes float {
          0%,100% { transform:translateY(0px) rotate(-2deg); }
          50%      { transform:translateY(-14px) rotate(2deg); }
        }
        @keyframes shimmer {
          0%   { background-position: -400px 0; }
          100% { background-position: 400px 0; }
        }
        @keyframes cartBounce {
          0%,100% { transform:scale(1); }
          40%      { transform:scale(1.35); }
          70%      { transform:scale(.9); }
        }
        @keyframes gridPulse {
          0%,100% { opacity:.04; }
          50%      { opacity:.08; }
        }

        .fade-up-1 { animation: fadeUp .7s ease both; }
        .fade-up-2 { animation: fadeUp .7s .18s ease both; }
        .fade-up-3 { animation: fadeUp .7s .34s ease both; }
        .fade-up-4 { animation: fadeUp .7s .5s ease both; }

        .float-card { animation: float 5s ease-in-out infinite; }

        .btn-glow {
          box-shadow: 0 0 0 0 #3b82f6;
          transition: box-shadow .3s, transform .15s;
        }
        .btn-glow:hover {
          box-shadow: 0 0 24px 4px #3b82f688;
          transform: translateY(-2px);
        }

        .product-card {
          transition: transform .3s cubic-bezier(.34,1.56,.64,1), box-shadow .3s;
        }
        .product-card:hover {
          transform: translateY(-10px) scale(1.02);
          box-shadow: 0 32px 64px -12px rgba(59,130,246,.25);
        }

        .grid-bg {
          background-image:
            linear-gradient(rgba(59,130,246,.06) 1px, transparent 1px),
            linear-gradient(90deg, rgba(59,130,246,.06) 1px, transparent 1px);
          background-size: 48px 48px;
          animation: gridPulse 4s ease-in-out infinite;
        }

        .shimmer-btn {
          background: linear-gradient(90deg, #1d4ed8 25%, #3b82f6 50%, #1d4ed8 75%);
          background-size: 400px 100%;
          transition: background-position .4s;
        }
        .shimmer-btn:hover {
          animation: shimmer .8s linear infinite;
        }

        .nav-link {
          position: relative;
          transition: color .2s;
        }
        .nav-link::after {
          content:'';
          position:absolute;
          bottom:-3px; right:0;
          width:0; height:2px;
          background:#3b82f6;
          transition:width .3s;
        }
        .nav-link:hover::after { width:100%; }
        .nav-link:hover { color:#60a5fa; }

        .tag-badge {
          background: linear-gradient(135deg, #1e40af, #3b82f6);
          font-size:.65rem;
          letter-spacing:.05em;
        }
      `}</style>

      {/* ─── HEADER ─── */}
      <header
        className={`fixed top-0 right-0 left-0 z-50 transition-all duration-500 ${
          scrolled
            ? "bg-[#0b1120]/90 backdrop-blur-lg border-b border-white/5 shadow-xl shadow-blue-950/30"
            : "bg-transparent"
        }`}
      >
        <div className="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
          {/* Logo */}
          <div className="flex items-center gap-2">
            <div className="w-9 h-9 rounded-xl bg-gradient-to-br from-blue-500 to-blue-700 flex items-center justify-center shadow-lg shadow-blue-700/40">
              <span className="text-white font-black text-lg leading-none">C</span>
            </div>
            <span className="text-xl font-black tracking-tight">
              Click<span className="text-blue-400">Mart</span>
            </span>
          </div>

          {/* Nav */}
          <nav className="hidden md:flex items-center gap-8">
            {navLinks.map((l) => (
              <a key={l} href="#" className="nav-link text-sm text-slate-300 font-medium">
                {l}
              </a>
            ))}
          </nav>

          {/* Cart */}
          <button
            className="relative flex items-center gap-2 bg-blue-600/20 hover:bg-blue-600/30 border border-blue-500/30 text-blue-300 text-sm font-semibold px-4 py-2 rounded-xl transition-all duration-200"
            style={{ animation: cartAnim ? "cartBounce .5s ease" : "none" }}
          >
            <span>🛒</span>
            <span>السلة</span>
            {cart.length > 0 && (
              <span className="absolute -top-2 -left-2 w-5 h-5 bg-blue-500 rounded-full text-xs flex items-center justify-center font-bold shadow-lg shadow-blue-500/50">
                {cart.length}
              </span>
            )}
          </button>
        </div>
      </header>

      {/* ─── HERO ─── */}
      <section className="relative min-h-screen flex items-center overflow-hidden">
        {/* bg layers */}
        <div className="absolute inset-0 grid-bg" />
        <div className="absolute inset-0 bg-gradient-to-b from-transparent via-[#0b1120]/60 to-[#0b1120]" />
        <div className="absolute top-24 left-1/2 -translate-x-1/2 w-[700px] h-[700px] bg-blue-700/10 rounded-full blur-3xl pointer-events-none" />
        <div className="absolute top-40 right-20 w-56 h-56 bg-indigo-600/10 rounded-full blur-2xl pointer-events-none" />

        <div className="relative max-w-6xl mx-auto px-6 pt-28 pb-16 flex flex-col md:flex-row items-center gap-16 w-full">
          {/* Text */}
          <div className="flex-1 text-center md:text-right">
            <div className="fade-up-1 inline-flex items-center gap-2 bg-blue-600/10 border border-blue-500/20 text-blue-300 text-xs font-semibold px-4 py-2 rounded-full mb-6 tracking-widest uppercase">
              <span className="w-2 h-2 bg-blue-400 rounded-full animate-pulse" />
              متجرك التقني المفضل
            </div>

            <h1 className="fade-up-2 text-5xl md:text-7xl font-black leading-tight mb-6">
              تقنية{" "}
              <span className="relative inline-block">
                <span className="relative z-10 text-transparent bg-clip-text bg-gradient-to-l from-blue-300 to-blue-500">
                  المستقبل
                </span>
                <span className="absolute inset-x-0 bottom-1 h-3 bg-blue-600/20 blur-sm rounded-full" />
              </span>
              <br />
              بين يديك الآن
            </h1>

            <p className="fade-up-3 text-slate-400 text-lg md:text-xl leading-relaxed max-w-lg md:mr-0 mx-auto mb-10">
              اكتشف أحدث الأجهزة الإلكترونية والمنتجات التقنية بأسعار تنافسية
              وتوصيل سريع لباب منزلك.
            </p>

            <div className="fade-up-4 flex flex-wrap gap-4 justify-center md:justify-start">
              <a
                href="#products"
                className="shimmer-btn btn-glow inline-flex items-center gap-3 text-white font-bold px-8 py-4 rounded-2xl text-base shadow-xl shadow-blue-700/30"
              >
                تسوق الآن
                <span className="text-xl">←</span>
              </a>
              <a
                href="#"
                className="inline-flex items-center gap-2 border border-white/10 hover:border-blue-500/40 text-slate-300 hover:text-white font-semibold px-8 py-4 rounded-2xl text-base transition-all duration-300 bg-white/5 backdrop-blur-sm"
              >
                تعرف علينا
              </a>
            </div>

            {/* Stats */}
            <div className="fade-up-4 flex gap-10 mt-12 justify-center md:justify-start">
              {[["+5000", "منتج"], ["98%", "رضا العملاء"], ["24/7", "دعم فني"]].map(([n, l]) => (
                <div key={l} className="text-center">
                  <div className="text-2xl font-black text-blue-400">{n}</div>
                  <div className="text-xs text-slate-500 mt-0.5">{l}</div>
                </div>
              ))}
            </div>
          </div>

          {/* Floating device illustration */}
          <div className="flex-1 flex justify-center items-center">
            <div className="float-card relative">
              {/* Glow ring */}
              <div className="absolute inset-0 rounded-3xl bg-blue-500/10 blur-2xl scale-110" />

              <div className="relative w-72 h-72 rounded-3xl bg-gradient-to-br from-[#0f1f3d] to-[#1a2d5a] border border-blue-500/20 flex flex-col items-center justify-center gap-4 shadow-2xl shadow-blue-900/40 overflow-hidden">
                {/* decorative grid inside card */}
                <div className="absolute inset-0 opacity-10"
                  style={{
                    backgroundImage:"linear-gradient(rgba(59,130,246,.3) 1px,transparent 1px),linear-gradient(90deg,rgba(59,130,246,.3) 1px,transparent 1px)",
                    backgroundSize:"24px 24px"
                  }}
                />
                <div className="text-8xl drop-shadow-2xl relative z-10">🖥️</div>
                <div className="relative z-10 text-center">
                  <div className="text-blue-400 font-bold text-sm tracking-wider uppercase">أفضل المنتجات</div>
                  <div className="text-white font-black text-lg mt-1">تقنية بلا حدود</div>
                </div>

                {/* corner decorations */}
                <div className="absolute top-3 right-3 w-8 h-8 border-t-2 border-r-2 border-blue-500/40 rounded-tr-lg" />
                <div className="absolute bottom-3 left-3 w-8 h-8 border-b-2 border-l-2 border-blue-500/40 rounded-bl-lg" />
              </div>

              {/* floating chips */}
              <div className="absolute -top-4 -right-4 bg-[#0f2040] border border-blue-500/30 rounded-xl px-3 py-2 shadow-xl text-xs font-bold text-blue-300 flex items-center gap-1.5">
                <span>✅</span> توصيل مجاني
              </div>
              <div className="absolute -bottom-4 -left-4 bg-[#0f2040] border border-indigo-500/30 rounded-xl px-3 py-2 shadow-xl text-xs font-bold text-indigo-300 flex items-center gap-1.5">
                <span>🔒</span> دفع آمن 100%
              </div>
            </div>
          </div>
        </div>

        {/* Scroll hint */}
        <div className="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 opacity-40">
          <span className="text-xs text-slate-500 tracking-widest uppercase">تمرير</span>
          <div className="w-5 h-8 border border-slate-600 rounded-full flex justify-center pt-1.5">
            <div className="w-1 h-2 bg-blue-500 rounded-full animate-bounce" />
          </div>
        </div>
      </section>

      {/* ─── PRODUCTS ─── */}
      <section id="products" className="relative py-28 px-6">
        <div className="absolute inset-0 bg-gradient-to-b from-[#0b1120] via-[#0d1526] to-[#0b1120]" />

        <div className="relative max-w-6xl mx-auto">
          {/* Section header */}
          <div className="text-center mb-16">
            <span className="inline-block text-blue-400 text-xs font-bold tracking-[.2em] uppercase border border-blue-500/20 bg-blue-500/5 px-4 py-2 rounded-full mb-4">
              منتجاتنا المميزة
            </span>
            <h2 className="text-4xl md:text-5xl font-black mb-4">
              الأكثر{" "}
              <span className="text-transparent bg-clip-text bg-gradient-to-l from-blue-300 to-blue-500">
                طلباً
              </span>{" "}
              هذا الموسم
            </h2>
            <p className="text-slate-400 text-lg max-w-xl mx-auto">
              منتجات مختارة بعناية لتلبية احتياجاتك التقنية بأعلى معايير الجودة
            </p>
          </div>

          {/* Grid */}
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {products.map((p, i) => (
              <div
                key={p.id}
                className="product-card relative bg-gradient-to-b from-[#111d35] to-[#0d1526] border border-white/5 rounded-3xl overflow-hidden group"
                style={{ animationDelay: `${i * 0.12}s` }}
              >
                {/* Tag */}
                <div className="absolute top-4 right-4 z-10">
                  <span className="tag-badge text-white font-bold px-3 py-1 rounded-full">
                    {p.tag}
                  </span>
                </div>

                {/* Image area */}
                <div className={`relative h-56 bg-gradient-to-br ${p.color} overflow-hidden`}>
                  <img
                    src={p.image}
                    alt={p.name}
                    className="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                    loading="lazy"
                  />
                  {/* dark overlay for readability */}
                  <div className="absolute inset-0 bg-gradient-to-t from-black/50 via-transparent to-transparent" />
                  {/* shine on hover */}
                  <div className="absolute inset-0 bg-gradient-to-br from-white/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500" />
                </div>

                {/* Info */}
                <div className="p-6">
                  <h3 className="text-lg font-bold text-white mb-1">{p.name}</h3>
                  <p className="text-slate-500 text-sm mb-5 leading-relaxed">{p.desc}</p>

                  <div className="flex items-center justify-between">
                    <span className="text-2xl font-black text-blue-400">{p.price}</span>
                    <button
                      onClick={() => addToCart(p)}
                      className="relative flex items-center gap-2 bg-blue-600 hover:bg-blue-500 active:scale-95 text-white text-sm font-bold px-5 py-2.5 rounded-xl transition-all duration-200 shadow-lg shadow-blue-700/30 overflow-hidden group/btn"
                    >
                      <span className="absolute inset-0 bg-white/0 group-hover/btn:bg-white/10 transition-all duration-300" />
                      <span className={`transition-transform duration-200 ${addedId === p.id ? "scale-125" : ""}`}>
                        🛒
                      </span>
                      <span>{addedId === p.id ? "تمت الإضافة!" : "إضافة للسلة"}</span>
                    </button>
                  </div>

                  {/* Stars */}
                  <div className="flex items-center gap-1.5 mt-4 pt-4 border-t border-white/5">
                    <div className="flex gap-0.5">
                      {"★★★★★".split("").map((s, i) => (
                        <span key={i} className="text-yellow-400 text-sm">{s}</span>
                      ))}
                    </div>
                    <span className="text-slate-500 text-xs">{p.rating} ({p.reviews} تقييم)</span>
                  </div>
                </div>
              </div>
            ))}
          </div>

          {/* CTA */}
          <div className="text-center mt-14">
            <a
              href="#"
              className="inline-flex items-center gap-3 border border-blue-500/30 hover:border-blue-400/60 text-blue-300 hover:text-blue-200 font-bold px-8 py-4 rounded-2xl text-base transition-all duration-300 bg-blue-600/5 hover:bg-blue-600/10 backdrop-blur-sm"
            >
              عرض جميع المنتجات
              <span>←</span>
            </a>
          </div>
        </div>
      </section>

      {/* ─── TRUST STRIP ─── */}
      <section className="py-16 px-6 border-y border-white/5">
        <div className="max-w-5xl mx-auto grid grid-cols-2 md:grid-cols-4 gap-8">
          {[
            { icon: "🚚", title: "توصيل مجاني", sub: "لجميع الطلبات فوق ₪299" },
            { icon: "🔒", title: "دفع آمن", sub: "تشفير SSL 256-bit" },
            { icon: "↩️", title: "إرجاع مجاني", sub: "خلال 30 يوماً" },
            { icon: "🎧", title: "دعم 24/7", sub: "فريق متخصص دائماً" },
          ].map((f) => (
            <div key={f.title} className="flex flex-col items-center text-center gap-3 group">
              <div className="w-14 h-14 rounded-2xl bg-blue-600/10 border border-blue-500/20 flex items-center justify-center text-2xl group-hover:bg-blue-600/20 transition-all duration-300">
                {f.icon}
              </div>
              <div>
                <div className="text-white font-bold text-sm">{f.title}</div>
                <div className="text-slate-500 text-xs mt-0.5">{f.sub}</div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* ─── FOOTER ─── */}
      <footer className="relative pt-20 pb-10 px-6">
        <div className="absolute inset-0 bg-gradient-to-t from-[#060c18] to-transparent pointer-events-none" />

        <div className="relative max-w-6xl mx-auto">
          <div className="grid grid-cols-1 md:grid-cols-4 gap-12 mb-14">
            {/* Brand */}
            <div className="md:col-span-2">
              <div className="flex items-center gap-2 mb-5">
                <div className="w-10 h-10 rounded-xl bg-gradient-to-br from-blue-500 to-blue-700 flex items-center justify-center shadow-lg shadow-blue-700/40">
                  <span className="text-white font-black text-xl leading-none">C</span>
                </div>
                <span className="text-2xl font-black">Click<span className="text-blue-400">Mart</span></span>
              </div>
              <p className="text-slate-400 text-sm leading-relaxed max-w-xs mb-6">
                وجهتك الأولى للمنتجات التقنية والإلكترونيات في فلسطين. نقدم أفضل
                الأجهزة بأسعار منافسة وخدمة عملاء استثنائية.
              </p>
              {/* Social */}
              <div className="flex gap-3">
                {[
                  { icon: "𝕏", label: "Twitter" },
                  { icon: "f", label: "Facebook" },
                  { icon: "▶", label: "YouTube" },
                  { icon: "📷", label: "Instagram" },
                ].map((s) => (
                  <a
                    key={s.label}
                    href="#"
                    title={s.label}
                    className="w-10 h-10 rounded-xl bg-white/5 hover:bg-blue-600/20 border border-white/8 hover:border-blue-500/40 flex items-center justify-center text-slate-400 hover:text-blue-300 text-sm font-bold transition-all duration-200"
                  >
                    {s.icon}
                  </a>
                ))}
              </div>
            </div>

            {/* Links */}
            <div>
              <h4 className="text-white font-bold text-sm mb-5 tracking-wider uppercase">
                روابط سريعة
              </h4>
              <ul className="space-y-3">
                {["الرئيسية", "المنتجات", "العروض", "المدونة", "من نحن"].map((l) => (
                  <li key={l}>
                    <a
                      href="#"
                      className="text-slate-400 hover:text-blue-300 text-sm transition-colors duration-200 flex items-center gap-2 group"
                    >
                      <span className="w-1 h-1 rounded-full bg-blue-600 group-hover:bg-blue-400 transition-colors" />
                      {l}
                    </a>
                  </li>
                ))}
              </ul>
            </div>

            {/* Contact */}
            <div>
              <h4 className="text-white font-bold text-sm mb-5 tracking-wider uppercase">
                تواصل معنا
              </h4>
              <ul className="space-y-4">
                {[
                  { icon: "📍", text: "نابلس، فلسطين" },
                  { icon: "📞", text: "+970 59 000 0000" },
                  { icon: "✉️", text: "support@clickmart.ps" },
                  { icon: "🕐", text: "السبت – الخميس، 9ص – 9م" },
                ].map((c) => (
                  <li key={c.text} className="flex items-start gap-2.5 text-sm text-slate-400">
                    <span className="text-base leading-tight">{c.icon}</span>
                    <span>{c.text}</span>
                  </li>
                ))}
              </ul>
            </div>
          </div>

          {/* Bottom bar */}
          <div className="border-t border-white/5 pt-8 flex flex-col md:flex-row items-center justify-between gap-4 text-xs text-slate-500">
            <span>© 2025 ClickMart. جميع الحقوق محفوظة.</span>
            <div className="flex gap-6">
              {["سياسة الخصوصية", "شروط الاستخدام", "سياسة الإرجاع"].map((l) => (
                <a key={l} href="#" className="hover:text-blue-400 transition-colors duration-200">
                  {l}
                </a>
              ))}
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
}
