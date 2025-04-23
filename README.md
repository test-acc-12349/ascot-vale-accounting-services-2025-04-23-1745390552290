# Ascot Vale Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Ascot Vale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original header text -->
<div class="text-2xl font-bold text-gray-800">
    Ascot Vale
</div>
```
To update the company name, simply replace "Ascot Vale" with your desired text while keeping the surrounding div tags intact.

#### Hero Section
The main headline and subheading can be found in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Ascot Vale accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Accounting excellence with a personal touch
</p>
```
Update these text elements while maintaining the surrounding HTML structure.

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:`: Applies styles at medium screen sizes (768px and up)
- `lg:`: Applies styles at large screen sizes (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile screens: text-4xl (2.25rem)
- Medium screens: text-5xl (3rem)
- Large screens: text-6xl (4rem)

#### Common Class Categories
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`
- Colors: `text-gray-900`, `bg-blue-600`, `text-white`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are internal anchors:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update these links:
1. For internal pages: Change `href="#section"` to `href="page-name.html"`
2. For external links: Use complete URLs: `href="https://example.com"`

### Call-to-Action Links
Update the main CTA button link:
```html
<!-- Original -->
<a href="https://theaccountants.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>

<!-- Example update -->
<a href="https://your-booking-page.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">About Us</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Services</a></li>
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Alternative Footer Addition
You can also add them to the copyright section:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Ascot Vale Accounting. All rights reserved.</p>
    <!-- Add this line -->
    <p class="mt-2">
        <a href="privacy.html" class="hover:text-white">Privacy Policy</a> | 
        <a href="terms.html" class="hover:text-white">Terms of Service</a>
    </p>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure all HTML files are in the same directory
   - Check for correct file names and extensions
   - Verify that anchor IDs match exactly (case-sensitive)

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Icon Display Problems**
   - Verify Font Awesome CDN link is present and working
   - Check for correct icon class names (e.g., `fas fa-chart-line`)

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all CDN links are accessible
3. Test the page across different browsers
4. Ensure all HTML tags are properly closed

Remember to always backup your files before making significant changes.