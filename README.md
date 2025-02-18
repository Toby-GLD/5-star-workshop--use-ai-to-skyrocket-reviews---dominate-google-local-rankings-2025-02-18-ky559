# RocketReviews.ai Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the RocketReviews.ai landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

```html
<!-- Logo Text (Line 20) -->
<a href="/" class="text-xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    RocketReviews.ai  <!-- Change this text to update the logo -->
</a>

<!-- Navigation Links (Lines 23-26) -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update navigation text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

**Key Tailwind Classes Explained:**
- `hidden md:flex`: Hides menu on mobile, shows on medium screens
- `space-x-8`: Adds horizontal spacing between menu items
- `bg-gradient-to-r`: Creates right-to-left gradient effect

### Hero Section
Update the main headline and subheading:

```html
<!-- Main Headline (Lines 38-40) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    5-Star Workshop: Use AI to Skyrocket Reviews & Dominate Google Local Rankings
</h1>

<!-- Subheading (Lines 41-43) -->
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    How to Get More Reviews & Rank Higher on Google Using AI
</p>
```

**Responsive Text Classes:**
- `text-4xl md:text-5xl lg:text-6xl`: Increases text size at different breakpoints
- `tracking-tight`: Reduces letter spacing
- `mb-8`: Adds margin bottom spacing

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="Eventbrite.com">Register Now</a>  <!-- Update this URL -->
```

### How to Update Links
1. Internal Links (sections on the same page):
   - Keep the `#` symbol
   - Match the ID of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. External Links:
   - Replace `Eventbrite.com` with full URLs
   - Always include `https://` or `http://`
   ```html
   <!-- Before -->
   <a href="Eventbrite.com">Register Now</a>
   
   <!-- After -->
   <a href="https://www.eventbrite.com/your-event-url">Register Now</a>
   ```

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:

```html
<!-- Current Footer Legal Links (Lines 164-167) -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>

<!-- Updated Footer Legal Links -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   ```html
   <!-- This won't work -->
   <a href="#Features">
   <section id="features">
   
   <!-- This will work -->
   <a href="#features">
   <section id="features">
   ```

2. **Responsive Design Issues**
   - If elements look wrong on mobile:
     - Check for `md:` and `lg:` prefixed classes
     - Ensure the viewport meta tag is present in the head
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent
     ```

### Need More Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML validity using [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools (F12)

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.