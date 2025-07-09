# Tema Cuandemy - Astro Theme

Tema khusus untuk situs e-learning dan blog edukasi **cuandemy.info** yang dibangun dengan framework Astro.

## 🚀 Fitur Utama

### Framework & Teknologi
- ⚡ **Astro Framework** - Static site generator modern
- 🎨 **Tailwind CSS** - Utility-first CSS framework
- 📝 **MDX Support** - Markdown dengan komponen React/Vue
- 🚀 **Partytown** - Optimasi third-party scripts
- 🗺️ **Sitemap** - SEO optimization otomatis
- 📱 **Responsive Design** - Mobile-first approach

### Desain & UI/UX
- 🎯 **Nuansa Kalem & Elegan** - Palet warna profesional
- 🔤 **Typography Modern** - Font Inter, Merriweather, JetBrains Mono
- 🎨 **Gradient & Shadows** - Visual yang menarik
- ♿ **Accessibility** - WCAG compliant

### Halaman & Konten
- 🏠 **Homepage** - Hero, features, latest articles
- 📚 **Blog** - Article grid dengan filter kategori
- ℹ️ **About** - Misi, visi, nilai perusahaan
- 📞 **Contact** - Form terintegrasi Formspree

## 📦 Instalasi

### Prerequisites
- Node.js 18+ 
- npm atau yarn

### Setup Proyek
```bash
# Clone atau download tema
cd cuandemy-theme

# Install dependencies
npm install

# Jalankan development server
npm run dev

# Build untuk production
npm run build

# Preview build
npm run preview
```

## 🛠️ Konfigurasi

### 1. Formspree Setup (Form Kontak)
Form kontak sudah dikonfigurasi dengan Formspree ID: `xrbkwwnr`

Untuk menggunakan form kontak:
1. Pastikan Formspree ID sudah benar di `src/pages/contact.astro`
2. Update URL redirect sesuai domain Anda
3. Test form dengan mengirim pesan

### 2. Site Configuration
Edit `astro.config.mjs` untuk mengubah URL situs:
```javascript
export default defineConfig({
  site: 'https://cuandemy.info', // Ganti dengan domain Anda
  // ...
});
```

### 3. Tailwind Customization
Sesuaikan warna dan styling di `tailwind.config.mjs`:
```javascript
theme: {
  extend: {
    colors: {
      primary: { /* Warna utama */ },
      secondary: { /* Warna sekunder */ },
      accent: { /* Warna aksen */ }
    }
  }
}
```

## 📁 Struktur Proyek

```
cuandemy-theme/
├── public/                 # Static assets
│   └── favicon.svg
├── src/
│   ├── components/         # Komponen reusable
│   │   ├── Header.astro   # Navigasi utama
│   │   └── Footer.astro   # Footer dengan links
│   ├── layouts/           # Layout templates
│   │   ├── BaseLayout.astro    # Layout dasar dengan SEO
│   │   └── MainLayout.astro    # Layout dengan header/footer
│   ├── pages/             # Halaman website
│   │   ├── index.astro    # Homepage
│   │   ├── about.astro    # Halaman tentang
│   │   ├── contact.astro  # Halaman kontak
│   │   └── blog/          # Blog pages
│   │       └── index.astro
│   └── styles/            # Custom CSS (opsional)
├── astro.config.mjs       # Konfigurasi Astro
├── tailwind.config.mjs    # Konfigurasi Tailwind
└── package.json
```

## 🎨 Customization

### Mengubah Warna Tema
1. Edit `tailwind.config.mjs`
2. Ubah nilai di `colors.primary`, `colors.secondary`, `colors.accent`
3. Restart development server

### Menambah Halaman Baru
1. Buat file `.astro` di folder `src/pages/`
2. Import dan gunakan `MainLayout`
3. Tambahkan link di navigasi (`Header.astro`)

### Menambah Komponen
1. Buat file `.astro` di folder `src/components/`
2. Import dan gunakan di halaman yang diinginkan

## 📝 Konten Management

### Blog Posts
Untuk menambah artikel blog:
1. Buat file `.astro` atau `.mdx` di `src/pages/blog/`
2. Gunakan frontmatter untuk metadata
3. Update grid artikel di `src/pages/blog/index.astro`

### Navigation Menu
Edit menu navigasi di `src/components/Header.astro`:
```javascript
const navItems = [
  { name: 'Beranda', href: '/', current: currentPath === '/' },
  { name: 'Blog', href: '/blog', current: currentPath.startsWith('/blog') },
  // Tambah item menu baru di sini
];
```

## 🚀 Deployment

### Vercel (Recommended)
```bash
npm run build
# Upload folder dist/ ke Vercel
```

### Netlify
```bash
npm run build
# Upload folder dist/ ke Netlify
```

### Manual Hosting
```bash
npm run build
# Upload isi folder dist/ ke web server
```

## 🔧 Development

### Commands
```bash
npm run dev          # Development server
npm run build        # Build untuk production
npm run preview      # Preview build lokal
npm run astro        # Astro CLI commands
```

### Hot Reload
Development server mendukung hot reload untuk:
- File `.astro`
- File `.ts/.js`
- File CSS/Tailwind
- File konfigurasi

## 📊 Performance

Tema ini dioptimalkan untuk:
- ⚡ **Core Web Vitals** - LCP, FID, CLS
- 🔍 **SEO** - Meta tags, structured data
- 📱 **Mobile Performance** - Responsive images, lazy loading
- 🚀 **Loading Speed** - Static generation, minimal JS

## 🆘 Troubleshooting

### Common Issues

**1. Tailwind styles tidak muncul**
```bash
# Restart development server
npm run dev
```

**2. Form kontak tidak berfungsi**
- Pastikan Formspree ID benar
- Check network tab di browser
- Verifikasi domain di Formspree dashboard

**3. Build error**
```bash
# Clear cache dan reinstall
rm -rf node_modules package-lock.json
npm install
npm run build
```

## 📞 Support

Untuk pertanyaan atau bantuan:
- 📧 Email: support@cuandemy.info
- 🌐 Website: https://cuandemy.info
- 📱 Form kontak di website

## 📄 License

Tema ini dibuat khusus untuk Cuandemy. Silakan gunakan dan modifikasi sesuai kebutuhan.

---

**Dibuat dengan ❤️ menggunakan Astro + Tailwind CSS**
