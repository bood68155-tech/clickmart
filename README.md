[index.html](https://github.com/user-attachments/files/28682747/index.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ClickMart – تقنية المستقبل بين يديك</title>
  <meta name="description" content="وجهتك الأولى للمنتجات التقنية والإلكترونيات في فلسطين." />

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Cairo Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet" />

  <!-- React + Babel (CDN) -->
  <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Cairo', 'Tajawal', sans-serif;
      background: #0b1120;
      color: #fff;
      overflow-x: hidden;
    }

    /* ── Animations ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(32px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(-2deg); }
      50%       { transform: translateY(-14px) rotate(2deg); }
    }
    @keyframes shimmer {
      0%   { background-position: -400px 0; }
      100% { background-position:  400px 0; }
    }
    @keyframes cartBounce {
      0%, 100% { transform: scale(1); }
      40%       { transform: scale(1.35); }
      70%       { transform: scale(.9); }
    }
    @keyframes gridPulse {
      0%, 100% { opacity: .04; }
      50%       { opacity: .08; }
    }
    @keyframes bounce-slow {
      0%, 100% { transform: translateY(0); }
      50%       { transform: translateY(-6px); }
    }
    @keyframes pulse-dot {
      0%, 100% { opacity: 1; }
      50%       { opacity: .4; }
    }

    /* ── Utility classes ── */
    .fade-up-1 { animation: fadeUp .7s ease both; }
    .fade-up-2 { animation: fadeUp .7s .18s ease both; }
    .fade-up-3 { animation: fadeUp .7s .34s ease both; }
    .fade-up-4 { animation: fadeUp .7s .50s ease both; }

    .float-card { animation: float 5s ease-in-out infinite; }

    .grid-bg {
      background-image:
        linear-gradient(rgba(59,130,246,.06) 1px, transparent 1px),
        linear-gradient(90deg, rgba(59,130,246,.06) 1px, transparent 1px);
      background-size: 48px 48px;
      animation: gridPulse 4s ease-in-out infinite;
    }

    /* Header glass on scroll */
    .header-scrolled {
      background: rgba(11,17,32,.9) !important;
      backdrop-filter: blur(20px);
      border-bottom: 1px solid rgba(255,255,255,.05);
      box-shadow: 0 20px 40px -12px rgba(15,32,86,.4);
    }

    /* Nav underline effect */
    .nav-link {
      position: relative;
      transition: color .2s;
      text-decoration: none;
    }
    .nav-link::after {
      content: '';
      position: absolute;
      bottom: -3px; right: 0;
      width: 0; height: 2px;
      background: #3b82f6;
      transition: width .3s;
    }
    .nav-link:hover::after { width: 100%; }
    .nav-link:hover { color: #60a5fa !important; }

    /* Hero CTA shimmer */
    .shimmer-btn {
      background: linear-gradient(90deg, #1d4ed8 25%, #3b82f6 50%, #1d4ed8 75%);
      background-size: 400px 100%;
      transition: background-position .4s, transform .15s, box-shadow .3s;
    }
    .shimmer-btn:hover {
      animation: shimmer .8s linear infinite;
      box-shadow: 0 0 24px 4px rgba(59,130,246,.5);
      transform: translateY(-2px);
    }

    /* Product card */
    .product-card {
      transition: transform .3s cubic-bezier(.34,1.56,.64,1), box-shadow .3s;
    }
    .product-card:hover {
      transform: translateY(-10px) scale(1.02);
      box-shadow: 0 32px 64px -12px rgba(59,130,246,.25);
    }
    .product-card:hover .card-img {
      transform: scale(1.10);
    }
    .product-card:hover .card-shine {
      opacity: 1 !important;
    }

    .card-img {
      transition: transform .7s ease;
    }

    /* Tag badge */
    .tag-badge {
      background: linear-gradient(135deg, #1e40af, #3b82f6);
      font-size: .65rem;
      letter-spacing: .05em;
    }

    /* Cart bounce */
    .cart-bounce { animation: cartBounce .5s ease; }

    /* Add-to-cart button */
    .add-btn {
      transition: background .2s, transform .1s;
    }
    .add-btn:hover { background: #3b82f6 !important; }
    .add-btn:active { transform: scale(.95); }

    /* Trust feature hover */
    .trust-item:hover .trust-icon {
      background: rgba(59,130,246,.2) !important;
    }

    /* Social icon hover */
    .social-icon {
      transition: background .2s, border-color .2s, color .2s;
    }
    .social-icon:hover {
      background: rgba(59,130,246,.2) !important;
      border-color: rgba(59,130,246,.4) !important;
      color: #93c5fd !important;
    }

    /* Footer link hover */
    .footer-link { text-decoration: none; transition: color .2s; }
    .footer-link:hover { color: #93c5fd !important; }

    /* Bounce scroll hint */
    .bounce-slow { animation: bounce-slow 1.8s ease-in-out infinite; }
    .pulse-dot   { animation: pulse-dot 1.5s ease-in-out infinite; }

    /* Outline btn */
    .outline-btn {
      transition: border-color .3s, color .3s, background .3s;
    }
    .outline-btn:hover {
      border-color: rgba(96,165,250,.6) !important;
      color: #e0eeff !important;
      background: rgba(59,130,246,.1) !important;
    }
  </style>
</head>

<body>
  <div id="root"></div>

  <script type="text/babel">
    const { useState, useEffect, useRef } = React;

    /* ── Data ── */
    const products = [
      {
        id: 1,
        name: "Sony WH-1000XM5 سماعات لاسلكية",
        price: "$349",
        tag: "الأكثر مبيعاً",
        image: "https://images.unsplash.com/photo-1618366712010-f4ae9c647dcb?w=600&q=80",
        gradientFrom: "#1d4ed8", gradientTo: "#312e81",
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
        gradientFrom: "#475569", gradientTo: "#0f172a",
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
        gradientFrom: "#047857", gradientTo: "#134e4a",
        desc: "شاحن GaN Pro مدمج بـ 3 منافذ يشحن لابتوبك وهاتفك معاً.",
        rating: "4.7",
        reviews: "983",
      },
    ];

    const navLinks = ["الرئيسية", "المنتجات", "العروض", "تواصل معنا"];

    const trust = [
      { icon: "🚚", title: "توصيل مجاني",  sub: "لجميع الطلبات فوق $50" },
      { icon: "🔒", title: "دفع آمن",       sub: "تشفير SSL 256-bit" },
      { icon: "↩️", title: "إرجاع مجاني",  sub: "خلال 30 يوماً" },
      { icon: "🎧", title: "دعم 24/7",      sub: "فريق متخصص دائماً" },
    ];

    const footerLinks = ["الرئيسية", "المنتجات", "العروض", "المدونة", "من نحن"];
    const contactInfo = [
      { icon: "📍", text: "نابلس، فلسطين" },
      { icon: "📞", text: "+970 59 000 0000" },
      { icon: "✉️", text: "support@clickmart.ps" },
      { icon: "🕐", text: "السبت – الخميس، 9ص – 9م" },
    ];
    const socials = [
      { icon: "𝕏",  label: "Twitter" },
      { icon: "f",  label: "Facebook" },
      { icon: "▶",  label: "YouTube" },
      { icon: "📷", label: "Instagram" },
    ];
    const legalLinks = ["سياسة الخصوصية", "شروط الاستخدام", "سياسة الإرجاع"];

    /* ── Component ── */
    function App() {
      const [cart,      setCart]      = useState([]);
      const [cartAnim,  setCartAnim]  = useState(false);
      const [addedId,   setAddedId]   = useState(null);
      const [scrolled,  setScrolled]  = useState(false);
      const headerRef = useRef(null);

      useEffect(() => {
        const onScroll = () => {
          const s = window.scrollY > 40;
          setScrolled(s);
          if (headerRef.current) {
            headerRef.current.classList.toggle("header-scrolled", s);
          }
        };
        window.addEventListener("scroll", onScroll);
        return () => window.removeEventListener("scroll", onScroll);
      }, []);

      const addToCart = (product) => {
        setCart(prev => [...prev, product]);
        setAddedId(product.id);
        setCartAnim(true);
        setTimeout(() => { setCartAnim(false); setAddedId(null); }, 950);
      };

      return (
        <div style={{ minHeight: "100vh" }}>

          {/* ══════════════════════════════ HEADER ══════════════════════════════ */}
          <header
            ref={headerRef}
            style={{
              position: "fixed", top: 0, right: 0, left: 0, zIndex: 50,
              transition: "all .4s ease",
            }}
          >
            <div style={{
              maxWidth: 1152, margin: "0 auto",
              padding: "1rem 1.5rem",
              display: "flex", alignItems: "center", justifyContent: "space-between",
            }}>
              {/* Logo */}
              <div style={{ display: "flex", alignItems: "center", gap: 8 }}>
                <div style={{
                  width: 36, height: 36, borderRadius: 12,
                  background: "linear-gradient(135deg,#3b82f6,#1d4ed8)",
                  display: "flex", alignItems: "center", justifyContent: "center",
                  boxShadow: "0 8px 16px -4px rgba(59,130,246,.5)",
                }}>
                  <span style={{ color: "#fff", fontWeight: 900, fontSize: 18 }}>C</span>
                </div>
                <span style={{ fontWeight: 900, fontSize: 20, letterSpacing: "-.5px" }}>
                  Click<span style={{ color: "#60a5fa" }}>Mart</span>
                </span>
              </div>

              {/* Nav – hidden on small screens via inline media would need JS; shown always here */}
              <nav style={{ display: "flex", gap: 32 }} className="hidden-mobile">
                {navLinks.map(l => (
                  <a key={l} href="#" className="nav-link"
                    style={{ fontSize: 14, color: "#cbd5e1", fontWeight: 500 }}>
                    {l}
                  </a>
                ))}
              </nav>

              {/* Cart button */}
              <button
                onClick={() => {}}
                className={cartAnim ? "cart-bounce" : ""}
                style={{
                  position: "relative",
                  display: "flex", alignItems: "center", gap: 8,
                  background: "rgba(59,130,246,.15)",
                  border: "1px solid rgba(59,130,246,.3)",
                  color: "#93c5fd",
                  fontSize: 14, fontWeight: 600,
                  padding: "8px 16px", borderRadius: 12,
                  cursor: "pointer", fontFamily: "inherit",
                  transition: "background .2s",
                }}
              >
                🛒 السلة
                {cart.length > 0 && (
                  <span style={{
                    position: "absolute", top: -8, left: -8,
                    width: 20, height: 20, borderRadius: "50%",
                    background: "#3b82f6",
                    fontSize: 11, fontWeight: 700,
                    display: "flex", alignItems: "center", justifyContent: "center",
                    boxShadow: "0 4px 12px rgba(59,130,246,.5)",
                  }}>
                    {cart.length}
                  </span>
                )}
              </button>
            </div>
          </header>

          {/* ══════════════════════════════ HERO ══════════════════════════════ */}
          <section style={{ position: "relative", minHeight: "100vh", display: "flex", alignItems: "center", overflow: "hidden" }}>
            {/* bg grid */}
            <div className="grid-bg" style={{ position: "absolute", inset: 0 }} />
            <div style={{
              position: "absolute", inset: 0,
              background: "linear-gradient(to bottom, transparent, rgba(11,17,32,.6) 60%, #0b1120)",
            }} />
            {/* glow blob */}
            <div style={{
              position: "absolute",
              top: "6rem", left: "50%", transform: "translateX(-50%)",
              width: 700, height: 700,
              background: "rgba(59,130,246,.08)",
              borderRadius: "50%", filter: "blur(80px)", pointerEvents: "none",
            }} />

            <div style={{
              position: "relative",
              maxWidth: 1152, margin: "0 auto",
              padding: "7rem 1.5rem 4rem",
              display: "flex", flexWrap: "wrap",
              alignItems: "center", gap: 64, width: "100%",
            }}>
              {/* ── Left: text ── */}
              <div style={{ flex: "1 1 340px" }}>
                <div className="fade-up-1" style={{
                  display: "inline-flex", alignItems: "center", gap: 8,
                  background: "rgba(59,130,246,.08)",
                  border: "1px solid rgba(59,130,246,.2)",
                  color: "#93c5fd",
                  fontSize: 11, fontWeight: 700,
                  padding: "8px 16px", borderRadius: 999,
                  marginBottom: 24, letterSpacing: ".15em", textTransform: "uppercase",
                }}>
                  <span className="pulse-dot" style={{
                    width: 8, height: 8, borderRadius: "50%", background: "#60a5fa",
                  }} />
                  متجرك التقني المفضل
                </div>

                <h1 className="fade-up-2" style={{
                  fontSize: "clamp(2.4rem, 6vw, 4.5rem)",
                  fontWeight: 900, lineHeight: 1.15, marginBottom: 24,
                }}>
                  تقنية{" "}
                  <span style={{
                    background: "linear-gradient(to left, #93c5fd, #3b82f6)",
                    WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent",
                    backgroundClip: "text",
                  }}>المستقبل</span>
                  <br />بين يديك الآن
                </h1>

                <p className="fade-up-3" style={{
                  color: "#94a3b8", fontSize: "1.1rem", lineHeight: 1.8,
                  maxWidth: 460, marginBottom: 40,
                }}>
                  اكتشف أحدث الأجهزة الإلكترونية والمنتجات التقنية بأسعار تنافسية
                  وتوصيل سريع لباب منزلك.
                </p>

                <div className="fade-up-4" style={{ display: "flex", flexWrap: "wrap", gap: 16, marginBottom: 48 }}>
                  <a href="#products" className="shimmer-btn"
                    style={{
                      display: "inline-flex", alignItems: "center", gap: 12,
                      color: "#fff", fontWeight: 700,
                      padding: "14px 32px", borderRadius: 16,
                      fontSize: 15, textDecoration: "none",
                      boxShadow: "0 20px 40px -12px rgba(29,78,216,.4)",
                    }}>
                    تسوق الآن ←
                  </a>
                  <a href="#" className="outline-btn"
                    style={{
                      display: "inline-flex", alignItems: "center",
                      border: "1px solid rgba(255,255,255,.1)",
                      color: "#cbd5e1", fontWeight: 600,
                      padding: "14px 32px", borderRadius: 16,
                      fontSize: 15, textDecoration: "none",
                      background: "rgba(255,255,255,.04)",
                    }}>
                    تعرف علينا
                  </a>
                </div>

                {/* Stats */}
                <div className="fade-up-4" style={{ display: "flex", gap: 40 }}>
                  {[["+5000","منتج"],["98%","رضا العملاء"],["24/7","دعم فني"]].map(([n,l]) => (
                    <div key={l} style={{ textAlign: "center" }}>
                      <div style={{ fontSize: "1.5rem", fontWeight: 900, color: "#60a5fa" }}>{n}</div>
                      <div style={{ fontSize: 11, color: "#64748b", marginTop: 2 }}>{l}</div>
                    </div>
                  ))}
                </div>
              </div>

              {/* ── Right: floating card ── */}
              <div style={{ flex: "1 1 280px", display: "flex", justifyContent: "center" }}>
                <div className="float-card" style={{ position: "relative" }}>
                  <div style={{
                    width: 280, height: 280, borderRadius: 24,
                    background: "linear-gradient(135deg, #0f1f3d, #1a2d5a)",
                    border: "1px solid rgba(59,130,246,.2)",
                    display: "flex", flexDirection: "column",
                    alignItems: "center", justifyContent: "center", gap: 16,
                    boxShadow: "0 40px 80px -20px rgba(15,32,86,.6)",
                    overflow: "hidden", position: "relative",
                  }}>
                    {/* inner grid */}
                    <div style={{
                      position: "absolute", inset: 0, opacity: .1,
                      backgroundImage: "linear-gradient(rgba(59,130,246,.3) 1px,transparent 1px),linear-gradient(90deg,rgba(59,130,246,.3) 1px,transparent 1px)",
                      backgroundSize: "24px 24px",
                    }} />
                    <div style={{ fontSize: 80, filter: "drop-shadow(0 8px 16px rgba(0,0,0,.5))", zIndex: 1 }}>🖥️</div>
                    <div style={{ textAlign: "center", zIndex: 1 }}>
                      <div style={{ color: "#60a5fa", fontWeight: 700, fontSize: 12, letterSpacing: ".15em", textTransform: "uppercase" }}>أفضل المنتجات</div>
                      <div style={{ color: "#fff", fontWeight: 900, fontSize: 17, marginTop: 4 }}>تقنية بلا حدود</div>
                    </div>
                    {/* corner decorations */}
                    <div style={{ position:"absolute", top:12, right:12, width:28, height:28, borderTop:"2px solid rgba(59,130,246,.4)", borderRight:"2px solid rgba(59,130,246,.4)", borderRadius:"0 8px 0 0" }} />
                    <div style={{ position:"absolute", bottom:12, left:12, width:28, height:28, borderBottom:"2px solid rgba(59,130,246,.4)", borderLeft:"2px solid rgba(59,130,246,.4)", borderRadius:"0 0 8px 0" }} />
                  </div>

                  {/* chips */}
                  <div style={{
                    position:"absolute", top:-16, right:-16,
                    background:"#0f2040", border:"1px solid rgba(59,130,246,.3)",
                    borderRadius:12, padding:"8px 12px",
                    boxShadow:"0 8px 24px rgba(0,0,0,.4)",
                    fontSize:12, fontWeight:700, color:"#93c5fd",
                    display:"flex", alignItems:"center", gap:6, whiteSpace:"nowrap",
                  }}>✅ توصيل مجاني</div>
                  <div style={{
                    position:"absolute", bottom:-16, left:-16,
                    background:"#0f2040", border:"1px solid rgba(99,102,241,.3)",
                    borderRadius:12, padding:"8px 12px",
                    boxShadow:"0 8px 24px rgba(0,0,0,.4)",
                    fontSize:12, fontWeight:700, color:"#a5b4fc",
                    display:"flex", alignItems:"center", gap:6, whiteSpace:"nowrap",
                  }}>🔒 دفع آمن 100%</div>
                </div>
              </div>
            </div>

            {/* Scroll hint */}
            <div style={{
              position:"absolute", bottom:32, left:"50%", transform:"translateX(-50%)",
              display:"flex", flexDirection:"column", alignItems:"center", gap:8, opacity:.4,
            }}>
              <span style={{ fontSize:10, color:"#64748b", letterSpacing:".2em", textTransform:"uppercase" }}>تمرير</span>
              <div style={{
                width:20, height:32, border:"1px solid #475569", borderRadius:999,
                display:"flex", justifyContent:"center", paddingTop:6,
              }}>
                <div className="bounce-slow" style={{ width:4, height:8, background:"#3b82f6", borderRadius:999 }} />
              </div>
            </div>
          </section>

          {/* ══════════════════════════════ PRODUCTS ══════════════════════════════ */}
          <section id="products" style={{
            position:"relative", padding:"7rem 1.5rem",
            background:"linear-gradient(to bottom, #0b1120, #0d1526 50%, #0b1120)",
          }}>
            <div style={{ maxWidth:1152, margin:"0 auto" }}>

              {/* Section header */}
              <div style={{ textAlign:"center", marginBottom:64 }}>
                <span style={{
                  display:"inline-block",
                  color:"#60a5fa", fontSize:11, fontWeight:700,
                  letterSpacing:".2em", textTransform:"uppercase",
                  border:"1px solid rgba(59,130,246,.2)",
                  background:"rgba(59,130,246,.05)",
                  padding:"8px 16px", borderRadius:999, marginBottom:16,
                }}>منتجاتنا المميزة</span>

                <h2 style={{ fontSize:"clamp(2rem,5vw,3rem)", fontWeight:900, marginBottom:16 }}>
                  الأكثر{" "}
                  <span style={{
                    background:"linear-gradient(to left,#93c5fd,#3b82f6)",
                    WebkitBackgroundClip:"text", WebkitTextFillColor:"transparent", backgroundClip:"text",
                  }}>طلباً</span>{" "}هذا الموسم
                </h2>
                <p style={{ color:"#94a3b8", fontSize:"1.1rem", maxWidth:520, margin:"0 auto" }}>
                  منتجات مختارة بعناية لتلبية احتياجاتك التقنية بأعلى معايير الجودة
                </p>
              </div>

              {/* Grid */}
              <div style={{
                display:"grid",
                gridTemplateColumns:"repeat(auto-fit, minmax(280px, 1fr))",
                gap:32,
              }}>
                {products.map((p, i) => (
                  <div key={p.id} className="product-card" style={{
                    position:"relative",
                    background:"linear-gradient(to bottom, #111d35, #0d1526)",
                    border:"1px solid rgba(255,255,255,.05)",
                    borderRadius:24, overflow:"hidden",
                  }}>
                    {/* Tag */}
                    <div style={{ position:"absolute", top:16, right:16, zIndex:10 }}>
                      <span className="tag-badge" style={{
                        color:"#fff", fontWeight:700,
                        padding:"4px 12px", borderRadius:999, display:"inline-block",
                      }}>{p.tag}</span>
                    </div>

                    {/* Image */}
                    <div style={{
                      position:"relative", height:220,
                      background:`linear-gradient(135deg, ${p.gradientFrom}, ${p.gradientTo})`,
                      overflow:"hidden",
                    }}>
                      <img
                        src={p.image}
                        alt={p.name}
                        className="card-img"
                        style={{ width:"100%", height:"100%", objectFit:"cover", display:"block" }}
                        loading="lazy"
                      />
                      {/* dark overlay */}
                      <div style={{
                        position:"absolute", inset:0,
                        background:"linear-gradient(to top, rgba(0,0,0,.45), transparent)",
                      }} />
                      {/* shine on hover */}
                      <div className="card-shine" style={{
                        position:"absolute", inset:0,
                        background:"linear-gradient(135deg, rgba(255,255,255,.12), transparent)",
                        opacity:0, transition:"opacity .5s",
                      }} />
                    </div>

                    {/* Info */}
                    <div style={{ padding:24 }}>
                      <h3 style={{ fontSize:"1rem", fontWeight:700, color:"#fff", marginBottom:6 }}>{p.name}</h3>
                      <p style={{ color:"#64748b", fontSize:13, lineHeight:1.7, marginBottom:20 }}>{p.desc}</p>

                      <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between" }}>
                        <span style={{ fontSize:"1.5rem", fontWeight:900, color:"#60a5fa" }}>{p.price}</span>
                        <button
                          className="add-btn"
                          onClick={() => addToCart(p)}
                          style={{
                            display:"flex", alignItems:"center", gap:8,
                            background:"#2563eb",
                            color:"#fff", fontSize:13, fontWeight:700,
                            padding:"10px 20px", borderRadius:12,
                            border:"none", cursor:"pointer", fontFamily:"inherit",
                            boxShadow:"0 8px 20px -6px rgba(37,99,235,.5)",
                          }}
                        >
                          🛒 {addedId === p.id ? "تمت الإضافة!" : "إضافة للسلة"}
                        </button>
                      </div>

                      {/* Stars */}
                      <div style={{
                        display:"flex", alignItems:"center", gap:8,
                        marginTop:16, paddingTop:16,
                        borderTop:"1px solid rgba(255,255,255,.05)",
                      }}>
                        <div style={{ display:"flex", gap:2 }}>
                          {"★★★★★".split("").map((s,j) => (
                            <span key={j} style={{ color:"#facc15", fontSize:13 }}>{s}</span>
                          ))}
                        </div>
                        <span style={{ color:"#475569", fontSize:12 }}>
                          {p.rating} ({p.reviews} تقييم)
                        </span>
                      </div>
                    </div>
                  </div>
                ))}
              </div>

              {/* View all CTA */}
              <div style={{ textAlign:"center", marginTop:56 }}>
                <a href="#" className="outline-btn"
                  style={{
                    display:"inline-flex", alignItems:"center", gap:12,
                    border:"1px solid rgba(59,130,246,.3)",
                    color:"#93c5fd", fontWeight:700,
                    padding:"14px 32px", borderRadius:16,
                    fontSize:15, textDecoration:"none",
                    background:"rgba(59,130,246,.05)",
                  }}>
                  عرض جميع المنتجات ←
                </a>
              </div>
            </div>
          </section>

          {/* ══════════════════════════════ TRUST STRIP ══════════════════════════════ */}
          <section style={{
            padding:"4rem 1.5rem",
            borderTop:"1px solid rgba(255,255,255,.05)",
            borderBottom:"1px solid rgba(255,255,255,.05)",
          }}>
            <div style={{
              maxWidth:1024, margin:"0 auto",
              display:"grid",
              gridTemplateColumns:"repeat(auto-fit, minmax(160px, 1fr))",
              gap:32,
            }}>
              {trust.map(f => (
                <div key={f.title} className="trust-item"
                  style={{ display:"flex", flexDirection:"column", alignItems:"center", textAlign:"center", gap:12 }}>
                  <div className="trust-icon" style={{
                    width:56, height:56, borderRadius:16,
                    background:"rgba(59,130,246,.08)",
                    border:"1px solid rgba(59,130,246,.2)",
                    display:"flex", alignItems:"center", justifyContent:"center",
                    fontSize:24, transition:"background .3s",
                  }}>{f.icon}</div>
                  <div>
                    <div style={{ color:"#fff", fontWeight:700, fontSize:14 }}>{f.title}</div>
                    <div style={{ color:"#64748b", fontSize:12, marginTop:2 }}>{f.sub}</div>
                  </div>
                </div>
              ))}
            </div>
          </section>

          {/* ══════════════════════════════ FOOTER ══════════════════════════════ */}
          <footer style={{
            position:"relative",
            padding:"5rem 1.5rem 2.5rem",
            background:"linear-gradient(to top, #060c18, #0b1120)",
          }}>
            <div style={{ maxWidth:1152, margin:"0 auto" }}>
              <div style={{
                display:"grid",
                gridTemplateColumns:"repeat(auto-fit, minmax(200px, 1fr))",
                gap:48, marginBottom:56,
              }}>
                {/* Brand */}
                <div style={{ gridColumn:"span 2" }}>
                  <div style={{ display:"flex", alignItems:"center", gap:10, marginBottom:20 }}>
                    <div style={{
                      width:40, height:40, borderRadius:12,
                      background:"linear-gradient(135deg,#3b82f6,#1d4ed8)",
                      display:"flex", alignItems:"center", justifyContent:"center",
                      boxShadow:"0 8px 16px -4px rgba(59,130,246,.5)",
                    }}>
                      <span style={{ color:"#fff", fontWeight:900, fontSize:20 }}>C</span>
                    </div>
                    <span style={{ fontWeight:900, fontSize:22 }}>
                      Click<span style={{ color:"#60a5fa" }}>Mart</span>
                    </span>
                  </div>
                  <p style={{ color:"#64748b", fontSize:13, lineHeight:1.8, maxWidth:280, marginBottom:24 }}>
                    وجهتك الأولى للمنتجات التقنية والإلكترونيات في فلسطين.
                    نقدم أفضل الأجهزة بأسعار منافسة وخدمة عملاء استثنائية.
                  </p>
                  {/* Social icons */}
                  <div style={{ display:"flex", gap:12 }}>
                    {socials.map(s => (
                      <a key={s.label} href="#" title={s.label} className="social-icon"
                        style={{
                          width:40, height:40, borderRadius:12,
                          background:"rgba(255,255,255,.04)",
                          border:"1px solid rgba(255,255,255,.06)",
                          display:"flex", alignItems:"center", justifyContent:"center",
                          color:"#64748b", fontSize:13, fontWeight:700,
                          textDecoration:"none",
                        }}>{s.icon}</a>
                    ))}
                  </div>
                </div>

                {/* Links */}
                <div>
                  <h4 style={{
                    color:"#fff", fontWeight:700, fontSize:12,
                    letterSpacing:".15em", textTransform:"uppercase", marginBottom:20,
                  }}>روابط سريعة</h4>
                  <ul style={{ listStyle:"none" }}>
                    {footerLinks.map(l => (
                      <li key={l} style={{ marginBottom:12 }}>
                        <a href="#" className="footer-link"
                          style={{ color:"#64748b", fontSize:13, display:"flex", alignItems:"center", gap:8 }}>
                          <span style={{ width:4, height:4, borderRadius:"50%", background:"#2563eb", flexShrink:0 }} />
                          {l}
                        </a>
                      </li>
                    ))}
                  </ul>
                </div>

                {/* Contact */}
                <div>
                  <h4 style={{
                    color:"#fff", fontWeight:700, fontSize:12,
                    letterSpacing:".15em", textTransform:"uppercase", marginBottom:20,
                  }}>تواصل معنا</h4>
                  <ul style={{ listStyle:"none" }}>
                    {contactInfo.map(c => (
                      <li key={c.text}
                        style={{
                          display:"flex", alignItems:"flex-start", gap:10,
                          color:"#64748b", fontSize:13, marginBottom:16,
                        }}>
                        <span style={{ fontSize:15, lineHeight:1.4 }}>{c.icon}</span>
                        <span>{c.text}</span>
                      </li>
                    ))}
                  </ul>
                </div>
              </div>

              {/* Bottom bar */}
              <div style={{
                borderTop:"1px solid rgba(255,255,255,.05)",
                paddingTop:32,
                display:"flex", flexWrap:"wrap",
                alignItems:"center", justifyContent:"space-between",
                gap:16,
              }}>
                <span style={{ color:"#374151", fontSize:12 }}>© 2025 ClickMart. جميع الحقوق محفوظة.</span>
                <div style={{ display:"flex", gap:24 }}>
                  {legalLinks.map(l => (
                    <a key={l} href="#" className="footer-link"
                      style={{ color:"#374151", fontSize:12, textDecoration:"none" }}>{l}</a>
                  ))}
                </div>
              </div>
            </div>
          </footer>

          {/* ── Mobile nav hidden style ── */}
          <style>{`
            @media (max-width: 768px) {
              .hidden-mobile { display: none !important; }
            }
          `}</style>
        </div>
      );
    }

    ReactDOM.createRoot(document.getElementById("root")).render(<App />);
  </script>
</body>
</html>
