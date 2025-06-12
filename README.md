# Texas Pros Garage Doors Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Pros Garage Doors landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<div class="text-2xl font-bold text-blue-600">
    Texas Pros Garage Doors  <!-- Edit this text -->
</div>
```

**Key Tailwind Classes Explained:**
- `text-2xl`: Sets large text size
- `font-bold`: Makes text bold
- `text-blue-600`: Sets text color to blue

### Hero Section
The main banner section contains the primary heading and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8">
    Texas Pros Garage Doors SA  <!-- Edit this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    We provide top-notch garage doors services in San Antonio  <!-- Edit this text -->
</p>
```

**Responsive Design Classes:**
- `text-4xl md:text-5xl lg:text-6xl`: Creates responsive text sizing
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Services Section
To modify service cards:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold mb-4">
        Garage Doors  <!-- Edit service title -->
    </h3>
    <p class="text-gray-600">
        High-quality garage doors for residential and commercial properties  <!-- Edit description -->
    </p>
</div>
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. Replace `#section-name` with:
   - Internal links: Use `#new-section-id`
   - External links: Use full URL (e.g., `https://example.com`)

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Replace # with actual social media URL -->
    </a>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert new links in the footer's Quick Links section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in the same directory
2. Copy the header and footer from `index.html`
3. Add new content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match link hrefs
   - Example: `href="#services"` should match `id="services"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Ensure proper Tailwind breakpoint classes are used:
     ```html
     class="text-base md:text-lg lg:text-xl"
     ```

3. **Missing Styles**
   - Verify Tailwind CSS CDN link is working
   - Check for typos in class names
   - Use browser inspector to debug

### Best Practices

1. Always test changes in multiple browsers
2. Maintain consistent spacing using Tailwind's spacing classes
3. Keep the responsive design intact when modifying classes
4. Back up files before making significant changes

For additional support or questions, please refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)