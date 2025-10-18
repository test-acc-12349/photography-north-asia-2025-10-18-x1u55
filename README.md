# Photography North Asia Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Troubleshooting Common Issues](#troubleshooting-common-issues)
7. [Best Practices](#best-practices)

---

## Overview

This landing page is built with:
- **HTML5** - Structure and content
- **Tailwind CSS** - Styling framework (loaded via CDN)
- **Custom CSS** - Animations and special effects
- **JavaScript** - Mobile menu toggle and accordion functionality

### File Structure
```
project-folder/
├── index.html (main landing page)
├── privacy.html (to be created)
├── terms.html (to be created)
└── styles/ (optional - for custom CSS)
```

---

## Updating Text Content

### Understanding the HTML Structure

The landing page is divided into sections. Each section contains text that you can easily modify without affecting the design.

### 1. **Announcement Bar** (Top Banner)

**Location:** Lines 79-83

**Current text:**
```html
<p class="text-sm md:text-base font-medium text-center">🚚 Free Worldwide Shipping on Orders Over $50</p>
```

**How to update:**
1. Open `index.html` in your text editor
2. Find the line containing `🚚 Free Worldwide Shipping on Orders Over $50`
3. Replace the text inside the `<p>` tags while keeping the emoji if desired
4. Save the file

**Example:**
```html
<!-- Before -->
<p class="text-sm md:text-base font-medium text-center">🚚 Free Worldwide Shipping on Orders Over $50</p>

<!-- After -->
<p class="text-sm md:text-base font-medium text-center">🎉 New Summer Collection Now Available!</p>
```

**Important:** Keep the `class="text-sm md:text-base font-medium text-center"` exactly as is. These are styling instructions that make the text look good.

---

### 2. **Navigation Menu** (Header)

**Location:** Lines 104-109

**Current links:**
```html
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Benefits</a>
<a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">FAQ</a>
<a href="#testimonials" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Reviews</a>
```

**How to update menu text:**
1. Locate the navigation section in the header (desktop menu)
2. Change the text between `>` and `</a>` tags
3. Do NOT change the `href="#"` part - these link to sections on the page

**Example:**
```html
<!-- Before -->
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Features</a>

<!-- After -->
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Our Products</a>
```

**Note:** The same menu appears twice in the code:
- **Desktop version** (lines 104-109) - visible on large screens
- **Mobile version** (lines 137-142) - visible on phones/tablets
- Update both for consistency

---

### 3. **Logo/Brand Name** (Header)

**Location:** Lines 93-98

**Current text:**
```html
<a href="#" class="text-2xl md:text-3xl font-bold text-gray-900 tracking-tight">
    <span class="bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-transparent">Photo</span>
    <span class="text-gray-900">NA</span>
</a>
```

**How to update:**
1. Find the logo section in the header
2. Replace `Photo` and `NA` with your brand name
3. You can split it into two parts (like `Photo` + `NA`) or use one part for both

**Example:**
```html
<!-- Before -->
<span class="bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-transparent">Photo</span>
<span class="text-gray-900">NA</span>

<!-- After -->
<span class="bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-transparent">LENS</span>
<span class="text-gray-900">PRO</span>
```

---

### 4. **Hero Section** (Large Banner with Image)

**Location:** Lines 166-185

**Current text:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-4 md:mb-6 leading-tight tracking-tight">
    Photography North Asia
</h1>
<p class="text-lg md:text-xl lg:text-2xl text-gray-100 mb-8 md:mb-10 font-light leading-relaxed">
    Best Photography Kit In North Asia
</p>
```

**How to update:**
1. Locate the hero section (the large banner at the top)
2. Update the main heading (h1) - this is the most prominent text
3. Update the subtitle (p) - the smaller text below
4. Keep all the `class="..."` attributes exactly as they are

**Example:**
```html
<!-- Before -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-4 md:mb-6 leading-tight tracking-tight">
    Photography North Asia
</h1>
<p class="text-lg md:text-xl lg:text-2xl text-gray-100 mb-8 md:mb-10 font-light leading-relaxed">
    Best Photography Kit In North Asia
</p>

<!-- After -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-4 md:mb-6 leading-tight tracking-tight">
    Professional Camera Equipment Store
</h1>
<p class="text-lg md:text-xl lg:text-2xl text-gray-100 mb-8 md:mb-10 font-light leading-relaxed">
    Premium Gear for Every Photographer
</p>
```

---

### 5. **Features Section** (Three Cards)

**Location:** Lines 206-308

**Card 1 - LED Lighting**
```html
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">LED Lighting</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Professional-grade LED lighting systems for perfect illumination...
</p>
```

**How to update feature cards:**
1. Find each feature card (there are 3 total)
2. Update the heading (h3) with your feature name
3. Update the description paragraph (p) with your feature details
4. Update the bullet points in the list below

**Example:**
```html
<!-- Before -->
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">LED Lighting</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Professional-grade LED lighting systems for perfect illumination in any environment. 
    Adjustable color temperature and brightness for complete creative control.
</p>

<!-- After -->
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">Studio Lighting Kits</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Complete lighting solutions with everything you need to start your studio. 
    Easy setup and professional results for all skill levels.
</p>
```

**Updating bullet points:**
```html
<!-- Before -->
<li class="flex items-center gap-2">
    <svg class="w-4 h-4 text-yellow-600" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
    </svg>
    Color Temperature Control
</li>

<!-- After -->
<li class="flex items-center gap-2">
    <svg class="w-4 h-4 text-yellow-600" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
    </svg>
    Wireless Remote Control
</li>
```

**Keep the SVG code as is** - it creates the checkmark icon. Only change the text after the closing `</svg>` tag.

---

### 6. **Benefits Section** (Three Large Sections)

**Location:** Lines 333-520

**Benefit 1 - Free Delivery**
```html
<h3 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 mb-4 leading-tight">
    Free Delivery
</h3>
<p class="text-gray-600 text-base md:text-lg leading-relaxed mb-6">
    Enjoy complimentary shipping on all orders...
</p>
```

**How to update:**
1. Find each benefit section (there are 3)
2. Update the heading (h3)
3. Update the main description (p)
4. Update the bullet points with benefits

**Example:**
```html
<!-- Before -->
<h3 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 mb-4 leading-tight">
    Free Delivery
</h3>

<!-- After -->
<h3 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 mb-4 leading-tight">
    Complimentary Shipping Worldwide
</h3>
```

---

### 7. **FAQ Section** (Expandable Questions)

**Location:** Lines 576-695

**Current structure:**
```html
<button class="w-full px-6 md:px-8 py-4 md:py-5 flex items-center justify-between bg-white hover:bg-gray-50 transition duration-300" onclick="toggleAccordion(this)" aria-expanded="false">
    <span class="text-left font-semibold text-gray-900 text-base md:text-lg">What is the warranty on your products?</span>
    ...
</button>
<div class="accordion-content px-6 md:px-8 pb-4 md:pb-5 bg-gray-50">
    <p class="text-gray-600 leading-relaxed">
        All our products come with a full manufacturer's warranty...
    </p>
</div>
```

**How to update FAQ:**
1. Find the question text in the `<span>` tag
2. Update the question text
3. Find the answer text in the `<p>` tag below
4. Update the answer text

**Example:**
```html
<!-- Before -->
<span class="text-left font-semibold text-gray-900 text-base md:text-lg">What is the warranty on your products?</span>

<!-- After -->
<span class="text-left font-semibold text-gray-900 text-base md:text-lg">What payment methods do you accept?</span>
```

**Note:** Keep the `onclick="toggleAccordion(this)"` exactly as is - this makes the accordion expand/collapse.

---

### 8. **Testimonials Section** (Customer Reviews)

**Location:** Lines 721-850

**Current structure:**
```html
<p class="text-gray-600 leading-relaxed mb-6">
    "The LED lighting system from Photography North Asia has completely transformed my studio setup..."
</p>
<div class="flex items-center gap-3">
    <div class="w-12 h-12 bg-gradient-to-br from-blue-400 to-blue-600 rounded-full flex items-center justify-center text-white font-bold">
        JC
    </div>
    <div>
        <p class="font-semibold text-gray-900">Jessica Chen</p>
        <p class="text-sm text-gray-600">Professional Photographer</p>
    </div>
</div>
```

**How to update testimonials:**
1. Find each testimonial (there are 3)
2. Update the review text in the `<p>` tag
3. Update the initials (JC, MK, etc.)
4. Update the customer name
5. Update the customer title/profession

**Example:**
```html
<!-- Before -->
<p class="text-gray-600 leading-relaxed mb-6">
    "The LED lighting system from Photography North Asia has completely transformed my studio setup. The color accuracy is incredible, and the free delivery made it even better. Highly recommended!"
</p>
<p class="font-semibold text-gray-900">Jessica Chen</p>
<p class="text-sm text-gray-600">Professional Photographer</p>

<!-- After -->
<p class="text-gray-600 leading-relaxed mb-6">
    "Outstanding quality and customer service! I received my order within 3 days and everything was perfectly packaged. Best purchase I've made for my photography business."
</p>
<p class="font-semibold text-gray-900">Sarah Martinez</p>
<p class="text-sm text-gray-600">Wedding Photographer</p>
```

---

## Modifying Tailwind CSS Classes

### What Are Tailwind Classes?

Tailwind CSS is a system of pre-made styling "classes" that you apply to HTML elements. Instead of writing CSS code, you use class names like `text-white`, `bg-blue-600`, etc.

**Example:**
```html
<p class="text-white bg-blue-600 p-4 rounded-lg">This text is white on a blue background</p>
```

### Common Tailwind Classes Used in This Landing Page

| Class | What It Does | Examples |
|-------|-------------|----------|
| `text-` | Text color | `text-white`, `text-gray-900`, `text-blue-600` |
| `bg-` | Background color | `bg-white`, `bg-gray-50`, `bg-gray-900` |
| `text-` (size) | Font size | `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl` |
| `font-` | Font weight | `font-light`, `font-medium`, `font-bold` |
| `p-`, `px-`, `py-` | Padding (spacing inside) | `p-4`, `px-6`, `py-3` |
| `m-`, `mb-`, `mt-` | Margin (spacing outside) | `m-4`, `mb-6`, `mt-8` |
| `rounded-` | Corner roundness | `rounded-lg`, `rounded-xl` |
| `shadow-` | Drop shadow | `shadow-sm`, `shadow-lg` |
| `hover:` | Hover effect | `hover:bg-gray-800`, `hover:text-gray-900` |
| `md:`, `lg:` | Responsive design | `md:text-2xl`, `lg:px-8` |

### Understanding Responsive Design

This landing page uses **responsive design**, which means it looks good on phones, tablets, and computers.

**Breakpoint prefixes:**
- No prefix (e.g., `text-lg`) = applies on all screen sizes
- `md:` (e.g., `md:text-2xl`) = applies on medium screens and larger (tablets and up)
- `lg:` (e.g., `lg:text-3xl`) = applies on large screens and larger (desktops and up)

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Photography North Asia
</h1>
```

This means:
- On phones: text size 4xl
- On tablets: text size 5xl
- On desktops: text size 6xl

---

### Practical Examples: Modifying Styles

#### Example 1: Changing Button Color

**Current button (Hero section):**
```html
<a href="https://ledx.com" class="bg-white text-gray-900 px-8 md:px-10 py-3 md:py-4 rounded-lg font-bold text-base md:text-lg hover:bg-gray-100 transform transition duration-300 hover:scale-105 shadow-lg">
    Explore Collection
</a>
```

**To change from white background to blue:**
```html
<!-- Before -->
<a href="https://ledx.com" class="bg-white text-gray-900 ...">

<!-- After -->
<a href="https://ledx.com" class="bg-blue-600 text-white ...">
```

**What changed:**
- `bg-white` → `bg-blue-600` (white background to blue background)
- `text-gray-900` → `text-white` (dark text to white text)
- `hover:bg-gray-100` → `hover:bg-blue-700` (hover effect matches new color)

---

#### Example 2: Changing Section Background Color

**Current features section:**
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

**To change to light gray background:**
```html
<!-- Before -->
<section id="features" class="py-16 md:py-24 bg-white">

<!-- After -->
<section id="features" class="py-16 md:py-24 bg-gray-50">
```

---

#### Example 3: Changing Text Color and Size

**Current heading:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Premium Photography Equipment
</h2>
```

**To make it larger and blue:**
```html
<!-- Before -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">

<!-- After -->
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-blue-600 mb-4 tracking-tight">
```

**What changed:**
- `text-3xl md:text-4xl lg:text-5xl` → `text-4xl md:text-5xl lg:text-6xl` (larger on all screen sizes)
- `text-gray-900` → `text-blue-600` (dark gray to blue)

---

#### Example 4: Adjusting Spacing (Padding/Margin)

**Current feature card:**
```html
<div class="hover-lift bg-white border border-gray-200 rounded-xl p-6 md:p-8 transition duration-300">
```

**To add more internal spacing:**
```html
<!-- Before -->
<div class="hover-lift bg-white border border-gray-200 rounded-xl p-6 md:p-8 transition duration-300">

<!-- After -->
<div class="hover-lift bg-white border border-gray-200 rounded-xl p-8 md:p-12 transition duration-300">
```

**What changed:**
- `p-6 md:p-8` → `p-8 md:p-12` (more padding inside the card)

---

### Color Reference

**Gray shades (most common):**
- `text-gray-900` - Dark gray/black (text)
- `text-gray-700` - Medium gray (text)
- `text-gray-600` - Lighter gray (text)
- `bg-white` - White background
- `bg-gray-50` - Very light gray background
- `bg-gray-900` - Dark gray/black background

**Accent colors:**
- `text-yellow-600`, `bg-yellow-100` - Yellow
- `text-blue-600`, `bg-blue-100` - Blue
- `text-purple-600`, `bg-purple-100` - Purple
- `text-green-600` - Green

---

### Text Size Reference

From smallest to largest:
- `text-sm` - Small (12px)
- `text-base` - Normal (16px)
- `text-lg` - Large (18px)
- `text-xl` - Extra large (20px)
- `text-2xl` - 2x large (24px)
- `text-3xl` - 3x large (30px)
- `text-4xl` - 4x large (36px)
- `text-5xl` - 5x large (48px)
- `text-6xl` - 6x large (60px)

---

## Fixing Broken Links

### Understanding Links

A link in HTML looks like this:
```html
<a href="https://example.com" class="...">Click here</a>
```

**Parts:**
- `<a>` - Opening link tag
- `href="https://example.com"` - Where the link goes
- `class="..."` - Styling (don't change)
- `Click here` - Text that appears to users
- `</a>` - Closing link tag

---

### Links in This Landing Page

#### 1. **Navigation Links** (Top Menu)

**Location:** Lines 104-109 (desktop) and 137-142 (mobile)

**Current links:**
```html
<a href="#features" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Benefits</a>
<a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">FAQ</a>
<a href="#testimonials" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Reviews</a>
```

**Status:** ✅ These are **internal links** (they link to sections on the same page using `#section-id`). They should work fine.

**To verify they work:**
1. Click each navigation item
2. The page should scroll to that section
3. If it doesn't scroll, check that the section has a matching `id` attribute

**Example - Feature section should have:**
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

---

#### 2. **Shop Now Buttons**

**Location:** Multiple locations (lines 113, 189, 197, 360, 430, 500, 548)

**Current links:**
```html
<a href="https://ledx.com" class="bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-gray-800 transform transition duration-300 hover:scale-105">Shop Now</a>
```

**Status:** ⚠️ These link to `https://ledx.com`. You need to update this to your actual website.

**How to fix:**
1. Find all instances of `href="https://ledx.com"`
2. Replace with your actual website URL
3. Use Ctrl+H (Cmd+H on Mac) to find and replace all at once

**Step-by-step:**
1. Open `index.html` in your text editor
2. Press **Ctrl+H** (or **Cmd+H** on Mac)
3. In "Find" field, type: `https://ledx.com`
4. In "Replace" field, type: `https://yourwebsite.com`
5. Click "Replace All"

**Example:**
```html
<!-- Before -->
<a href="https://ledx.com" class="...">Shop Now</a>

<!-- After -->
<a href="https://mystore.com" class="...">Shop Now</a>
```

---

#### 3. **Contact Email Links**

**Location:** Lines 548 and 695

**Current links:**
```html
<a href="mailto:adminx@led.com" class="...">Contact Us</a>
```

**Status:** ⚠️ These use `adminx@led.com`. Update to your email address.

**How to fix:**
1. Find all instances of `mailto:adminx@led.com`
2. Replace with your email address
3. Keep `mailto:` at the beginning

**Example:**
```html
<!-- Before -->
<a href="mailto:adminx@led.com" class="...">Contact Us</a>

<!-- After -->
<a href="mailto:info@mystore.com" class="...">Contact Us</a>
```

---

#### 4. **All External Links - Complete List**

Use this checklist to fix all links:

| Link | Current Value | Status | Action |
|------|---------------|--------|--------|
| Shop Now buttons | `https://ledx.com` | ⚠️ Broken | Replace with your website |
| Contact Us links | `mailto:adminx@led.com` | ⚠️ Broken | Replace with your email |
| Logo link | `href="#"` | ⚠️ Broken | Replace with your homepage |
| Navigation links | `href="#features"` etc. | ✅ OK | No action needed |

---

### Fixing the Logo Link

**Location:** Lines 93-98

**Current:**
```html
<a href="#" class="text-2xl md:text-3xl font-bold text-gray-900 tracking-tight">
    <span class="bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-transparent">Photo</span>
    <span class="text-gray-900">NA</span>
</a>
```

**The `href="#"` is broken.** Change it to link to your homepage:

```html
<!-- Before -->
<a href="#" class="...">

<!-- After -->
<a href="https://mystore.com" class="...">
```

Or if you want it to scroll to top:
```html
<a href="/" class="...">
```

---

### Step-by-Step: Fix All Links at Once

**Best Practice - Use Find & Replace:**

1. **Open your text editor** (VS Code, Sublime Text, Notepad++, etc.)
2. **Open index.html**
3. **Press Ctrl+H** (or Cmd+H on Mac) to open Find & Replace
4. **Replace `https://ledx.com`:**
   - Find: `https://ledx.com`
   - Replace with: `https://yourwebsite.com`
   - Click "Replace All"

5. **Replace the email:**
   - Find: `adminx@led.com`
   - Replace with: `youremail@yourcompany.com`
   - Click "Replace All"

6. **Fix the logo link manually:**
   - Find: `<a href="#"` (in the logo section)
   - Change to: `<a href="https://yourwebsite.com"`

7. **Save the file** (Ctrl+S or Cmd+S)

---

### Testing Your Links

After fixing links, test each one:

1. **Navigation links** - Click each menu item, page should scroll to section
2. **Shop Now buttons** - Should open your website
3. **Contact Us** - Should open your email client
4. **Logo** - Should go to your homepage

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

Privacy and Terms pages are legally important for any website that:
- Collects customer information
- Processes orders
- Uses cookies or analytics
- Operates in the EU, UK, or California

### Creating the Files

#### Step 1: Create `privacy.html`

Create a new file called `privacy.html` in the same folder as `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Photography North Asia">
    <title>Privacy Policy - Photography North Asia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16 md:h-20">
                <div class="flex items-center">
                    <a href="index.html" class="text-2xl md:text-3xl font-bold text-gray-900 tracking-tight">
                        <span class="bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-transparent">Photo</span>
                        <span class="text-gray-900">NA</span>
                    </a>
                </div>
                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Benefits</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">FAQ</a>
                    <a href="index.html#testimonials" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Reviews</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24">
        <div class="max-w-4xl mx-auto px-4 md:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <p>
                    <strong>Last Updated:</strong> [DATE]
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>
                    Photography North Asia ("we," "us," "our," or "Company") is committed to protecting your privacy. 
                    This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you 
                    visit our website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information We Collect</h2>
                <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Personal Data: Name, email address, phone number, shipping address, billing address</li>
                    <li>Payment Information: Credit card details (processed securely through payment processors)</li>
                    <li>Device Information: Browser type, IP address, operating system</li>
                    <li>Usage Data: Pages visited, time spent on pages, links clicked</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. How We Use Your Information</h2>
                <p>We use the information we collect in the following ways:</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>To process your orders and send related information</li>
                    <li>To respond to your inquiries and provide customer support</li>
                    <li>To send marketing communications (with your consent)</li>
                    <li>To improve our website and services</li>
                    <li>To comply with legal obligations</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Sharing Your Information</h2>
                <p>
                    We do not sell, trade, or rent your personal information. We may share information with:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Service providers (shipping, payment processing)</li>
                    <li>Legal authorities when required by law</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Security</h2>
                <p>
                    We implement appropriate technical and organizational measures to protect your personal information 
                    against unauthorized access, alteration, disclosure, or destruction.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Your Rights</h2>
                <p>You have the right to:</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Access your personal data</li>
                    <li>Correct inaccurate data</li>
                    <li>Request deletion of your data</li>
                    <li>Opt-out of marketing communications</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Contact Us</h2>
                <p>
                    If you have questions about this Privacy Policy, please contact us at:
                    <br><strong>Email:</strong> info@photographyna.com
                    <br><strong>Address:</strong> [Your Business Address]
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                <div>
                    <h3 class="text-lg font-bold mb-4">Photography North Asia</h3>
                    <p class="text-gray-400">Premium photography equipment for professionals.</p>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Quick Links</h3>
                    <ul class="space-y-2 text-gray-400">
                        <li><a href="index.html" class="hover:text-white transition">Home</a></li>
                        <li><a href="privacy.html" class="hover:text-white transition">Privacy Policy</a></li>
                        <li><a href="terms.html" class="hover:text-white transition">Terms & Conditions</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Contact</h3>
                    <p class="text-gray-400">Email: info@photographyna.com</p>
                </div>
            </div>
            <div class="border-t border-gray-800 pt-8 text-center text-gray-400">
                <p>&copy; 2024 Photography North Asia. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

#### Step 2: Create `terms.html`

Create a new file called `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms & Conditions - Photography North Asia">
    <title>Terms & Conditions - Photography North Asia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16 md:h-20">
                <div class="flex items-center">
                    <a href="index.html" class="text-2xl md:text-3xl font-bold text-gray-900 tracking-tight">
                        <span class="bg-gradient-to-r from-gray-900 to-gray-600 bg-clip-text text-transparent">Photo</span>
                        <span class="text-gray-900">NA</span>
                    </a>
                </div>
                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Benefits</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">FAQ</a>
                    <a href="index.html#testimonials" class="text-gray-700 hover:text-gray-900 font-medium transition duration-300">Reviews</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24">
        <div class="max-w-4xl mx-auto px-4 md:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms & Conditions</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <p>
                    <strong>Last Updated:</strong> [DATE]
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision 
                    of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) 
                    on Photography North Asia's website for personal, non-commercial transitory viewing only. This is 
                    the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Disclaimer</h2>
                <p>
                    The materials on Photography North Asia's website are provided on an 'as is' basis. Photography 
                    North Asia makes no warranties, expressed or implied, and hereby disclaims and negates all other 
                    warranties including, without limitation, implied warranties or conditions of merchantability, 
                    fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Limitations</h2>
                <p>
                    In no event shall Photography North Asia or its suppliers be liable for any damages (including, 
                    without limitation, damages for loss of data or profit, or due to business interruption) arising 
                    out of the use or inability to use the materials on Photography North Asia's website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Photography North Asia's website could include technical, typographical, 
                    or photographic errors. Photography North Asia does not warrant that any of the materials on its 
                    website are accurate, complete, or current.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Links</h2>
                <p>
                    Photography North Asia has not reviewed all of the sites linked to its website and is not responsible 
                    for the contents of any such linked site. The inclusion of any link does not imply endorsement by 
                    Photography North Asia of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Modifications</h2>
                <p>
                    Photography North Asia may revise these terms of service for its website at any time without notice. 
                    By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of [YOUR COUNTRY/STATE] 
                    and you irrevocably submit to the exclusive jurisdiction of the courts located in [YOUR LOCATION].
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">9. Contact Information</h2>
                <p>
                    If you have any questions about these Terms & Conditions, please contact us at:
                    <br><strong>Email:</strong> info@photographyna.com
                    <br><strong>Address:</strong> [Your Business Address]
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                <div>
                    <h3 class="text-lg font-bold mb-4">Photography North Asia</h3>
                    <p class="text-gray-400">Premium photography equipment for professionals.</p>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Quick Links</h3>
                    <ul class="space-y-2 text-gray-400">
                        <li><a href="index.html" class="hover:text-white transition">Home</a></li>
                        <li><a href="privacy.html" class="hover:text-white transition">Privacy Policy</a></li>
                        <li><a href="terms.html" class="hover:text-white transition">Terms & Conditions</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Contact</h3>
                    <p class="text-gray-400">Email: info@photographyna.com</p>
                </div>
            </div>
            <div class="border-t border-gray-800 pt-8 text-center text-gray-400">
                <p>&copy; 2024 Photography North Asia. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Add Links to Footer in `index.html`

You need to add a footer to your main landing page with links to these new pages.

**Add this code before the closing `</body>` tag (at the very end of index.html):**

```html
<!-- Footer -->
<footer class="bg-gray-900 text-white py-12">
    <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
            <div>
                <h3 class="text-lg font-bold mb-4">Photography North Asia</h3>
                <p class="text-gray-400">Premium photography equipment for professionals.</p>
            </div>
            <div>
                <h3 class="text-lg font-bold mb-4">Quick Links</h3>
                <ul class="space-y-2 text-gray-400">
                    <li><a href="#features" class="hover:text-white transition">Features</a></li>
                    <li><a href="#benefits" class="hover:text-white transition">Benefits</a></li>
                    <li><a href="#faq" class="hover:text-white transition">FAQ</a></li>
                </ul>
            </div>
            <div>
                <h3 class="text-lg font-bold mb-4">Legal</h3>
                <ul class="space-y-2 text-gray-400">
                    <li><a href="privacy.html" class="hover:text-white transition">Privacy Policy</a></li>
                    <li><a href="terms.html" class="hover:text-white transition">Terms & Conditions</a></li>
                </ul>
            </div>
        </div>
        <div class="border-t border-gray-800 pt-8 text-center text-gray-400">
            <p>&copy; 2024 Photography North Asia. All rights reserved.</p>
        </div>
    </div>
</footer>
```

---

### Step 4: Update the New Pages

Before publishing, update these placeholders in both `privacy.html` and `terms.html`:

1. **Replace `[DATE]`** with today's date (e.g., "January 15, 2024")
2. **Replace email addresses** with your actual email
3. **Replace `[Your Business Address]`** with your actual address
4. **Replace `[YOUR COUNTRY/STATE]`** with your location
5. **Replace `info@photographyna.com`** with your email address

---

### Customizing Your Privacy & Terms Pages

The template pages provided are basic. Consider customizing them with:

- **Your specific business practices**
- **Payment methods you accept**
- **Shipping policies**
- **Return policies**
- **Warranty information**
- **Data retention practices**

---

### File Structure After Adding Pages

```
project-folder/
├── index.html (main landing page - now with footer)
├── privacy.html (new privacy policy)
├── terms.html (new terms & conditions)
└── [other files]
```

---

### Testing Your New Pages

1. **Save all files**
2. **Open index.html in your browser**
3. **Scroll to the bottom (footer)**
4. **Click "Privacy Policy" link** - should open privacy.html
5. **Click "Terms & Conditions" link** - should open terms.html
6. **On privacy.html and terms.html, click the logo** - should return to index.html

---

## Troubleshooting Common Issues

### Issue 1: Links Don't Work

**Problem:** Clicking a link does nothing or shows a 404 error.

**Solutions:**

1. **Check the file path:**
   - If `privacy.html` is in the same folder as `index.html`, use: `href="privacy.html"`
   - If it's in a subfolder, use: `href="pages/privacy.html"`

2. **Verify the filename:**
   - Make sure the filename matches exactly (case-sensitive on some systems)
   - `privacy.html` is different from `Privacy.html`

3. **Check for typos:**
   - `href="privicy.html"` (wrong) vs `href="privacy.html"` (correct)

---

### Issue 2: Navigation Links Don't Scroll to Section

**Problem:** Clicking "Features" doesn't scroll to the Features section.

**Solutions:**

1. **Check the section has an `id` attribute:**
   ```html
   <!-- This should exist -->
   <section id="features" class="py-16 md:py-24 bg-white">
   ```

2. **Check the link matches the id:**
   ```html
   <!-- This link should match the id above -->
   <a href="#features" class="...">Features</a>
   ```

3. **Make sure there are no typos:**
   - Link says `href="#feature"` but section says `id="features"` (missing 's')

---

### Issue 3: Images Not Displaying

**Problem:** Images show as broken or don't appear.

**Solutions:**

1. **Check the image URL:**
   - All images in this landing page use external URLs from Unsplash
   - They should work as long as you have internet connection

2. **If using local images:**
   - Place images in the same folder as `index.html`
   - Use: `src="image-name.jpg"` (not the full path)

3. **Check file extension:**
   - `.jpg`, `.jpeg`, `.png`, `.gif` are common formats
   - Make sure extension matches actual file

---

### Issue 4: Buttons Don't Look Right After Changing Colors

**Problem:** Button text is hard to read or colors don't match.

**Solutions:**

1. **Change both text and background color:**
   ```html
   <!-- Before -->
   <a class="bg-white text-gray-900 ...">Shop Now</a>
   
   <!-- After -->
   <a class="bg-blue-600 text-white ...">Shop Now</a>
   ```

2. **Update hover color to match:**
   ```html
   <!-- Change this too -->
   hover:bg-gray-100  →  hover:bg-blue-700
   ```

---

### Issue 5: Page Looks Different on Mobile

**Problem:** Layout breaks or text is too small on phones.

**Solutions:**

1. **Don't remove responsive classes** like `md:` and `lg:`
2. **Test in mobile view:**
   - Open browser DevTools (F12)
   - Click the mobile device icon
   - Select different phone sizes

3. **Common classes to keep:**
   ```html
   <!-- Don't remove these -->
   text-4xl md:text-5xl lg:text-6xl
   px-4 md:px-6 lg:px-8
   grid-cols-1 md:grid-cols-2 lg:grid-cols-3
   ```

---

### Issue 6: Text Color Hard to Read

**Problem:** Text blends into background.

**Solutions:**

1. **Ensure good contrast:**
   - Dark text on light background: `text-gray-900` on `bg-white`
   - Light text on dark background: `text-white` on `bg-gray-900`

2. **Avoid:**
   - `text-gray-600` on `bg-gray-50` (too light)
   - `text-gray-700` on `bg-gray-800` (too dark)

3. **Fix example:**
   ```html
   <!-- Before - hard to read -->
   <p class="text-gray-600 bg-gray-50">...</p>
   
   <!-- After - easier to read -->
   <p class="text-gray-900 bg-gray-50">...</p>
   ```

---

### Issue 7: Mobile Menu Not Working

**Problem:** Mobile menu button doesn't open menu on phones.

**Solutions:**

1. **Check the JavaScript function exists:**
   - Find `function toggleMobileMenu()` in your code
   - It should be in a `<script>` tag

2. **Add this code if missing:**
   ```html
   <script>
   function toggleMobileMenu() {
       const menu = document.getElementById('mobileMenu');
       menu.classList.toggle('hidden');
   }
   
   function toggleAccordion(button) {
       const item = button.closest('.accordion-item');
       item.classList.toggle('active');
   }
   </script>
   ```

3. **Add this before closing `</body>` tag**

---

### Issue 8: Accordion (FAQ) Not Expanding

**Problem:** Clicking FAQ questions doesn't expand answers.

**Solutions:**

1. **Check the JavaScript function exists** (see Issue 7)
2. **Verify the button has the right class:**
   ```html
   <!-- Should have this -->
   <button class="w-full ... accordion-item ..." onclick="toggleAccordion(this)">
   ```

3. **Check for typos in class names:**
   - `accordion-item` (correct)
   - `accordian-item` (wrong)

---

## Best Practices

### 1. **Always Back Up Before Making Changes**

```
Before editing index.html:
1. Make a copy: index.html.backup
2. Make your changes
3. Test thoroughly
4. If something breaks, you can restore from backup
```

---

### 2. **Use Find & Replace for Bulk Changes**

**Instead of manually changing each link:**
```
❌ Wrong - Manual editing each link
✅ Right - Use Ctrl+H to find & replace all at once
```

---

### 3. **Test Responsive Design**

Always test your changes on:
- **Desktop** (large screen)
- **Tablet** (medium screen)
- **Mobile** (small screen)

**How to test:**
1. Open browser DevTools (F12)
2. Click mobile device icon
3. Test different sizes

---

### 4. **Keep Styling Classes Intact**

```
❌ Wrong - Removing styling classes
<h1>Photography North Asia</h1>

✅ Right - Keep classes, only change text
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white">Photography North Asia</h1>
```

---

### 5. **Use Semantic HTML**

- `<h1>` for main title (only one per page)
- `<h2>` for section titles
- `<h3>` for subsection titles
- `<p>` for paragraphs
- `<a>` for links
- `<button>` for clickable elements

---

### 6. **Validate Your Links**

After editing, check:
- [ ] All external links work (Shop Now, Contact Us)
- [ ] All internal links work (navigation)
- [ ] All section IDs match their links
- [ ] Email links open your email client
- [ ] Privacy and Terms links work

---

### 7. **Keep Consistent Branding**

- Use the same colors throughout
- Use the same fonts (Inter is already imported)
- Keep consistent spacing
- Use consistent button styles

---

### 8. **Update All Instances**

When changing something like your website URL:
- Update in Shop Now buttons
- Update in footer
- Update in any other locations
- Use Find & Replace to catch all instances

---

### 9. **Mobile Menu Appears in Both Places**

Remember:
- **Desktop menu** (lines 104-109) - shown on tablets/desktops
- **Mobile menu** (lines 137-142) - shown on phones
- Update both if you change menu items

---

### 10. **Maintain Accessibility**

- Keep `alt` attributes on images
- Keep `aria-label` on buttons
- Don't remove semantic HTML tags
- Ensure good color contrast

---

## Quick Reference: File Locations

### Key Sections to Update

| Section | Location | What to Change |
|---------|----------|-----------------|
| Announcement Bar | Line 80 | Promo message |
| Logo | Line 94 | Brand name |
| Navigation | Line 104 | Menu items |
| Hero Title | Line 169 | Main heading |
| Hero Subtitle | Line 173 | Tagline |
| Features Cards | Lines 206-308 | Feature names & descriptions |
| Benefits Section | Lines 333-520 | Benefit titles & details |
| FAQ | Lines 576-695 | Questions & answers |
| Testimonials | Lines 721-850 | Reviews & customer names |
| Footer | End of file | Contact info & links |

---

## Final Checklist Before Publishing

- [ ] All text content updated
- [ ] All links verified and working
- [ ] Email addresses updated
- [ ] Website URLs updated
- [ ] Privacy policy created and linked
- [ ] Terms page created and linked
- [ ] Images loading correctly
- [ ] Mobile menu working
- [ ] Accordion (FAQ) working
- [ ] Navigation links scroll to sections
- [ ] Tested on mobile, tablet, desktop
- [ ] All buttons clickable
- [ ] Colors and branding consistent
- [ ] No broken links
- [ ] No typos in content

---

## Support & Next Steps

### When You're Ready to Publish

1. **Choose a hosting provider** (Netlify, Vercel, AWS, GoDaddy, etc.)
2. **Upload your files** to the hosting provider
3. **Set up a domain name** (yourwebsite.com)
4. **Test the live website** thoroughly
5. **Set up SSL certificate** (for security - usually automatic)

### Ongoing Maintenance

- Update testimonials regularly
- Keep product information current
- Monitor links for breakage
- Update privacy policy if business practices change
- Keep contact information current
- Regularly back up your files

---

**Congratulations!** You now have a fully customizable, professional landing page. Remember to test all changes before publishing, and don't hesitate to refer back to this guide whenever you need to make updates.