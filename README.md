# Houston Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Houston Web landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Locate this line in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-900">Houston<span class="text-blue-600">Web</span></a>
```
- Change "Houston" and "Web" to your preferred text
- The blue color is applied to "Web" using `text-blue-600`

2. **Navigation Links**: Find these lines:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <!-- ... -->
</div>
```
- Update text between `>` and `</a>` for each link
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 text-gray-900">Best Websites In Houston</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen sizes

### Understanding Tailwind Classes
Common classes used throughout:
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (6 units)
- `py-24`: Adds vertical padding (24 units)
- `text-gray-600`: Sets text color
- `hover:text-blue-600`: Changes text color on hover
- `transition-colors`: Enables smooth color transitions

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Locate the section ID you want to link to (e.g., `id="features"`)
2. Add `#` before the ID in the `href` attribute
3. Ensure the ID exists in your HTML

### Call-to-Action Buttons
Current buttons link to "https://sigmaseo.io". To update:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600 text-white">Start Your Project</a>
```
- Replace `https://sigmaseo.io` with your desired URL
- Test the link after updating

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <!-- Twitter SVG -->
    </a>
</div>
```
- Replace `#` with your social media profile URLs
- Update the `sr-only` text to match the platform

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```
Replace the `#` with:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
- Copy the header and footer from `index.html` to your new pages
- Use the same Tailwind CSS classes for consistent styling
- Test navigation between all pages

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the head section
   - Test on different screen sizes

3. **Style Changes Not Applying**
   - Verify Tailwind CDN link is working
   - Check for typos in class names
   - Ensure classes are space-separated

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers

Remember to always backup your files before making significant changes, and test thoroughly across different devices and browsers.