# Landing Page Maintenance Guide

This guide will help you maintain and customize the Anti Halo Nachtbril landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<span class="text-2xl font-bold text-indigo-600">Nachtbril</span>
```
- Replace "Nachtbril" with your desired text
- Maintain the existing classes to preserve styling

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Kenmerken</a>
```
- Replace "Kenmerken" with your new menu item name
- Keep the classes to maintain hover effects and transitions

### Hero Section
Located at the top of the page with gradient background:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight">Anti Halo Nachtbril</h1>
```
- Update the text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

2. **Promotional Banner:**
```html
<span class="inline-block px-4 py-1.5 mb-6 text-sm font-semibold text-indigo-100 bg-indigo-500 bg-opacity-30 rounded-full">Speciale Aanbieding - 10% Korting</span>
```
- Update the promotional text while keeping all classes
- `bg-opacity-30` controls the background transparency

### Features Section
To modify feature cards:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-bold mb-2">Anti-Halo Technologie</h3>
    <p class="text-gray-600">Vermindert verblinding en halo-effecten...</p>
</div>
```
- Update the `<h3>` and `<p>` text
- Maintain the container classes for consistent styling

## Fixing Broken Links

### Navigation Links
Current links in the navigation:

```html
<!-- Desktop Navigation -->
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Kenmerken</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="https://nachtbril.com/shop">Bestel Nu</a>
</div>
```

To update:
1. Internal links (starting with #) connect to section IDs
2. External links (starting with http) should be updated to your actual URLs
3. Replace `https://nachtbril.com/shop` with your shop URL

### Call-to-Action Buttons
```html
<a href="https://nachtbril.com/shop" class="inline-flex items-center justify-center px-8 py-4...">
    Bestel Nu Met 10% Korting
</a>
```
- Update all instances of `https://nachtbril.com/shop` with your actual shop URL
- Ensure consistency across all CTA buttons

## Linking Privacy and Terms Pages

### Footer Links Section
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add proper links:
1. Create your privacy and terms pages (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout:**
- Check that you haven't removed any essential Tailwind classes
- Verify all opening tags have corresponding closing tags
- Maintain the responsive classes (md:, lg:) for proper scaling

2. **Non-Working Links:**
- Ensure section IDs match their corresponding links
- Verify external URLs start with `http://` or `https://`
- Test all links after updating

3. **Missing Styles:**
- Confirm the Tailwind CSS CDN link is present in the head section
- Check for typos in class names
- Maintain spacing between multiple classes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Validate your HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different screen sizes and browsers before publishing updates to your live site.