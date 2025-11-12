# Cascadia Living Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the Cascadia Living real estate landing page. Whether you're updating text, fixing links, or adding new pages, you'll find clear, step-by-step instructions designed for beginners.

---

## Table of Contents

1. [Understanding the Page Structure](#understanding-the-page-structure)
2. [Updating Text and Content](#updating-text-and-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Updating Links](#fixing-and-updating-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Color Customization](#color-customization)
7. [Troubleshooting Common Issues](#troubleshooting-common-issues)

---

## Understanding the Page Structure

Before making changes, let's understand how the page is organized:

### Main Sections

The landing page is divided into clear sections that repeat throughout:

```
1. Header & Navigation (sticky at top)
2. Hero Section (large welcome area with main message)
3. Features Section (3 feature cards)
4. Benefits Section (3 benefit cards with statistics)
5. Testimonials Section (4 customer reviews)
6. About Us Section (company information)
7. Call-to-Action Section (large promotional area)
8. Contact Section (contact form)
9. Footer (links and company info)
```

### File Organization

Your project should have this basic structure:

```
project-folder/
├── index.html          (main landing page)
├── privacy.html        (privacy policy page)
├── terms.html          (terms of service page)
├── blog.html           (blog/resources page)
└── style.css           (optional: external styles)
```

---

## Updating Text and Content

### Finding Text to Edit

All text content in your landing page is written directly in the HTML file. To find what you want to change, open `index.html` in your text editor and use **Find & Replace** (Ctrl+F on Windows, Cmd+F on Mac).

### Section 1: Header Navigation

**Location:** Lines 117-140 (approximately)

The navigation menu appears at the top of every page. Here's what to look for:

```html
<!-- Desktop Menu -->
<div class="hidden md:flex items-center gap-8">
    <a href="#features" class="nav-link">Features</a>
    <a href="#benefits" class="nav-link">Benefits</a>
    <a href="#testimonials" class="nav-link">Testimonials</a>
    <a href="#about" class="nav-link">About</a>
    <a href="#contact" class="nav-link">Contact</a>
</div>
```

**To update:** Simply replace the text between the `>` and `</a>` tags. For example:
- `<a href="#features" class="nav-link">Features</a>` → `<a href="#features" class="nav-link">Our Services</a>`

**Important:** Do NOT change the `href="#features"` part—this tells the link where to go. Only change the visible text.

### Section 2: Hero Section (Main Welcome Area)

**Location:** Lines 161-189

This is the large section users see first. Here's the main heading:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight tracking-tight">
    Snohomish County's <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#5B4BFF] to-[#00E5A8]">#1 Real Estate Agent</span>
</h1>
```

**To update the main headline:**
1. Find: `Snohomish County's #1 Real Estate Agent`
2. Replace with your text (keep it short and impactful)
3. Example: `Your Local Real Estate Expert` or `Find Your Dream Home Today`

**To update the description below the headline:**

```html
<p class="text-xl md:text-2xl text-slate-300 mb-8 leading-relaxed font-medium">
    Expert guidance, proven results, and unparalleled local market expertise to help you navigate confidently and achieve your real estate goals.
</p>
```

**To update:** Replace the text between `<p>` and `</p>` with your own description.

### Section 3: Feature Cards

**Location:** Lines 207-270

There are three feature cards with titles and descriptions. Here's the first one:

```html
<h3 class="text-2xl font-bold text-white mb-4">Local Market Expertise</h3>
<p class="text-slate-300 leading-relaxed mb-4">
    With over a decade of experience in Snohomish County, we possess unparalleled knowledge of neighborhood trends, property values, and market dynamics...
</p>
```

**To update:**
1. Change the `<h3>` text to a new feature title
2. Change the `<p>` text to a new description
3. Do this for all three cards

**Quick Tip:** Each feature card has a bullet list. To update those:

```html
<li class="flex items-center gap-2">
    <svg class="w-5 h-5 text-[#00E5A8]" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
    </svg>
    Neighborhood-specific insights
</li>
```

Just replace `Neighborhood-specific insights` with your text. Keep the SVG code as-is (it's the checkmark icon).

### Section 4: Benefits Section

**Location:** Lines 285-340

Similar to features, this section has three benefit cards with icons and descriptions:

```html
<h3 class="text-2xl font-bold text-white mb-2">Navigate Market Confidently</h3>
<p class="text-slate-300 leading-relaxed">
    Make informed decisions backed by comprehensive market analysis...
</p>
```

**To update:** Replace the `<h3>` and `<p>` text with your own content.

**Statistics Box:** Around line 350, you'll find the statistics display:

```html
<div class="text-4xl md:text-5xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-[#5B4BFF] to-[#00E5A8] mb-2">500+</div>
<p class="text-slate-300 font-medium">Successful Transactions</p>
```

**To update:** Replace `500+` and `Successful Transactions` with your own statistics.

### Section 5: Testimonials

**Location:** Lines 378-440

Each testimonial card has a star rating, quote, and author name:

```html
<p class="text-slate-300 mb-6 leading-relaxed">
    "Bryce helped us find our dream home in Mill Creek. His knowledge of the area was incredible, and he negotiated a fantastic deal on our behalf. Highly recommend!"
</p>
<div>
    <p class="font-bold text-white">Sarah Mitchell</p>
    <p class="text-slate-400 text-sm">Homebuyer, Mill Creek</p>
</div>
```

**To update:**
1. Replace the quoted text with a real customer testimonial
2. Replace `Sarah Mitchell` with the customer's name
3. Replace `Homebuyer, Mill Creek` with their role and location

**To add more testimonials:** Copy an entire testimonial card (from `<div class="testimonial-card...">` to `</div>`) and paste it after the last one. Update the content.

### Section 6: About Us

**Location:** Lines 450-475

```html
<h2 class="section-heading">About Cascadia Living</h2>
<div class="space-y-6">
    <p class="text-lg text-slate-300 leading-relaxed font-medium">
        Founded in 2010, Cascadia Living emerged from a simple vision...
    </p>
```

**To update:** Replace the paragraphs with your company's story.

### Section 7: Contact Section

**Location:** Lines 540-590

The contact form has several fields:

```html
<label for="name" class="block text-sm font-semibold text-gray-700 mb-2">
    Full Name <span class="text-red-500">*</span>
</label>
<input 
    type="text" 
    name="name" 
    id="name" 
    required 
    class="w-full px-4 py-3 border border-gray-300 rounded-lg..."
    placeholder="John Doe"
>
```

**To update placeholder text:** Change `placeholder="John Doe"` to `placeholder="Your Name"` or similar.

**To update labels:** Change the text between `<label>` and `</label>` tags.

### Section 8: Footer

**Location:** Lines 630-720

The footer has company info, links, and social media:

```html
<p class="text-slate-400 mb-6">
    Snohomish County's premier real estate agent, delivering expert guidance and proven results for every client.
</p>
```

**To update:** Replace this text with your company description.

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first framework that uses pre-made classes to style elements. Don't worry—you don't need to write CSS code!

### Understanding Tailwind Classes

Each HTML element has multiple classes that control its appearance. Here's an example:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight tracking-tight">
```

Let's break this down:

| Class | What It Does |
|-------|-------------|
| `text-5xl` | Makes text very large |
| `md:text-6xl` | On medium screens, makes text even larger |
| `lg:text-7xl` | On large screens, makes text huge |
| `font-bold` | Makes text bold |
| `text-white` | Makes text white |
| `mb-6` | Adds margin (space) below the element |
| `leading-tight` | Tightens line spacing |
| `tracking-tight` | Tightens letter spacing |

### Common Tailwind Classes to Modify

#### Text Size

```html
<!-- Current: text-5xl -->
<!-- Change to: text-4xl (smaller) or text-6xl (larger) -->
<h1 class="text-4xl">Smaller Heading</h1>
```

Size options: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`, `text-7xl`

#### Text Color

```html
<!-- Current: text-white -->
<!-- Change to: text-slate-300 (lighter) or text-slate-700 (darker) -->
<p class="text-slate-300">Light gray text</p>
```

Common colors: `text-white`, `text-slate-300`, `text-slate-400`, `text-slate-600`

#### Spacing (Padding & Margin)

```html
<!-- Current: p-8 (padding) -->
<!-- p = padding, m = margin -->
<!-- 8 = size (larger numbers = more space) -->
<div class="p-8">Content with padding</div>
<div class="p-4">Less padding</div>
<div class="p-12">More padding</div>
```

Spacing options: `p-4`, `p-6`, `p-8`, `p-12`, `p-16` (and same for `m-`)

#### Display & Layout

```html
<!-- Current: hidden md:flex -->
<!-- hidden = hide on small screens -->
<!-- md:flex = show as flex on medium+ screens -->
<div class="hidden md:flex">Only visible on medium+ screens</div>

<!-- Current: grid grid-cols-1 md:grid-cols-3 -->
<!-- grid-cols-1 = 1 column on small screens -->
<!-- md:grid-cols-3 = 3 columns on medium+ screens -->
<div class="grid grid-cols-1 md:grid-cols-3">
    <div>Column 1</div>
    <div>Column 2</div>
    <div>Column 3</div>
</div>
```

#### Responsive Design (Mobile-First)

This page uses responsive design, meaning it looks good on all screen sizes:

- No prefix (e.g., `text-5xl`) = applies to all screen sizes
- `md:` prefix = applies to medium screens and larger
- `lg:` prefix = applies to large screens and larger

**Example:**
```html
<!-- This heading is:
     - text-5xl on small screens (phones)
     - text-6xl on medium screens (tablets)
     - text-7xl on large screens (desktops)
-->
<h1 class="text-5xl md:text-6xl lg:text-7xl">Responsive Heading</h1>
```

### Common Modifications

#### Make a Button Larger

**Current:**
```html
<a href="http://cascadialiving.com" class="btn-primary px-8 py-3 rounded-full font-semibold">
    Get Started
</a>
```

**To make larger:**
```html
<a href="http://cascadialiving.com" class="btn-primary px-12 py-4 rounded-full font-semibold text-lg">
    Get Started
</a>
```

Changes made:
- `px-8` → `px-12` (wider horizontal padding)
- `py-3` → `py-4` (taller vertical padding)
- Added `text-lg` (larger text)

#### Adjust Section Spacing

**Current:**
```html
<section class="py-20 md:py-32 bg-[#0f172a]">
```

**To reduce spacing:**
```html
<section class="py-12 md:py-20 bg-[#0f172a]">
```

Changes made:
- `py-20` → `py-12` (less padding on small screens)
- `md:py-32` → `md:py-20` (less padding on medium+ screens)

#### Change Grid Columns

**Current (3 columns):**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**To 2 columns:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

**To 4 columns:**
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
```

### Testing Your Changes

After modifying classes:

1. **Save the file** (Ctrl+S or Cmd+S)
2. **Refresh your browser** (F5 or Cmd+R)
3. **Check different screen sizes** (open browser developer tools: F12)
4. **Test on actual devices** if possible

---

## Fixing and Updating Links

### Understanding Links in HTML

Links in HTML use the `<a>` tag. Here's the structure:

```html
<a href="https://example.com" class="styling-classes">Click Me</a>
```

- `href` = where the link goes
- Text between `>` and `</a>` = what users see and click
- `class` = styling (don't change this unless you want different styling)

### Finding All Links on the Page

Use Find & Replace (Ctrl+F) to search for `href=` to locate all links.

### Current Links That Need Updating

#### 1. External Link to Cascadia Living Website

**Location:** Multiple places throughout the page

**Current:**
```html
<a href="http://cascadialiving.com" class="btn-primary px-8 py-4 rounded-full font-bold text-lg inline-flex items-center justify-center gap-2 shadow-lg hover:shadow-xl">
    Schedule Consultation
    <i class="fas fa-arrow-right"></i>
</a>
```

**Issue:** This links to `http://cascadialiving.com`. If this isn't your actual website, update it.

**To fix:**
1. Open your text editor
2. Use Find & Replace (Ctrl+H or Cmd+H)
3. Find: `http://cascadialiving.com`
4. Replace with: Your actual website URL (e.g., `https://yourwebsite.com`)
5. Click "Replace All"

**Important:** Use `https://` not `http://` for security.

**Locations of this link:**
- Line 142: Header "Get Started" button
- Line 155: Hero section "Schedule Consultation" button
- Line 160: Hero section "Learn More" button
- Line 485: CTA section "Start Your Journey" button
- Line 490: CTA section "Get More Information" button
- Line 516: Contact section "Schedule Now" button
- Line 635: Footer "Home Buying" link
- Line 636: Footer "Home Selling" link
- Line 637: Footer "Investment Properties" link
- Line 638: Footer "Consultations" link

#### 2. Email Link

**Current:**
```html
<a href="mailto:johnson.bryce@gmail.com" class="text-[#00E5A8] hover:text-white transition-colors font-semibold">
    johnson.bryce@gmail.com
</a>
```

**To update:**
1. Find: `johnson.bryce@gmail.com`
2. Replace with: Your email address

**Locations:**
- Line 510: Contact section email link
- Line 646: Footer email link

### Navigation Links (Anchor Links)

These links jump to sections on the same page:

```html
<a href="#features" class="nav-link">Features</a>
<a href="#benefits" class="nav-link">Benefits</a>
<a href="#testimonials" class="nav-link">Testimonials</a>
<a href="#about" class="nav-link">About</a>
<a href="#contact" class="nav-link">Contact</a>
```

**How they work:**
- `href="#features"` links to an element with `id="features"`
- When clicked, the page scrolls to that section

**These are already set up correctly.** Don't change them unless you rename sections.

### Social Media Links

**Location:** Lines 656-672 (Footer)

```html
<a href="#" class="w-10 h-10 rounded-full bg-[rgba(91,75,255,0.1)] flex items-center justify-center text-[#5B4BFF] hover:bg-[#5B4BFF] hover:text-white transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**Current:** Links to `#` (does nothing)

**To add social media links:**

Replace `#` with your actual social media URLs:

```html
<!-- Facebook -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 rounded-full...">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/yourhandle" class="w-10 h-10 rounded-full...">
    <i class="fab fa-twitter"></i>
</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/in/yourprofile" class="w-10 h-10 rounded-full...">
    <i class="fab fa-linkedin-in"></i>
</a>

<!-- Instagram -->
<a href="https://instagram.com/yourprofile" class="w-10 h-10 rounded-full...">
    <i class="fab fa-instagram"></i>
</a>
```

---

## Linking Privacy and Terms Pages

### Overview

Currently, the footer links to `privacy.html`, `terms.html`, and `blog.html`, but these pages don't exist yet. We'll show you how to:

1. Create these files
2. Ensure links work properly
3. Maintain consistent styling

### Step 1: Create the Privacy Policy Page

1. **Create a new file:**
   - Open your text editor
   - Go to File → New
   - Save as `privacy.html` in the same folder as `index.html`

2. **Add this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Cascadia Living Real Estate">
    <title>Privacy Policy | Cascadia Living</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        body {
            background-color: #0f172a;
            color: #f1f5f9;
        }
        header {
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(91, 75, 255, 0.1);
        }
        .nav-link {
            color: #cbd5e1;
            transition: color 0.3s ease-out;
            font-weight: 500;
        }
        .nav-link:hover {
            color: #5B4BFF;
        }
        .gradient-primary {
            background: linear-gradient(135deg, #5B4BFF 0%, #7c3aed 100%);
        }
    </style>
</head>
<body>
    <!-- Header (Same as index.html) -->
    <header class="sticky top-0 z-50 w-full">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-lg gradient-primary flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-white hidden sm:inline">Cascadia Living</span>
            </div>
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html" class="nav-link">Home</a>
                <a href="privacy.html" class="nav-link">Privacy</a>
                <a href="terms.html" class="nav-link">Terms</a>
                <a href="blog.html" class="nav-link">Blog</a>
            </div>
        </nav>
    </header>

    <!-- Content -->
    <section class="py-20 md:py-32">
        <div class="max-w-4xl mx-auto px-8 md:px-16">
            <h1 class="text-4xl md:text-5xl font-bold text-white mb-8">Privacy Policy</h1>
            
            <div class="space-y-8 text-slate-300">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Introduction</h2>
                    <p>
                        At Cascadia Living, we are committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Information We Collect</h2>
                    <p>
                        We may collect information about you in a variety of ways. The information we may collect on the site includes:
                    </p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>Name</li>
                        <li>Email address</li>
                        <li>Phone number</li>
                        <li>Message content</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">How We Use Your Information</h2>
                    <p>
                        Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the site to:
                    </p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>Respond to your inquiries and fulfill your requests</li>
                        <li>Send you marketing and promotional communications</li>
                        <li>Improve our website and services</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Contact Us</h2>
                    <p>
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        Email: <a href="mailto:johnson.bryce@gmail.com" class="text-[#00E5A8] hover:text-white">johnson.bryce@gmail.com</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-[#0a0f1f] border-t border-[rgba(91,75,255,0.1)] py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-8 md:px-16">
            <div class="text-center border-t border-[rgba(91,75,255,0.1)] pt-8">
                <p class="text-slate-400 text-sm">
                    &copy; 2025 Cascadia Living. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

1. **Create a new file:**
   - File → New
   - Save as `terms.html` in the same folder as `index.html`

2. **Add this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Cascadia Living Real Estate">
    <title>Terms of Service | Cascadia Living</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        body {
            background-color: #0f172a;
            color: #f1f5f9;
        }
        header {
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(91, 75, 255, 0.1);
        }
        .nav-link {
            color: #cbd5e1;
            transition: color 0.3s ease-out;
            font-weight: 500;
        }
        .nav-link:hover {
            color: #5B4BFF;
        }
        .gradient-primary {
            background: linear-gradient(135deg, #5B4BFF 0%, #7c3aed 100%);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="sticky top-0 z-50 w-full">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-lg gradient-primary flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-white hidden sm:inline">Cascadia Living</span>
            </div>
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html" class="nav-link">Home</a>
                <a href="privacy.html" class="nav-link">Privacy</a>
                <a href="terms.html" class="nav-link">Terms</a>
                <a href="blog.html" class="nav-link">Blog</a>
            </div>
        </nav>
    </header>

    <!-- Content -->
    <section class="py-20 md:py-32">
        <div class="max-w-4xl mx-auto px-8 md:px-16">
            <h1 class="text-4xl md:text-5xl font-bold text-white mb-8">Terms of Service</h1>
            
            <div class="space-y-8 text-slate-300">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on Cascadia Living's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Disclaimer</h2>
                    <p>
                        The materials on Cascadia Living's website are provided on an 'as is' basis. Cascadia Living makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Limitations</h2>
                    <p>
                        In no event shall Cascadia Living or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Cascadia Living's website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Contact Us</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        Email: <a href="mailto:johnson.bryce@gmail.com" class="text-[#00E5A8] hover:text-white">johnson.bryce@gmail.com</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-[#0a0f1f] border-t border-[rgba(91,75,255,0.1)] py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-8 md:px-16">
            <div class="text-center border-t border-[rgba(91,75,255,0.1)] pt-8">
                <p class="text-slate-400 text-sm">
                    &copy; 2025 Cascadia Living. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Create a Blog Page (Optional)

If you want a blog page, follow the same process:

1. **Create `blog.html`**
2. **Add similar header and footer**
3. **Add blog post sections**

### Step 4: Verify Links in index.html

Now let's make sure the footer links in `index.html` are correct.

**Current footer links (around lines 642-648):**

```html
<li><a href="privacy.html" class="text-slate-400 hover:text-[#00E5A8] transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-slate-400 hover:text-[#00E5A8] transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-slate-400 hover:text-[#00E5A8] transition-colors duration-300">Blog</a></li>
<li><a href="#contact" class="text-slate-400 hover:text-[#00E5A8] transition-colors duration-300">Contact Us</a></li>
```

**These are already correct!** They link to:
- `privacy.html` (the file you created)
- `terms.html` (the file you created)
- `blog.html` (optional blog page)

### Step 5: Add Links to Return to Home

In the policy pages we created, there's a link back to the home page:

```html
<a href="index.html" class="nav-link">Home</a>
```

This allows users to navigate back to the main landing page.

### Step 6: Update Footer Links in New Pages

In the `privacy.html` and `terms.html` files we created, update the footer to match your actual links:

**Current:**
```html
<p class="text-slate-400 text-sm">
    &copy; 2025 Cascadia Living. All rights reserved.
</p>
```

**You can add:**
```html
<div class="flex flex-col md:flex-row items-center justify-between gap-4">
    <p class="text-slate-400 text-sm">
        &copy; 2025 Cascadia Living. All rights reserved.
    </p>
    <div class="flex gap-6">
        <a href="privacy.html" class="text-slate-400 hover:text-[#00E5A8] text-sm">Privacy</a>
        <a href="terms.html" class="text-slate-400 hover:text-[#00E5A8] text-sm">Terms</a>
        <a href="index.html" class="text-slate-400 hover:text-[#00E5A8] text-sm">Home</a>
    </div>
</div>
```

### File Structure After Setup

Your project should now look like:

```
project-folder/
├── index.html          ✓ Main landing page (already exists)
├── privacy.html        ✓ Privacy policy (newly created)
├── terms.html          ✓ Terms of service (newly created)
└── blog.html           ✓ Blog page (optional, newly created)
```

---

## Color Customization

The page uses a custom color scheme defined at the top of the HTML. You can easily change these colors.

### Color Variables

**Location:** Lines 15-20

```html
<style>
    :root {
        --primary: #5B4BFF;      /* Purple - main brand color */
        --secondary: #EEF0FF;    /* Light purple - backgrounds */
        --accent: #00E5A8;       /* Green/teal - highlights */
    }
</style>
```

### Understanding Hex Colors

Hex colors are 6-character codes that represent colors:
- `#5B4BFF` = Purple
- `#00E5A8` = Green/Teal
- `#ffffff` = White
- `#000000` = Black

To find hex color codes, use:
- [Coolors.co](https://coolors.co)
- [Color-Hex.com](https://www.color-hex.com)
- Your browser's built-in color picker

### Changing the Primary Color (Purple)

**Current:**
```html
--primary: #5B4BFF;
```

**To change to blue:**
```html
--primary: #3B82F6;
```

**Where this color is used:**
- Logo background
- Button backgrounds
- Text highlights
- Border colors
- Gradient overlays

### Changing the Accent Color (Green)

**Current:**
```html
--accent: #00E5A8;
```

**To change to orange:**
```html
--accent: #FF6B35;
```

**Where this color is used:**
- Checkmarks in feature lists
- Hover effects
- Text links
- Icon colors

### Changing the Background Color

**Current:**
```html
body {
    background-color: #0f172a;  /* Very dark blue */
    color: #f1f5f9;             /* Light text */
}
```

**To change to a lighter background:**
```html
body {
    background-color: #f8f9fa;  /* Light gray */
    color: #1a1a1a;             /* Dark text */
}
```

### Gradient Colors

The page uses gradients in several places:

```html
.gradient-primary {
    background: linear-gradient(135deg, #5B4BFF 0%, #7c3aed 100%);
}
```

**To change the gradient:**
1. Find the gradient definition
2. Change the hex colors
3. The `135deg` controls the direction (135 degrees = diagonal)

**Direction options:**
- `90deg` = left to right
- `180deg` = top to bottom
- `270deg` = right to left
- `45deg` = diagonal (bottom-left to top-right)
- `135deg` = diagonal (top-left to bottom-right)

### Example: Complete Color Scheme Change

**From purple/green to blue/orange:**

Find and replace:
- `#5B4BFF` → `#3B82F6` (purple → blue)
- `#7c3aed` → `#2563EB` (purple → darker blue)
- `#00E5A8` → `#FF6B35` (green → orange)
- `#10b981` → `#EA580C` (green → darker orange)

---

## Troubleshooting Common Issues

### Issue 1: Links Don't Work

**Problem:** Clicking a link does nothing or gives an error.

**Solutions:**

1. **Check the file path:**
   ```html
   <!-- Wrong: file is in a subfolder but link doesn't specify it -->
   <a href="privacy.html">Privacy</a>  <!-- Won't find it if privacy.html is in a subfolder -->
   
   <!-- Right: specify the subfolder -->
   <a href="pages/privacy.html">Privacy</a>
   ```

2. **Check for typos:**
   - Make sure filenames match exactly (including .html)
   - File names are case-sensitive on some servers
   - Use lowercase filenames: `privacy.html` not `Privacy.html`

3. **External links need https://**
   ```html
   <!-- Wrong -->
   <a href="cascadialiving.com">Visit Site</a>
   
   <!-- Right -->
   <a href="https://cascadialiving.com">Visit Site</a>
   ```

4. **Test in browser:**
   - Right-click the link
   - Select "Inspect" or "Inspect Element"
   - Look at the href value in the code

### Issue 2: Text Looks Broken or Overlaps

**Problem:** Text is overlapping other content or looks distorted.

**Solutions:**

1. **Check responsive classes:**
   ```html
   <!-- Make sure you have responsive sizing -->
   <h1 class="text-5xl md:text-6xl lg:text-7xl">
   ```

2. **Verify padding/margin:**
   ```html
   <!-- If text is too crowded, increase spacing -->
   <div class="p-4 md:p-8">Text here</div>
   ```

3. **Check line height:**
   ```html
   <!-- Add leading class for better spacing -->
   <p class="leading-relaxed">Your text here</p>
   ```

### Issue 3: Colors Look Wrong

**Problem:** Colors don't match what you expected.

**Solutions:**

1. **Clear browser cache:**
   - Press Ctrl+Shift+Delete (Windows) or Cmd+Shift+Delete (Mac)
   - Select "Cached images and files"
   - Click "Clear"

2. **Hard refresh:**
   - Press Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)

3. **Check hex code format:**
   ```html
   <!-- Wrong: missing # -->
   <div class="bg-[5B4BFF]">
   
   <!-- Right: include # -->
   <div class="bg-[#5B4BFF]">
   ```

4. **Verify color is applied to right element:**
   ```html
   <!-- Color on text -->
   <p class="text-white">White text</p>
   
   <!-- Color on background -->
   <div class="bg-white">White background</div>
   ```

### Issue 4: Mobile Version Looks Bad

**Problem:** The page doesn't look good on phones.

**Solutions:**

1. **Check responsive classes:**
   ```html
   <!-- Must have mobile-first design -->
   <div class="text-sm md:text-base lg:text-lg">
   ```

2. **Test in browser DevTools:**
   - Press F12 to open DevTools
   - Click the phone icon in the top-left
   - Select a device (iPhone, Android, etc.)

3. **Check breakpoints:**
   - `md:` = 768px and above (tablets)
   - `lg:` = 1024px and above (desktops)
   - No prefix = all screen sizes

### Issue 5: Form Not Submitting

**Problem:** Contact form doesn't send messages.

**Solutions:**

1. **Check Web3Forms API key:**
   ```html
   <!-- Around line 545 -->
   <input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
   ```
   
   This should have your actual API key, not "YOUR_WEB3FORMS_ACCESS_KEY"

2. **Get your API key:**
   - Go to [web3forms.com](https://web3forms.com)
   - Sign up for a free account
   - Get your access key
   - Replace the placeholder

3. **Verify required fields:**
   ```html
   <!-- These fields have "required" attribute -->
   <input type="text" name="name" required>
   <input type="email" name="email" required>
   <textarea name="message" required></textarea>
   ```

4. **Check browser console for errors:**
   - Press F12
   - Click "Console" tab
   - Look for error messages in red

### Issue 6: Images Not Loading

**Problem:** Images show broken image icons.

**Solutions:**

1. **Check image URLs:**
   ```html
   <!-- Current: uses external URLs from unsplash -->
   <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=600&fit=crop" alt="Real estate team">
   ```

2. **To use local images:**
   - Save image to your project folder
   - Update the src:
   ```html
   <!-- Place image.jpg in your project folder -->
   <img src="image.jpg" alt="Description">
   ```

3. **Always include alt text:**
   ```html
   <!-- Good: describes the image -->
   <img src="photo.jpg" alt="Team members discussing real estate">
   
   <!-- Bad: missing alt text -->
   <img src="photo.jpg">
   ```

### Issue 7: Buttons Don't Look Right

**Problem:** Buttons have wrong colors, size, or styling.

**Solutions:**

1. **Check button classes:**
   ```html
   <!-- Primary button (blue) -->
   <a href="#" class="btn-primary px-8 py-4">Click Me</a>
   
   <!-- Outline button (hollow) -->
   <a href="#" class="btn-outline px-8 py-4">Click Me</a>
   ```

2. **Adjust size:**
   ```html
   <!-- Smaller button -->
   <a class="btn-primary px-4 py-2">Small</a>
   
   <!-- Larger button -->
   <a class="btn-primary px-12 py-6">Large</a>
   ```

3. **Check hover state:**
   - Hover over button
   - It should change color and scale up slightly
   - If not, check browser console (F12) for errors

### Issue 8: Mobile Menu Not Working

**Problem:** Mobile menu button doesn't open the menu.

**Solutions:**

1. **Check JavaScript is enabled:**
   - Look at browser console (F12)
   - Check for JavaScript errors (red text)

2. **Verify mobile menu HTML:**
   ```html
   <!-- Should have both button and menu -->
   <button class="mobile-menu-button md:hidden">
       <i class="fas fa-bars"></i>
   </button>
   
   <div class="mobile-menu hidden">
       <!-- Menu content here -->
   </div>
   ```

3. **Test on actual mobile device:**
   - Desktop browser mobile view may behave differently
   - Test on real phone if possible

### Issue 9: Page Not Scrolling Smoothly

**Problem:** Anchor links jump instantly instead of scrolling smoothly.

**Solutions:**

1. **Check smooth-scroll class:**
   ```html
   <!-- Should be on body tag -->
   <body class="smooth-scroll">
   ```

2. **Verify scroll-behavior CSS:**
   ```html
   <style>
       .smooth-scroll {
           scroll-behavior: smooth;
       }
   </style>
   ```

3. **Test with browser DevTools:**
   - Some browsers may not support smooth scroll
   - Try different browser if issue persists

### Issue 10: Custom Fonts Not Loading

**Problem:** Text doesn't look like it should.

**Solutions:**

1. **Check Google Fonts link:**
   ```html
   <!-- Should be in <head> section -->
   <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
   ```

2. **Verify font-family CSS:**
   ```html
   <style>
       * {
           font-family: 'Inter', sans-serif;
       }
   </style>
   ```

3. **Check internet connection:**
   - Google Fonts requires internet
   - Offline pages won't load custom fonts

4. **Clear cache and reload:**
   - Press Ctrl+Shift+Delete
   - Clear cached images and files
   - Reload page

---

## Quick Reference: Common Tasks

### Update Company Name
1. Find: `Cascadia Living`
2. Replace with: Your company name
3. Update in: Header, Hero, About, Footer

### Update Email
1. Find: `johnson.bryce@gmail.com`
2. Replace with: Your email
3. Update in: Contact section, Footer

### Update Website URL
1. Find: `http://cascadialiving.com`
2. Replace with: Your website URL (use `https://`)
3. Update in: All buttons and links

### Change Primary Color (Purple)
1. Find: `#5B4BFF`
2. Replace with: Your hex color code
3. Locations: CSS variables, gradients, button styles

### Change Accent Color (Green)
1. Find: `#00E5A8`
2. Replace with: Your hex color code
3. Locations: Checkmarks, highlights, hover effects

### Add New Testimonial
1. Copy entire testimonial card (from `<div class="testimonial-card">` to `</div>`)
2. Paste after last testimonial
3. Update: Quote, name, and role

### Update Statistics
1. Find numbers in Benefits section
2. Replace: `500+`, `$2B+`, `98%`
3. Update corresponding labels below

### Add Social Media Links
1. Find social media links in footer (around line 656)
2. Replace `href="#"` with actual social media URLs
3. Example: `href="https://facebook.com/yourpage"`

---

## Best Practices

### 1. Always Back Up Before Making Changes
- Save a copy of `index.html` before editing
- Name it `index.html.backup`
- If something breaks, you can restore it

### 2. Test After Every Change
- Save file (Ctrl+S)
- Refresh browser (F5)
- Check desktop and mobile views

### 3. Use Find & Replace Carefully
- Use "Find" first to see all occurrences
- Use "Replace All" only when sure
- Double-check the search term

### 4. Keep File Names Consistent
- Use lowercase: `privacy.html` not `Privacy.html`
- Use hyphens for spaces: `my-page.html` not `my page.html`
- No special characters except hyphens

### 5. Maintain Responsive Design
- Always include mobile (`text-sm`) and desktop (`md:text-base`) sizes
- Test on multiple screen sizes
- Use DevTools mobile view (F12)

### 6. Keep Styling Consistent
- Use same color scheme throughout
- Maintain consistent spacing (padding/margin)
- Use same font sizes for similar elements

### 7. Optimize Images
- Compress images before uploading
- Use appropriate file formats (JPG for photos, PNG for graphics)
- Include descriptive alt text

### 8. Test All Links
- Click every link on the page
- Verify external links open in new tab (if desired)
- Test email links (they should open email client)

---

## Getting Help

### If Something Breaks

1. **Check the browser console:**
   - Press F12
   - Click "Console" tab
   - Red text = errors

2. **Use browser DevTools:**
   - Right-click element
   - Select "Inspect" or "Inspect Element"
   - Look at HTML and CSS

3. **Undo your changes:**
   - Ctrl+Z (undo) multiple times
   - Or restore from backup

4. **Search online:**
   - Copy error message into Google
   - Add "Tailwind CSS" or "HTML" to search

### Resources

- **Tailwind CSS Documentation:** [tailwindcss.com/docs](https://tailwindcss.com/docs)
- **HTML Tutorial:** [w3schools.com/html](https://www.w3schools.com/html)
- **Color Picker:** [coolors.co](https://coolors.co)
- **Font Awesome Icons:** [fontawesome.com](https://fontawesome.com)
- **Web3Forms:** [web3forms.com](https://web3forms.com)

---

## Summary

You now have a complete guide to maintaining and customizing the Cascadia Living landing page. Remember:

✅ **Always back up before making changes**
✅ **Test after every modification**
✅ **Use Find & Replace carefully**
✅ **Keep responsive design in mind**
✅ **Update all necessary links and contact info**
✅ **Maintain consistent styling**

Good luck with your landing page! If you have questions, refer back to this guide or consult the resources listed above.