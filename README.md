# SolarVegas Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the SolarVegas landing page. Whether you're updating text, fixing links, or adding new pages, this document provides step-by-step instructions tailored to this specific landing page.

---

## Table of Contents

1. [Before You Start](#before-you-start)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Updating Links](#fixing-and-updating-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Troubleshooting Common Issues](#troubleshooting-common-issues)
8. [Best Practices](#best-practices)

---

## Before You Start

### What You'll Need

- A text editor (we recommend **Visual Studio Code** - it's free!)
- Basic understanding of HTML tags and CSS
- The `index.html` file open in your editor
- File explorer to manage your website files

### How to Open the File

1. **Download Visual Studio Code** from [code.visualstudio.com](https://code.visualstudio.com)
2. **Open the folder** containing your website files in VS Code
3. **Click on `index.html`** in the left sidebar to view and edit it

### Important: Making Backups

Before making any changes, **always create a backup**:

1. Right-click on `index.html`
2. Select "Copy"
3. Right-click in the same folder
4. Select "Paste"
5. Rename the copy to `index.html.backup`

This way, if something goes wrong, you can restore the original file.

---

## Understanding the Page Structure

The landing page is organized into distinct sections. Understanding this structure will help you navigate and make changes confidently.

### Main Sections of the Page

```
1. HEADER/NAVIGATION (Lines 53-92)
   ├─ Logo and Brand Name
   ├─ Desktop Navigation Menu
   └─ Mobile Navigation Menu

2. HERO SECTION (Lines 94-169)
   ├─ Main Headline
   ├─ Subheading
   ├─ Call-to-Action Buttons
   ├─ Statistics Cards
   └─ Hero Image

3. FEATURES SECTION (Lines 171-232)
   ├─ Section Heading
   └─ Three Feature Cards
       ├─ Expert Local Installers
       ├─ Top-Tier Solar Panels
       └─ Seamless Permitting Process

4. BENEFITS SECTION (Lines 234-289)
   ├─ Section Heading
   └─ Three Benefit Cards
       ├─ Significant Energy Savings
       ├─ Increased Home Value
       └─ Reduced Carbon Footprint

5. ABOUT US SECTION (Lines 291-340)
   ├─ Company Image
   ├─ About Text
   └─ Statistics

6. TESTIMONIALS SECTION (Lines 342-395)
   ├─ Section Heading
   └─ Four Customer Testimonials

7. FAQ SECTION (Lines 397-510)
   ├─ Section Heading
   └─ Five FAQ Accordion Items

8. CALL-TO-ACTION SECTION (Lines 512-532)
   ├─ Main CTA Headline
   ├─ CTA Subheading
   └─ CTA Buttons

9. FOOTER (Lines 534-610)
   ├─ Company Info
   ├─ Quick Links
   ├─ Resources
   ├─ Contact Information
   └─ Copyright Notice
```

---

## Updating Text Content

Updating text is one of the most common maintenance tasks. Here's how to do it safely and effectively.

### Step-by-Step: Finding and Replacing Text

#### 1. **Using Find and Replace (Recommended)**

This is the safest method for beginners:

1. In VS Code, press `Ctrl+H` (Windows) or `Cmd+H` (Mac)
2. A "Find and Replace" box will appear at the top
3. Type the text you want to find in the top field
4. Type the replacement text in the bottom field
5. Click the single arrow icon to replace just one instance, or click "Replace All" to replace all instances

**Example: Changing the Company Name**

- **Find:** `America's Home Contractors`
- **Replace:** `Your Company Name`

#### 2. **Manual Editing (For Precise Changes)**

For specific sections, you can manually edit:

1. Use `Ctrl+F` (Windows) or `Cmd+F` (Mac) to find text
2. Click on the text in the editor to position your cursor
3. Select the text you want to change (double-click a word or click-drag to select)
4. Type your new text

### Key Text Areas to Update

#### **Header/Logo Text** (Line 62)

**Current:**
```html
<span class="text-xl font-bold text-gray-900 hidden sm:inline">SolarVegas</span>
```

**To Change:**
1. Find: `SolarVegas`
2. Replace with: `Your Business Name`

**Why the `hidden sm:inline` classes?** These mean the text is hidden on small screens (mobile) and visible on larger screens. This keeps mobile navigation clean.

---

#### **Hero Section Headline** (Lines 70-73)

**Current:**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Power Your Vegas Home with <span class="gradient-text">Solar!</span>
</h1>
```

**To Change:**
1. Find: `Power Your Vegas Home with`
2. Replace with: `Your Headline Here`

**Note:** Keep the `<span class="gradient-text">Solar!</span>` part if you want the blue gradient effect on that word. If you want to change what word has the gradient:

```html
<!-- Before -->
Power Your Vegas Home with <span class="gradient-text">Solar!</span>

<!-- After - if you want "Clean Energy" to be blue/gradient -->
Power Your Vegas Home with <span class="gradient-text">Clean Energy!</span>
```

---

#### **Hero Section Subheading** (Lines 74-78)

**Current:**
```html
<p class="text-lg sm:text-xl text-gray-600 leading-relaxed font-light">
    Embrace clean energy and slash your electricity bills in the heart of the desert. 
    Join thousands of Las Vegas homeowners who are saving money while protecting the planet.
</p>
```

**To Change:**
1. Find: `Embrace clean energy and slash your electricity bills in the heart of the desert. Join thousands of Las Vegas homeowners who are saving money while protecting the planet.`
2. Replace with: `Your subheading text here.`

**Tip:** Keep your subheading concise (1-2 sentences) for better readability.

---

#### **Statistics Cards** (Lines 109-125)

These are the three number boxes showing "50%", "25+", and "5000+".

**To Update the First Statistic (50% - Average Bill Reduction):**

**Current (Lines 109-112):**
```html
<div class="text-center">
    <p class="text-3xl font-bold text-blue-600">50%</p>
    <p class="text-sm text-gray-600 mt-1">Avg. Bill Reduction</p>
</div>
```

**To Change:**
1. Replace `50%` with your number
2. Replace `Avg. Bill Reduction` with your label

**Example:**
```html
<div class="text-center">
    <p class="text-3xl font-bold text-blue-600">45%</p>
    <p class="text-sm text-gray-600 mt-1">Average Savings</p>
</div>
```

---

#### **Feature Cards Titles and Descriptions** (Lines 171-232)

There are three feature cards. Here's how to update the first one:

**Current (Lines 182-197):**
```html
<div class="feature-card bg-gradient-to-br from-blue-50 to-cyan-50 p-8 rounded-xl border border-blue-100 hover:shadow-xl transition-all duration-300">
    <div class="w-16 h-16 bg-blue-600 rounded-lg flex items-center justify-center mb-6 shadow-lg">
        <i class="fas fa-tools text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Expert Local Installers</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Our team of certified, licensed professionals has over 15 years of combined experience...
    </p>
```

**To Change the Title:**
1. Find: `Expert Local Installers`
2. Replace with: `Your Feature Title`

**To Change the Description:**
1. Find the paragraph text starting with "Our team of certified..."
2. Replace with your new description

**To Change the Icon:**
The icon is controlled by this line: `<i class="fas fa-tools text-white text-2xl"></i>`

Available icon examples:
- `fa-tools` (wrench) - for installation/service
- `fa-solar-panel` - for solar panels
- `fa-leaf` - for environment
- `fa-dollar-sign` - for savings
- `fa-award` - for quality
- `fa-shield-alt` - for protection

**To change the icon:**
1. Find: `<i class="fas fa-tools text-white text-2xl"></i>`
2. Replace `fa-tools` with a different icon code (keep `fas` and the other classes)

**Example:**
```html
<i class="fas fa-leaf text-white text-2xl"></i>
```

---

#### **Bullet Points in Feature Cards** (Lines 198-207)

**Current:**
```html
<ul class="space-y-2 text-sm text-gray-700">
    <li class="flex items-start">
        <i class="fas fa-check text-green-500 mr-3 mt-1 flex-shrink-0"></i>
        <span>Licensed and Insured Professionals</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-green-500 mr-3 mt-1 flex-shrink-0"></i>
        <span>Local Desert Climate Expertise</span>
    </li>
    ...
</ul>
```

**To Change a Bullet Point:**
1. Find: `Licensed and Insured Professionals`
2. Replace with: `Your benefit text`

**Repeat for each `<span>` tag containing bullet text.**

---

#### **Benefits Section Cards** (Lines 234-289)

The Benefits section has three cards with icons, titles, and descriptions.

**To Update the First Benefit Card (Savings):**

**Current (Lines 243-255):**
```html
<div class="bg-white/10 backdrop-blur-sm border border-white/20 rounded-xl p-8 hover:bg-white/15 transition-all duration-300 transform hover:scale-105">
    <div class="flex items-center mb-6">
        <div class="w-14 h-14 bg-white/20 rounded-lg flex items-center justify-center mr-4">
            <i class="fas fa-piggy-bank text-white text-2xl"></i>
        </div>
        <h3 class="text-2xl font-bold text-white">Significant Energy Savings</h3>
    </div>
    <p class="text-blue-50 leading-relaxed mb-4">
        Reduce your electricity bills by up to 50-90% with solar power...
    </p>
```

**To Change:**
- Title: Find and replace `Significant Energy Savings`
- Icon: Change `fa-piggy-bank` to another icon
- Description: Find and replace the paragraph text
- Bottom stat: Find and replace `Average Monthly Savings: $150-300+`

---

#### **Testimonials** (Lines 342-395)

Each testimonial has a quote, name, and title.

**Current (Lines 357-369):**
```html
<div class="testimonial-card bg-white rounded-xl shadow-md p-8 border border-gray-200 hover:shadow-lg transition-all duration-300">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-700 mb-6 leading-relaxed">
        "The team at America's Home Contractors made the entire process effortless..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-gray-900">Michael Rodriguez</p>
        <p class="text-sm text-gray-600">Homeowner, Las Vegas</p>
    </div>
</div>
```

**To Change a Testimonial:**

1. **Change the quote:**
   - Find: `"The team at America's Home Contractors made the entire process effortless..."`
   - Replace with: `"Your testimonial text here"`

2. **Change the customer name:**
   - Find: `Michael Rodriguez`
   - Replace with: `Customer Name`

3. **Change the customer title/location:**
   - Find: `Homeowner, Las Vegas`
   - Replace with: `Your Title, Your Location`

**To Change the Star Rating:**
The testimonials currently show 5 stars. To change to 4 stars:

1. Find the section with 5 `<i class="fas fa-star"></i>` tags
2. Delete one of them
3. Add an empty star: `<i class="fas fa-star-half-alt"></i>` or just remove one

---

#### **FAQ Questions and Answers** (Lines 397-510)

**Current (Lines 411-420):**
```html
<button class="faq-question w-full px-6 py-5 text-left font-semibold text-gray-900 hover:bg-blue-50 transition-colors duration-300 flex items-center justify-between cursor-pointer" aria-expanded="false">
    <span class="flex items-center">
        <i class="fas fa-bolt text-blue-600 mr-4"></i>
        How much can I save with solar panels?
    </span>
    <i class="faq-icon fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
</button>
<div class="faq-answer hidden px-6 py-5 bg-blue-50 border-t border-gray-200">
    <p class="text-gray-700 leading-relaxed">
        The amount you save depends on several factors...
    </p>
</div>
```

**To Change an FAQ Question:**
1. Find: `How much can I save with solar panels?`
2. Replace with: `Your question`

**To Change an FAQ Answer:**
1. Find: `The amount you save depends on several factors...`
2. Replace with: `Your answer`

**To Change the FAQ Icon:**
1. Find: `<i class="fas fa-bolt text-blue-600 mr-4"></i>`
2. Replace `fa-bolt` with another icon (keep the rest of the classes)

---

#### **Footer Text** (Lines 534-610)

**Company Description (Line 546):**
```html
<p class="text-gray-400 leading-relaxed">
    Powering Las Vegas homes with clean, renewable solar energy since 2008.
</p>
```

**To Change:**
1. Find: `Powering Las Vegas homes with clean, renewable solar energy since 2008.`
2. Replace with: `Your company description`

**Contact Information (Lines 593-599):**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span>x_n2deep_x@yahoo.com</span>
</li>
```

**To Change Email:**
1. Find: `x_n2deep_x@yahoo.com`
2. Replace with: `your-email@example.com`

**To Change Location:**
1. Find: `Las Vegas, Nevada`
2. Replace with: `Your City, Your State`

**Copyright Year (Line 608):**
```html
<p>&copy; 2025 America's Home Contractors. All rights reserved.</p>
```

**To Change:**
1. Find: `2025 America's Home Contractors`
2. Replace with: `2025 Your Company Name`

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first framework that uses predefined classes to style elements. The good news: you don't need to write CSS code! You just add or remove class names.

### Understanding Tailwind Classes on This Page

#### **Common Classes and What They Do**

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-xl` | Makes text larger | `<h1 class="text-xl">` |
| `text-gray-900` | Makes text dark gray | `<p class="text-gray-900">` |
| `bg-blue-600` | Makes background blue | `<div class="bg-blue-600">` |
| `px-8` | Adds left/right padding | `<div class="px-8">` |
| `py-4` | Adds top/bottom padding | `<div class="py-4">` |
| `rounded-lg` | Rounds corners | `<div class="rounded-lg">` |
| `shadow-lg` | Adds a shadow | `<div class="shadow-lg">` |
| `hover:bg-blue-700` | Changes color on hover | `<button class="hover:bg-blue-700">` |
| `transition-all` | Smooth animation | `<div class="transition-all">` |
| `hidden` | Hides element | `<div class="hidden">` |
| `md:flex` | Shows on medium screens and up | `<div class="md:flex">` |

#### **Responsive Classes (Mobile-First Design)**

The landing page uses responsive design, meaning it looks good on phones, tablets, and desktops.

**Key Responsive Prefixes:**
- `sm:` - Small screens (640px+) - tablets
- `md:` - Medium screens (768px+) - larger tablets
- `lg:` - Large screens (1024px+) - desktops

**Example from the Hero Section (Line 71):**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900">
```

This means:
- On mobile: text size is `4xl`
- On tablets and up: text size is `5xl`
- On desktops: text size is `6xl`

### Common Modifications

#### **Changing Text Color**

**Current (Hero Headline):**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
```

**To Change Text Color:**

1. Find: `text-gray-900`
2. Replace with one of these options:
   - `text-blue-600` (blue)
   - `text-gray-700` (dark gray)
   - `text-gray-900` (darker gray - current)
   - `text-white` (white)

**Example (Change headline to blue):**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-blue-600 leading-tight tracking-tight">
```

---

#### **Changing Background Color**

**Current (Hero Section):**
```html
<section class="relative py-20 sm:py-24 lg:py-32 bg-gradient-to-br from-blue-50 via-white to-cyan-50 overflow-hidden">
```

**To Change Background:**

1. Find: `bg-gradient-to-br from-blue-50 via-white to-cyan-50`
2. Replace with:
   - `bg-white` (solid white)
   - `bg-gray-50` (light gray)
   - `bg-blue-50` (light blue)
   - `bg-gradient-to-r from-blue-600 to-cyan-500` (blue to cyan gradient)

**Example (Solid white background):**
```html
<section class="relative py-20 sm:py-24 lg:py-32 bg-white overflow-hidden">
```

---

#### **Changing Button Color**

**Current (Primary Button):**
```html
<a href="https://americashomecontractors.com/actnow" class="btn-primary inline-flex items-center justify-center bg-blue-600 text-white px-8 py-4 rounded-lg hover:bg-blue-700 transition-all duration-300 font-semibold text-lg shadow-lg hover:shadow-xl">
```

**To Change Button Color:**

1. Find: `bg-blue-600` (button background)
2. Replace with:
   - `bg-green-600` (green)
   - `bg-purple-600` (purple)
   - `bg-red-600` (red)
   - `bg-yellow-500` (yellow)

3. Also update the hover state: `hover:bg-blue-700`
   - Change to: `hover:bg-green-700` (if you chose green)

**Example (Change to green button):**
```html
<a href="https://americashomecontractors.com/actnow" class="btn-primary inline-flex items-center justify-center bg-green-600 text-white px-8 py-4 rounded-lg hover:bg-green-700 transition-all duration-300 font-semibold text-lg shadow-lg hover:shadow-xl">
```

---

#### **Changing Spacing (Padding and Margins)**

**Understanding Padding and Margins:**
- **Padding:** Space inside an element (between content and border)
- **Margin:** Space outside an element (between elements)

**Common Spacing Classes:**
- `p-4` = padding on all sides
- `px-8` = padding on left and right
- `py-4` = padding on top and bottom
- `m-4` = margin on all sides
- `mx-auto` = centers element horizontally

**Example (Feature Card - Line 182):**
```html
<div class="feature-card bg-gradient-to-br from-blue-50 to-cyan-50 p-8 rounded-xl border border-blue-100">
```

**To Add More Padding:**
- Change `p-8` to `p-12` (more padding)
- Or change to `p-4` (less padding)

**To Add More Margin Between Cards:**
- Find: `gap-8` (in the grid that contains cards)
- Change to: `gap-12` (more space) or `gap-4` (less space)

---

#### **Changing Border Radius (Rounded Corners)**

**Current (Feature Card):**
```html
<div class="feature-card bg-gradient-to-br from-blue-50 to-cyan-50 p-8 rounded-xl border border-blue-100">
```

**To Change Corner Roundness:**

1. Find: `rounded-xl`
2. Replace with:
   - `rounded-none` (no rounding - square)
   - `rounded-sm` (slightly rounded)
   - `rounded` (medium rounded)
   - `rounded-lg` (more rounded)
   - `rounded-xl` (very rounded - current)
   - `rounded-full` (completely round/circle)

**Example (Less rounded corners):**
```html
<div class="feature-card bg-gradient-to-br from-blue-50 to-cyan-50 p-8 rounded-lg border border-blue-100">
```

---

#### **Changing Shadow Effects**

**Current (Hero Image):**
```html
<img src="https://images.unsplash.com/photo-1509391366360-2e938d440dbb?w=600&h=600&fit=crop" alt="Solar panels on Vegas home" class="rounded-2xl shadow-2xl w-full h-auto object-cover">
```

**To Change Shadow:**

1. Find: `shadow-2xl`
2. Replace with:
   - `shadow-none` (no shadow)
   - `shadow-sm` (small shadow)
   - `shadow` (medium shadow)
   - `shadow-lg` (large shadow)
   - `shadow-xl` (very large shadow)
   - `shadow-2xl` (huge shadow - current)

**Example (Smaller shadow):**
```html
<img src="..." class="rounded-2xl shadow-lg w-full h-auto object-cover">
```

---

#### **Hiding/Showing Elements on Different Screen Sizes**

**Current (Logo Text - Line 62):**
```html
<span class="text-xl font-bold text-gray-900 hidden sm:inline">SolarVegas</span>
```

**What This Means:**
- `hidden` = Hidden on all screens initially
- `sm:inline` = Shown on small screens (tablets) and up

**To Show on All Screens:**
1. Remove the `hidden` class
2. Result: `<span class="text-xl font-bold text-gray-900 sm:inline">`

**To Hide on Mobile Only:**
1. Replace `hidden sm:inline` with `md:inline` (shown on medium screens up)
2. Result: `<span class="text-xl font-bold text-gray-900 md:inline">`

---

### Making a Section Full-Width

**Current (Benefits Section):**
```html
<section id="benefits" class="py-20 sm:py-24 lg:py-32 bg-gradient-to-r from-blue-600 to-cyan-500">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
```

The `max-w-7xl` class limits the section width. To make it truly full-width:

1. Keep the `<section>` classes as is
2. Inside, the `<div class="max-w-7xl mx-auto">` controls the content width

**If you want full-width content:**
- Remove or change `max-w-7xl` to `w-full`
- Result: `<div class="w-full mx-auto px-4 sm:px-6 lg:px-8">`

---

## Fixing and Updating Links

Links are critical for navigation. This section shows you exactly where all the links are and how to update them.

### Understanding Links

A link looks like this:
```html
<a href="https://example.com">Click Here</a>
```

**Parts:**
- `<a>` = Link tag
- `href="..."` = Where the link goes
- `Click Here` = Text that shows on the page

### All Links on This Page

Here's a complete list of every link and where to find it:

#### **Header Navigation Links** (Lines 65-69)

**Current:**
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
<a href="#faq" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">FAQ</a>
<a href="https://americashomecontractors.com/actnow" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-all duration-300 transform hover:scale-105 font-medium">Get Started</a>
```

**What These Do:**
- `#features` = Scrolls to Features section
- `#benefits` = Scrolls to Benefits section
- `#about` = Scrolls to About section
- `#faq` = Scrolls to FAQ section
- `https://americashomecontractors.com/actnow` = External link to sign-up page

**To Update the "Get Started" Button Link:**
1. Find: `https://americashomecontractors.com/actnow`
2. Replace with: `https://yourwebsite.com/your-page`

**Example:**
```html
<a href="https://yourcompany.com/get-solar-quote" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-all duration-300 transform hover:scale-105 font-medium">Get Started</a>
```

---

#### **Mobile Menu Links** (Lines 83-88)

**Current:**
```html
<a href="#features" class="block py-2 px-4 text-gray-700 hover:text-blue-600 hover:bg-gray-50 rounded transition-colors duration-300">Features</a>
<a href="#benefits" class="block py-2 px-4 text-gray-700 hover:text-blue-600 hover:bg-gray-50 rounded transition-colors duration-300">Benefits</a>
<a href="#about" class="block py-2 px-4 text-gray-700 hover:text-blue-600 hover:bg-gray-50 rounded transition-colors duration-300">About</a>
<a href="#faq" class="block py-2 px-4 text-gray-700 hover:text-blue-600 hover:bg-gray-50 rounded transition-colors duration-300">FAQ</a>
<a href="https://americashomecontractors.com/actnow" class="block mt-3 mx-4 bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-all duration-300 text-center font-medium">Get Started</a>
```

**These are the same as desktop links, just formatted for mobile.**

**To Update the Mobile "Get Started" Button:**
1. Find the last link in the mobile menu
2. Change: `https://americashomecontractors.com/actnow`
3. To: Your new URL (same as you did for desktop)

---

#### **Hero Section Buttons** (Lines 80-82 and 84-88)

**Current:**
```html
<a href="https://americashomecontractors.com/actnow" class="btn-primary inline-flex items-center justify-center bg-blue-600 text-white px-8 py-4 rounded-lg hover:bg-blue-700 transition-all duration-300 font-semibold text-lg shadow-lg hover:shadow-xl">
    <span>Start Your Solar Journey</span>
    <i class="fas fa-arrow-right ml-2"></i>
</a>
<button class="inline-flex items-center justify-center border-2 border-blue-600 text-blue-600 px-8 py-4 rounded-lg hover:bg-blue-50 transition-all duration-300 font-semibold text-lg" aria-label="Learn more about solar benefits">
    <i class="fas fa-play mr-2"></i>
    <span>Learn More</span>
</button>
```

**To Update the "Start Your Solar Journey" Button:**
1. Find: `https://americashomecontractors.com/actnow`
2. Replace with: Your URL

**Note:** The "Learn More" button is a `<button>` not a link. It currently doesn't go anywhere. To make it functional, change it to:

```html
<a href="#features" class="inline-flex items-center justify-center border-2 border-blue-600 text-blue-600 px-8 py-4 rounded-lg hover:bg-blue-50 transition-all duration-300 font-semibold text-lg">
    <i class="fas fa-play mr-2"></i>
    <span>Learn More</span>
</a>
```

---

#### **CTA Section Buttons** (Lines 525-532)

**Current:**
```html
<a href="https://americashomecontractors.com/actnow" class="btn-primary inline-flex items-center justify-center bg-white text-blue-600 px-8 py-4 rounded-lg hover:bg-blue-50 transition-all duration-300 font-semibold text-lg shadow-lg hover:shadow-xl">
    <span>Get Free Assessment</span>
    <i class="fas fa-arrow-right ml-2"></i>
</a>
<button class="inline-flex items-center justify-center border-2 border-white text-white px-8 py-4 rounded-lg hover:bg-white/10 transition-all duration-300 font-semibold text-lg" aria-label="Schedule a consultation">
    <i class="fas fa-calendar mr-2"></i>
    <span>Schedule Consultation</span>
</button>
```

**To Update the "Get Free Assessment" Button:**
1. Find: `https://americashomecontractors.com/actnow`
2. Replace with: Your URL

**To Make "Schedule Consultation" Functional:**

Change from `<button>` to `<a>`:

```html
<a href="https://yourwebsite.com/schedule" class="inline-flex items-center justify-center border-2 border-white text-white px-8 py-4 rounded-lg hover:bg-white/10 transition-all duration-300 font-semibold text-lg">
    <i class="fas fa-calendar mr-2"></i>
    <span>Schedule Consultation</span>
</a>
```

---

#### **Footer Navigation Links** (Lines 574-582)

**Current:**
```html
<a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a>
<a href="#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About Us</a>
<a href="#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a>
```

**These are internal links (scroll to sections). They're already correct.**

---

#### **Footer Resource Links** (Lines 587-592)

**Current:**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
<a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact Us</a>
```

**These are placeholder links. See the next section for how to create and link these pages.**

---

#### **Footer Contact Links** (Lines 597-606)

**Current:**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span>x_n2deep_x@yahoo.com</span>
</li>
<li class="flex items-start">
    <i class="fas fa-map-marker-alt text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span>Las Vegas, Nevada</span>
</li>
<li class="flex items-start">
    <i class="fas fa-clock text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span>24/7 Support Available</span>
</li>
```

**To Change Email:**
1. Find: `x_n2deep_x@yahoo.com`
2. Replace with: `your-email@company.com`

**To Change Location:**
1. Find: `Las Vegas, Nevada`
2. Replace with: `Your City, Your State`

**To Add an Email Link:**

Change from plain text to a clickable link:

```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:your-email@company.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">your-email@company.com</a>
</li>
```

---

#### **Footer Social Media Links** (Lines 552-561)

**Current:**
```html
<a href="#" aria-label="Facebook" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-blue-400 hover:bg-gray-700 transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
<a href="#" aria-label="Twitter" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-blue-400 hover:bg-gray-700 transition-all duration-300">
    <i class="fab fa-twitter"></i>
</a>
<!-- More social links... -->
```

**To Add Social Media Links:**

1. Find: `<a href="#" aria-label="Facebook"`
2. Replace `#` with your Facebook URL: `https://facebook.com/yourpage`
3. Repeat for Twitter, Instagram, LinkedIn

**Example:**
```html
<a href="https://facebook.com/yourcompany" aria-label="Facebook" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-blue-400 hover:bg-gray-700 transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

---

### Link Checklist

Use this checklist to ensure all your links are working:

- [ ] Header "Get Started" button links to correct URL
- [ ] Mobile "Get Started" button links to correct URL
- [ ] Hero "Start Your Solar Journey" button links to correct URL
- [ ] CTA "Get Free Assessment" button links to correct URL
- [ ] All internal links (#features, #benefits, etc.) work
- [ ] Footer "Privacy Policy" link works
- [ ] Footer "Terms of Service" link works
- [ ] Footer "Blog" link works (if you have a blog)
- [ ] Footer "Contact Us" link works
- [ ] Email address in footer is correct and clickable
- [ ] Social media links point to your profiles

---

## Adding Privacy and Terms Pages

Now let's create and link your Privacy Policy and Terms of Service pages.

### Step 1: Create the Privacy Policy Page

#### **Creating a New File**

1. In VS Code, right-click in the file explorer on the left
2. Select "New File"
3. Name it: `privacy.html`
4. Press Enter

#### **Adding Content to Privacy Policy**

1. Copy this template into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for SolarVegas">
    <meta name="keywords" content="privacy, policy, solar">
    <meta name="author" content="America's Home Contractors">
    <title>Privacy Policy | SolarVegas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header/Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex-shrink-0">
                    <div class="flex items-center space-x-2">
                        <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-cyan-500 rounded-lg flex items-center justify-center">
                            <i class="fas fa-sun text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-gray-900 hidden sm:inline">SolarVegas</span>
                    </div>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                    <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">FAQ</a>
                    <a href="https://americashomecontractors.com/actnow" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-all duration-300 font-medium">Get Started</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 sm:py-24 lg:py-32 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="space-y-8 text-gray-700 leading-relaxed">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p>
                        America's Home Contractors ("we," "us," "our," or "Company") operates the SolarVegas website. 
                        This page informs you of our policies regarding the collection, use, and disclosure of personal 
                        data when you use our Service and the choices you have associated with that data.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information Collection and Use</h2>
                    <p>We collect several different types of information for various purposes to provide and improve our Service:</p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li><strong>Personal Data:</strong> While using our Service, we may ask you to provide us with certain personally identifiable information ("Personal Data").</li>
                        <li><strong>Usage Data:</strong> We may also collect information on how the Service is accessed and used ("Usage Data").</li>
                        <li><strong>Cookies and Tracking:</strong> We use cookies and similar tracking technologies to track activity on our Service.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Data</h2>
                    <p>America's Home Contractors uses the collected data for various purposes:</p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>To provide and maintain our Service</li>
                        <li>To notify you about changes to our Service</li>
                        <li>To allow you to participate in interactive features of our Service</li>
                        <li>To provide customer support</li>
                        <li>To gather analysis or valuable information so that we can improve our Service</li>
                        <li>To monitor the usage of our Service</li>
                        <li>To detect, prevent and address technical issues</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Security of Data</h2>
                    <p>
                        The security of your data is important to us but remember that no method of transmission over the Internet 
                        or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect 
                        your Personal Data, we cannot guarantee its absolute security.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Contact Us</h2>
                    <p>
                        If you have any questions about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> x_n2deep_x@yahoo.com<br>
                        <strong>Address:</strong> Las Vegas, Nevada
                    </p>
                </div>

                <div class="bg-blue-50 border border-blue-200 rounded-lg p-6 mt-8">
                    <p class="text-sm text-gray-600">
                        Last updated: January 2025. This Privacy Policy may be updated from time to time. 
                        We will notify you of any changes by updating the "Last updated" date of this Privacy Policy.
                    </p>
                </div>
            </div>

            <!-- Back Button -->
            <div class="mt-12">
                <a href="index.html" class="inline-flex items-center text-blue-600 hover:text-blue-700 font-semibold transition-colors duration-300">
                    <i class="fas fa-arrow-left mr-2"></i>
                    Back to Home
                </a>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16 sm:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center text-gray-400">
                <p>&copy; 2025 America's Home Contractors. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

2. **Save the file** (Ctrl+S or Cmd+S)

---

### Step 2: Create the Terms of Service Page

#### **Creating a New File**

1. In VS Code, right-click in the file explorer
2. Select "New File"
3. Name it: `terms.html`
4. Press Enter

#### **Adding Content to Terms of Service**

1. Copy this template into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for SolarVegas">
    <meta name="keywords" content="terms, service, solar">
    <meta name="author" content="America's Home Contractors">
    <title>Terms of Service | SolarVegas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header/Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex-shrink-0">
                    <div class="flex items-center space-x-2">
                        <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-cyan-500 rounded-lg flex items-center justify-center">
                            <i class="fas fa-sun text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-gray-900 hidden sm:inline">SolarVegas</span>
                    </div>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                    <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">FAQ</a>
                    <a href="https://americashomecontractors.com/actnow" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-all duration-300 font-medium">Get Started</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 sm:py-24 lg:py-32 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="space-y-8 text-gray-700 leading-relaxed">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision 
                        of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) 
                        on SolarVegas for personal, non-commercial transitory viewing only. This is the grant of a license, 
                        not a transfer of title, and under this license you may not:
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
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on SolarVegas are provided on an 'as is' basis. America's Home Contractors makes no 
                        warranties, expressed or implied, and hereby disclaims and negates all other warranties including, 
                        without limitation, implied warranties or conditions of merchantability, fitness for a particular 
                        purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p>
                        In no event shall America's Home Contractors or its suppliers be liable for any damages (including, 
                        without limitation, damages for loss of data or profit, or due to business interruption) arising out 
                        of the use or inability to use the materials on SolarVegas, even if we or an authorized representative 
                        has been notified orally or in writing of the possibility of such damage.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on SolarVegas could include technical, typographical, or photographic errors. 
                        America's Home Contractors does not warrant that any of the materials on its website are accurate, 
                        complete, or current. We may make changes to the materials contained on our website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p>
                        America's Home Contractors has not reviewed all of the sites linked to its website and is not responsible 
                        for the contents of any such linked site. The inclusion of any link does not imply endorsement by 
                        America's Home Contractors of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p>
                        America's Home Contractors may revise these terms of service for our website at any time without notice. 
                        By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of Nevada, 
                        and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div class="bg-blue-50 border border-blue-200 rounded-lg p-6 mt-8">
                    <p class="text-sm text-gray-600">
                        Last updated: January 2025. These Terms of Service may be updated from time to time. 
                        We will notify you of any changes by updating the "Last updated" date of this Terms of Service.
                    </p>
                </div>
            </div>

            <!-- Back Button -->
            <div class="mt-12">
                <a href="index.html" class="inline-flex items-center text-blue-600 hover:text-blue-700 font-semibold transition-colors duration-300">
                    <i class="fas fa-arrow-left mr-2"></i>
                    Back to Home
                </a>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16 sm:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center text-gray-400">
                <p>&copy; 2025 America's Home Contractors. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

2. **Save the file** (Ctrl+S or Cmd+S)

---

### Step 3: Verify Links in index.html

The footer links to these pages should already be correct. Let's verify:

**In your `index.html` file, find lines 587-592:**

```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
<a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact Us</a>
```

**These are correct!** The links point to:
- `privacy.html` ✓
- `terms.html` ✓

---

### Step 4: Test Your Links

1. **Open your website in a browser**
   - Double-click `index.html` or open it with your browser
   
2. **Scroll to the footer**

3. **Click on "Privacy Policy"**
   - You should see the privacy page
   - Click "Back to Home" to return

4. **Click on "Terms of Service"**
   - You should see the terms page
   - Click "Back to Home" to return

### Troubleshooting Link Issues

**Problem: "Page not found" when clicking links**

1. Make sure your files are in the same folder:
   ```
   your-website-folder/
   ├── index.html
   ├── privacy.html
   └── terms.html
   ```

2. Check that file names match exactly (including lowercase/uppercase)

3. Make sure you saved both new files

---

### Optional: Create a Contact Page

Follow the same steps to create `contact.html`:

1. Create new file: `contact.html`
2. Update the footer link from:
   ```html
   <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact Us</a>
   ```
   To:
   ```html
   <a href="contact.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact Us</a>
   ```

---

## Troubleshooting Common Issues

### Issue 1: Changes Don't Show Up

**Problem:** You edited the HTML but the website looks the same.

**Solution:**
1. **Save your file:** Ctrl+S (Windows) or Cmd+S (Mac)
2. **Refresh the browser:** Ctrl+R (Windows) or Cmd+R (Mac)
3. **Clear browser cache:** 
   - In Chrome: Ctrl+Shift+Delete
   - In Firefox: Ctrl+Shift+Delete
   - Select "All time" and click "Clear"

---

### Issue 2: Links Not Working

**Problem:** When you click a link, nothing happens or you get a "404 Not Found" error.

**Solution:**
1. **Check file names:** Make sure file names are spelled exactly right
   - `privacy.html` (not `Privacy.html` or `privacy.HTML`)
2. **Check file location:** All files must be in the same folder
3. **Check link syntax:** Make sure the link looks like:
   ```html
   <a href="privacy.html">Privacy Policy</a>
   ```
   Not:
   ```html
   <a href="privacy.html/">Privacy Policy</a>  <!-- Extra slash -->
   <a href="./privacy.html">Privacy Policy</a>  <!-- Unnecessary ./ -->
   ```

---

### Issue 3: Text Looks Wrong

**Problem:** Text is too big, too small, or the wrong color.

**Solution:**
1. **Check your edits:** Did you accidentally delete a class name?
2. **Restore from backup:** Use your backup file to compare
3. **Use Find and Replace:** Search for the original text to see what classes are missing

---

### Issue 4: Button Colors Don't Change

**Problem:** You changed `bg-blue-600` to `bg-green-600` but the button is still blue.

**Solution:**
1. **Check both hover states:**
   ```html
   <!-- Make sure you changed BOTH -->
   bg-blue-600 → bg-green-600
   hover:bg-blue-700 → hover:bg-green-700
   ```

2. **Clear browser cache** (see Issue 1)

3. **Check for typos:** `bg-green-600` (not `bg-green600` or `bg-grn-600`)

---

### Issue 5: Mobile Menu Not Working

**Problem:** The hamburger menu doesn't open on mobile devices.

**Solution:**
1. **Don't modify the JavaScript** (lines 612-665)
2. **Keep the HTML structure intact:**
   - The button must have class: `mobile-menu-button`
   - The menu must have class: `mobile-menu`
3. **Test on actual mobile:** Use browser developer tools (F12) to test responsive view

---

### Issue 6: Images Not Showing

**Problem:** You see broken image icons instead of pictures.

**Solution:**
1. **Check the image URL:** The current page uses URLs from Unsplash (free stock photos)
2. **Replace with your own image:**
   ```html
   <!-- Current -->
   <img src="https://images.unsplash.com/photo-1509391366360-2e938d440dbb?w=600&h=600&fit=crop" alt="Solar panels on Vegas home">
   
   <!-- Your image (if you have a local file) -->
   <img src="solar-panel.jpg" alt="Solar panels on Vegas home">
   ```

3. **Make sure image file is in the same folder as index.html**

---

### Issue 7: Styling Looks Broken After Edits

**Problem:** The page looks messy or elements are overlapping.

**Solution:**
1. **Check for missing closing tags:**
   ```html
   <!-- Wrong - missing closing tag -->
   <div class="...">
       <p>Text here
   </div>
   
   <!-- Correct -->
   <div class="...">
       <p>Text here</p>
   </div>
   ```

2. **Check for broken class names:**
   - All Tailwind classes must be exact
   - `text-gray-900` (not `text-gray900` or `textgray-900`)

3. **Use VS Code's error checking:**
   - Red squiggly lines indicate problems
   - Hover over them to see what's wrong

---

## Best Practices

### 1. Always Make Backups

Before making significant changes:
1. Copy the file and rename it with the date
2. Example: `index.html.backup.2025-01-15`

---

### 2. Test on Multiple Devices

After making changes:
1. **Desktop:** Test in Chrome, Firefox, Safari
2. **Tablet:** Test in browser developer tools (F12) → Tablet view
3. **Mobile:** Test in browser developer tools (F12) → Mobile view

---

### 3. Use Browser Developer Tools

**To open Developer Tools:**
- Windows: Press F12 or Ctrl+Shift+I
- Mac: Press Cmd+Option+I

**Useful features:**
- **Inspect Element:** Right-click any element to see its HTML
- **Responsive View:** See how page looks on different screen sizes
- **Console:** Check for errors (red messages)

---

### 4. Keep Content Consistent

- Use the same terminology throughout
- Keep colors consistent (don't use 5 different blues)
- Use the same tone of voice

---

### 5. Update All Instances

When changing something like a company name:
1. Use Find and Replace (Ctrl+H)
2. Check "Replace All" to ensure consistency
3. Verify the results

---

### 6. Version Control (Advanced)

If you're comfortable with Git:
1. Initialize a repository: `git init`
2. Create a commit before changes: `git add .` then `git commit -m "Before major changes"`
3. If something goes wrong, you can revert

---

### 7. Keep Your Files Organized

**Recommended folder structure:**
```
your-website/
├── index.html
├── privacy.html
├── terms.html
├── contact.html (optional)
├── images/
│   ├── logo.png
│   ├── hero.jpg
│   └── ...
├── css/
│   └── custom.css (if you add custom styles)
└── js/
    └── custom.js (if you add custom scripts)
```

---

### 8. SEO Best Practices

When updating content:

**Page Title (Line 18):**
```html
<title>Power Your Vegas Home with Solar! | Premium Solar Solutions</title>
```
- Keep under 60 characters
- Include your main keyword
- Make it compelling

**Meta Description (Line 17):**
```html
<meta name="description" content="Power Your Vegas Home with Solar! Embrace clean energy and slash your electricity bills...">
```
- Keep under 160 characters
- Summarize page content
- Include relevant keywords

**Headings:**
- Use only one `<h1>` per page (main headline)
- Use `<h2>` for section titles
- Use `<h3>` for subsections

---

### 9. Accessibility Best Practices

When editing:

**Always keep alt text for images:**
```html
<!-- Good -->
<img src="solar-panel.jpg" alt="Solar panels installed on residential roof">

<!-- Bad -->
<img src="solar-panel.jpg">
```

**Use semantic HTML:**
```html
<!-- Good -->
<button aria-label="Open mobile menu">Menu</button>

<!-- Bad -->
<div onclick="...">Menu</div>
```

**Maintain color contrast:**
- Text should be dark on light backgrounds
- Don't rely only on color to convey information

---

### 10. Performance Tips

**Optimize images:**
- Use web-friendly formats (JPG, PNG, WebP)
- Compress images before uploading
- Use appropriate sizes (don't use a 4000px image for a 300px space)

**Minimize CSS and JavaScript:**
- The current page uses CDN links (optimal)
- Don't add unnecessary scripts

**Test page speed:**
- Use Google PageSpeed Insights
- Aim for a score above 80

---

## Quick Reference Guide

### Common Edits

| What to Change | Where to Find It | How to Change It |
|---|---|---|
| Company name | Lines 62, 608 | Find & Replace |
| Hero headline | Line 71 | Find & Replace |
| Button links | Lines 82, 88, 525, 528 | Change href attribute |
| Feature titles | Lines 187, 207, 227 | Find & Replace |
| Testimonials | Lines 357-395 | Find & Replace |
| FAQ items | Lines 411-510 | Find & Replace |
| Footer text | Lines 546, 598-606, 608 | Find & Replace |
| Colors | Throughout | Find & Replace Tailwind class |

---

### Common Tailwind Classes

| Purpose | Classes |
|---------|---------|
| Text Size | `text-sm`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl` |
| Text Color | `text-gray-900`, `text-blue-600`, `text-white`, etc. |
| Background | `bg-white`, `bg-blue-600`, `bg-gray-50`, etc. |
| Padding | `p-4`, `p-8`, `px-6`, `py-4`, etc. |
| Margin | `m-4`, `mx-auto`, `mb-6`, etc. |
| Rounded Corners | `rounded`, `rounded-lg`, `rounded-xl`, `rounded-full` |
| Shadow | `shadow`, `shadow-lg`, `shadow-xl`, `shadow-2xl` |
| Display | `hidden`, `block`, `flex`, `grid` |
| Responsive | `sm:`, `md:`, `lg:` (prefixes) |

---

## Getting Help

### Resources

- **Tailwind CSS Documentation:** [tailwindcss.com](https://tailwindcss.com)
- **Font Awesome Icons:** [fontawesome.com](https://fontawesome.com)
- **HTML/CSS Learning:** [MDN Web Docs](https://developer.mozilla.org)
- **VS Code Help:** [code.visualstudio.com/docs](https://code.visualstudio.com/docs)

### When You're Stuck

1. **Check the backup file** to see what was there before
2. **Use browser Developer Tools** (F12) to inspect elements
3. **Search for the error message** on Google
4. **Ask for help** on Stack Overflow or development forums

---

## Final Checklist

Before launching your updated website:

- [ ] All text content is updated and proofread
- [ ] All links work correctly
- [ ] Images load properly
- [ ] Page looks good on mobile (test with F12)
- [ ] Page looks good on tablet (test with F12)
- [ ] Page looks good on desktop
- [ ] All buttons are clickable and go to correct URLs
- [ ] Contact information is correct
- [ ] Social media links are correct
- [ ] Privacy Policy link works
- [ ] Terms of Service link works
- [ ] No broken images or 404 errors
- [ ] Page loads quickly
- [ ] No console errors (check F12 → Console tab)

---

## Conclusion

Congratulations! You now have the knowledge to maintain and customize this landing page. Remember:

- **Start small:** Make one change at a time
- **Test frequently:** Check your work after each change
- **Use backups:** Always have a backup before major changes
- **Keep learning:** HTML and CSS are easy once you understand the basics

The landing page is built with modern, clean code that's easy to modify. If you follow these guidelines, you'll be able to keep your website fresh and up-to-date with confidence.

Happy editing! 🚀