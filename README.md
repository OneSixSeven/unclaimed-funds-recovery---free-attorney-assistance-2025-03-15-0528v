# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Unclaimed Funds Recovery landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm shadow-sm z-50">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex-shrink-0">
            <a href="/" class="text-xl font-bold text-blue-600">Elsa Figueras CPA</a>
        </div>
    </nav>
</header>
```

To update the company name:
1. Locate the `<a>` tag containing "Elsa Figueras CPA"
2. Replace the text between `>` and `</a>`
3. Keep the existing classes to maintain styling

Key Tailwind classes explained:
- `fixed`: Keeps header at top of page
- `w-full`: Makes header full width
- `bg-white/95`: Sets background color to white with 95% opacity
- `shadow-sm`: Adds subtle shadow
- `z-50`: Ensures header stays above other content

### Hero Section
```html
<section class="pt-32 pb-24 bg-gradient-to-br from-blue-50 to-white">
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
        Unclaimed Funds Recovery
        <span class="block text-blue-600">Free Attorney Assistance</span>
    </h1>
</section>
```

To modify hero text:
1. Find the `<h1>` tag
2. Update the main heading text
3. Modify the blue subtitle in the `<span>` tag

Responsive text classes explained:
- `text-4xl`: Base size on mobile
- `md:text-5xl`: Medium screens
- `lg:text-6xl`: Large screens

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update navigation links:
1. Locate the `href` attribute in each `<a>` tag
2. Replace "#section-name" with:
   - Internal links: Use `#section-id`
   - External links: Use full URL (e.g., `https://example.com`)
3. Update the text between `>` and `</a>`

### Call-to-Action Links
```html
<a href="https://elsafigueras.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Start Your Free Claim Review
</a>
```

To update CTA buttons:
1. Find `<a>` tags with `href="https://elsafigueras.com"`
2. Replace URL with your desired destination
3. Modify button text as needed

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Example: `href="#services"` needs matching `id="services"` in section tag

2. **Responsive Design Issues**
   - Check responsive classes are properly ordered:
   ```html
   class="text-base md:text-lg lg:text-xl"
   ```
   - Test on different screen sizes using browser dev tools

3. **Missing Styles**
   - Verify Tailwind CSS CDN link is present in `<head>`
   - Check for typos in class names
   - Use official Tailwind documentation to verify class names

4. **Social Media Links**
   - Replace placeholder "#" with actual social media URLs
   - Example:
   ```html
   <a href="https://linkedin.com/in/your-profile" class="hover:text-blue-400">
   ```

Remember to:
- Test all links after updating
- Maintain consistent styling across pages
- Back up files before making changes
- Test on multiple browsers and devices

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.