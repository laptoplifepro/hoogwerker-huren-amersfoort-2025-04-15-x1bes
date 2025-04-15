# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Huren Amersfoort landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo text. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">
    Hoogwerker Huren  <!-- Replace this text -->
</a>
```

2. Modify navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these text values as needed -->
    <a href="#diensten" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Diensten</a>
    <a href="#voordelen" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
```

### Hero Section
Update the main headline and description:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Hoogwerker Huren in Amersfoort  <!-- Replace main headline -->
</h1>
<p class="text-xl sm:text-2xl text-gray-600 mb-12 leading-relaxed">
    Professionele hoogwerkers voor elk project.  <!-- Replace description -->
</p>
```

### Understanding Tailwind Classes
Key classes explained:
- `text-4xl`: Large text size (increases with sm: and lg: prefixes)
- `font-bold`: Bold text weight
- `mb-8`: Margin bottom spacing (8 units)
- `hover:text-blue-600`: Text color changes to blue on hover
- `transition-colors`: Smooth color transitions

To modify styling:
1. Font sizes: Use `text-sm` through `text-6xl`
2. Colors: Replace `blue-600` with options like `red-600`, `green-600`
3. Spacing: Adjust `m-` (margin) and `p-` (padding) values (1-16)

## Managing Links

### Navigation Links
Current internal links structure:
```html
<!-- In both desktop and mobile menus -->
<a href="#diensten">Diensten</a>
<a href="#voordelen">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Update both desktop AND mobile menu versions

### External Links
The main call-to-action button:
```html
<a href="https://hoogwerkerhurenamersfoort.nl" class="inline-block bg-blue-600...">
    Direct Huren
</a>
```

To update:
1. Replace the URL in `href`
2. Ensure URLs include `https://` or `http://`
3. Test links after updating

## Adding Privacy and Terms Pages

### Footer Link Setup
Current footer link structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

3. Maintain consistent styling by copying these classes:
   - `text-gray-400`: Default text color
   - `hover:text-white`: Hover state color
   - `transition-colors`: Smooth transition effect

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Check for extra spaces in IDs
   - Verify # prefix in href attributes

2. **Styling Issues**
   - Check for proper class spelling
   - Maintain responsive prefixes (sm:, md:, lg:)
   - Keep original utility class order

3. **Mobile Menu Problems**
   - Verify Alpine.js is properly loaded
   - Check x-data and x-show attributes
   - Test menu button functionality

For additional help:
- Reference [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check [Alpine.js documentation](https://alpinejs.dev/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test changes across different screen sizes using browser developer tools.