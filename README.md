# Zaide Landing Page - Maintenance Guide

This guide will help you maintain and customize the Zaide landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this section and replace "Zaide" with your desired text:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Zaide
</div>
```

2. **Navigation Items**: Located in two places for desktop and mobile views:
```html
<!-- Desktop Menu -->
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>

<!-- Mobile Menu -->
<div class="md:hidden" x-show="isOpen" x-transition>
    <div class="pt-4 pb-3 space-y-3">
        <a href="#features" class="block text-gray-600 hover:text-gray-900">Features</a>
        <!-- Add or modify mobile menu items here -->
    </div>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Zaide - Plataforma de multi Atendimento com IA
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Seu atendimento com IA é fantástico!
</p>
```

### Tailwind CSS Tips
- `text-{size}`: Controls text size (xs, sm, base, lg, xl, 2xl, etc.)
- `font-{weight}`: Controls text thickness (normal, medium, bold, etc.)
- `bg-{color}-{shade}`: Sets background color (purple-600, blue-500, etc.)
- `p-{size}`: Sets padding (1-12, representing 0.25rem to 3rem)
- `m-{size}`: Sets margin (same scale as padding)

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Update both desktop and mobile menus

### Call-to-Action Buttons
The page includes WhatsApp links that need customization:
```html
<a href="https://wa.me/5521999561515" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-500 text-white rounded-full">
    Começar Agora
</a>
```

To update WhatsApp links:
1. Replace `5521999561515` with your WhatsApp number
2. Update all instances in the header and hero section

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the footer legal section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacidade</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Termos</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update the footer links:
   ```html
   <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacidade</a></li>
   <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Termos</a></li>
   ```

3. Ensure consistent styling by copying the header and footer from index.html to your new pages

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in ID names
   - Verify that sections have the correct ID attribute

2. **Responsive Design Problems**
   - Check that you've maintained the responsive classes:
     - `md:` prefix for medium screens
     - `lg:` prefix for large screens
   - Don't remove `container` and `mx-auto` classes from main sections

3. **Gradient Text Not Showing**
   - Ensure these classes remain together:
     ```html
     bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent
     ```

### Need Help?
- Double-check your changes against the original HTML
- Use browser developer tools (F12) to inspect elements
- Maintain the existing class structure when making changes
- Test on multiple screen sizes using browser developer tools

Remember to always backup your files before making changes, and test thoroughly across different devices and browsers.