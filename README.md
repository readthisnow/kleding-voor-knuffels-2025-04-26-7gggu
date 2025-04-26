# Landing Page Maintenance Guide

This guide will help you maintain and customize the KnuffelMode landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu. To update:

1. **Logo Text**: Find this line and replace "KnuffelMode" with your desired text:
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    KnuffelMode
</a>
```

2. **Navigation Items**: Locate the navigation div and modify menu items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
The main banner section contains:

1. **Main Heading**: Update the h1 text:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Kleding Voor Knuffels
</h1>
```

2. **Subheading**: Modify the paragraph text:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Koop Kleding Voor Knuffels Met Korting
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `bg-{color}-{shade}`: Sets background color (e.g., `bg-gray-900`)
- `p-{number}`: Sets padding (e.g., `p-8`)
- `m-{number}`: Sets margin (e.g., `mb-8`)
- `flex`: Creates flexible container
- `grid`: Creates grid layout

Example of modifying a feature card's padding:
```html
<!-- Original -->
<div class="bg-gray-900 rounded-xl p-8 transform hover:scale-105">

<!-- Modified with more padding -->
<div class="bg-gray-900 rounded-xl p-12 transform hover:scale-105">
```

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute:
   - For internal sections: Use `#section-name`
   - For external pages: Use full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
The main CTA buttons currently point to:
```html
<a href="https://amzn.to/4jtNeXe" class="inline-flex items-center px-8 py-4 rounded-full...">
```

To update:
1. Replace `https://amzn.to/4jtNeXe` with your desired URL
2. Ensure the link starts with `https://` for external sites

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<footer class="bg-gray-900 border-t border-gray-800 py-12">
```

2. Add new links using this template:
```html
<div class="mt-8 pt-8 border-t border-gray-800 text-center text-gray-400">
    <p>&copy; 2024 Kleding Voor Knuffels. Alle rechten voorbehouden.</p>
    <!-- Add these lines -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Gradients**
   - Ensure all gradient classes include both `from-` and `to-` components
   - Example: `bg-gradient-to-r from-purple-500 to-pink-500`

2. **Responsive Issues**
   - Check that responsive classes are properly ordered (e.g., `text-xl md:text-2xl lg:text-3xl`)
   - Verify `container` class is present on parent elements

3. **Missing Styles**
   - Confirm Tailwind CSS is properly linked in the head section
   - Check for typos in class names

Need help? Contact support@example.com for assistance.

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Back up files before making changes
- Keep consistent styling throughout the page