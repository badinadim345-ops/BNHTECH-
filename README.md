# BNHTECH-
1000+ AI Prompts Bundle 
import { useState, useEffect } from "react";

const categories = [
  { icon: "✍️", name: "Writing & Content", count: 50, color: "#7c5cfc", desc: "Blog posts, articles, essays, newsletters, press releases & more" },
  { icon: "💻", name: "Coding & Dev", count: 50, color: "#5ca8fc", desc: "Functions, APIs, debugging, refactoring, testing & architecture" },
  { icon: "💼", name: "Business & Strategy", count: 50, color: "#fcb55c", desc: "Business plans, SWOT, competitive analysis, OKRs & more" },
  { icon: "📢", name: "Marketing & Sales", count: 50, color: "#fc5c7d", desc: "Ad copy, email sequences, landing pages, launch strategies" },
  { icon: "📚", name: "Education & Learning", count: 50, color: "#5cf8d6", desc: "Curriculums, lesson plans, study guides, flashcards & quizzes" },
  { icon: "🎨", name: "Creative & Fiction", count: 50, color: "#fc5c7d", desc: "Stories, characters, screenplays, poetry & world-building" },
  { icon: "📱", name: "Social Media", count: 50, color: "#5ca8fc", desc: "Instagram, TikTok, YouTube, LinkedIn & Twitter strategies" },
  { icon: "⚡", name: "Productivity & Life", count: 50, color: "#fcb55c", desc: "Morning routines, goal setting, habits, deep work & planning" },
  { icon: "🤖", name: "AI & ChatGPT", count: 50, color: "#7c5cfc", desc: "Roleplay personas, prompt chains, custom GPTs & workflows" },
  { icon: "📧", name: "Email & Comms", count: 50, color: "#5cf8d6", desc: "Cold outreach, negotiations, apologies, follow-ups & more" },
  { icon: "💪", name: "Health & Wellness", count: 50, color: "#5cf8d6", desc: "Workout plans, nutrition, sleep, mindfulness & recovery" },
  { icon: "💰", name: "Finance & Investing", count: 50, color: "#fcb55c", desc: "Budgeting, index funds, debt payoff, tax optimization & more" },
  { icon: "👥", name: "HR & Leadership", count: 50, color: "#fc5c7d", desc: "1:1s, performance reviews, hiring, team building & culture" },
  { icon: "🎧", name: "Customer Service", count: 50, color: "#5ca8fc", desc: "Complaint handling, scripts, policies & CX playbooks" },
  { icon: "🖌️", name: "Design & UX", count: 50, color: "#fc5c7d", desc: "UX research, design briefs, audits, systems & accessibility" },
];

const testimonials = [
  { name: "Aisha K.", role: "Content Creator", avatar: "👩‍💼", text: "I used to spend 2 hours writing a single blog post. Now I get a full draft in 15 minutes. This bundle literally changed my workflow.", stars: 5 },
  { name: "Rahul M.", role: "Startup Founder", avatar: "👨‍💻", text: "The business & marketing prompts alone are worth 10x the price. My pitch deck went from average to investor-ready in one session.", stars: 5 },
  { name: "Sarah L.", role: "Freelance Designer", avatar: "👩‍🎨", text: "The UX and design prompts are incredibly detailed. My client briefs are now professional and thorough. Highly recommended!", stars: 5 },
  { name: "James T.", role: "Digital Marketer", avatar: "👨‍💼", text: "I've tried other prompt packs before. Nothing comes close to this level of depth and detail. Every prompt is genuinely actionable.", stars: 5 },
];

const faqs = [
  { q: "What format do I receive the prompts in?", a: "You get instant access to a beautifully designed web page with all 1000+ prompts. You can copy any prompt with one click, search across all categories, and download the full collection as a PDF." },
  { q: "Which AI tools do these prompts work with?", a: "Every prompt works with ChatGPT, Claude, Gemini, Grok, Copilot, and any other AI tool. The prompts are tool-agnostic and optimized for maximum output quality." },
  { q: "I'm a beginner. Will these work for me?", a: "Absolutely. Every prompt includes clear placeholders like [topic] or [your goal] so you just fill in your specifics. No prompt engineering experience needed." },
  { q: "Are these prompts truly detailed and long?", a: "Yes — unlike basic prompt packs with one-liners, every prompt here is a comprehensive multi-part instruction that tells the AI exactly what to do, how to structure the output, and what quality standards to meet." },
  { q: "Do I get lifetime access?", a: "Yes. Once you purchase, you have lifetime access including all future updates and additions to the bundle." },
  { q: "Is there a refund policy?", a: "Yes — 30-day money back guarantee, no questions asked. If it doesn't work for you, you get a full refund." },
];

export default function App() {
  const [openFaq, setOpenFaq] = useState(null);
  const [timeLeft, setTimeLeft] = useState({ h: 5, m: 59, s: 47 });
  const [copied, setCopied] = useState(false);
  const [activeTab, setActiveTab] = useState(0);

  useEffect(() => {
    const t = setInterval(() => {
      setTimeLeft(prev => {
        let { h, m, s } = prev;
        if (s > 0) return { h, m, s: s - 1 };
        if (m > 0) return { h, m: m - 1, s: 59 };
        if (h > 0) return { h: h - 1, m: 59, s: 59 };
        return { h: 5, m: 59, s: 47 };
      });
    }, 1000);
    return () => clearInterval(t);
  }, []);

  const pad = n => String(n).padStart(2, "0");

  const scrollToPricing = () => {
    document.getElementById("pricing")?.scrollIntoView({ behavior: "smooth" });
  };

  return (
    <div style={{ background: "#07070d", color: "#e8e8f0", fontFamily: "'Segoe UI', system-ui, sans-serif", lineHeight: 1.6 }}>

      {/* TOP BANNER */}
      <div style={{ background: "linear-gradient(90deg,#7c5cfc,#fc5c7d)", textAlign: "center", padding: "10px 16px", fontSize: 13, fontWeight: 600, letterSpacing: 0.5 }}>
        🔥 Limited Launch Price — Ends in {pad(timeLeft.h)}:{pad(timeLeft.m)}:{pad(timeLeft.s)} &nbsp;|&nbsp; <span style={{ textDecoration: "underline", cursor: "pointer" }} onClick={scrollToPricing}>Grab it now →</span>
      </div>

      {/* HERO */}
      <div style={{ background: "linear-gradient(160deg,#07070d 0%,#1a0a2e 50%,#07070d 100%)", padding: "72px 20px 60px", textAlign: "center", position: "relative", overflow: "hidden" }}>
        <div style={{ position: "absolute", top: "20%", left: "50%", transform: "translateX(-50%)", width: 600, height: 600, background: "radial-gradient(ellipse,rgba(124,92,252,0.12),transparent 70%)", borderRadius: "50%", pointerEvents: "none" }} />

        <div style={{ display: "inline-flex", alignItems: "center", gap: 6, background: "rgba(124,92,252,0.15)", border: "1px solid rgba(124,92,252,0.3)", color: "#b39dfc", fontSize: 12, fontWeight: 600, padding: "6px 16px", borderRadius: 50, letterSpacing: 1.5, textTransform: "uppercase", marginBottom: 24 }}>
          ✦ The Ultimate AI Toolkit
        </div>

        <h1 style={{ fontSize: "clamp(32px,6vw,68px)", fontWeight: 900, lineHeight: 1.1, margin: "0 0 16px", position: "relative" }}>
          Stop Wasting Hours on<br />
          <span style={{ background: "linear-gradient(90deg,#7c5cfc,#fc5c7d,#5cf8d6)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>Weak AI Prompts</span>
        </h1>

        <p style={{ color: "#aaa", fontSize: "clamp(15px,2vw,19px)", maxWidth: 640, margin: "0 auto 16px" }}>
          Get <strong style={{ color: "#e8e8f0" }}>1000+ professionally written, deeply detailed prompts</strong> across 15 categories — and make AI actually do the heavy lifting for you.
        </p>
        <p style={{ color: "#7c5cfc", fontSize: 14, marginBottom: 36, fontWeight: 600 }}>
          Works with ChatGPT · Claude · Gemini · Copilot · Any AI Tool
        </p>

        <div style={{ display: "flex", gap: 12, justifyContent: "center", flexWrap: "wrap", marginBottom: 40 }}>
          <button onClick={scrollToPricing} style={{ background: "linear-gradient(135deg,#7c5cfc,#fc5c7d)", color: "white", border: "none", padding: "16px 36px", borderRadius: 12, fontSize: 16, fontWeight: 800, cursor: "pointer", boxShadow: "0 8px 32px rgba(124,92,252,0.4)", letterSpacing: 0.3 }}>
            🚀 Get Instant Access — $9
          </button>
          <button onClick={() => document.getElementById("preview")?.scrollIntoView({ behavior: "smooth" })} style={{ background: "transparent", color: "#aaa", border: "1px solid #2a2a3d", padding: "16px 28px", borderRadius: 12, fontSize: 15, fontWeight: 600, cursor: "pointer" }}>
            👀 See Sample Prompts
          </button>
        </div>

        {/* Social proof bar */}
        <div style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 6, color: "#aaa", fontSize: 13 }}>
          <span style={{ color: "#fcb55c", fontSize: 15 }}>★★★★★</span>
          <span>Rated 4.9/5 by 2,400+ customers</span>
          <span style={{ color: "#2a2a3d" }}>|</span>
          <span>🔒 30-day money-back guarantee</span>
        </div>

        {/* Stats */}
        <div style={{ display: "flex", justifyContent: "center", gap: "clamp(20px,4vw,60px)", flexWrap: "wrap", marginTop: 48, padding: "32px 20px", background: "rgba(255,255,255,0.03)", borderRadius: 16, maxWidth: 700, margin: "48px auto 0", border: "1px solid #1a1a2e" }}>
          {[["1,000+","Detailed Prompts"],["15","Categories"],["2,400+","Happy Buyers"],["30-Day","Money Back"]].map(([n,l]) => (
            <div key={l} style={{ textAlign: "center" }}>
              <div style={{ fontSize: "clamp(24px,3vw,36px)", fontWeight: 900, background: "linear-gradient(90deg,#7c5cfc,#5cf8d6)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>{n}</div>
              <div style={{ color: "#8888aa", fontSize: 12, textTransform: "uppercase", letterSpacing: 1, marginTop: 2 }}>{l}</div>
            </div>
          ))}
        </div>
      </div>

      {/* PROBLEM SECTION */}
      <div style={{ padding: "64px 20px", background: "#0d0d18" }}>
        <div style={{ maxWidth: 780, margin: "0 auto", textAlign: "center" }}>
          <h2 style={{ fontSize: "clamp(24px,4vw,40px)", fontWeight: 800, marginBottom: 16 }}>
            You're Getting <span style={{ color: "#fc5c7d" }}>Mediocre Results</span> from AI — and It's Not Your Fault
          </h2>
          <p style={{ color: "#aaa", fontSize: 16, marginBottom: 40 }}>
            Most people type vague prompts and get generic, unusable output. The secret isn't the AI model — it's the quality of the prompt.
          </p>
          <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 16, textAlign: "left" }}>
            {[
              ["❌", "Getting generic, copy-paste answers that need total rewrites"],
              ["❌", "Spending 30+ minutes trying to get the AI to 'just understand' what you want"],
              ["❌", "Output that sounds robotic and unusable for real work"],
              ["❌", "Starting from a blank page every single time"],
            ].map(([icon, text]) => (
              <div key={text} style={{ background: "rgba(252,92,125,0.06)", border: "1px solid rgba(252,92,125,0.15)", borderRadius: 10, padding: "14px 16px", display: "flex", gap: 10, alignItems: "flex-start" }}>
                <span style={{ fontSize: 18 }}>{icon}</span>
                <span style={{ color: "#ccc", fontSize: 14 }}>{text}</span>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* SOLUTION */}
      <div style={{ padding: "64px 20px", background: "#07070d", textAlign: "center" }}>
        <div style={{ maxWidth: 780, margin: "0 auto" }}>
          <div style={{ color: "#7c5cfc", fontSize: 13, fontWeight: 700, letterSpacing: 2, textTransform: "uppercase", marginBottom: 12 }}>The Solution</div>
          <h2 style={{ fontSize: "clamp(24px,4vw,42px)", fontWeight: 900, marginBottom: 16 }}>
            1,000+ Prompts That Are <span style={{ background: "linear-gradient(90deg,#7c5cfc,#5cf8d6)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>Already Engineered for You</span>
          </h2>
          <p style={{ color: "#aaa", fontSize: 16, maxWidth: 600, margin: "0 auto 48px" }}>
            Not one-liners. Not vague instructions. Each prompt is a complete, multi-part brief that tells the AI exactly what to produce — formatted, structured, and ready to copy-paste.
          </p>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(260px,1fr))", gap: 12 }}>
            {[
              ["✅", "Copy-paste ready", "No editing needed — just swap in your topic"],
              ["✅", "Deeply detailed", "Multi-part instructions with quality standards built-in"],
              ["✅", "Instant results", "Get professional-quality output in seconds"],
              ["✅", "All tools supported", "ChatGPT, Claude, Gemini — works everywhere"],
              ["✅", "15 categories", "Every use case from business to creative to coding"],
              ["✅", "Lifetime access", "Yours forever, including all future updates"],
            ].map(([icon, title, desc]) => (
              <div key={title} style={{ background: "rgba(124,92,252,0.06)", border: "1px solid rgba(124,92,252,0.15)", borderRadius: 12, padding: "18px 16px", textAlign: "left" }}>
                <div style={{ fontSize: 20, marginBottom: 6 }}>{icon}</div>
                <div style={{ fontWeight: 700, fontSize: 15, color: "#e8e8f0", marginBottom: 4 }}>{title}</div>
                <div style={{ color: "#888", fontSize: 13 }}>{desc}</div>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* CATEGORIES */}
      <div style={{ padding: "64px 20px", background: "#0d0d18" }}>
        <div style={{ maxWidth: 1100, margin: "0 auto" }}>
          <div style={{ textAlign: "center", marginBottom: 40 }}>
            <div style={{ color: "#7c5cfc", fontSize: 13, fontWeight: 700, letterSpacing: 2, textTransform: "uppercase", marginBottom: 10 }}>What's Included</div>
            <h2 style={{ fontSize: "clamp(24px,4vw,40px)", fontWeight: 900, marginBottom: 8 }}>15 Categories. 1,000+ Prompts.</h2>
            <p style={{ color: "#aaa", fontSize: 15 }}>Every professional use case, covered in depth.</p>
          </div>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(300px,1fr))", gap: 14 }}>
            {categories.map((cat) => (
              <div key={cat.name} style={{ background: "#12121e", border: "1px solid #1e1e30", borderRadius: 12, padding: "18px 16px", display: "flex", gap: 14, alignItems: "flex-start", transition: "border-color 0.2s" }}
                onMouseEnter={e => e.currentTarget.style.borderColor = cat.color + "55"}
                onMouseLeave={e => e.currentTarget.style.borderColor = "#1e1e30"}>
                <div style={{ width: 44, height: 44, borderRadius: 10, background: cat.color + "20", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 22, flexShrink: 0 }}>{cat.icon}</div>
                <div>
                  <div style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 4 }}>
                    <span style={{ fontWeight: 700, fontSize: 14 }}>{cat.name}</span>
                    <span style={{ background: cat.color + "25", color: cat.color, fontSize: 10, fontWeight: 700, padding: "2px 7px", borderRadius: 20 }}>{cat.count} prompts</span>
                  </div>
                  <p style={{ color: "#888", fontSize: 12, margin: 0 }}>{cat.desc}</p>
                </div>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* SAMPLE PROMPTS PREVIEW */}
      <div id="preview" style={{ padding: "64px 20px", background: "#07070d" }}>
        <div style={{ maxWidth: 860, margin: "0 auto" }}>
          <div style={{ textAlign: "center", marginBottom: 32 }}>
            <div style={{ color: "#7c5cfc", fontSize: 13, fontWeight: 700, letterSpacing: 2, textTransform: "uppercase", marginBottom: 10 }}>Sample Prompts</div>
            <h2 style={{ fontSize: "clamp(22px,3vw,36px)", fontWeight: 900, marginBottom: 8 }}>See the Difference. Feel the Quality.</h2>
            <p style={{ color: "#aaa", fontSize: 14 }}>These are the actual prompts you'll get — not watered-down previews.</p>
          </div>

          {/* Tab switcher */}
          <div style={{ display: "flex", gap: 8, marginBottom: 20, overflowX: "auto", paddingBottom: 4 }}>
            {["✍️ Writing","💻 Coding","💼 Business","📢 Marketing","🤖 AI Tools"].map((tab, i) => (
              <button key={tab} onClick={() => setActiveTab(i)} style={{ background: activeTab === i ? "linear-gradient(90deg,#7c5cfc,#fc5c7d)" : "#12121e", color: activeTab === i ? "white" : "#888", border: `1px solid ${activeTab === i ? "transparent" : "#1e1e30"}`, padding: "8px 16px", borderRadius: 8, cursor: "pointer", fontSize: 13, fontWeight: 600, whiteSpace: "nowrap" }}>
                {tab}
              </button>
            ))}
          </div>

          {[
            [
              "Write a comprehensive, SEO-optimized blog post about [topic] targeting [specific audience]. Structure it with an attention-grabbing introduction that hooks the reader in the first sentence, at least 5 detailed key sections each with subheadings, relevant examples or data points, internal linking suggestions, a meta description, and a compelling call-to-action at the end. Aim for 1500–2000 words and a Flesch reading score above 60.",
              "Write a powerful persuasive essay arguing for [position]. Open with a compelling hook — a startling statistic, vivid scenario, or provocative question. State your thesis clearly in the introduction. Develop 3 well-reasoned arguments, each in its own section with evidence and examples. Acknowledge and dismantle opposing views. Conclude with an emotional and logical appeal that motivates the reader to think or act differently.",
            ],
            [
              "Write a production-ready [language] function that [does X]. Requirements: include comprehensive input validation with descriptive error messages, handle all edge cases explicitly, add JSDoc/docstring comments explaining parameters, return values, and thrown exceptions, provide a detailed usage example with multiple test cases including edge cases, and follow the language's idiomatic style guide. Also suggest 2–3 potential optimizations with their tradeoffs.",
              "Perform a thorough code review of the following code and provide: (1) a severity-rated list of bugs found (critical/major/minor), (2) security vulnerabilities with CVE references where applicable, (3) performance bottlenecks with profiling suggestions, (4) maintainability and readability issues, (5) test coverage gaps, and (6) a refactored version of the most problematic sections with explanations.",
            ],
            [
              "Create a comprehensive, investor-ready business plan for [business idea] including: a one-page executive summary with the core value proposition and key metrics, detailed market analysis (TAM/SAM/SOM with sources), competitive landscape with positioning map, revenue model with 3 pricing scenarios, unit economics (CAC, LTV, payback period), go-to-market strategy with phased rollout, and financial projections for 3 years.",
              "Write a deep, actionable SWOT analysis for [company/business idea]. For each quadrant, provide 5–7 specific, evidence-based points (not generic statements). Then add a SO/ST/WO/WT strategy matrix showing how to leverage strengths, shore up weaknesses, capture opportunities, and mitigate threats.",
            ],
            [
              "Write 5 distinct, high-converting ad copy variations for [product] targeting [specific audience] on Facebook/Instagram. For each variation: provide the primary text, headline, description, and a CTA button selection. Use a different emotional angle for each (curiosity, FOMO, social proof, aspirational, problem-solution). Include notes on which audience segment each variant is optimized for.",
              "Create a strategic 5-email nurture sequence for leads who signed up for [offer]. For each email: subject line + preview text, optimal send timing, primary goal and psychological principle at work, full email body, personalization tokens, one clear CTA with button text, and A/B test suggestion.",
            ],
            [
              "Act as a world-class expert in [field] with 20+ years of practical experience. I need your help with [specific task]. Before you begin: ask me 3–5 clarifying questions to understand my context, constraints, and desired outcome. Then provide your response with: a common mistake warning for my situation, a suggested next step, and a question that would help me think more deeply about this.",
              "Simulate a sophisticated brainstorming session with 5 distinct expert personas: The Optimist, The Critic, The Creative, The Analyst, and The Pragmatist — each responding to this challenge: [describe challenge]. Have each persona respond in character and then react to each other's ideas. End with a synthesis of the most promising directions.",
            ]
          ][activeTab].map((prompt, i) => (
            <div key={i} style={{ background: "#12121e", border: "1px solid #1e1e30", borderRadius: 12, padding: 20, marginBottom: 12, position: "relative" }}>
              <div style={{ fontSize: 10, color: "#666", fontFamily: "monospace", marginBottom: 8 }}>SAMPLE PROMPT #{i + 1}</div>
              <p style={{ margin: 0, fontSize: 14, color: "#ccc", lineHeight: 1.7 }}>{prompt}</p>
              <button onClick={() => { navigator.clipboard.writeText(prompt); setCopied(i); setTimeout(() => setCopied(null), 1500); }}
                style={{ marginTop: 12, background: copied === i ? "rgba(92,248,214,0.15)" : "rgba(124,92,252,0.1)", border: `1px solid ${copied === i ? "#5cf8d6" : "rgba(124,92,252,0.3)"}`, color: copied === i ? "#5cf8d6" : "#7c5cfc", padding: "6px 14px", borderRadius: 6, cursor: "pointer", fontSize: 12, fontWeight: 600 }}>
                {copied === i ? "✅ Copied!" : "📋 Copy Prompt"}
              </button>
            </div>
          ))}
        </div>
      </div>

      {/* TESTIMONIALS */}
      <div style={{ padding: "64px 20px", background: "#0d0d18" }}>
        <div style={{ maxWidth: 1000, margin: "0 auto" }}>
          <div style={{ textAlign: "center", marginBottom: 40 }}>
            <div style={{ color: "#fcb55c", fontSize: 22, marginBottom: 8 }}>★★★★★</div>
            <h2 style={{ fontSize: "clamp(22px,3vw,36px)", fontWeight: 900, marginBottom: 8 }}>2,400+ Customers Love It</h2>
            <p style={{ color: "#aaa", fontSize: 14 }}>Real results from real people who use these prompts every day.</p>
          </div>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(260px,1fr))", gap: 14 }}>
            {testimonials.map(t => (
              <div key={t.name} style={{ background: "#12121e", border: "1px solid #1e1e30", borderRadius: 14, padding: 22 }}>
                <div style={{ color: "#fcb55c", marginBottom: 10 }}>{"★".repeat(t.stars)}</div>
                <p style={{ color: "#ccc", fontSize: 14, lineHeight: 1.65, margin: "0 0 16px" }}>"{t.text}"</p>
                <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
                  <div style={{ width: 36, height: 36, borderRadius: "50%", background: "linear-gradient(135deg,#7c5cfc,#fc5c7d)", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 18 }}>{t.avatar}</div>
                  <div>
                    <div style={{ fontWeight: 700, fontSize: 13 }}>{t.name}</div>
                    <div style={{ color: "#888", fontSize: 12 }}>{t.role}</div>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* PRICING */}
      <div id="pricing" style={{ padding: "72px 20px", background: "#07070d", textAlign: "center" }}>
        <div style={{ maxWidth: 520, margin: "0 auto" }}>
          <div style={{ color: "#7c5cfc", fontSize: 13, fontWeight: 700, letterSpacing: 2, textTransform: "uppercase", marginBottom: 12 }}>Simple Pricing</div>
          <h2 style={{ fontSize: "clamp(24px,4vw,42px)", fontWeight: 900, marginBottom: 8 }}>One Price. Lifetime Access.</h2>
          <p style={{ color: "#aaa", fontSize: 15, marginBottom: 32 }}>No subscriptions. No upsells. Just 1,000+ prompts, yours forever.</p>

          <div style={{ background: "linear-gradient(145deg,#12121e,#1a1a2e)", border: "2px solid rgba(124,92,252,0.4)", borderRadius: 20, padding: "40px 32px", position: "relative", overflow: "hidden" }}>
            {/* Glow */}
            <div style={{ position: "absolute", top: -60, right: -60, width: 200, height: 200, background: "radial-gradient(ellipse,rgba(124,92,252,0.2),transparent 70%)", borderRadius: "50%", pointerEvents: "none" }} />

            <div style={{ display: "inline-block", background: "linear-gradient(90deg,#fc5c7d,#fcb55c)", color: "white", fontSize: 11, fontWeight: 800, padding: "5px 14px", borderRadius: 50, letterSpacing: 1, textTransform: "uppercase", marginBottom: 20 }}>🔥 Launch Special</div>

            <div style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 12, marginBottom: 6 }}>
              <span style={{ fontSize: 22, color: "#666", textDecoration: "line-through" }}>$49</span>
              <span style={{ fontSize: 56, fontWeight: 900, background: "linear-gradient(90deg,#7c5cfc,#fc5c7d)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>$9</span>
            </div>
            <p style={{ color: "#888", fontSize: 13, marginBottom: 28 }}>One-time payment · Instant access · Lifetime updates</p>

            <div style={{ textAlign: "left", marginBottom: 28 }}>
              {[
                "1,000+ long, detailed AI prompts",
                "15 professional categories",
                "Copy with one click — works instantly",
                "Search across all 1,000+ prompts",
                "Download as full PDF",
                "Works with ALL AI tools",
                "Lifetime access + free updates",
                "30-day money-back guarantee",
              ].map(item => (
                <div key={item} style={{ display: "flex", alignItems: "center", gap: 10, padding: "7px 0", borderBottom: "1px solid #1e1e30", fontSize: 14, color: "#ccc" }}>
                  <span style={{ color: "#5cf8d6", fontSize: 16, flexShrink: 0 }}>✓</span> {item}
                </div>
              ))}
            </div>

            <button onClick={() => alert("🚀 Connect your payment link here!\n\nIntegrate: Gumroad, Stripe, Lemon Squeezy, or PayHip")}
              style={{ width: "100%", background: "linear-gradient(135deg,#7c5cfc,#fc5c7d)", color: "white", border: "none", padding: "18px 24px", borderRadius: 12, fontSize: 17, fontWeight: 800, cursor: "pointer", boxShadow: "0 8px 40px rgba(124,92,252,0.5)", letterSpacing: 0.3, marginBottom: 12 }}>
              🚀 Get Instant Access for $9
            </button>
            <p style={{ color: "#666", fontSize: 12 }}>🔒 Secure checkout · Instant delivery · 30-day refund</p>
          </div>

          {/* Timer */}
          <div style={{ marginTop: 20, background: "rgba(252,92,125,0.08)", border: "1px solid rgba(252,92,125,0.2)", borderRadius: 10, padding: "12px 20px" }}>
            <span style={{ color: "#fc5c7d", fontWeight: 700, fontSize: 14 }}>⏰ Launch price expires in {pad(timeLeft.h)}:{pad(timeLeft.m)}:{pad(timeLeft.s)}</span>
          </div>
        </div>
      </div>

      {/* FAQ */}
      <div style={{ padding: "64px 20px", background: "#0d0d18" }}>
        <div style={{ maxWidth: 700, margin: "0 auto" }}>
          <div style={{ textAlign: "center", marginBottom: 40 }}>
            <h2 style={{ fontSize: "clamp(22px,3vw,36px)", fontWeight: 900, marginBottom: 8 }}>Frequently Asked Questions</h2>
            <p style={{ color: "#aaa", fontSize: 14 }}>Everything you need to know before you buy.</p>
          </div>
          {faqs.map((faq, i) => (
            <div key={i} style={{ background: "#12121e", border: "1px solid #1e1e30", borderRadius: 12, marginBottom: 10, overflow: "hidden" }}>
              <button onClick={() => setOpenFaq(openFaq === i ? null : i)}
                style={{ width: "100%", background: "none", border: "none", color: "#e8e8f0", padding: "18px 20px", fontSize: 15, fontWeight: 600, textAlign: "left", cursor: "pointer", display: "flex", justifyContent: "space-between", alignItems: "center", gap: 12 }}>
                {faq.q}
                <span style={{ color: "#7c5cfc", fontSize: 20, flexShrink: 0, transition: "transform 0.2s", transform: openFaq === i ? "rotate(45deg)" : "none" }}>+</span>
              </button>
              {openFaq === i && (
                <div style={{ padding: "0 20px 18px", color: "#aaa", fontSize: 14, lineHeight: 1.7, borderTop: "1px solid #1e1e30", paddingTop: 14 }}>
                  {faq.a}
                </div>
              )}
            </div>
          ))}
        </div>
      </div>

      {/* FINAL CTA */}
      <div style={{ padding: "72px 20px", background: "linear-gradient(135deg,#0a0a1e,#1a0a2e)", textAlign: "center" }}>
        <div style={{ maxWidth: 600, margin: "0 auto" }}>
          <h2 style={{ fontSize: "clamp(26px,4vw,44px)", fontWeight: 900, marginBottom: 14 }}>
            Start Getting <span style={{ background: "linear-gradient(90deg,#7c5cfc,#5cf8d6)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>10x Better Results</span><br />from AI — Today
          </h2>
          <p style={{ color: "#aaa", fontSize: 16, marginBottom: 32 }}>
            Join 2,400+ professionals who use these prompts to save hours, produce better work, and unlock the real power of AI.
          </p>
          <button onClick={scrollToPricing}
            style={{ background: "linear-gradient(135deg,#7c5cfc,#fc5c7d)", color: "white", border: "none", padding: "18px 48px", borderRadius: 14, fontSize: 18, fontWeight: 800, cursor: "pointer", boxShadow: "0 8px 40px rgba(124,92,252,0.5)", letterSpacing: 0.3, display: "block", margin: "0 auto 16px" }}>
            🚀 Get All 1,000+ Prompts — $9
          </button>
          <p style={{ color: "#666", fontSize: 13 }}>🔒 30-Day Money-Back Guarantee · Instant Access · Lifetime Updates</p>
        </div>
      </div>

      <footer style={{ textAlign: "center", padding: "24px 20px", borderTop: "1px solid #1a1a2e", color: "#555", fontSize: 12 }}>
        © 2025 AI Prompts Bundle · All rights reserved · Made with ❤️ for AI enthusiasts
      </footer>
    </div>
  );
}
