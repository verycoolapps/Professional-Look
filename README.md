# PROFESSIONAL LOOK
## Multi-File Professional Communication Intelligence Ecosystem

> Transform raw drafts, rough ideas, and corporate copy into executive-grade, platform-native, reputation-safe content — across nine tone profiles, seven platforms, and two languages.

---

## ENGLISH

### What Is PROFESSIONAL LOOK?

PROFESSIONAL LOOK is a Claude Code skill — a modular, multi-file intelligence system designed to operate at the intersection of editorial excellence and professional communication strategy.

It is not a grammar checker. It is not a thesaurus. It does not suggest synonyms or fix typos.

PROFESSIONAL LOOK thinks about what you are trying to communicate, who you are communicating with, where you are communicating, and what reputation you are building — then produces content that achieves all four simultaneously.

The system covers nine professional tone profiles (from CEO-level sparse authority to warm intellectual credibility), seven major platforms with platform-native logic, executive communication templates, personal brand strategy, anti-AI-slop detection, and a reputation protection layer that flags risks before you publish.

Everything is built into a progressive disclosure architecture: only the modules relevant to your specific task are loaded, ensuring precise, focused intelligence rather than generic output.

---

### Installation

PROFESSIONAL LOOK is a Claude Code skill. Install it through the Claude Code skill interface.

**Via Claude Code CLI:**
```bash
# Install from the verycoolapps skill registry
claude skill install verycoolapps/professional-look
```

**Manual Installation:**
1. Clone this repository:
   ```bash
   git clone https://github.com/verycoolapps/Professional-Look.git
   ```
2. Place the directory in your Claude Code skills folder:
   ```bash
   mv Professional-Look ~/.claude/skills/professional-look
   ```
3. The skill activates automatically on the next Claude Code session.

---

### Activation

PROFESSIONAL LOOK activates on these trigger phrases:

| Trigger | What Happens |
|---|---|
| "improve this" | Rewrite mode — elevates existing draft |
| "make this professional" | Full professional calibration |
| "rewrite" | Deep edit or full rebuild |
| "sound like a CEO" | CEO tone profile activated |
| "LinkedIn post" | LinkedIn platform module + relevant engines |
| "Instagram caption" | Instagram platform module + tone |
| "personal brand" | Brand strategy intelligence loaded |
| "write for me" | Original writing mode |
| "content strategy" | Full content intelligence layer |
| "clean this up" | Light Polish rewrite mode |
| "bio" | Profile optimization mode |
| "announcement" | Announcement Frame pattern activated |
| "crisis statement" | Reputation Protection + Crisis tone |
| "executive message" | Executive Communication module |
| "make this premium" | Luxury/Premium tone profile |
| "thought leadership" | Thought Leader tone + LinkedIn/Medium |

You can also be direct:
- "Write a CEO-level LinkedIn post about our product launch"
- "Rewrite this Instagram caption for a luxury brand audience"
- "Build a personal brand strategy for a senior finance executive"
- "Translate and adapt this announcement for an Indonesian professional audience"
- "Check this post for reputational risks before I publish it"

---

### Supported Platforms

| Platform | Capability |
|---|---|
| **LinkedIn** | Executive posts, articles, profile optimization, thought leadership, comments, connection messages, recommendations |
| **Instagram** | Captions, Reels scripts, Stories text, carousels, bio optimization |
| **Facebook** | Community posts, organizational announcements, business pages, event promotion |
| **X / Twitter** | Tweets, threads, quote-tweet commentary, professional opinion |
| **TikTok** | Hook writing, script structure, creator voice, caption |
| **YouTube** | Titles, descriptions, scripts, channel about, community posts |
| **Threads / Reddit / Medium / Substack / WhatsApp Business / Telegram** | Via universal-platforms module |

---

### Core Capabilities

**Writing**
- Original content creation from a brief, idea, or blank slate
- Platform-calibrated structure and length
- Hook writing that earns attention without clickbait
- CTAs that invite without desperation

**Rewriting**
- Four modes: Light Polish / Deep Edit / Full Rebuild / Structural Overhaul
- Preserves your voice while eliminating weaknesses
- Upgrades vocabulary without adding inflation
- Fixes logic gaps, redundancy, and flow

**Tone Profiles**
- CEO/Founder — Visionary, decisive, sparse
- Executive — Structured, authoritative, measured
- Diplomatic — Balanced, inclusive, precise
- Corporate — Formal, compliant, reliable
- Leadership — Inspirational, clear, human
- Luxury/Premium — Elevated, understated, tasteful
- Intellectual/Thought Leader — Nuanced, evidence-backed, original
- Warm Professional — Approachable, genuine, credible
- Crisis/Sensitive — Careful, accountable, clear

**Anti-AI-Slop Detection**
- 50+ banned phrase dictionary
- Pattern recognition for generic, hollow writing
- Substitution with language that actually means something

**Reputation Protection**
- Confidentiality risk detection
- Legal sensitivity flags
- Cultural insensitivity scanning
- Overclaiming and defamation risk alerts
- Pre-publication checklist

**Strategic Intelligence**
- Personal brand identity framework
- Content pillar development
- Editorial calendar logic
- Platform cross-posting strategy
- Audience psychology and persuasion architecture
- Multilingual and cultural adaptation (EN ↔ ID)

---

### Directory Structure

```
professional-look/
├── SKILL.md                          ← Entry point and orchestration
├── README.md                         ← This file
├── CHANGELOG.md                      ← Version history
├── LICENSE                           ← MIT
│
├── core/
│   ├── identity.md                   ← Skill persona and philosophy
│   ├── operating-system.md           ← Operational workflow
│   ├── decision-engine.md            ← Routing and decision logic
│   ├── professional-standards.md     ← Writing laws
│   └── quality-control.md           ← Scoring and revision
│
├── engines/
│   ├── writing-engine.md
│   ├── rewriting-engine.md
│   ├── tone-intelligence.md
│   ├── anti-ai-slop-engine.md
│   ├── recommendation-engine.md
│   └── reputation-protection.md
│
├── platforms/
│   ├── linkedin.md
│   ├── instagram.md
│   ├── facebook.md
│   ├── x-twitter.md
│   ├── tiktok.md
│   ├── youtube.md
│   └── universal-platforms.md
│
├── intelligence/
│   ├── executive-communication.md
│   ├── personal-branding.md
│   ├── audience-psychology.md
│   ├── multilingual-communication.md
│   └── content-strategy.md
│
├── reference/
│   ├── professional-language-library.md
│   ├── writing-patterns.md
│   ├── platform-formats.md
│   └── anti-patterns.md
│
└── tests/
    ├── test-cases.md
    ├── quality-benchmarks.md
    └── evaluation-protocol.md
```

---

### Quality Standard

Every output from this skill is scored against a seven-dimension rubric:

1. **Clarity** — Is the message immediately understood?
2. **Tone Fit** — Does the voice match the profile and platform?
3. **Platform Fit** — Is the format, length, and structure native?
4. **Authenticity** — Does this sound like a real, knowledgeable human?
5. **Impact** — Will this achieve its communication objective?
6. **Originality** — Is this free from clichés and AI patterns?
7. **Reputation Safety** — Could this damage professional standing?

Minimum acceptance: 85/100. Anything below is revised before delivery.

---

### Contributing

Pull requests are welcome. To contribute a new module, platform guide, or reference collection:

1. Fork this repository
2. Create your module following the structure in existing modules (Purpose → Scope → Activation → Workflow → Standards → Failure Modes → Examples → Dependencies)
3. Add internal references using correct relative paths
4. Update SKILL.md's module routing table if you add a new activation trigger
5. Submit a pull request with a clear description of what the module adds

---

### License

MIT License. See `LICENSE` for details.

---

---

## BAHASA INDONESIA

### Apa Itu PROFESSIONAL LOOK?

PROFESSIONAL LOOK adalah skill Claude Code — sistem kecerdasan modular multi-file yang dirancang untuk beroperasi di persimpangan antara keunggulan editorial dan strategi komunikasi profesional.

Ini bukan pemeriksa tata bahasa. Ini bukan tesaurus. Bukan alat yang menyarankan sinonim atau memperbaiki typo.

PROFESSIONAL LOOK berpikir tentang apa yang ingin kamu komunikasikan, kepada siapa kamu berbicara, di mana kamu berkomunikasi, dan reputasi seperti apa yang sedang kamu bangun — lalu menghasilkan konten yang mencapai keempat tujuan tersebut sekaligus.

Sistem ini mencakup sembilan profil nada profesional (dari otoritas singkat level CEO hingga kredibilitas intelektual yang hangat), tujuh platform utama dengan logika native masing-masing, template komunikasi eksekutif, strategi personal brand, deteksi AI slop, dan lapisan perlindungan reputasi yang menandai risiko sebelum kamu mempublikasikan konten.

Semuanya dibangun dalam arsitektur progressive disclosure: hanya modul yang relevan dengan tugasmu yang dimuat, memastikan kecerdasan yang tepat sasaran alih-alih output generik.

---

### Instalasi

PROFESSIONAL LOOK adalah skill Claude Code. Instal melalui antarmuka skill Claude Code.

**Melalui CLI Claude Code:**
```bash
# Instal dari registri skill verycoolapps
claude skill install verycoolapps/professional-look
```

**Instalasi Manual:**
1. Clone repositori ini:
   ```bash
   git clone https://github.com/verycoolapps/Professional-Look.git
   ```
2. Tempatkan direktori di folder skill Claude Code kamu:
   ```bash
   mv Professional-Look ~/.claude/skills/professional-look
   ```
3. Skill akan aktif otomatis di sesi Claude Code berikutnya.

---

### Aktivasi

PROFESSIONAL LOOK aktif pada frasa trigger berikut:

| Trigger | Yang Terjadi |
|---|---|
| "improve this" / "perbaiki ini" | Mode rewrite — meningkatkan draft yang ada |
| "make this professional" / "buat ini profesional" | Kalibrasi profesional penuh |
| "rewrite" / "tulis ulang" | Deep edit atau full rebuild |
| "sound like a CEO" / "seperti CEO" | Profil nada CEO diaktifkan |
| "LinkedIn post" / "post LinkedIn" | Modul platform LinkedIn + engine yang relevan |
| "Instagram caption" / "caption Instagram" | Modul platform Instagram + nada |
| "personal brand" / "personal branding" | Kecerdasan strategi brand dimuat |
| "content strategy" / "strategi konten" | Lapisan kecerdasan konten penuh |
| "bio" | Mode optimasi profil |
| "announcement" / "pengumuman" | Pola Announcement Frame diaktifkan |
| "crisis statement" / "pernyataan krisis" | Perlindungan Reputasi + nada Krisis |

Kamu juga bisa langsung:
- "Tulis postingan LinkedIn bergaya CEO tentang peluncuran produk kami"
- "Tulis ulang caption Instagram ini untuk audiens brand mewah"
- "Buat strategi personal brand untuk eksekutif keuangan senior"
- "Terjemahkan dan adaptasi pengumuman ini untuk audiens profesional Indonesia"
- "Periksa post ini dari risiko reputasi sebelum aku publikasikan"

---

### Platform yang Didukung

| Platform | Kemampuan |
|---|---|
| **LinkedIn** | Post eksekutif, artikel, optimasi profil, thought leadership, komentar, pesan koneksi, rekomendasi |
| **Instagram** | Caption, skrip Reels, teks Stories, carousel, optimasi bio |
| **Facebook** | Post komunitas, pengumuman organisasi, halaman bisnis, promosi acara |
| **X / Twitter** | Tweet, thread, komentar quote-tweet, opini profesional |
| **TikTok** | Penulisan hook, struktur skrip, suara kreator, caption |
| **YouTube** | Judul, deskripsi, skrip, about channel, community post |
| **Threads / Reddit / Medium / Substack / WhatsApp Business / Telegram** | Melalui modul universal-platforms |

---

### Kemampuan Inti

**Penulisan**
- Pembuatan konten orisinal dari brief, ide, atau halaman kosong
- Struktur dan panjang yang dikalibrasi untuk platform
- Penulisan hook yang mendapatkan perhatian tanpa clickbait
- CTA yang mengundang tanpa terkesan putus asa

**Penulisan Ulang**
- Empat mode: Light Polish / Deep Edit / Full Rebuild / Structural Overhaul
- Mempertahankan suaramu sambil menghilangkan kelemahan
- Meningkatkan kosakata tanpa inflasi berlebihan
- Memperbaiki celah logika, redundansi, dan alur

**Profil Nada**
- CEO/Founder — Visioner, tegas, singkat
- Executive — Terstruktur, otoritatif, terukur
- Diplomatic — Seimbang, inklusif, presisi
- Corporate — Formal, patuh, dapat diandalkan
- Leadership — Inspiratif, jelas, manusiawi
- Luxury/Premium — Tinggi, halus, berkelas
- Intellectual/Thought Leader — Bernuansa, berbasis bukti, orisinal
- Warm Professional — Mudah didekati, tulus, kredibel
- Crisis/Sensitive — Hati-hati, akuntabel, jelas

**Deteksi AI Slop**
- Kamus frasa terlarang 50+ entri
- Pengenalan pola untuk tulisan generik dan kosong
- Substitusi dengan bahasa yang benar-benar bermakna

**Perlindungan Reputasi**
- Deteksi risiko kerahasiaan
- Penanda sensitivitas hukum
- Pemindaian ketidakpekaan budaya
- Alert risiko overclaiming dan defamasi
- Daftar periksa pra-publikasi

**Kecerdasan Strategis**
- Kerangka identitas personal brand
- Pengembangan pilar konten
- Logika kalender editorial
- Strategi cross-posting antar platform
- Psikologi audiens dan arsitektur persuasi
- Adaptasi multibahasa dan budaya (EN ↔ ID)

---

### Standar Kualitas

Setiap output dari skill ini dinilai berdasarkan rubrik tujuh dimensi:

1. **Clarity / Kejelasan** — Apakah pesan langsung dipahami?
2. **Tone Fit / Kesesuaian Nada** — Apakah suara sesuai dengan profil dan platform?
3. **Platform Fit / Kesesuaian Platform** — Apakah format, panjang, dan struktur native untuk platform tersebut?
4. **Authenticity / Keaslian** — Apakah ini terdengar seperti manusia nyata yang tahu apa yang mereka bicarakan?
5. **Impact / Dampak** — Apakah ini akan mencapai tujuan komunikasinya?
6. **Originality / Orisinalitas** — Apakah ini bebas dari klise dan pola AI?
7. **Reputation Safety / Keamanan Reputasi** — Bisakah ini merusak posisi profesional?

Penerimaan minimum: 85/100. Apa pun di bawahnya direvisi sebelum dikirimkan.

---

### Berkontribusi

Pull request disambut baik. Untuk berkontribusi modul baru, panduan platform, atau koleksi referensi:

1. Fork repositori ini
2. Buat modulmu mengikuti struktur di modul yang ada (Purpose → Scope → Activation → Workflow → Standards → Failure Modes → Examples → Dependencies)
3. Tambahkan referensi internal menggunakan path relatif yang benar
4. Perbarui tabel routing modul di SKILL.md jika kamu menambahkan trigger aktivasi baru
5. Kirimkan pull request dengan deskripsi jelas tentang apa yang ditambahkan modul tersebut

---

### Lisensi

MIT License. Lihat `LICENSE` untuk detailnya.
