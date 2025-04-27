# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Olney Shower Glass Company landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold tracking-tight text-white hover:text-blue-400">
    Olney Glass
</a>
```
- Replace "Olney Glass" with your company name
- Adjust text size using `text-2xl` (can be `text-xl` for smaller or `text-3xl` for larger)

### Hero Section
The main banner section contains your primary message:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Sliding Shower Doors Save Space
</h1>
```
- Update the heading text between the `<h1>` tags
- Text sizes are responsive:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Common Tailwind Classes Explained
- `container`: Centers content and sets max-width
- `mx-auto`: Centers element horizontally
- `px-6`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `text-gray-300`: Sets text color
- `hover:text-white`: Changes text color on hover
- `transition-colors`: Enables smooth color transitions

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (starting with #) connect to section IDs
2. External links need full URLs
3. Example of updating a link:
```html
<!-- Before -->
<a href="#features">Features</a>
<!-- After -->
<a href="https://yourwebsite.com/features">Features</a>
```

### Call-to-Action Links
The main CTA button currently points to:
```html
<a href="http://www.customeuroglass.com" class="inline-flex items-center...">
```

To update:
1. Replace `http://www.customeuroglass.com` with your desired URL
2. Ensure the URL includes `http://` or `https://`
3. Test the link after updating

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's "Links" section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Privacy and Terms Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Check mobile-first classes (without prefix)
   - Then tablet (`md:`) and desktop (`lg:`) variants
   - Example: `text-xl md:text-2xl lg:text-3xl`

3. **Style Changes Not Applying**
   - Verify Tailwind CDN link is working
   - Check class spelling and hyphens
   - Ensure classes are in the correct order

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser inspector tools to debug layout issues
- Test on multiple devices and browsers

Remember to always backup your files before making changes, and test thoroughly across different devices and browsers after updates.